# RP2350B_DualADC_DualPCM
This is a PCB to neatly package a RP2350B, two AD9226 ADC PCBs and two PCM1802 audio boards for capture with hsdaoh.
Specifically designed to still be usefull without smds (no head switch input then). Through-hole soldering only works just fine.

For use with [https://github.com/steve-m/hsdaoh-rp2350/tree/pcm1802](https://github.com/steve-m/hsdaoh/tree/dual_12bit_adc)

<img src="https://github.com/Sev5000/RP2350B_DualADC_DualPCM/blob/main/DualADC.png?raw=true" alt="">

Features:
- No SMD soldering needed! Works fine just connecting breakout boards
- Socket for a Pimoroni LGA2350B and RP2350 and its periphery
- The protected head switch input with footprints for edge and horizontal SMA/SMB
- Socket for USB C and Micro B breakouts
  
<img src="https://github.com/Sev5000/RP2350B_DualADC_DualPCM/blob/main/DualADC.webp?raw=true" alt="">

Bill of material: 
- 1x This PCB (Send the Gerber .zip to JLC, PCBWay, ..)
- 2x AD9226: https://aliexpress.com/item/1005003038271519.html
- 2x PCM1802: https://aliexpress.com/item/1005006412873984.html
- 4x RCA-105 or RCA-106: https://aliexpress.com/item/1005006152724809.html
- 2x 9pin 2.54mm pin-socket header 
- 2x 2x10pin 2.54mm pin-socket header
- 2x 3pin 2.54mm pin header (remove the center pin for connecting R/L of the PCM1802)
- 2x 3pin 2.54mm pin-socket header (remove the center pin for connecting R/L of the PCM1802)
- 1x vertical 6mm push button: https://aliexpress.com/item/1005005831153897.html (horizontal soldered in vertical and a drop of glue for stability works as well)

No SMD variant:
- 1x Adafruit DVI breakout board
- 4x 2x8pin 2.54mm pin-socket header
- Either Adafruit USB Micro-B Breakout Board or Adafruit USB C Breakout Board

SMD Variant with LGA2350B:
- Regular HDMI connector
- micro USB connector
- 8× 0402 270 ohm resistors
- 4x 0805 100nF ceramic capacitors
- For experimental EDID communication and HPD: 4x SOD123 3.3V Zener, 4x 0402 ~27 ohm resistors, 2x 0402 2k2 ohm resistors

For head switch input:
- 1x SOD123 3.3V zener diode
- 1x SOD123 standard diode
- 1x 0805 1k resistor
- 1x edge SMA/SMB or horizontal SMA/SMB and/or 2pin header

Notes:
- Soldering the RP2350B and its periphery might work but was not tested so far.
- The PCM1802 board needs MODE0 and MODE1 bridged *and* connected to 3.3V with a wire (Those boards have a design error):

<img src="https://raw.githubusercontent.com/Sev5000/Pico2_12bitADC_PCMAudio/refs/heads/main/PCM1802Mod.webp" alt="">
