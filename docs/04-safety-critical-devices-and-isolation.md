# 04 Safety-critical devices and isolation

[← Back to README](../README.md)

## Isolation points

| Work on | Isolate | Notes |
|---|---|---|
| Heating junction box, BDR91s, zone valves, Danfoss TS715Si | **Boiler: Wylex B6 30 mA RCBO** | The box's only supply; the timer is on the same circuit |
| Cylinder wiring panels | **Boiler B6 and Water heater: Wylex B16 30 mA RCBO** | Each panel also carries the immersion supply |
| Boiler internals | Boiler B6 + the boiler's own isolator | **Gas Safe engineer only** |

Prove dead at the point of work every time. Long parallel runs can show tens of volts of induced pickup on dead conductors with a high-impedance meter: cross-check before trusting a reading ([A4 §1](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A4-junction-box-survey-and-wiring.md#1-safe-isolation)).

## Devices that must never be bypassed

| Device | Where | Why |
|---|---|---|
| Cylinder **boiler-control module**: stat + **manual-reset overheat cut-out** (×2) | Each cylinder's lower panel; probes in the element head's **bottom pocket** | G3: stops the primary heating the cylinder whatever the controls do. In series with the valve motor |
| Cylinder temperature/pressure relief valves, expansion relief valves, tundishes | Plant room | G3 discharge safety |
| **Cotherm element control** (thermostat + safety cut-out), when the immersion is used | Top pocket of the element head (swapped with the CS92) | The immersion must never run without it ([A7](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration/blob/main/docs/A7-immersion-backup-swap-procedure.md)) |
| Boiler internal limits | Boiler | Gas Safe |
| Smoke/heat/CO alarms | Separate circuit | Life safety |

## Re-energising the heating
1. **Danfoss TS715Si on permanent ON** (it still gates both hot-water relays).
2. BDR91s reporting in Home Assistant.
3. Heating and hot water both run; cylinder stats set at or above the Evohome DHW setpoint.
