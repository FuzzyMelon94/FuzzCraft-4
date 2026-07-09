# FuzzCraft 4 — Batch 4 Testing: Magic

## Summary
**Pack version:** 0.4.1
**Test date:** <tester fills in>
**Tester:** <tester fills in>
**Play mode:** Single player

## Known Issues
None known.

---

## 1. Launch & Stability

- [ ] Game launches without crash
- [ ] No errors in the log related to Ars Nouveau, Patchouli, GeckoLib, or Ars Delight
- [ ] Main menu loads normally; no missing textures or broken UI

---

## 2. Regression — Batch 1–3

- [ ] EMI recipe viewer opens and shows recipes (no blank UI)
- [ ] Create machines still function (place a Mechanical Press, verify it works)
- [ ] Farmer's Delight cooking pots still function
- [ ] Botany Pots still grow crops
- [ ] No obvious performance regression — framerate consistent with prior batches

---

## 3. Ars Nouveau — Core

- [ ] Ars Nouveau Patchouli guide book (Worn Notebook) is obtainable and readable
- [ ] Spellbook can be crafted (`/recipe give @s ars_nouveau:novice_spellbook` or craft from guide)
- [ ] At least one spell can be learned (Glyph press or touch spell)
- [ ] Casting a spell (e.g. Projectile + Harm) works and deals damage
- [ ] Mana bar appears on HUD while holding the spellbook
- [ ] Mana regenerates over time
- [ ] Source Jar can be crafted and placed — source accumulates in it over time
- [ ] Imbuement Chamber can be crafted — imbuing works (test with Source Gem recipe)
- [ ] Enchanting Apparatus can be crafted and used for at least one enchant
- [ ] Arcane Pedestal functions correctly alongside the Apparatus
- [ ] Familiar (e.g. Bookwyrm) can be summoned via spell or ritual
- [ ] At least one ritual can be performed (e.g. Sunrise ritual)

---

## 4. Ars Nouveau — Curios Integration

- [ ] Curios slots are present on the player inventory screen
- [ ] Ars Nouveau accessory items (e.g. rings, amulets) equip correctly into Curios slots
- [ ] No crash or conflict between Curios and existing Create: Curios Jetpack mod

---

## 5. Ars Nouveau — EMI Integration

- [ ] Ars Nouveau recipes are visible in EMI (Source Gem, Spellbook, glyphs, etc.)
- [ ] Glyph recipes via Enchanting Apparatus show in EMI
- [ ] Imbuement Chamber recipes are visible

---

## 6. Ars Delight — Farmer's Delight Compat

- [ ] Ars Delight items appear in EMI (search "Ars Delight")
- [ ] At least one Ars Delight recipe can be viewed (Cooking Pot or Cutting Board)
- [ ] No conflict or crash with existing Farmer's Delight installation

---

## 7. Deferred — Requires Server / Multiplayer

- Multiplayer magic combat: verify spell lag/sync is acceptable with multiple players casting
- Source generation in shared bases (multiple players drawing from same Source network)

---

## 8. Tester Notes

<!-- Broken things, surprises, config concerns, feedback -->
