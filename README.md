# Plimsoll

![plimsoll](plimsoll.png)

Prototype design for STM32F072 and HX717 based strain gauge for use as a Klipper load cell.

Initial batch ordered for testing with JLCPCB.  About 5.5 USD cost per board.

Smallish size, 20x50 mm footprint.  M2.5 mounting holes.

4 layer PCB all parts on top side.

MCU selected for crystal less USB operation with minimum of 64k flash for firmware.  

Separate low noise, high PSRR for analog Vdd supply.

HX717 default data rate 320 Hz.  Adjustable with solder jumpers.

### Todo:

- [ ] Evaluate alternate MCUs / USB options for cost/availability
- [ ] Evaluate variants using other ADCs
- [ ] Would MCU less design be better (does firmware support multiple ADC)
- [ ] Test performance of initial batch