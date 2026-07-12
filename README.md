# VOIDWELL 2

**Advanced 3D tunnel flight game.** A successor to [VOIDWELL](https://github.com/arecibo-sys/voidwell) — pilot a drift pod through a morphing alien megastructure with abilities, power-ups, bosses, and an upgrade shop.

**▶ Play online:** https://arecibo-sys.github.io/voidwell-2/

![Genre](https://img.shields.io/badge/genre-tunnel%20flight-8b5cff) ![Engine](https://img.shields.io/badge/engine-Three.js-00f0ff) ![Files](https://img.shields.io/badge/files-1%20HTML-ff2bd6)

## What's New

- **Dynamic tunnel morphing** — cross-section shifts between circular, hexagonal, and star shapes; radius pulses to the beat
- **Abilities** — boost (speed surge + trail) and shield (invulnerability bubble) with cooldowns
- **4 enemy types** — patrol drones, hunter drones, turret sentinels (fire energy bolts), swarm mines
- **Power-ups** — Rapid Core, Magnet, Time Dilation, Overcharge (golden orbs)
- **3 boss encounters** — The Gatekeeper, The Coil, The Singularity
- **Upgrade shop** — spend salvage credits on permanent upgrades (localStorage)
- **Enhanced visuals** — screen shake, particle explosions, speed lines, zone transitions, damage vignette
- **Advanced procedural audio** — per-zone music, boss music, stingers, power-up sounds
- **Progression** — combo heat meter, near-miss bonuses, distance milestones, high score (localStorage)
- **Mobile + adaptive quality** — virtual joystick, touch buttons, auto FPS scaling

## How to Play

**Goal:** collect energy cores, avoid enemies and walls, outrun the collapse, defeat bosses.

**Controls:**
- **Desktop:** WASD/arrows to steer, mouse to look, Shift to boost, Space for shield
- **Mobile:** Virtual joystick + boost/shield buttons

## Tech

- Single self-contained `index.html` — Three.js r128 from CDN, everything else inline
- Bloom + chromatic aberration post-processing
- Fully procedural Web Audio soundtrack
- No external assets

## Run Locally

Open `index.html` in any modern browser. (Needs internet once to fetch Three.js from CDN.)