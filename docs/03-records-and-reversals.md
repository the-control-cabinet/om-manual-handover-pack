# 03 Records and reversals

[← Back to README](../README.md)

As-built and modification records, each with its reversal. The full survey and procedures live in the system repos; this is the index.

## Modification register

| # | Modification | Date | Record | Reversal |
|---|---|---|---|---|
| M1 | **Evohome replaced the original controls**: landing stats → landing BDR91s on the same cables; Heatmiser UFH controls → HCC80R; hot-water BDR91s between the timer and the cylinder stats; TF/MF zone-valve heads electrically disconnected and latched in manual override | 2018 | [A4 Junction box survey](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A4-junction-box-survey-and-wiring.md) · [A8 Wiring schematics, three stages](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A8-wiring-schematics-three-stages.md) | [A5 Reversal procedure and commissioning tests](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A5-as-built-vs-evohome-and-reversal.md) |
| M2 | **Immersion element controls (Cotherm) removed**; CS92 sensors fitted in their pockets; immersions disconnected (Water heater B16 RCBO off) | 2018 | [A3 Cylinders and sensor placement](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A3-dhw-cylinders-and-sensor-placement.md) | [A7 Immersion backup swap procedure](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A7-immersion-backup-swap-procedure.md) |
| M3 | Plant monitoring added (non-invasive sensors) | 2026 | [Plant monitoring repo](https://github.com/the-control-cabinet/heating-plant-monitoring-esphome) | Remove sensors; no change to the controls |
| M4 | **Junction box tidy-up** (planned): hot-water BDR91s re-wired in 3095Y 5-core on pattresses; Wago 221 at four joints; opto board in its own enclosure; sleeving and labels | Nov 2026 | [A4 §7](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A4-junction-box-survey-and-wiring.md#7-planned-tidy-up-box-still-isolated) · [A8 stage 3](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A8-wiring-schematics-three-stages.md) · [Opto install](https://github.com/the-control-cabinet/heating-plant-monitoring-esphome/blob/main/docs/11-opto-board-installation.md) | Remove the opto tails and board; the control wiring is unchanged in function |
| M5 | OpenTherm control (planned) | ⟨date⟩ | [OpenTherm repo](https://github.com/the-control-cabinet/opentherm-boiler-control-esphome) | Changeover to Mode A; remove the changeover to restore the original wiring |

## Open and closed checks (raised on a heating-controls wiring course, Oct 2026)

| # | Check | Status | Record |
|---|---|---|---|
| 1 | **Radiator zone valves in manual override:** how far open? | ⏳ Open | Re-power the heads on a permanent live, or replace the bodies (drain-down) |
| 2 | **Pump overrun / minimum-flow path** | ⚠️ **Likely non-compliant**: no automatic bypass found; the boiler manual requires one with TRVs on all radiators or two-port valves. Evidence still to gather: fault history (L1), pipework search, Benchmark sheet | [A6](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A6-pump-overrun-and-bypass.md). Remedy by a Gas Safe engineer: ABV, or one radiator ≥ 0.6 kW left open |
| 3 | **Unvented cylinder high-limit cut-outs** in series with each valve | ✅ **Closed 29 Oct 2026**: verified on both cylinders | [A4 §5](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A4-junction-box-survey-and-wiring.md#5-cylinder-wiring-panels) |
