# Plimsoll

Prototype designs for klipper load cell ADC implementations.

### Alpha Test

<img src="alpha_test/plimsoll%20r0.jpg" alt="plimsoll" style="zoom: 25%;" />

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

### Mini HX717 / Mini ADS1220

<img src="mini_hx717/Screenshot%202025-12-27%20220855.png" alt="mini" style="zoom:25%;" />

Addon for a FYTSEC H36 Toolhead board.  Uses the 2x6 expansion header for clean mounting.

4 layer PCB all parts on top side.

Separate low noise, high PSRR for analog Vdd supply.

HX717 data rate 320 Hz.  

ADS1220 all SPI connections.

### 4ch Underbed

<img src="underbed/underbed.png" alt="mini" style="zoom:25%;" />

4 channel ADS131M04 for underbed applications.  Each load cell can be individually measured and digitally summed.

8.192 MHz clock hardware generator.

Separate low noise, high PSRR for analog Vdd supply.

### Todo:

- [x] Finish Mini ADS1220 design
- [x] Design 4ch underbed sensor board with ADS131M04 
- [x] Place order for boards

## Automated PDF Generation

This repository includes a GitHub Action workflow that automatically generates PDF plots for all KiCad projects. The workflow runs on:
- Pushes to the `main` or `master` branch
- Pull requests
- Manual trigger via workflow dispatch

For each project, schematic diagram PDFs are generated.

The generated PDFs are available as workflow artifacts and can be downloaded from the Actions tab.
