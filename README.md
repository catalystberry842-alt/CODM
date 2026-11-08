<div align="center">

# STRIKE ZONE

**A mobile-first 3D tactical shooter that runs in the browser.**

5v5 Team Deathmatch · AI squads · Three weapon classes · Touch and keyboard controls

[![Play](https://img.shields.io/badge/Play-szfps.vercel.app-ffb400?style=flat-square)](https://szfps.vercel.app)
[![Mirror](https://img.shields.io/badge/Mirror-GitHub_Pages-24292f?style=flat-square&logo=github)](https://catalystberry842-alt.github.io/strike-zone/)
[![Engine](https://img.shields.io/badge/Engine-Three.js_r128-000000?style=flat-square&logo=three.js)](https://threejs.org)
[![Platform](https://img.shields.io/badge/Platform-Web_%7C_Mobile-3fa2ff?style=flat-square)](#controls)

</div>

---

## Overview

Strike Zone is a first-person shooter built for mobile browsers. Players join a five-person squad alongside four AI teammates and compete against a five-bot enemy team on **Crossroads Yard**, a compact military shipping yard designed for fast, close-to-mid-range engagements.

There is nothing to install and no account required. Open the link, rotate to landscape and press **START**.

The entire game — rendering, map, AI, weapons, HUD, menus and audio — ships as a single self-contained `index.html`.

---

## Quick Start

1. Open **[szfps.vercel.app](https://szfps.vercel.app)** on a phone or desktop browser
2. On mobile, rotate to landscape (use the fullscreen button in the lobby for best results)
3. Select a weapon in **Loadout**
4. Press **START**

**Objective:** You play on the Blue team. The first team to reach **30 eliminations** wins. If the **5:00** match timer expires, the team with more eliminations wins; equal scores result in a draw.

---

## Controls

### Mobile

| Action | Input |
|---|---|
| Move | Drag on the left half of the screen (floating joystick) |
| Sprint | Push the joystick fully forward |
| Look | Drag on the right half of the screen |
| Fire | Primary fire button (right) or secondary fire button (left) |
| Fire while aiming | Hold a fire button and drag to adjust aim |
| Aim down sights | Scope button (toggle) |
| Reload | Reload button |
| Jump | Jump button |
| Pause | Pause button, top right |

### Desktop

| Action | Input |
|---|---|
| Move | `W` `A` `S` `D` or arrow keys |
| Sprint | `Shift` |
| Look | Mouse (click to capture cursor) |
| Fire | Left mouse button |
| Aim down sights | Right mouse button (hold) |
| Reload | `R` |
| Jump | `Space` |
| Pause | `Esc` or `P` |

---

## Weapons

One primary weapon is selected before each match. The selection persists between sessions.

| Weapon | Class | Damage | Fire Rate | Magazine / Reserve | Reload | Role |
|---|---|---|---|---|---|---|
| M7 Ranger | Assault Rifle | 27 | 600 RPM | 30 / 150 | 1.9 s | Versatile mid-range |
| Viper-9 | Submachine Gun | 19 | ~900 RPM | 36 / 180 | 1.5 s | Close quarters, high mobility |
| Longbow | Sniper Rifle | 100 | Bolt action | 5 / 30 | 2.5 s | Long-range precision |

**Ballistics**

- Headshot multipliers: ×1.6 (AR), ×1.5 (SMG), ×2.2 (Sniper)
- Damage falloff beyond 22 m (SMG) and 45 m (AR)
- Spread increases while moving or airborne and tightens when aiming down sights
- Per-shot vertical recoil, reduced while aiming
- Red-dot sight on the AR and SMG; full scope overlay with 20° zoom on the sniper
- Automatic reload on an empty magazine

---

## Features

### Combat

- Hitscan shooting with full line-of-sight — terrain and cover block shots
- Hit markers with distinct kill confirmation and audio feedback
- Directional damage indicator
- Health regeneration after four seconds without taking damage
- Two seconds of spawn protection
- Kill cam that follows the eliminating player during the respawn timer

### Medals

| Medal | Condition |
|---|---|
| Eliminated | Standard elimination |
| Headshot | Elimination with a head hit |
| Double Kill · Triple Kill · Quad Kill · Rampage | Consecutive eliminations within four seconds |
| 5 Streak | Five eliminations without dying |
| Unstoppable | Ten eliminations without dying |

### Artificial Intelligence

- Nine AI combatants: four allies and five opponents
- Vision based on line-of-sight and a forward field of view, which allows flanking
- Awareness of nearby gunfire and incoming damage
- Combat movement including strafing, advancing and retreating to preferred range
- Burst fire with difficulty-dependent reaction times
- Pursuit of last-known enemy positions
- Bots engage each other, not only the player
- Path recovery when blocked by obstacles

| Difficulty | Accuracy | Reaction Time | Damage per Hit |
|---|---|---|---|
| Easy | Low | ~1.0 s | 7 |
| Normal | Medium | ~0.65 s | 9 |
| Hard | High | ~0.4 s | 11 |

### Interface

- Rotating minimap; allies always visible, opponents revealed briefly when they fire
- Score bar with progress toward the score limit and match timer
- Kill feed with weapon and headshot indicators
- Health bar and damage vignette
- Ammunition counter with low-ammo and reload states
- Dynamic crosshair reflecting current spread, with enemy highlight and name tag
- Ally markers visible through walls

### Menus

- Lobby with live 3D map flyover, player name and win/loss record
- Loadout screen with comparative stat bars
- Settings: player name, look sensitivity, volume, graphics quality, bot difficulty, FPS counter
- Pause menu with live scoreboard
- Post-match summary with result, eliminations, deaths, K/D ratio, accuracy and full scoreboards

### Visuals and Audio

- Real-time directional shadows
- Procedurally generated textures for concrete, containers, crates, sandbags and terrain
- Distance fog, gradient sky and low-poly mountain backdrop
- Muzzle flashes, tracers and impact effects
- First-person weapon model with sway, bob, recoil, sprint pose and reload animation
- Animated character models with locomotion and death animations
- Three graphics presets (Low, Medium, High)
- Synthesized weapon audio with distance attenuation (no audio assets)

### Persistence

Player name, settings, loadout and win/loss record are stored locally in the browser.

---

## Map: Crossroads Yard

An enclosed 80 × 80 m military yard.

- **Central compound** — four walls with a doorway on each side and a partial roof
- **Shipping containers** — twelve units, some stacked two high, for long sightlines and cover
- **Side lanes** — tall walls separating the flanks
- **Sandbag lines** — in front of each spawn and across the mid lanes
- **Supply crates** — twenty-four in total, climbable for elevated positions
- **Spawns** — Blue in the north, Red in the south

Crates can be used to reach the tops of containers for elevated sniper positions.

---

## Technical Details

| Component | Implementation |
|---|---|
| Rendering | Three.js r128 (WebGL), loaded from cdnjs |
| Language | Vanilla JavaScript — no framework, no build step |
| Distribution | Single `index.html`, approximately 72 KB |
| Render pipeline | Two passes: world scene, then a separate view-model scene so the weapon never clips into geometry |
| Physics | Custom circle-versus-AABB collision with gravity, step-up and jumping |
| AI | State-driven agents using raycast line-of-sight checks |
| Audio | Web Audio API, fully synthesized |
| Hosting | Vercel (primary), GitHub Pages (mirror) |

---

## Running Locally

```bash
git clone https://github.com/catalystberry842-alt/strike-zone.git
cd strike-zone
```

Open `index.html` in any modern browser, or serve the directory:

```bash
npx serve .
```

An internet connection is required on first load to fetch Three.js.

---

## Performance

- Set **Settings → Graphics** to **Low** on older devices; this disables shadows and lowers render resolution
- Enable **Show FPS** to monitor frame rate
- Chrome (Android) and Safari (iOS) are recommended

---

## Roadmap

- [ ] Additional modes: Zombies, Mini Battle Royale, Gun Game
- [ ] Additional maps
- [ ] Secondary weapons and grenades
- [ ] Weapon attachments and cosmetics
- [ ] Crouch and slide
- [ ] Online multiplayer
- [ ] Global leaderboard
- [ ] Customizable mobile control layout

Suggestions and bug reports are welcome via [Issues](https://github.com/catalystberry842-alt/strike-zone/issues).

---

## Credits

Built by **[@omaofweb3](https://x.com/omaofweb3)**.

Strike Zone is an original work and is not affiliated with or endorsed by any other game or publisher.
