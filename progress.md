Original prompt: build VOIDWELL 2 as a complete single-file Three.js browser game with dynamic tunnel morphing, abilities, enemies, power-ups, bosses, shop, audio, progression, mobile controls, and adaptive quality.

implemented initial single-file build and deterministic browser hooks.
added required three.js r128 post-processing cdn stack with composer fallback, fixed enemy collision syntax, and passed `node --check` on the inline script.
playwright smoke test passed on 2026-07-12 after installing the matching chromium runtime. state confirmed play mode, shield activation, boost input, score and distance updates, near-miss tracking, and active power-up state. screenshot inspection confirmed the neon tunnel and bloom render correctly.
