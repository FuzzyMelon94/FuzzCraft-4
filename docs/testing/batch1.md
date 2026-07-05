# FuzzCraft 4 — Batch 1 Testing: Foundation

## Summary
**Pack version:** 0.1.1
**Test date:** 
**Tester:** FuzzyMelon94
**Play mode:** Single player

## Known Issues
None known.

---

## 1. Launch & Stability

- [ ] Game launches without crash
- [ ] No errors on the main menu log (check Log Begone isn't swallowing anything relevant)
- [ ] Load into a new world — no crash on world gen
- [ ] Load into a new world — no errors in latest.log worth investigating
- [ ] Shaders load correctly via Iris (Complementary recommended — install manually per README)
- [ ] FPS baseline ≥ 60 with shaders enabled

---

## 2. Performance Mods

- [ ] Sodium is active — confirm version `0.6.13` in mod list
- [ ] Sodium Extra options visible in Video Settings
- [ ] Reese's Sodium Options menu present and functional
- [ ] Iris shader selection screen accessible (Options → Video Settings → Shader Packs)
- [ ] ModernFix active — check startup time feels reasonable
- [ ] Spark present — run `/spark profiler start`, wait 30s, `/spark profiler stop` — report generates without error
- [ ] Clumps active — kill a mob, confirm XP orbs merge into single entity

---

## 3. Chunk Management

- [ ] FTB Chunks loaded — `/ftbchunks` command available
- [ ] Claim a chunk — appears highlighted on FTB Chunks map overlay
- [ ] Forceload a claimed chunk — confirm forceload toggles correctly
- [ ] Chunky present — `/chunky` command available
- [ ] Run a small pregen: `/chunky start` with default radius — completes without error
- [ ] Chunky Offline present — confirm mod shows in mod list

---

## 4. Recipe & UI

- [ ] EMI opens correctly (default: `R` on an item)
- [ ] Vanilla recipe book button absent (NERB working)
- [ ] EMI recipe lookup works for a vanilla item (e.g. crafting table)
- [ ] JourneyMap minimap visible in-world
- [ ] JourneyMap full-screen map opens (`J`) and shows explored chunks
- [ ] Waypoint creation works in JourneyMap

---

## 5. QoL Mods

- [ ] BetterF3 — press `F3`, confirm debug screen is formatted/coloured correctly
- [ ] Jade — look at a block/mob, confirm tooltip appears
- [ ] Just Zoom — zoom keybind works (default: `C` hold)
- [ ] Controlling — open keybind screen, confirm search box present
- [ ] Monsters in the Closet — attempt to sleep during the day to confirm it works; at night with nearby mobs, confirm they are highlighted
- [ ] No Chat Reports — confirm icon/indicator present in chat or mod list
- [ ] Better Compatibility Checker — no false mismatch warnings on join
- [ ] Crash Assistant — no interference with normal play; if a crash occurs, confirm it provides a helpful screen
- [ ] ToastBegone — confirm advancement/recipe toasts are suppressed
- [ ] Log Begone — check `config/logbegone.json` filters are loaded; no obviously noisy spam in log
- [ ] Default Options — confirm sprint is toggled on, no view bobbing, other defaults correct
- [ ] NERB — vanilla recipe book absent (covered in §4 but worth a deliberate check here)

---

## 6. Deferred — Requires Server / Multiplayer

- FTB Chunks — chunk claim visibility between players, team claiming
- FTB Teams — team creation and management
- JourneyMap — player position sharing between clients
- No Chat Reports — server-side behaviour

---

## 7. Tester Notes

<!-- Anything broken, surprising, or worth flagging for the next session -->
