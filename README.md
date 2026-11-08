<div align="center">

# 🎯 STRIKE ZONE

### A 3D mobile-first tactical shooter that runs right in your browser

**5v5 Team Deathmatch · AI squads · 3 weapon classes · Touch & keyboard controls**

[![Play Now](https://img.shields.io/badge/▶_PLAY_NOW-szfps.vercel.app-ffb400?style=for-the-badge)](https://szfps.vercel.app)
[![GitHub Pages](https://img.shields.io/badge/ALT_LINK-GitHub_Pages-222?style=for-the-badge&logo=github)](https://catalystberry842-alt.github.io/CODM/)

![Three.js](https://img.shields.io/badge/Engine-Three.js_r128-black?logo=three.js)
![HTML5](https://img.shields.io/badge/HTML5-Single_File-e34f26?logo=html5&logoColor=white)
![Mobile](https://img.shields.io/badge/Mobile-Touch_Controls-3fa2ff)
![No Install](https://img.shields.io/badge/Install-None_Needed-3fdc6a)

</div>

---

## 📖 About

**Strike Zone** is a fast-paced first-person shooter inspired by mobile FPS games. You drop into **Crossroads Yard** — a military shipping yard packed with containers, crates, sandbag cover and a central compound — alongside 4 AI teammates to fight a 5-bot enemy squad.

No app store. No download. No account. Open the link on your phone, turn it sideways, hit **START**.

The entire game — engine setup, map, AI, weapons, HUD, menus and sound — lives in a **single `index.html` file**.

---

## 🎮 How to Play

1. Open **[szfps.vercel.app](https://szfps.vercel.app)** on your phone or computer
2. 📱 On phone: **rotate to landscape** (tap ⛶ in the lobby for fullscreen)
3. Pick your weapon in **LOADOUT**
4. Tap **START**
5. You're on **🔵 BLUE**. Eliminate **🔴 RED**.

### 🏆 Win Condition
- First team to **30 kills** wins
- Or the team with the **most kills when the 5:00 timer** runs out
- Ties end in a **DRAW**

---

## 🕹️ Controls

### 📱 Phone / Tablet

| Action | Control |
|---|---|
| Move | Drag anywhere on the **left side** (floating joystick) |
| Sprint | Push the joystick **all the way forward** (knob turns gold) |
| Look around | Drag anywhere on the **right side** |
| Fire | **Big red button** (right) or **small red button** (left) |
| Aim + shoot together | Hold fire and **drag your thumb** — it aims while shooting |
| Aim down sights | Tap the **scope** button (toggle) |
| Reload | Tap the **circular arrow** |
| Jump | Tap the **chevron** |
| Pause | **❚❚** top-right |

### ⌨️ Keyboard & Mouse

| Action | Key |
|---|---|
| Move | `W` `A` `S` `D` / Arrow keys |
| Sprint | `Shift` |
| Look | Mouse (click the screen to lock the cursor) |
| Fire | Left click |
| Aim down sights | Right click (hold) |
| Reload | `R` |
| Jump | `Space` |
| Pause | `Esc` / `P` |

---

## 🔫 Arsenal

Choose one primary weapon in **LOADOUT** before the match. Your pick is saved for next time.

| Weapon | Class | Damage | Fire Rate | Magazine | Reload | Best For |
|---|---|---|---|---|---|---|
| **M7 Ranger** | Assault Rifle | 27 | 600 RPM | 30 / 150 | 1.9s | All-round — mid range, steady recoil |
| **Viper-9** | SMG | 19 | ~900 RPM | 36 / 180 | 1.5s | Close quarters, fastest movement |
| **Longbow** | Sniper | 100 | Bolt-action | 5 / 30 | 2.5s | Long range one-shot kills with scope |

**Weapon mechanics**
- 🎯 **Headshots** deal bonus damage — ×1.6 (AR), ×1.5 (SMG), ×2.2 (Sniper)
- 📉 **Damage falloff** — SMG loses damage past 22m, AR past 45m
- 🌀 **Bullet spread** grows when moving or jumping; tightens when aiming down sights
- 💥 **Recoil** kicks the camera up with each shot; reduced while aiming
- 🔭 **Sniper scope** — full-screen scope overlay with 20° zoom
- 🔴 **Red-dot sight** on AR and SMG when aiming
- 🔄 **Auto-reload** when the magazine runs dry

---

## ✨ Features

### Combat
- **Hitscan shooting** with real line-of-sight — walls and containers block bullets
- **Hit markers** (white on hit, red on kill) with audio feedback
- **Damage direction indicator** — red arc points to where you're being shot from
- **Health regeneration** after 4 seconds out of combat
- **Spawn protection** — 2 seconds of invulnerability after respawning
- **Death cam** — camera lifts and tracks your killer during the 4s respawn

### Kill Streaks & Medals
| Medal | How |
|---|---|
| `ELIMINATED` | Standard kill |
| `HEADSHOT` | Kill with a head hit |
| `DOUBLE KILL` → `TRIPLE KILL` → `QUAD KILL` → `RAMPAGE` | Kills within 4s of each other |
| `5 STREAK` | 5 kills without dying |
| `UNSTOPPABLE` | 10 kills without dying |

### AI Bots
- **9 AI soldiers** — 4 teammates (Ghost, Ace, Nova, Bolt) and 5 enemies (Rex, Havoc, Raven, Blitz, Cobra)
- Bots **see you** only with line-of-sight and a forward field of view — you can flank them
- They **hear gunfire** and **react when shot**, turning to face the attacker
- **Combat movement** — strafing, closing distance, backing off when too close
- **Burst fire** with reaction delays based on difficulty
- **Hunt last-known positions** of enemies who break line of sight
- Bots fight **each other**, not just you
- Unstuck logic — bots reroute if blocked by cover

### Difficulty
| Level | Accuracy | Reaction Time | Damage to You |
|---|---|---|---|
| Easy | Low | ~1.0s | 7 per hit |
| Normal | Medium | ~0.65s | 9 per hit |
| Hard | High | ~0.4s | 11 per hit |

### HUD
- 🗺️ **Rotating minimap** — teammates in blue; enemies show as **red dots only when they fire**
- 📊 **Live scoreboard bar** with team progress toward 30 kills + match timer
- 📰 **Kill feed** (top-right) with weapon and headshot icon
- ❤️ **Health bar** (turns red when low) + red screen vignette as you take damage
- 🔢 **Ammo counter** (turns red when low) + "RELOADING" indicator
- ➕ **Dynamic crosshair** that widens with spread and turns red over enemies
- 🏷️ **Enemy name tag** appears when your crosshair is on them
- 🔷 **Ally markers** above teammates' heads (visible through walls)

### Menus
- **Lobby** with live 3D map flyover, player name and win/loss record
- **Loadout** cards with stat bars for each weapon
- **Settings** — player name, look sensitivity, volume, graphics, bot difficulty, FPS counter
- **Pause menu** with live scoreboard
- **End screen** — Victory / Defeat / Draw, your kills, deaths, K/D, accuracy and full team scoreboards

### Graphics
- Real-time **dynamic shadows** from a sun light
- Procedurally generated **textures** (concrete, corrugated containers, crates, sandbags, ground)
- **Distance fog**, gradient sky and low-poly mountain backdrop
- **Muzzle flashes**, bullet **tracers**, impact dust and hit puffs
- **First-person weapon model** with sway, bob, recoil kick, sprint pose and reload animation
- Animated soldier models with walking legs and death falls
- **3 graphics presets** (Low / Med / High) for weaker or stronger phones

### Audio
- Synthesized gunshot sounds per weapon (no audio files needed)
- **Distance-based volume** for enemy gunfire
- Hit, kill, damage, reload and match-end sound cues

### Saved Between Sessions
Your **name, settings, loadout and win/loss record** are stored in your browser.

---

## 🗺️ Map: Crossroads Yard

An 80×80m enclosed military yard:

- **Central compound** — four walls with a doorway on each side and a partial roof
- **12 shipping containers** (some stacked two-high) for long-range cover
- **Side lanes** with tall walls splitting the flanks
- **Sandbag lines** in front of each spawn and in the mid-lanes
- **24 supply crates** — some stacked — you can **jump on top** for height advantage
- Blue spawns **north**, Red spawns **south**

> 💡 **Tip:** Jump onto a crate, then onto a container for a sniper perch.

---

## 🛠️ Tech

| | |
|---|---|
| Engine | [Three.js](https://threejs.org) r128 (WebGL), loaded from cdnjs |
| Language | Vanilla JavaScript — no frameworks, no build step |
| Size | One ~72 KB `index.html` |
| Rendering | Two-pass: world scene + separate weapon view-model scene (gun never clips into walls) |
| Physics | Custom circle-vs-box collision, gravity, step-up and jumping |
| AI | State-based bots with raycast line-of-sight checks |
| Audio | Web Audio API (synthesized) |
| Hosting | Vercel + GitHub Pages |

---

## 💻 Run It Yourself

```bash
git clone https://github.com/catalystberry842-alt/CODM.git
cd CODM
# open index.html in any modern browser
```

Or serve it locally:

```bash
npx serve .
```

Needs an internet connection the first time (to load Three.js).

---

## 🚧 Roadmap

- [ ] More game modes — **Zombies**, **Battle Royale (mini)**, **Gun Game**
- [ ] More maps
- [ ] Secondary weapons (pistol) + grenades
- [ ] Weapon attachments and skins
- [ ] Crouch / slide
- [ ] Real online multiplayer with friends
- [ ] Global leaderboard
- [ ] Custom button layout for phone controls

Got an idea? [Open an issue](https://github.com/catalystberry842-alt/CODM/issues).

---

## 📱 Performance Tips

- Lagging? **Settings → Graphics → LOW** (turns off shadows, lowers resolution)
- Turn on **Show FPS** to check performance
- Close other apps / browser tabs
- Use **Chrome** on Android or **Safari** on iPhone for best results

---

<div align="center">

**Built by [@catalystberry842-alt](https://github.com/catalystberry842-alt)**

*Strike Zone is an original game. It is not affiliated with or endorsed by any other game or publisher.*

⭐ Star the repo if you enjoyed it!

</div>
