# FuzzCraft 4 — Batch 5 Testing: World Gen & Combat

## Summary
**Pack version:** 0.5.1
**Test date:** <tester fills in>
**Tester:** <tester fills in>
**Play mode:** Single player

## Known Issues
- YUNG's Bridges spawn rates may be very low — if you don't see one while exploring, bump `min_distance_from_poi` or `count` in the YUNG's Bridges config during testing.
- CTOV Terralith and BOP compat datapacks could not be added via packwiz — village building pool compatibility with modded biomes is untested. Watch for mismatched village styles in Terralith/BOP biomes.
- Apotheosis version warning during add (Placebo 9.9.1 vs 1.21.1-9.9.1 label inconsistency) — cosmetic, not functional; version is correct.
- Born in Chaos + Legendary Monsters intentionally increase difficulty. Note any balance concerns in Tester Notes.

---

## 1. Launch & Stability

- [ ] Game launches without crash
- [ ] No errors in the log related to world gen mods (Terralith, Tectonic, BOP, Incendium, Nullscape, YUNG's, CTOV)
- [ ] No errors related to combat mods (Better Combat, Apotheosis, Born in Chaos, Legendary Monsters)
- [ ] No errors related to mob mods (Enderman/Creeper Overhaul, Ribbits, Nyf's Spiders, Critters and Companions, Illager Invasion, Naturalist)
- [ ] Main menu loads normally — no missing textures or broken UI

---

## 2. Regression — Batches 1–4

- [ ] EMI recipe viewer opens and shows recipes — no blank UI
- [ ] Create machines still function (place a Mechanical Press, verify it works)
- [ ] Farmer's Delight cooking pot still functions
- [ ] Ars Nouveau spell casting still works (Projectile + Harm)
- [ ] No obvious performance regression — framerate consistent with prior batches

---

## 3. World Generation — Overworld

- [ ] Create a new world and load in
- [ ] Open JourneyMap full map — verify terrain shows varied biomes (not just vanilla plains/forest)
- [ ] Confirm Terralith biomes are generating (e.g. Scarlet Mountains, Lavender Valley, Siberian Taiga — check F3 biome name)
- [ ] Confirm Biomes O' Plenty biomes are generating (e.g. Bayou, Cherry Blossom Grove — check F3)
- [ ] Terrain feels varied in shape — hills, cliffs, valleys (Tectonic)
- [ ] No world gen crashes or corrupted chunks

---

## 4. World Generation — Nether & End

- [ ] Enter the Nether — verify Incendium biomes are generating (F3 biome check: Volcanic Caves, Quartz Flats, etc.)
- [ ] Nether Fortresses look improved (YUNG's Better Nether Fortresses)
- [ ] Enter the End — verify Nullscape is active (varied end islands, not just vanilla void)
- [ ] End Island looks improved (YUNG's Better End Island)

---

## 5. YUNG's Structures

Test each while exploring — use `/locate` commands if needed to avoid spending hours walking.

- [ ] **Better Caves** — `/locate structure yungs_better_caves:great_cave` — verify cave is present and looks improved
- [ ] **Better Dungeons** — `/locate structure yungs_better_dungeons:big_dungeon` — verify dungeon has new layout
- [ ] **Better Mineshafts** — `/locate structure yungs_better_mineshafts:abandoned_mineshaft` — verify new mineshaft style
- [ ] **Better Ocean Monuments** — `/locate structure yungs_better_ocean_monuments:ocean_monument` — verify monument looks improved
- [ ] **Better Strongholds** — `/locate structure yungs_better_strongholds:stronghold` — verify new layout
- [ ] **Better Witch Huts** — `/locate structure yungs_better_witch_huts:witch_hut` — verify new style
- [ ] **Better Desert Temples** — `/locate structure yungs_better_desert_temples:desert_temple` — verify new layout
- [ ] **Better Jungle Temples** — `/locate structure yungs_better_jungle_temples:jungle_temple` — verify new layout
- [ ] **Better Nether Fortresses** — tested in Nether section above
- [ ] **Better End Island** — tested in End section above
- [ ] **Bridges** ⚠️ — `/locate structure yungs_bridges:bridge` — if not found within 5000 blocks, note it; spawn rate may need a config bump

---

## 6. CTOV Villages

- [ ] `/locate structure minecraft:village_plains` (or any biome variant) — locate a village
- [ ] Village uses varied building styles (not vanilla default layout)
- [ ] Village generates in modded biomes (Terralith/BOP) without corruption — note any mismatched styles

---

## 7. Combat — Better Combat & Apotheosis

- [ ] Better Combat: Equip a sword and verify attack animations are improved (side swing, stab, etc.)
- [ ] Better Combat: Try a different weapon type (axe, halberd if available) — verify different moveset
- [ ] Apotheosis: Open the enchanting table — verify new enchanting UI/system
- [ ] Apotheosis: Verify at least one Apothic Attributes tooltip appears on a piece of gear
- [ ] AttributeFix: No errors in log; enchant values look sane (no extreme number overflow)

---

## 8. Mob Overhauls

- [ ] **Enderman Overhaul** — find Endermen in multiple biomes; verify they have biome-specific variants
- [ ] **Creeper Overhaul** — find Creepers in multiple biomes; verify they have biome-specific variants  
- [ ] **Ribbits** — find frogs in swamp/jungle; verify colour variants exist
- [ ] **Nyf's Spiders** — find spiders at night; verify new spider variants spawn
- [ ] **Critters and Companions** — find passive critters (e.g. ferret, otter, koi fish) in the wild
- [ ] **Naturalist** — find Naturalist animals (deer, moose, bear, etc.) in appropriate biomes

---

## 9. Combat Difficulty — Born in Chaos & Legendary Monsters

⚠️ These intentionally increase difficulty — note balance concerns.

- [ ] **Born in Chaos** — encounter a Born in Chaos mob variant (dark/chaos-themed enemies); verify they spawn at appropriate difficulty
- [ ] **Legendary Monsters** — encounter a Legendary Monster (elite variant with special abilities); verify it's challenging but fair
- [ ] No crashes from these mods during combat
- [ ] **Illager Invasion** — trigger an Illager Invasion event or find patrol; verify it works
- [ ] Note in Tester Notes: does the difficulty feel right? Any biomes/situations where spawns feel overwhelming?

---

## 10. Passive Mob Mods

- [ ] **Critters and Companions** — try taming a critter (e.g. ferret or robin); verify taming mechanic works
- [ ] **Critters and Companions** — verify no conflict with existing mob mods or crashes near new animals

---

## 11. Sparse Structures

- [ ] Structures feel less dense than vanilla (harder to find, more meaningful when found)
- [ ] No crashes or world gen errors related to structure frequency changes

---

## 12. Deferred — Requires Server / Multiplayer

- Illager Invasion group event: verify the event scales appropriately with multiple players online
- Born in Chaos + Legendary Monsters difficulty at scale: note if mob counts/difficulty feels overwhelming with a full group
- CTOV village trading: verify multiple players can use the same village's trading hall without conflict
- Chunk loading with new world gen: run Chunky pregen after establishing a base and verify no TPS drop

---

## 13. Tester Notes

<!-- Broken things, surprises, difficulty feedback, structure quality notes -->
