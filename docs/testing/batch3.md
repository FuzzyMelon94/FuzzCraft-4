# FuzzCraft 4 — Batch 3 Testing: Tech Extras & Food

## Summary
**Pack version:** 0.3.4
**Test date:** <tester fills in>
**Tester:** <tester fills in>
**Play mode:** Single player

## Known Issues
None known.

---

## 1. Launch & Stability

- [ ] Client launches without crash
- [ ] No error splash on startup
- [ ] Title screen loads correctly
- [ ] New world generates and loads without crash
- [ ] No immediately obvious console errors on world load

---

## 2. Regression — Batch 1 & 2

- [ ] EMI recipe viewer opens and is functional
- [ ] JourneyMap minimap visible in-game
- [ ] Create contraptions load and run (e.g. basic shaft + gear setup)
- [ ] CC: Tweaked — place and open a computer, confirm Lua prompt
- [ ] Refined Storage grid accessible and functional
- [ ] Silent Gear — craft a basic tool using Silent Gear parts
- [ ] Sophisticated Backpacks — craft and open a basic backpack
- [ ] Better ModList — press F8 (or configured key) to open the mod list overlay; confirm it works

---

## 3. Productive Bees

- [ ] Honeycomb block placed, bees visible and active in world
- [ ] Productive Bee spawn eggs present in EMI / creative
- [ ] Check EMI for Productive Bees recipes (nest, honeycomb processing)
- [ ] Place an Advanced Beehive; confirm bees can be housed
- [ ] Productive Bees — confirm a config screen is accessible somewhere in-game (Fzzy Config is back as a dep; check Options → Mod Options or similar)

---

## 4. Farmer's Delight

- [ ] Farmer's Delight crops appear in creative and in EMI
- [ ] Craft a Cutting Board and Knife; perform a cutting recipe
- [ ] Craft a Cooking Pot; cook a Farmer's Delight recipe
- [ ] Check basic food items appear in EMI with correct recipes

---

## 5. Create: Slice & Dice

- [ ] Slicer machine appears in EMI
- [ ] Place a Slicer connected to a Create rotation source; confirm it spins
- [ ] Run a Farmer's Delight cutting recipe through the Slicer via Create automation
- [ ] Check EMI for Slice & Dice compat recipes (note from round 1: Slicer automates Cutting Board recipes — look up the Cutting Board recipe for an item, the Slicer runs those same recipes in-world)

---

## 6. Botany Pots + Botany Trees

- [ ] Craft a Botany Pot; plant a vanilla crop in it
- [ ] Confirm crop grows over time in the pot
- [ ] Craft a Botany Tree Pot (from Botany Trees); plant a sapling
- [ ] Confirm tree grows in the pot
- [ ] Check EMI for Botany Pots recipes and crop growth entries (note from round 1: growth times don't appear as "use" recipes — this is expected; look up the Botany Pot item in EMI for the full list of what can be grown)
- [ ] Hopper below a Botany Pot — confirm auto-harvest works

---

## 7. Spice of Life: Carrot Edition

- [ ] Food diversity tracker visible — it's a book; craft with a Book + Carrot to get the food list
- [ ] Eat several different foods; confirm heart bonus accumulates at milestones
- [ ] Check `/foodlist size` to see eaten food history
- [ ] Confirm eating the same food repeatedly does NOT increase the counter (expected — no negatives in Carrot Edition)

---

## 8. AppleSkin

- [ ] Hunger/saturation tooltip visible when hovering over food in inventory
- [ ] Hunger restore preview visible on HUD while holding food
- [ ] Saturation bar visible on HUD (overlay on hunger bar)

---

## 9. Powah

- [ ] Powah creative tab visible with all items
- [ ] Craft or spawn a Furnator (basic generator); place it and fuel with coal — confirm RF generation
- [ ] Place an Energy Cell; confirm it receives RF from the Furnator
- [ ] Wire up a basic consumer (e.g. place a Refined Storage Controller nearby); confirm RF transfer
- [ ] Check EMI for Powah recipes
- [ ] GuideME guide book — check if accessible (right-click or recipe)

---

## 10. Delight Suite

These mods are all Farmer's Delight addons. The goal is to spot crashes, missing recipes, or obvious conflicts — not to test every item in every mod.

- [ ] Launch with delight suite loaded — no crash on world load
- [ ] Open EMI and confirm delight mod items are present (spot-check a few: Ocean's Delight fish dish, Cultural Delights, Nether's Delight)
- [ ] Craft one recipe from at least 3 different delight mods to confirm Cooking Pot / Cutting Board integration works
- [ ] Brewin' & Chewin' — craft a basic drink; confirm brewing mechanic works
- [ ] Aquaculture 2 — fish with a basic rod; confirm new fish types catch correctly
- [ ] Aquaculture Delight — check EMI for Aquaculture fish cooking recipes
- [ ] TofuDelight / TofuCraftReload — check tofu items appear in EMI with recipes
- [ ] Crabber's Delight — check crab items appear in EMI
- [ ] Farmer's Knives — craft a knife variant; confirm it performs cutting recipes like the FD knife
- [ ] Dungeon's Delight — check dungeon loot table items appear in EMI (loot bags etc.)
- [ ] Display Delight — place a food display item; confirm food can be placed on it
- [ ] Storage Delight — craft a storage item from the mod; confirm it functions
- [ ] No obvious recipe conflicts between delight mods visible in EMI (flag any duplicates)

---

## 11. Botany Pots Tiers

- [ ] Botany Pots Tiers items appear in EMI / creative
- [ ] Craft a tiered pot (e.g. Iron Botany Pot); confirm it accepts crops
- [ ] Confirm tiered pot grows crops faster than the base Botany Pot
- [ ] Hopper below a tiered pot — confirm auto-harvest still works

---

## 12. EMI Suite

- [ ] EMI opens cleanly with no error toasts on first load
- [ ] TMRV — no crash; any JEI-only mod recipes visible in EMI (hard to test directly — just confirm no errors)
- [ ] EMI++ — opens cleanly; check if any UI enhancements are visible (favourites, search improvements) ⚠️ config tuning deferred to Batch 7
- [ ] Refined Storage EMI Integration — open RS grid; confirm crafting recipes visible in EMI from the grid interface
- [ ] EMI Ores — search "ore" in EMI; confirm ore generation info entries are present
- [ ] EMI Loot — look up a mob (e.g. Zombie) in EMI; confirm loot table entries are visible
- [ ] EMI Enchanting — open an enchanting table; confirm EMI shows enchant cost/level info
- [ ] EMIffect — hover over a potion or food with an effect in EMI; confirm effect details shown
- [ ] Extra Mod Integrations — spot-check a mod that wouldn't normally have EMI support (e.g. Aquaculture, a delight addon); confirm recipes visible

---

## 13. Jade Addons

- [ ] Jade tooltip visible when looking at a Create machine (shaft, press, etc.)
- [ ] Jade tooltip visible when looking at a Productive Bee hive
- [ ] Jade tooltip visible when looking at an Aquaculture fishing spot or fish trap (if applicable)
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
1. Productive Bees: config button greyed out — resolved (Fzzy Config is back as dep; retest)
2. Spice of Life: UI is a book — crafted with Book + Carrot; working
3. Spice of Life: command is `/foodlist size` — working; updated in checklist above
4. Spice of Life: no negative effects in Carrot Edition; eating same food doesn't increase counter — expected
5. Spice of Life: milestone hearts working — milestone values need config tuning (deferred, open item)
6. Slice & Dice: no "uses" for Slicer in EMI — expected behaviour; Slicer automates Cutting Board recipes
7. Botany Pots: growth times not shown in EMI — expected; look up pot item directly

### Round 2 (v0.3.4)
<!-- Broken things, surprises, unexpected behaviour, suggestions -->