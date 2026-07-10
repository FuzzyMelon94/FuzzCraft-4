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

- [ ] Game launches without crash
- [ ] No errors in log related to dimension mods (Twilight Forest, Aether, Deeper and Darker, Bumblezone, Dimensional Dungeons, Dimensional Pockets II)
- [ ] No errors related to delight addons (Twilight's Flavor & Delight, Aether's Delight)
- [ ] No errors related to Lootr
- [ ] Main menu loads normally — no missing textures or broken UI

---

## 2. Regression — Batches 1–5

- [ ] EMI recipe viewer opens and shows recipes — no blank UI
- [ ] Create machines still function (place a Mechanical Press, verify it works)
- [ ] Farmer's Delight cooking pot still functions
- [ ] Ars Nouveau spell casting still works (Projectile + Harm)
- [ ] Overworld world gen intact — open JourneyMap and verify varied biomes still present
- [ ] No obvious performance regression — framerate consistent with prior batches

---

## 3. The Twilight Forest

Use `/forge generate` or just build a TF portal (2×2 water pool surrounded by flowers, drop a diamond in).

- [ ] Portal crafting works — place flowers around a 2×2 water pool and drop a diamond in
- [ ] Portal opens and transports to Twilight Forest dimension
- [ ] Twilight Forest generates correctly — trees, twilight biomes, no corrupted terrain
- [ ] At least one TF structure is visible or locatable — `/locate structure twilightforest:hedge_maze` or similar
- [ ] Mobs spawn in TF correctly (Twilight Wraiths, Skeleton Druids, etc.)
- [ ] Twilight's Flavor & Delight — find a TF food ingredient (e.g. Torchberries, Meef) and verify it shows a recipe in EMI
- [ ] JourneyMap renders the TF dimension map correctly (no black void)
- [ ] Return portal works — death in TF or re-entering the portal exits correctly

---

## 4. The Aether

Build an Aether portal (glowstone frame, water bucket to activate).

- [ ] Portal crafts and activates correctly (glowstone frame + water)
- [ ] Portal transports to the Aether
- [ ] Aether generates correctly — floating islands, Aether biomes, no corrupted terrain
- [ ] Vanilla Aether content present — Golden Oak trees, Aerwhales, Phyg, Moa
- [ ] **Deep Aether** — locate the Deep Aether sub-dimension or Deep Aether-specific biomes/structures; verify generation
- [ ] **Aether Villages** — `/locate structure aether_villages:village` or explore until a village is found; verify it generates correctly and has villagers
- [ ] **Explore Ruins: The Aether** — `/locate structure explore_ruins_aether:` (tab-complete for a structure name) — verify a ruin generates
- [ ] **Aether's Delight** ⚠️ — find an Aether food ingredient and verify it appears in EMI; no crashes during crafting/cooking
- [ ] JourneyMap renders the Aether dimension map correctly
- [ ] Return portal / falling through the void returns to overworld correctly

---

## 5. Deeper and Darker

Deeper and Darker expands the deep dark. No portal — find an Ancient City.

- [ ] `/locate structure minecraft:ancient_city` — locate an Ancient City
- [ ] Deeper and Darker blocks and content are present in or around the Ancient City (check for Sculk Stone, Otherside blocks, etc.)
- [ ] The Otherside dimension portal (if present) opens and transports correctly
- [ ] No crashes near Ancient Cities or Deeper and Darker content
- [ ] Deeper and Darker mobs spawn (if any) — verify no conflict with Born in Chaos / Legendary Monsters variants

---

## 6. The Bumblezone

Find a bee nest in the overworld (or craft a bee-related item to trigger the portal).

- [ ] Bumblezone portal/entry method works — enter the dimension
- [ ] Bumblezone generates correctly — honeycomb terrain, bee-themed structures
- [ ] Bees spawn and behave correctly inside the Bumblezone
- [ ] No crashes on entry/exit
- [ ] JourneyMap renders the Bumblezone map

---

## 7. Dimensional Dungeons

Dimensional Dungeons are instanced — triggered by finding a dungeon entrance or using the mod's item.

- [ ] Locate or trigger a Dimensional Dungeon entrance (check mod's advancement or crafting recipe in EMI)
- [ ] Dungeon instance generates and loads without crash
- [ ] Dungeon has procedurally generated rooms and loot chests
- [ ] Lootr — dungeon loot chests are instanced (each player sees their own loot)
- [ ] Exiting the dungeon returns to the correct overworld position
- [ ] No TPS drop or lag spike on dungeon generation

---

## 8. Dimensional Pockets II

- [ ] Craft a Pocket Dimension Linker or equivalent entry item (check EMI for recipe)
- [ ] Pocket dimension opens and is a personal empty space
- [ ] Place a few blocks inside — verify they persist on re-entry
- [ ] Exit pocket dimension returns to correct overworld position
- [ ] No crash on entry/exit

---

## 9. Lootr

- [ ] Find a vanilla dungeon or structure chest — verify it is a Lootr chest (right-click opens personal loot)
- [ ] Loot a Lootr chest — verify the chest does not show as looted to others (multiplayer test deferred)
- [ ] Lootr chests appear in TF structures (if accessible during testing)
- [ ] No EMI recipe errors or Lootr-related log spam

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
