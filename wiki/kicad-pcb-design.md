# KiCad PCB Design

## Summary

This page tracks the PCB design for the table football feedback system.

## Components

Known components from project notes:

- Raspberry Pi Pico 2W main board
- Raspberry Pi Pico 2W I/O or secondary board
- EA DOGL128L-6 display, 128x64 reflective LCD
- Connector option A with 8 pins

## Design Notes

The user is designing the PCB step by step in KiCad and wants to add both the LCD connector and the LCD representation.

## LCD Notes

Display: EA DOGL128L-6, 128x64 reflective LCD.

Important checks before final PCB:

- Confirm exact pinout from the datasheet.
- Confirm voltage levels.
- Confirm interface type.
- Confirm connector footprint and pin numbering.
- Confirm backlight or no-backlight variant, if applicable.
- Confirm contrast circuitry requirements.

## Connector Notes

Current decision: Option A, 8 pins.

Add exact connector pin mapping here:

| Pin | Signal | Notes |
|---:|---|---|
| 1 | TBD | |
| 2 | TBD | |
| 3 | TBD | |
| 4 | TBD | |
| 5 | TBD | |
| 6 | TBD | |
| 7 | TBD | |
| 8 | TBD | |

## Open Questions

- What is the exact LCD interface wiring?
- Which Pico pins are assigned to LCD signals?
- Is level shifting required?
- Is the selected KiCad footprint correct for the physical connector?
- Does the schematic include power, ground, decoupling, and reference labels correctly?

## Related Pages

- [[index]]
