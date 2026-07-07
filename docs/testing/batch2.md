# FuzzCraft 4 — Batch 2 Testing: Tech Core

## Summary
**Pack version:** 0.2.1–0.2.x
**Test date:** 2026-07-06
**Tester:** 
**Play mode:** Single player

## Known Issues

- **Create: Enchantment Industry** was added at a `preview-alpha` version (`2.5.0-preview-alpha1`). Requires Create: Dragons Plus dep (included). Expect rough edges — watch for crashes around enchanting contraptions.
- **Steam 'n' Rails** is an unofficial 1.21.1 port (`railways-0.3.0-alpha.2`). Alpha status — trains and scheduling are the primary risk area.
- **Create: CC Better Recipes** was added unintentionally via the `cc-create` slug. It adds CC:Tweaked recipe access to Create's recipe system. Verify this is wanted or remove it.
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
- [ ] Curios Jetpack: equip jetpack in Curios slot, verify flight
- [x] Enchantment Industry ⚠️: liquid XP tank and inscription machine available in creative — place one and verify no crash
- [x] Ore Excavation: mechanical drill with excavation upgrade mines ore veins
- [x] Molten Vents: check if vents generate in world (may require exploring or using `/locate` — see mod docs for structure name)
- [x] Fishing Bobber Detector: place detector over water, cast rod, verify redstone signal on bite

---

## 4. Steam 'n' Rails ⚠️

- [ ] SnR tab visible in EMI/creative menu
- [ ] Track pieces can be placed
- [ ] Locomotive can be placed on track
- [ ] Train schedule screen opens without crash
- [ ] Bells & Whistles cosmetic parts available in creative
- [ ] Blocks & Bogies: additional bogies available
- [ ] Threaded Trains: check no console errors on train movement
- [ ] Railways Navigator: open navigator GUI (check keybind or item), verify no crash

---

## 5. ComputerCraft

- [x] Place a computer, power it, open terminal
- [x] `help` command works in terminal
- [x] CC:C Bridge: attach a Create peripheral (e.g. speedometer) to a computer, verify it's accessible via `peripheral.find()`
- [x] Advanced Peripherals: place an Energy Detector or Geo Scanner, verify peripheral wraps in CC terminal
- [x] Advanced Peripherals RS Bridge: attach to a Refined Storage controller, verify RS system readable from CC (requires RS to be set up)
- [x] CC Total Logistics: check mod items available in creative
- [ ] CC Redstone Link Bridge: verify Create redstone links accessible from CC peripheral

---

## 6. Silent Gear

- [x] Open EMI, find Silent Gear material analysis recipe
- [x] Craft basic gear part (head, rod) using available materials
- [x] Craft a tool from parts, verify it works
- [x] No crash on tooltip hover for Silent Gear items

---

## 7. Storage

- [ ] **Refined Storage:** Place controller, disk drive, crafting grid — verify RS system powers on and items can be stored/retrieved
- [x] **Storage Drawers:** Place a drawer, insert items, verify display updates
- [x] **Sophisticated Backpacks:** Craft a basic backpack, equip in Curios slot, verify inventory opens

---

## 8. Create Decorative & Utility Addons

This batch includes many decorative/building mods. A quick creative sanity check — not exhaustive.

- [ ] Copycats+: copycat panel available and accepts a block texture
- [ ] Create Deco / Create Connected / Create Encased / Create Framed / Create Oxidized / Design n' Decor / Create Interiors: each has items visible in creative — no missing textures or crash on placement
- [ ] Power Loader: place a Power Loader, verify it chunk-loads the target area while receiving rotational power
- [ ] Dynamic Lights: Create items (e.g. blaze lantern) emit dynamic light when held
- [ ] Sound of Steam: Create machines produce enhanced audio
- [ ] Shuffle Filter / Extra Gauges: items exist in creative, no crash on placement
- [ ] Trading Floor: trading post block available, opens UI without crash
- [ ] Create Ore Excavation Deposits: deposits config visible (check config or log output for generation)

---

## 9. Deferred — Requires Server / Multiplayer

- Train network with multiple players, scheduling across server chunks
- FTB Chunks forceloading interaction with Power Loader
- RS system shared between multiple players
- CC scripts running on server tick (Total Logistics, Chunky automation)

---

## Tester Notes

<!-- Broken things, surprises, anything to feed back -->
1. Appears you missed the actual Create: Jetpack mod - we have curios, but no actual jetpack.
2. Doesn't look like the Redstone Link is visible via the `peripherals` command