# FuzzCraft 4 — Batch 1 Testing: Foundation

## Summary
**Pack version:** 0.1.1–0.1.2
**Test date:** 2026/07/06
**Tester:** FuzzyMelon94
**Play mode:** Single player

## Known Issues
None known.

---

## 1. Launch & Stability

- [x] Game launches without crash
- [x] No errors on the main menu log (check Log Begone isn't swallowing anything relevant)
- [x] Load into a new world — no crash on world gen
- [x] Load into a new world — no errors in latest.log worth investigating
- [x] Shaders load correctly via Iris (Complementary recommended — install manually per README)
- [x] FPS baseline ≥ 60 with shaders enabled

---

## 2. Performance Mods

- [x] Sodium is active — confirm version `0.6.13` in mod list
- [x] Sodium Extra options visible in Video Settings
- [x] Reese's Sodium Options menu present and functional
- [x] Iris shader selection screen accessible (Options → Video Settings → Shader Packs)
- [x] ModernFix active — check startup time feels reasonable
- [x] Spark present — run `/spark profiler start`, wait 30s, `/spark profiler stop` — report generates without error
- [x] Clumps active — kill a mob, confirm XP orbs merge into single entity

---

## 3. Chunk Management

- [x] FTB Chunks loaded — `/ftbchunks` command available
- [x] Claim a chunk — appears highlighted on FTB Chunks map overlay
- [x] Forceload a claimed chunk — confirm forceload toggles correctly
- [x] Chunky present — `/chunky` command available
- [x] Run a small pregen: `/chunky start` with default radius — completes without error
- [x] Chunky Offline present — confirm mod shows in mod list

---

## 4. Recipe & UI

- [x] EMI opens correctly (default: `R` on an item)
- [~] Vanilla recipe book button absent (NERB working) — NERB ScreenMixin broken in v0.4.3 due to Java 21 class version issue; button remains but is cosmetic. Server-side payload reduction confirmed working. Config set to DISABLED — will take effect when NERB is fixed.
- [x] EMI recipe lookup works for a vanilla item (e.g. crafting table)
- [x] JourneyMap minimap visible in-world
- [x] JourneyMap full-screen map opens (`J`) and shows explored chunks
- [x] Waypoint creation works in JourneyMap

---

## 5. QoL Mods

- [x] BetterF3 — press `F3`, confirm debug screen is formatted/coloured correctly
- [x] Jade — look at a block/mob, confirm tooltip appears
- [x] Just Zoom — zoom keybind works (default: `C` hold)
- [x] Controlling — open keybind screen, confirm search box present
- [x] Monsters in the Closet — attempt to sleep during the day to confirm it works; at night with nearby mobs, confirm they are highlighted
- [x] No Chat Reports — confirm icon/indicator present in chat or mod list
- [x] Better Compatibility Checker — no false mismatch warnings on join
- [x] Crash Assistant — no interference with normal play; if a crash occurs, confirm it provides a helpful screen
- [x] ToastBegone — confirm advancement/recipe toasts are suppressed
- [x] Log Begone — check `config/logbegone.json` filters are loaded; no obviously noisy spam in log
- [x] Default Options — sprint=Shift, sneak=Ctrl, bobView off confirmed (required keybindings.txt separate from options.txt)
- [~] NERB — see §4 note; button visible but non-harmful

---

## 6. Deferred — Requires Server / Multiplayer

- FTB Chunks — chunk claim visibility between players, team claiming
- FTB Teams — team creation and management
- JourneyMap — player position sharing between clients
- No Chat Reports — server-side behaviour

---

## 7. Tester Notes

<!-- Anything broken, surprising, or worth flagging for the next session -->
### Performance:
| Metric | Value |
|---|---|
| FPS (no shaders) | 600 min / 1000 max |
| FPS (with shaders) | 300 min / 400 max |
| Client RAM max | 2 GB |
| Server RAM max | 3.2 GB |
| Server TPS (min/med/95%ile/max ms) | 3.4 / 13.3 / 17.0 / 32.2 |

### Issues
1. NERB - recipe button still present, clicking it shows an empty page 1/1 of EMI, nothing else.
2. Default Options - loaded with Ctrl as sprint and Shift as crouch, bobbing is enabled, these are the opposite of what should be set as the defaults, did we add the config?