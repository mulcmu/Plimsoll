# Plimsoll

![plimsoll](alpha_test/plimsoll%20r0.jpg)

Prototype designs for load cell ADC implementations.

### Alpha Test

STM32F072 and HX717 based strain gauge for use as a Klipper load cell.

Initial batch ordered for testing with JLCPCB.  About 5.5 USD cost per board.

Firmware and configuration tested with [current community test branch](https://github.com/garethky/klipper/tree/load-cell-probe-community-testing).

Smallish size, 20x50 mm footprint.  M2.5 mounting holes.  Fab house added the smaller tooling holes...

4 layer PCB all parts on top side.

MCU selected for crystal less USB operation with minimum of 64k flash for firmware.

Separate low noise, high PSRR for analog Vdd supply.

HX717 default data rate 320 Hz.  Adjustable with solder jumpers.

> [!NOTE]
>
> Crystal less main clock is problematic with Klipper and maybe the HX717 code.
>
> Works fine 90% of time, but suffers from occasional timeouts during probes.

### Mini HX717

![mini](mini/Screenshot%202025-12-27%20220855.png)

HX717 addon for a FYTSEC H36 Toolhead board.  Uses the 2x6 expansion header for clean mounting.

Untested but ready to order.

4 layer PCB all parts on top side.

Separate low noise, high PSRR for analog Vdd supply.

HX717 data rate 320 Hz.  

### Mini ADS1220

Planned, update mini to use the ADS1220

### Todo:

- [ ] Finish Mini ADS1220 design
- [ ] Design 4ch underbed sensor board with ADS131M04 
- [ ] Place order for boards
