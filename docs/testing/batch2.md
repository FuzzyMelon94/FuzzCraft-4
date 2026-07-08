# FuzzCraft 4 — Batch 2 Testing: Tech Core

## Summary
**Pack version:** 0.2.1–0.2.5
**Test date:** 2026-07-06
**Tester:** FuzzyMelon94
**Play mode:** Single player

## Known Issues

- **Create: Enchantment Industry** was added at a `preview-alpha` version (`2.5.0-preview-alpha1`). Requires Create: Dragons Plus dep (included). Expect rough edges — watch for crashes around enchanting contraptions.
- **Steam 'n' Rails** is an unofficial 1.21.1 port (`railways-0.3.0-alpha.2`). Alpha status — trains and scheduling are the primary risk area.
- **Create: CC Better Recipes** was added unintentionally via the `cc-create` slug — confirmed wanted, keeping it.
- **Railways Navigator** depends on DragonLib (beta). Watch for any startup warnings from this dep.

---

## 1. Launch & Stability

- [x] Game launches without crashes
- [x] No errors in log related to Create, CC:Tweaked, or any new mod on startup
- [x] All mods show as loaded in the mod list (check count ~77)

---

## 2. Regression — Batch 1

- [x] EMI opens and shows recipes correctly
- [x] JourneyMap minimap renders
- [x] Jade tooltips appear on blocks
- [x] FTB Chunks map opens (`/ftbchunks map`)
- [x] Sodium/Iris options accessible (Video Settings → Shaders)

---

## 3. Create Core

- [x] Create tab visible in EMI/creative menu
- [x] Kinetic blocks (shaft, cogwheel, mechanical bearing) can be placed and connected
- [x] Stress/RPM display works on a shaft (right-click with wrench or goggles)
- [x] Crafts & Additions: motor and generator available in creative
- [x] Curios Jetpack: equip jetpack in Curios slot, verify flight
- [x] Enchantment Industry ⚠️: liquid XP tank and inscription machine available in creative — place one and verify no crash
- [x] Ore Excavation: mechanical drill with excavation upgrade mines ore veins
- [x] Molten Vents: check if vents generate in world (may require exploring or using `/locate` — see mod docs for structure name)
- [x] Fishing Bobber Detector: place detector over water, cast rod, verify redstone signal on bite

---

## 4. Steam 'n' Rails ⚠️

- [x] SnR tab visible in EMI/creative menu
- [x] Track pieces can be placed
- [x] Locomotive can be placed on track
- [x] Train schedule screen opens without crash
- [x] Bells & Whistles cosmetic parts available in creative
- [x] Blocks & Bogies: additional bogies available
- [x] Threaded Trains: check no console errors on train movement
- [x] Railways Navigator: open navigator GUI (check keybind or item), verify no crash

---

## 5. ComputerCraft

- [x] Place a computer, power it, open terminal
- [x] `help` command works in terminal
- [x] CC:C Bridge: attach a Create peripheral (e.g. speedometer) to a computer, verify it's accessible via `peripheral.find()`
- [x] Advanced Peripherals: place an Energy Detector or Geo Scanner, verify peripheral wraps in CC terminal
- [x] Advanced Peripherals RS Bridge: attach to a Refined Storage controller, verify RS system readable from CC (requires RS to be set up)
- [x] CC Total Logistics: check mod items available in creative
- [ ] CC Redstone Link Bridge: verify Create redstone links accessible from CC peripheral — not confirmed via `peripherals` command; try `peripheral.getNames()` adjacent to bound Redstone Link block. Deferred.

---

## 6. Silent Gear

- [x] Open EMI, find Silent Gear material analysis recipe
- [x] Craft basic gear part (head, rod) using available materials
- [x] Craft a tool from parts, verify it works
- [x] No crash on tooltip hover for Silent Gear items

---

## 7. Storage

- [x] **Refined Storage:** Place controller, disk drive, crafting grid — verify RS system powers on and items can be stored/retrieved
- [x] **Storage Drawers:** Place a drawer, insert items, verify display updates
- [x] **Sophisticated Backpacks:** Craft a basic backpack, equip in Curios slot, verify inventory opens

---

## 8. Create Decorative & Utility Addons

This batch includes many decorative/building mods. A quick creative sanity check — not exhaustive.

- [x] Copycats+: blocks visible in creative tab; framed shapes not in EMI item list — resolved via Fzzy Config. EMI absence is by design (no standard recipe to index; blocks applied via right-click mechanic).
- [x] Create Deco / Create Connected / Create Encased / Create Framed / Create Oxidized / Design n' Decor / Create Interiors: each has items visible in creative — no missing textures or crash on placement
- [x] Power Loader: place a Power Loader, verify it chunk-loads the target area while receiving rotational power
- [x] Dynamic Lights: Create items (e.g. blaze lantern) emit dynamic light when held
- [x] Sound of Steam: Create machines produce enhanced audio
- [x] Shuffle Filter / Extra Gauges: items exist in creative, no crash on placement
- [x] Trading Floor: trading post block available, opens UI without crash
- [x] Create Ore Excavation Deposits: deposits config visible (check config or log output for generation)

---

## 9. Deferred — Requires Server / Multiplayer

- Train network with multiple players, scheduling across server chunks
- FTB Chunks forceloading interaction with Power Loader
- RS system shared between multiple players
- CC scripts running on server tick (Total Logistics, Chunky automation)

---

## Tester Notes

<!-- Broken things, surprises, anything to feed back -->
1. ~~Appears you missed the actual Create: Jetpack mod - we have curios, but no actual jetpack.~~ Fixed in 0.2.3 — Create: Jetpack added. Swapped for Create: Stuff 'N Additions in 0.2.4 (includes jetpack + more).
2. Doesn't look like the Redstone Link is visible via the `peripherals` command — try `peripheral.getNames()` in CC terminal with computer placed directly adjacent to a bound Redstone Link block.
3. Note: Trading floor doesn't have a UI - tested as per in game ponder, working as expected (no issue, just a note)
4. Note: Sound of Steam doesn't just give Create machines enhanced audio, it adds functional organs (also working, just a note)
5. Note: Dynamic Lights - again, not what the mod does. This one adds dynamic lighting support for contraptions (also working, no issues, just a note)
6. Copycats+ not in EMI — resolved via Fzzy Config. EMI absence is expected (no standard recipe; apply texture by right-clicking a copycat block with any block).