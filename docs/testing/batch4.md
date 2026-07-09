# FuzzCraft 4 — Batch 4 Testing: Magic

## Summary
**Pack version:** 0.4.1–0.4.2
**Test date:** <tester fills in>
**Tester:** <tester fills in>
**Play mode:** Single player

## Known Issues
None known.

---

## 1. Launch & Stability

- [1] Game launches without crash
- [x] No errors in the log related to Ars Nouveau, Patchouli, GeckoLib, or Ars Delight
- [x] Main menu loads normally; no missing textures or broken UI

---

## 2. Regression — Batch 1–3
e
- [x] EMI recipe viewer opens and shows recipes (no blank UI)
- [x] Create machines still function (place a Mechanical Press, verify it works)
- [x] Farmer's Delight cooking pots still function
- [x] Botany Pots still grow crops
- [x] No obvious performance regression — framerate consistent with prior batches

---

## 3. Ars Nouveau — Core

- [x] Ars Nouveau Patchouli guide book (Worn Notebook) is obtainable and readable
- [x] Spellbook can be crafted (`/recipe give @s ars_nouveau:novice_spellbook` or craft from guide)
- [x] At least one spell can be learned (Glyph press or touch spell)
- [x] Casting a spell (e.g. Projectile + Harm) works and deals damage
- [x] Mana bar appears on HUD while holding the spellbook
- [x] Mana regenerates over time
- [x] Source Jar can be crafted and placed — source accumulates in it over time
- [x] Imbuement Chamber can be crafted — imbuing works (test with Source Gem recipe)
- [x] Enchanting Apparatus can be crafted and used for at least one enchant
- [x] Arcane Pedestal functions correctly alongside the Apparatus
- [x] Familiar (e.g. Bookwyrm) can be summoned via spell or ritual
- [x] At least one ritual can be performed (e.g. Sunrise ritual)

---

## 4. Ars Nouveau — Curios Integration

- [x] Curios slots are present on the player inventory screen
- [x] Ars Nouveau accessory items (e.g. rings, amulets) equip correctly into Curios slots
- [x] No crash or conflict between Curios and existing Create: Curios Jetpack mod

---

## 5. Ars Nouveau — EMI Integration

- [x] Ars Nouveau recipes are visible in EMI (Source Gem, Spellbook, glyphs, etc.)
- [x] Glyph recipes via Enchanting Apparatus show in EMI
- [x] Imbuement Chamber recipes are visible

---

## 6. Ars Delight — Farmer's Delight Compat

- [x] Ars Delight items appear in EMI (search "Ars Delight")
- [x] At least one Ars Delight recipe can be viewed (Cooking Pot or Cutting Board)
- [x] No conflict or crash with existing Farmer's Delight installation

---

## 7. Deferred — Requires Server / Multiplayer

- Multiplayer magic combat: verify spell lag/sync is acceptable with multiple players casting
- Source generation in shared bases (multiple players drawing from same Source network)

---

## 8. Tester Notes

<!-- Broken things, surprises, config concerns, feedback -->
1. Had to remove Sodium Dynamic Lights and Create Dynamic Lights due to Ars bundling the same jar