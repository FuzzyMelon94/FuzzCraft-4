# FuzzCraft — Project Charter
**Author:** FuzzyMelon94
**Working Title:** FuzzCraft
**Status:** Active — Pre-Production
**Last Updated:** 2026-07-05

---

## 1. Vision

FuzzCraft is a modpack for a casual friend group of 4–7 players. It is built around **two pillars**: factory automation and dimension exploration. Everything else is a supporting layer.

The pack is designed to be playable — not exhaustive. Scope is a hard constraint, not a soft guideline. If a mod doesn't serve one of the two pillars or fill a genuine supporting gap, it isn't in.

The questing system ties both pillars together at the end: each major mod gets a questline, and new players should be able to pick up the pack and understand what to work toward without external wikis.

> This pack was designed with lessons from FuzzCraft 4. See `docs/post-mortem.md` for what didn't work and why.

---

## 2. Hard Constraints

These are enforced at every mod addition decision. They are not targets — they are limits.

| Constraint | Limit |
|---|---|
| Server RAM | ≤ 10 GB allocated |
| Client RAM | ≤ 6 GB allocated |
| Client FPS | ≥ 60 FPS baseline (including shaders) |
| Server hardware | HP EliteDesk 800 G4 Micro — i5-8600 (6 cores), 32 GB DDR4, 256 GB SSD |
| Minimum client spec | ~= server hardware |
| Mod count target | ≤ 120 mods (including deps) — soft cap, enforced with intent |

Before adding any mod, ask: does this fit the hardware budget? If uncertain, performance-test before committing.

---

## 3. Technical Foundation

| Property | Decision | Notes |
|---|---|---|
| **Loader** | NeoForge | 1.21.1 — stable, wide ecosystem coverage |
| **Minecraft Version** | 1.21.1 | Not planning a version bump mid-playthrough — that means a new pack |
| **Java Version** | 21+ | Hard minimum |
| **Server Hardware** | HP EliteDesk 800 G4 Micro | Ubuntu Server + Pterodactyl + Wings; MC server runs alongside others |
| **Distribution** | Modrinth (primary) | CurseForge as fallback; packwiz handles both |
| **Pack Toolchain** | packwiz | Bootstrap jar + GitHub Pages to serve `pack.toml` |
| **Player Updates** | packwiz bootstrap (pre-launch command) | ATLauncher and Prism Launcher tested |
| **Version Control** | Git repository | Configs, manifests, docs all tracked |

**Pre-launch command (ATLauncher & Prism):**
```
"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://fuzzymelon94.github.io/FuzzCraft/pack.toml
```

---

## 4. Design Principles

- **Constraints first.** Hardware limits and mod budget are set before the first mod is added. Every addition is measured against them.
- **Two pillars only.** Factory automation and dimension exploration drive mod selection. Supporting mods (food, combat, decoration) get one or two focused picks — not suites.
- **Performance-test early.** Don't wait until the full modlist is assembled to ask whether the server can handle it. Test with all active mods running together after each batch.
- **Multiplayer-test each batch.** The pack is for multiplayer. SP testing is necessary but not sufficient — server testing happens before a batch is considered done.
- **Questing is designed in, not retrofitted.** When adding a mod, consider its questline. If a mod would need significant quest work to be worth including, plan for it now.
- **No progression gates.** Quests guide and reward — they never lock content.
- **Config over removal.** Problems are solved by tweaking configs before reaching for mod removal.
- **If partial coverage makes it worse than nothing, don't add it.** Mods that need compat addons which don't exist are liabilities. (Lesson: Dynamic Trees in FC4.)

---

## 5. The Two Pillars

### Pillar 1 — Factory Automation

Create is the spine. The goal is a deep, satisfying automation experience where players can build factories, automate resource processing, and script complex systems with ComputerCraft.

**Core mods:**
| Mod | Role |
|---|---|
| Create + addons (Create: Big Cannons, Steam 'n' Rails, etc.) | Core automation, contraptions, trains |
| CC: Tweaked | Scripted automation, turtles, computer control |
| Silent Gear | Modular tools and weapons — doesn't break, fully upgradeable |
| Alloy Forgery | Alloy smelting and processing (fills Tinkers'-style smeltery gap) |
| Refined Storage | Late-game digital storage |
| Storage Drawers | Early/mid visual bulk storage |
| Sophisticated Backpacks | Player inventory management |
| Productive Bees | Passive resource generation; planned questline |
| Mob automation | TBD — research Industrial Foregoing or equivalent for mob farm automation |

**Watchlist:**
- Tinkers' Construct — NeoForge 1.21.1 port in progress, no timeline. Add as a batch when it lands; coexists with Silent Gear.

### Pillar 2 — Dimension Exploration & Adventure

Twilight Forest and The Aether are the flagships. The goal is a progression of increasingly dangerous dimensions that generate "adventure night" moments for the group. Questing ties the progression together.

**Dimensions:**
| Mod | Notes |
|---|---|
| Twilight Forest | Flagship adventure dimension |
| The Aether | Flagship sky dimension |
| Deep Aether | Aether expansion content |
| Aether Villages | Village structures in the Aether |
| Explore Ruins (Aether) | Ruin structures in the Aether |
| Deeper and Darker | Deep dark expansion; tied to vanilla progression |
| The Bumblezone | Lightweight bee dimension; fun detour |
| Dimensional Dungeons | Instanced procedural dungeons; low persistent overhead |
| Dimensional Pockets II | Personal pocket dimensions |

**Watchlist:**
- Aether's Delight — no 1.21.1 version
- Aether: Lost Content Addon — no 1.21.1 version

---

## 6. Supporting Layers

These are not pillars — each gets a focused, minimal selection.

### World Generation
| Layer | Mod(s) |
|---|---|
| Overworld biomes | Terralith + Tectonic (terrain shape) + Biomes O' Plenty |
| Nether | Incendium + YUNG's Better Nether Fortresses + Formations Nether |
| End | Nullscape + YUNG's Better End Island |
| Structures | YUNG's full suite (all 1.21.1 NeoForge builds) |
| Villages | ChoiceTheorem's Overhauled Village + compat datapacks |

### Magic
| Mod | Notes |
|---|---|
| Ars Nouveau | One focused magic system; planned questline |

### Combat & Mobs
| Mod | Notes |
|---|---|
| Better Combat | Weapon movesets and combat depth |
| Apotheosis | Enchanting overhaul, looting depth |
| Born in Chaos | Dark-themed mob variants |
| Enderman Overhaul | Biome-variant Endermen |
| Creeper Overhaul | Biome-variant Creepers |
| Ribbits | Frog variants (lightweight) |
| Friends & Foes | Bedrock/vote mob additions (lightweight) |
| Legendary Monsters | Elite mob variants with special abilities |

> Note: Born in Chaos + Legendary Monsters together make the game noticeably harder. This is intentional — flag it in the player onboarding quest.

### Food & Farming
| Mod | Notes |
|---|---|
| Farmer's Delight | Core food expansion |
| Botany Pots + Botany Trees | Passive crop and tree growing |
| Spice of Life: Carrot Edition | Rewards eating variety |

### Navigation & Exploration
| Mod | Notes |
|---|---|
| Waystones | Fast travel network |
| Towers of the Wild | Places waystones in the world; exploration incentive |
| Paragliders | Gliding traversal |
| JourneyMap | Minimap and full map |
| FTB Chunks | Chunk claiming and forceloading |

### Loot
| Mod | Notes |
|---|---|
| Lootr | Instanced loot chests — each player gets their own loot from shared chests |

### Performance Foundation
Standard performance stack — confirmed during Batch 1:
- Sodium (NeoForge build, pinned to Iris-compatible version)
- Iris Shaders
- Complementary Shaders + Euphoria Patches (bundled in `shaderpacks/`)
- FerriteCore
- ModernFix
- Starlight / Canary
- FTB Chunks + Chunky + Chunky Offline (pregen)
- Spark (profiler, keep for debugging)

### QoL Utilities
Confirmed carry-forwards from FC4; full list confirmed during Batch 1:
- EMI (recipe viewer)
- JourneyMap
- Default Options (sprint/sneak defaults, no bobbing)
- Log Begone
- ToastBegone
- GraveStone
- Controlling + Searchables
- BetterF3
- Sound Physics Remastered
- Dynamic FPS
- TrashSlot

---

## 7. Batch Plan

| Batch | Name | Scope |
|---|---|---|
| 1 | Foundation | Performance, Sodium/Iris + shaders, EMI, JourneyMap, FTB Chunks, Chunky, QoL utilities, Default Options |
| 2 | Tech Core | Create + addons, CC: Tweaked, Silent Gear, Alloy Forgery, Refined Storage, Storage Drawers, Sophisticated Backpacks |
| 3 | Tech Extras & Food | Productive Bees, mob automation TBD, Farmer's Delight, Botany Pots + Trees, Spice of Life |
| 4 | Magic | Ars Nouveau + any deps/addons |
| 5 | World Gen & Combat | Terralith + Tectonic + BOP, Incendium + nether structure mods, Nullscape + End Island, YUNG's suite, CTOV, Better Combat, Apotheosis, all mob mods |
| 6 | Dimensions | TF, Aether suite, Deeper & Darker, Bumblezone, Dimensional Dungeons, Dimensional Pockets II |
| 7 | Navigation & QoL | Waystones + Towers of the Wild, Paragliders, Lootr, final QoL pass, compat review |
| 8 | Questing | FTB Quests — questlines for all major mods; no new content mods |

---

## 8. Questing Philosophy

Quests are a **guided tutorial and reward system**, not a progression gate.

- Nothing is locked behind quest completion
- TF, Aether, Deeper & Darker, Bumblezone, and Dimensional Dungeons each get a dedicated questline
- Create, CC, Ars Nouveau, and Productive Bees each get a dedicated questline
- Smaller mods are grouped thematically or given short standalone introductions
- Quest rewards should feel meaningful but not mandatory
- Difficulty note: player onboarding should flag that Born in Chaos + Legendary Monsters intentionally increase challenge

---

## 9. Chunk Management Strategy

- **FTB Chunks** — per-player claiming and forceloading
- **Chunky** — targeted pregen at player base coordinates (300–500 block radius per base)
- Jobs run during server idle via Chunky Offline
- No automatic large-radius generation — storage on a 256 GB SSD is a real constraint
- New player onboarding includes a Chunky job as a standard step

---

## 10. Batch Progress Tracker

| Batch | Name | Status | Notes |
|---|---|---|---|
| 1 | Foundation | ⬜ Not started | |
| 2 | Tech Core | ⬜ Not started | |
| 3 | Tech Extras & Food | ⬜ Not started | |
| 4 | Magic | ⬜ Not started | |
| 5 | World Gen & Combat | ⬜ Not started | |
| 6 | Dimensions | ⬜ Not started | |
| 7 | Navigation & QoL | ⬜ Not started | |
| 8 | Questing | ⬜ Not started | |

---

## 11. Issue & Debug Log

*Issues are logged here as they arise. Format: date, batch, description, resolution.*

| Date | Batch | Issue | Resolution |
|---|---|---|---|

---

## 12. Handoff Protocol

Each batch is implemented in its own conversation. The handoff contains:
- Relevant charter sections
- Specific mod list for the batch
- Any known compat concerns going in
- Success criteria (launches, no crashes, core features functional)

On completion, the batch conversation produces a summary folded back into this charter.

```
Charter → Batch Handoff → Implementation Chat → Summary → Charter updated
```

---

*FuzzCraft is a personal project by FuzzyMelon94. Not affiliated with any modpack platform or mod author.*
*Designed with lessons from FuzzCraft 4 — see `docs/post-mortem.md`.*
