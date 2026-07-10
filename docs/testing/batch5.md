# FuzzCraft 4 — Batch 5 Testing: World Gen & Combat

## Summary
**Pack version:** 0.5.1 (all testing at this version)
**Test date:** <tester fills in>
**Tester:** <tester fills in>
**Play mode:** Single player

## Known Issues
- YUNG's Bridges removed — no config system for spawn rate tuning; watchlisted for future re-evaluation.
- CTOV Terralith and BOP compat datapacks could not be added via packwiz — village building pool compatibility with modded biomes is untested. Watch for mismatched village styles in Terralith/BOP biomes.
- Apotheosis version warning during add (Placebo 9.9.1 vs 1.21.1-9.9.1 label inconsistency) — cosmetic, not functional; version is correct.
- Born in Chaos + Legendary Monsters intentionally increase difficulty. Note any balance concerns in Tester Notes.

---

## 1. Launch & Stability

- [x] Game launches without crash
- [x] No errors in the log related to world gen mods (Terralith, Tectonic, BOP, Incendium, Nullscape, YUNG's, CTOV)
- [x] No errors related to combat mods (Better Combat, Apotheosis, Born in Chaos, Legendary Monsters)
- [x] No errors related to mob mods (Enderman/Creeper Overhaul, Ribbits, Nyf's Spiders, Critters and Companions, Illager Invasion, Naturalist)
- [x] Main menu loads normally — no missing textures or broken UI

---

## 2. Regression — Batches 1–4

- [x] EMI recipe viewer opens and shows recipes — no blank UI
- [x] Create machines still function (place a Mechanical Press, verify it works)
- [x] Farmer's Delight cooking pot still functions
- [x] Ars Nouveau spell casting still works (Projectile + Harm)
- [x] No obvious performance regression — framerate consistent with prior batches

---

## 3. World Generation — Overworld

- [x] Create a new world and load in
- [x] Open JourneyMap full map — verify terrain shows varied biomes (not just vanilla plains/forest)
- [x] Confirm Terralith biomes are generating (e.g. Scarlet Mountains, Lavender Valley, Siberian Taiga — check F3 biome name)
- [x] Confirm Biomes O' Plenty biomes are generating (e.g. Bayou, Cherry Blossom Grove — check F3)
- [x] Terrain feels varied in shape — hills, cliffs, valleys (Tectonic)
- [x] No world gen crashes or corrupted chunks

---

## 4. World Generation — Nether & End

- [x] Enter the Nether — verify Incendium biomes are generating (F3 biome check: Volcanic Caves, Quartz Flats, etc.)
- [x] Nether Fortresses look improved (YUNG's Better Nether Fortresses)
- [x] Enter the End — verify Nullscape is active (varied end islands, not just vanilla void)
- [x] End Island looks improved (YUNG's Better End Island)

---

## 5. YUNG's Structures

Test each while exploring — use `/locate` commands if needed to avoid spending hours walking.

- [x] **Better Caves** — `/locate structure yungs_better_caves:great_cave` — verify cave is present and looks improved
- [x] **Better Dungeons** — `/locate structure yungs_better_dungeons:big_dungeon` — verify dungeon has new layout
- [x] **Better Mineshafts** — `/locate structure yungs_better_mineshafts:abandoned_mineshaft` — verify new mineshaft style
- [x] **Better Ocean Monuments** — `/locate structure yungs_better_ocean_monuments:ocean_monument` — verify monument looks improved
- [x] **Better Strongholds** — `/locate structure yungs_better_strongholds:stronghold` — verify new layout
- [x] **Better Witch Huts** — `/locate structure yungs_better_witch_huts:witch_hut` — verify new style
- [x] **Better Desert Temples** — `/locate structure yungs_better_desert_temples:desert_temple` — verify new layout
- [x] **Better Jungle Temples** — `/locate structure yungs_better_jungle_temples:jungle_temple` — verify new layout
- [x] **Better Nether Fortresses** — tested in Nether section above
- [x] **Better End Island** — tested in End section above
- [N/A] **Bridges** — removed from pack (no config system for spawn rate tuning)

---

## 6. CTOV Villages

- [x] `/locate structure minecraft:village_plains` (or any biome variant) — locate a village
- [x] Village uses varied building styles (not vanilla default layout)
- [x] Village generates in modded biomes (Terralith/BOP) without corruption — note any mismatched styles

---

## 7. Combat — Better Combat & Apotheosis

- [x] Better Combat: Equip a sword and verify attack animations are improved (side swing, stab, etc.)
- [x] Better Combat: Try a different weapon type (axe, halberd if available) — verify different moveset
- [x] Apotheosis: Open the enchanting table — verify new enchanting UI/system
- [x] Apotheosis: Verify at least one Apothic Attributes tooltip appears on a piece of gear
- [x] AttributeFix: No errors in log; enchant values look sane (no extreme number overflow)

---

## 8. Mob Overhauls

- [x] **Enderman Overhaul** — find Endermen in multiple biomes; verify they have biome-specific variants
- [x] **Creeper Overhaul** — find Creepers in multiple biomes; verify they have biome-specific variants  
- [x] **Ribbits** — find frogs in swamp/jungle; verify colour variants exist
- [x] **Nyf's Spiders** — find spiders at night; verify new spider variants spawn
- [x] **Critters and Companions** — find passive critters (e.g. ferret, otter, koi fish) in the wild
- [x] **Naturalist** — find Naturalist animals (deer, moose, bear, etc.) in appropriate biomes

---

## 9. Combat Difficulty — Born in Chaos & Legendary Monsters

⚠️ These intentionally increase difficulty — note balance concerns.

- [x] **Born in Chaos** — encounter a Born in Chaos mob variant (dark/chaos-themed enemies); verify they spawn at appropriate difficulty
- [x] **Legendary Monsters** — encounter a Legendary Monster (elite variant with special abilities); verify it's challenging but fair
- [x] No crashes from these mods during combat
- [x] **Illager Invasion** — trigger an Illager Invasion event or find patrol; verify it works
- [x] Note in Tester Notes: does the difficulty feel right? Any biomes/situations where spawns feel overwhelming?

---

## 10. Passive Mob Mods

- [x] **Critters and Companions** — try taming a critter (e.g. ferret or robin); verify taming mechanic works
- [x] **Critters and Companions** — verify no conflict with existing mob mods or crashes near new animals

---

## 11. Sparse Structures

- [x] Structures feel less dense than vanilla (harder to find, more meaningful when found)
- [x] No crashes or world gen errors related to structure frequency changes

---

## 12. Deferred — Requires Server / Multiplayer

- Illager Invasion group event: verify the event scales appropriately with multiple players online
- Born in Chaos + Legendary Monsters difficulty at scale: note if mob counts/difficulty feels overwhelming with a full group
- CTOV village trading: verify multiple players can use the same village's trading hall without conflict
- Chunk loading with new world gen: run Chunky pregen after establishing a base and verify no TPS drop

---

## 13. Tester Notes

<!-- Broken things, surprises, difficulty feedback, structure quality notes -->
1. didn't seem to be any commands for this - will keep an eye out while playing and probably bump the config up a little then lower if needed.