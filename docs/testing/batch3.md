# FuzzCraft 4 — Batch 3 Testing: Tech Extras & Food

## Summary
**Pack version:** 0.3.1 (initial) → 0.3.4 (current)
**Test date:** <tester fills in>
**Tester:** <tester fills in>
**Play mode:** Single player

## Known Issues
None known.

---

## 1. Launch & Stability

- [x] Client launches without crash
- [x] No error splash on startup
- [x] Title screen loads correctly
- [x] New world generates and loads without crash
- [x] No immediately obvious console errors on world load

---

## 2. Regression — Batch 1 & 2

- [x] EMI recipe viewer opens and is functional
- [x] JourneyMap minimap visible in-game
- [x] Create contraptions load and run (e.g. basic shaft + gear setup)
- [x] CC: Tweaked — place and open a computer, confirm Lua prompt
- [x] Refined Storage grid accessible and functional
- [x] Silent Gear — craft a basic tool using Silent Gear parts
- [x] Sophisticated Backpacks — craft and open a basic backpack
- [ ] Better ModList — press F8 (or configured key) to open the mod list overlay; confirm it works *(replaced Fzzy Config — not yet tested)*

---

## 3. Productive Bees

- [x] Honeycomb block placed, bees visible and active in world
- [x] Productive Bee spawn eggs present in EMI / creative
- [x] Check EMI for Productive Bees recipes (nest, honeycomb processing)
- [x] Place an Advanced Beehive; confirm bees can be housed
- [x] Productive Bees config screen accessible *(config button greyed out — cosmetic only, not a real issue)*

---

## 4. Farmer's Delight

- [x] Farmer's Delight crops appear in creative and in EMI
- [x] Craft a Cutting Board and Knife; perform a cutting recipe
- [x] Craft a Cooking Pot; cook a Farmer's Delight recipe
- [x] Check basic food items appear in EMI with correct recipes

---

## 5. Create: Slice & Dice

- [x] Slicer machine appears in EMI
- [x] Place a Slicer connected to a Create rotation source; confirm it spins
- [x] Run a Farmer's Delight cutting recipe through the Slicer via Create automation
- [x] Check EMI for Slice & Dice compat recipes *(Slicer automates Cutting Board recipes — no separate "Slicer" recipe type in EMI; this is expected behaviour)*

---

## 6. Botany Pots + Botany Trees

- [x] Craft a Botany Pot; plant a vanilla crop in it
- [x] Confirm crop grows over time in the pot
- [x] Craft a Botany Tree Pot (from Botany Trees); plant a sapling
- [x] Confirm tree grows in the pot
- [x] Check EMI for Botany Pots recipes and crop growth entries *(recipes visible; growth times not shown as "use" recipes — expected, look up the Botany Pot item directly)*
- [x] Hopper below a Botany Pot — confirm auto-harvest works

---

## 7. Spice of Life: Carrot Edition

- [x] Food diversity tracker visible — craft Book + Carrot to get the food list book
- [x] Eat several different foods; confirm heart bonus accumulates at milestones *(milestone values need config tuning — open item)*
- [x] Check food history — command is `/foodlist size`
- [x] Confirm eating the same food repeatedly does NOT increase the counter *(no negatives in Carrot Edition — expected)*

---

## 8. AppleSkin

- [x] Hunger/saturation tooltip visible when hovering over food in inventory
- [x] Hunger restore preview visible on HUD while holding food
- [x] Saturation bar visible on HUD (overlay on hunger bar)

---

## 9. Powah

- [x] Powah creative tab visible with all items
- [x] Craft or spawn a Furnator (basic generator); place it and fuel with coal — confirm RF generation
- [x] Place an Energy Cell; confirm it receives RF from the Furnator
- [x] Wire up a basic consumer (e.g. place a Refined Storage Controller nearby); confirm RF transfer
- [x] Check EMI for Powah recipes
- [x] GuideME guide book — check if accessible (right-click or recipe)

---

## 10. Delight Suite *(new — v0.3.3)*

These mods are all Farmer's Delight addons. The goal is to spot crashes, missing recipes, or obvious conflicts — not to test every item in every mod.

- [ ] Launch with delight suite loaded — no crash on world load
- [ ] Open EMI and confirm delight mod items are present (spot-check a few: Ocean's Delight fish dish, Cultural Delights, My Nether's Delight)
- [ ] Craft one recipe from at least 3 different delight mods to confirm Cooking Pot / Cutting Board integration works
- [ ] Brewin' & Chewin' — craft a basic drink; confirm brewing mechanic works
- [ ] Aquaculture 2 — fish with a basic rod; confirm new fish types catch correctly
- [ ] Aquaculture Delight — check EMI for Aquaculture fish cooking recipes
- [ ] TofuDelight / TofuCraftReload — check tofu items appear in EMI with recipes
- [ ] Crabber's Delight — check crab items appear in EMI
- [ ] Farmer's Knives — craft a knife variant; confirm it performs cutting recipes like the FD knife
- [ ] Dungeon's Delight — check dungeon loot table items appear in EMI
- [ ] Display Delight — place a food display item; confirm food can be placed on it
- [ ] Storage Delight — craft a storage item; confirm it functions
- [ ] No obvious recipe conflicts between delight mods in EMI (flag any duplicates)

---

## 11. Botany Pots Tiers *(new — v0.3.3)*

- [ ] Botany Pots Tiers items appear in EMI / creative
- [ ] Craft a tiered pot (e.g. Iron Botany Pot); confirm it accepts crops
- [ ] Confirm tiered pot grows crops faster than the base Botany Pot
- [ ] Hopper below a tiered pot — confirm auto-harvest still works

---

## 12. EMI Suite *(new — v0.3.4)*

- [ ] EMI opens cleanly with no error toasts on first load
- [ ] TMRV — no crash on load; confirms no errors in log
- [ ] EMI++ — opens cleanly; UI enhancements visible (favourites, search) ⚠️ config tuning deferred to Batch 7
- [ ] Refined Storage EMI Integration — open RS grid; confirm crafting recipes visible in EMI from the grid
- [ ] EMI Ores — search "ore" in EMI; confirm ore generation info entries are present
- [ ] EMI Loot — look up a mob (e.g. Zombie) in EMI; confirm loot table entries are visible
- [ ] EMI Enchanting — open an enchanting table; confirm EMI shows enchant cost/level info
- [ ] EMIffect — hover over a potion or food with an effect in EMI; confirm effect details shown
- [ ] Extra Mod Integrations — spot-check a mod that wouldn't normally have EMI support (e.g. Aquaculture, a delight addon); confirm recipes visible

---

## 13. Jade Addons *(new — v0.3.4)*

- [ ] Jade tooltip visible when looking at a Create machine (shaft, press, etc.)
- [ ] Jade tooltip visible when looking at a Productive Bee hive
- [ ] Jade tooltip visible when looking at a Powah generator — confirm RF output shown
- [ ] Jade tooltip visible when looking at a Refined Storage machine
- [ ] No crash or missing tooltip errors in the Jade overlay

---

## 14. Deferred — Requires Server / Multiplayer

- FTB Chunks — chunk claiming with multiple players
- Productive Bees — bee syncing across server/client
- Powah — RF network under load with multiple players consuming

---

## 15. Tester Notes

### Round 1 (v0.3.1)
1. Productive Bees: config button greyed out — cosmetic only, not a real issue; resolved in checklist
2. Spice of Life: UI is a book crafted with Book + Carrot — working; updated in checklist
3. Spice of Life: command is `/foodlist size` — working; updated in checklist
4. Spice of Life: no negative effects in Carrot Edition; eating same food doesn't increase counter — expected
5. Spice of Life: milestone hearts working — milestone values need config tuning (open item, deferred)
6. Slice & Dice: no "Slicer uses" in EMI — expected; Slicer automates Cutting Board recipes
7. Botany Pots: growth times not shown in EMI — expected; look up pot item directly

### Round 2 (v0.3.4)
<!-- Broken things, surprises, unexpected behaviour, suggestions -->