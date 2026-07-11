# FuzzCraft 4 — Batch 6 Testing: Dimensions

## Summary
**Pack version:** 0.6.1
**Test date:** <tester fills in>
**Tester:** <tester fills in>
**Play mode:** Single player

## Known Issues
- Aether's Delight is beta (v0.1.4.2) — watch for crashes or missing recipes; note anything odd in Tester Notes.
- Mob overhaul mods (Born in Chaos, Legendary Monsters, Enderman/Creeper Overhaul) may spawn in new dimensions — difficulty impact untested. Flag anything that feels unbalanced.
- Lootr scope: default config may not cover all dimension structures. If loot chests in TF/Aether/D&D aren't instanced, note it — config tweak likely needed.
- CTOV + Aether Villages coexistence in the Aether is untested. Flag any village generation weirdness.

---

## 1. Launch & Stability

- [x] Game launches without crash
- [x] No errors in log related to dimension mods (Twilight Forest, Aether, Deeper and Darker, Bumblezone, Dimensional Dungeons, Dimensional Pockets II)
- [x] No errors related to delight addons (Twilight's Flavor & Delight, Aether's Delight)
- [x] No errors related to Lootr
- [x] Main menu loads normally — no missing textures or broken UI

---

## 2. Regression — Batches 1–5

- [x] EMI recipe viewer opens and shows recipes — no blank UI
- [x] Create machines still function (place a Mechanical Press, verify it works)
- [x] Farmer's Delight cooking pot still functions
- [x] Ars Nouveau spell casting still works (Projectile + Harm)
- [x] Overworld world gen intact — open JourneyMap and verify varied biomes still present
- [x] No obvious performance regression — framerate consistent weith prior batches

---

## 3. The Twilight Forest

Use `/forge generate` or just build a TF portal (2×2 water pool surrounded by flowers, drop a diamond in).

- [x] Portal crafting works — place flowers around a 2×2 water pool and drop a diamond in
- [x] Portal opens and transports to Twilight Forest dimension
- [x] Twilight Forest generates correctly — trees, twilight biomes, no corrupted terrain
- [x] At least one TF structure is visible or locatable — `/locate structure twilightforest:hedge_maze` or similar
- [x] Mobs spawn in TF correctly (Twilight Wraiths, Skeleton Druids, etc.)
- [x] Twilight's Flavor & Delight — find a TF food ingredient (e.g. Torchberries, Meef) and verify it shows a recipe in EMI
- [x] JourneyMap renders the TF dimension map correctly (no black void)
- [x] Return portal works — death in TF or re-entering the portal exits correctly

---

## 4. The Aether

Build an Aether portal (glowstone frame, water bucket to activate).

- [x] Portal crafts and activates correctly (glowstone frame + water)
- [x] Portal transports to the Aether
- [x] Aether generates correctly — floating islands, Aether biomes, no corrupted terrain
- [x] Vanilla Aether content present — Golden Oak trees, Aerwhales, Phyg, Moa
- [x] **Deep Aether** — locate the Deep Aether sub-dimension or Deep Aether-specific biomes/structures; verify generation
- [x] **Aether Villages** — `/locate structure aether_villages:village` or explore until a village is found; verify it generates correctly and has villagers
- [x] **Explore Ruins: The Aether** — `/locate structure explore_ruins_aether:` (tab-complete for a structure name) — verify a ruin generates
- [x] **Aether's Delight** ⚠️ — find an Aether food ingredient and verify it appears in EMI; no crashes during crafting/cooking
- [x] JourneyMap renders the Aether dimension map correctly
- [x] Return portal / falling through the void returns to overworld correctly

---

## 5. Deeper and Darker

Deeper and Darker expands the deep dark. No portal — find an Ancient City.

- [x] `/locate structure minecraft:ancient_city` — locate an Ancient City
- [x] Deeper and Darker blocks and content are present in or around the Ancient City (check for Sculk Stone, Otherside blocks, etc.)
- [x] The Otherside dimension portal (if present) opens and transports correctly
- [x] No crashes near Ancient Cities or Deeper and Darker content
- [x] Deeper and Darker mobs spawn (if any) — verify no conflict with Born in Chaos / Legendary Monsters variants

---

## 6. The Bumblezone

Find a bee nest in the overworld (or craft a bee-related item to trigger the portal).

- [x] Bumblezone portal/entry method works — enter the dimension
- [x] Bumblezone generates correctly — honeycomb terrain, bee-themed structures
- [x] Bees spawn and behave correctly inside the Bumblezone
- [x] No crashes on entry/exit
- [x] JourneyMap renders the Bumblezone map

---

## 7. Dimensional Dungeons

Dimensional Dungeons are instanced — triggered by finding a dungeon entrance or using the mod's item.

- [x] Locate or trigger a Dimensional Dungeon entrance (check mod's advancement or crafting recipe in EMI)
- [x] Dungeon instance generates and loads without crash
- [x] Dungeon has procedurally generated rooms and loot chests
- [x] Lootr — dungeon loot chests are instanced (each player sees their own loot)
- [x] Exiting the dungeon returns to the correct overworld position
- [x] No TPS drop or lag spike on dungeon generation

---

## 8. Dimensional Pockets II

- [x] Craft a Pocket Dimension Linker or equivalent entry item (check EMI for recipe)
- [x] Pocket dimension opens and is a personal empty space
- [x] Place a few blocks inside — verify they persist on re-entry
- [x] Exit pocket dimension returns to correct overworld position
- [x] No crash on entry/exit

---

## 9. Lootr

- [x] Find a vanilla dungeon or structure chest — verify it is a Lootr chest (right-click opens personal loot)
- [x] Loot a Lootr chest — verify the chest does not show as looted to others (multiplayer test deferred)
- [x] Lootr chests appear in TF structures (if accessible during testing)
- [x] No EMI recipe errors or Lootr-related log spam

---

## 10. Deferred — Requires Server / Multiplayer

- Lootr instanced loot: verify two players opening the same chest each see their own loot pool
- Twilight Forest progression locks with multiple players: TF bosses lock the next area — test that the lock/unlock is shared correctly across players
- Aether multiplayer: verify portal sync and shared Aether dimension works correctly for all players
- Dimensional Pockets II shared access: test whether another player can enter your pocket dimension and what happens
- Dimensional Dungeons with multiple players: verify dungeon instances are personal or properly shared
- Born in Chaos / Legendary Monsters in new dimensions: note difficulty at group scale
- Aether Villages trading: verify multiple players can interact with the same Aether villager without conflict
- Dimensional Pockets II disk usage: monitor `/data` disk after multiple players have created and used pocket dims

---

## 11. Tester Notes

<!-- Broken things, surprises, difficulty feedback, structure quality notes -->
