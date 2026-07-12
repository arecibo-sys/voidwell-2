# VOIDWELL 2 — Advanced Tunnel Flight Game

## Role
You are an expert game developer specializing in Three.js, WebGL shaders, Web Audio API, and single-file HTML games. You build visually stunning, performant, mobile-friendly browser games.

## Task
Build VOIDWELL 2 — a more advanced successor to the original VOIDWELL tunnel flight game. The original was a single self-contained `index.html` using Three.js r128 from CDN with inline everything. It featured:
- A procedurally winding 3D tunnel (cylinder segments with winding centerline)
- A drift pod the player steers through the tunnel
- Energy cores to collect (with chain multiplier system)
- Security drones that patrol and home in on the player
- A collapse front chasing the player from behind (if it catches you, game over)
- 3 escalating zones (Outer Hull → Reactor Core → Singularity Chamber)
- Bloom + chromatic aberration post-processing
- Fully procedural Web Audio soundtrack (ambient drone, kick, sub bass, hats, arpeggiated synth)
- Touch controls (virtual joystick + look drag + pinch zoom)
- Desktop controls (WASD/arrows + mouse look)
- Neon-on-black sci-fi aesthetic (cyan, magenta, purple)

## VOIDWELL 2 — New Advanced Features (ALL must be implemented)

### 1. Dynamic Tunnel Morphing
- Tunnel cross-section morphs between circular, hexagonal, and star-shaped as you progress
- Radius pulses and breathing effect synced to the music beat
- Branching paths — occasionally the tunnel forks into two paths that merge later, with different rewards in each branch

### 2. Enhanced Pod & Abilities
- The pod has a **boost** ability (Shift key / double-tap on mobile) — temporary speed surge with cooldown, leaves a brilliant trail
- **Shield ability** (Space / tap top-right) — 3-second invulnerability bubble with visual effect, cooldown 12s
- Pod trail — persistent glowing trail ribbon behind the pod
- Pod banking/tilt animation more pronounced, responds to steering input

### 3. Expanded Enemy System
- **Patrol drones** (original style, orbit the tunnel)
- **Hunter drones** (zone 2+, actively home in on pod, faster)
- **Turret sentinels** (wall-mounted, fire energy bolts at the pod, telegraph with laser sight)
- **Swarm mines** (zone 3, clusters of small mines that drift in formation)
- Each enemy type has distinct visual design, color, and behavior

### 4. Power-Up System
- **Rapid Core** — doubles core spawn rate for 10s
- **Magnet** — pulls nearby cores toward you for 8s
- **Time Dilation** — slows everything except the pod for 5s
- **Overcharge** — next 5 cores worth 5× score
- Power-ups spawn as floating glowing orbs, distinct from cores (golden color)
- Active power-up icons shown in HUD with countdown rings

### 5. Boss Encounters
- **Zone 1 Boss: The Gatekeeper** — a massive drone that blocks the tunnel, has weak points you must hit with collected cores (auto-fire when near)
- **Zone 2 Boss: The Coil** — a serpentine entity that weaves through the tunnel, must survive its attacks for 30s while collecting cores
- **Zone 3 Boss: The Singularity** — the tunnel itself becomes the enemy, walls close in, geometry distorts, must navigate to the exit
- Boss intro banner + health bar + unique music

### 6. Upgrade Shop Between Runs
- After game over, spend accumulated "salvage credits" (earned from score) on permanent upgrades:
  - +Max Hull, +Hull Regen, Faster Boost, Shorter Cooldowns, Starting Shield, Core Magnet (passive), Score Multiplier
- Upgrades persist in localStorage
- Simple but stylish shop UI

### 7. Enhanced Visual Systems
- **Screen shake** on hits, explosions, boss roars
- **Particle explosions** when drones are destroyed (if you add a shooting mechanic) or when the pod hits walls hard
- **Speed lines** effect at high velocity (radial blur lines from screen center)
- **Zone transition** — dramatic flash + tunnel color shift + camera FOV punch
- **Damage vignette** pulses red, **low hull** constant red pulse
- **Core collection burst** — ring of particles + light flash on pickup
- **Energy bolt projectiles** from turrets with glowing trails

### 8. Advanced Procedural Audio
- Per-zone music intensity and instrumentation changes
- Boss music: heavier, darker, double-time kick
- Stinger hits on core collection, wall hit, drone contact, boss intro
- Audio rises in pitch/key as zone difficulty increases
- Power-up activation sound, boost whoosh, shield bubble hum
- Sub-bass swell on collapse proximity increase

### 9. Score & Progression
- Combo system extended: chains now have visual "heat" meter — the longer the chain, the more intense the visual effects
- Near-miss bonus: passing close to a drone without being hit gives bonus points + "NEAR MISS" popup
- Distance milestones with popups (1km, 5km, 10km)
- High score persisted in localStorage
- Run summary with detailed stats: cores, distance, max chain, near misses, time survived, zone reached

### 10. Mobile & Performance
- Must run smoothly on iPad (60fps target)
- Adaptive quality: detect low FPS and reduce particle counts / post-processing automatically
- Virtual joystick + touch look + ability buttons (boost, shield) visible on mobile
- Responsive HUD that scales

## Technical Requirements
- **Single self-contained `index.html`** — no external files, no build step
- Three.js from CDN: `https://cdn.jsdelivr.net/npm/three@0.128.0/build/three.min.js`
- Post-processing libs from CDN (same as original: CopyShader, LuminosityHighPass, EffectComposer, RenderPass, ShaderPass, UnrealBloomPass)
- All code inline in `<script>` tags
- All CSS inline in `<style>` tags
- Must work offline after first load (except Three.js CDN fetch)
- No external assets — all textures, sounds, geometry procedural

## Aesthetic
- Neon-on-black sci-fi: deep blacks with cyan (#00f0ff), magenta (#ff2bd6), purple (#8b5cff) accents
- Glowing wireframes, bloom, chromatic aberration
- Scanline overlay + vignette (carried from original)
- Clean modern HUD with glass panels (backdrop-filter blur)
- Bold monospace typography (Courier New / ui-monospace)

## Output
Write the COMPLETE `index.html` file. Do not use placeholders, do not skip sections, do not write "// rest of the code here". Every feature listed above must be fully implemented in working code. The file should be ready to open in a browser and play.

Start with `<!DOCTYPE html>` and end with `</html>`. Write the entire file now.