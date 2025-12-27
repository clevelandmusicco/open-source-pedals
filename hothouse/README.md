# Hothouse DSP Pedal Kit

>[!IMPORTANT]
> Remember that all of these materials are made available as [Open Source Hardware](https://oshwa.org/resources/open-source-hardware-definition/) distributed under a [Creative Commons Attribution-ShareAlike 4.0 International license](https://creativecommons.org/licenses/by-sa/4.0/). Before using these materials, be sure to follow the links above and read the [main repo README](/README.md) and [LICENSE](/LICENSE).

The Hothouse is a compact pedal kit for the [Electrosmith Daisy Seed](https://electro-smith.com/products/daisy-seed). You can use it to easily get your Daisy Seed DSP projects off the breadboard and onto your pedalboard, either by compiling and flashing any of the code in [the official repository](https://github.com/clevelandmusicco/HothouseExamples), or by using the [Daisy Web Programmer](https://electro-smith.github.io/Programmer/) with the [pre-compiled binaries](https://github.com/clevelandmusicco/HothouseExamples/releases). And of course, you can also [write your own DSP code for the Hothouse](https://github.com/clevelandmusicco/HothouseExamples/wiki/Creating-your-own-effects). Basically, anything that runs on the Daisy Seed will run on the Hothouse.

This directory contains the open source hardware files for the [Cleveland Music Co. Hothouse DSP Pedal Kit](https://clevelandmusicco.com/hothouse-diy-digital-signal-processing-platform-kit/). Included are the required gerber, BOM, and CPL files required to fabricate your own PCBs at JLCPCB. Also included are suggestions for the various through-hole components and other hardware required.

>[!NOTE]
> No step-by-step tutorial for having the boards fabricated is provided. It's assumed that anyone interested in using these files is already familiar with the fabrication process.

## Overview

The Hothouse design is comprised of three PCBs:
1. The Main PCB,
2. A Switching & LED daughterboard,
3. A Power & Audio I/O daughterboard.

The main PCB is designed for a mix of through-hole and surface-mount components, while the two daughterboards use only through-hole components. The three PCBs are connected by 6-pin ribbon cables. Refer to [the commercial product build docs](https://github.com/clevelandmusicco/HothouseExamples/wiki/Cleveland-Music-Co.-Hothouse-DIY-Digital-Signal-Processing-Pedal-Kit-Build-Guide-(Stereo-Version)) for more information.

All commercial branding has been removed from the PCBs in this repository.

## Resources

* The commercial Cleveland Music Co. Hothouse product based on these files can be found [here](https://clevelandmusicco.com/hothouse-diy-digital-signal-processing-platform-kit/).
* The build documentation for the commercial product is [here](https://github.com/clevelandmusicco/HothouseExamples/wiki/Cleveland-Music-Co.-Hothouse-DIY-Digital-Signal-Processing-Pedal-Kit-Build-Guide-(Stereo-Version)).
* Non-CAD schematics are [here](https://github.com/clevelandmusicco/HothouseExamples/wiki/Frequently-Asked-Questions#schematics). (Handy if you don't have Eagle or KiCad.)
* A DIY 125B enclosure drill template is included in [drill-template.pdf](fabrication/hothouse-drill-template.pdf). It assumes you assemble everything according to the build docs for proper fit.
* For custom-machined enclosures from Tayda, a 125B drill template is [here](https://drill.taydakits.com/box-designs/new?public_key=Q2luT1FRTVZRM3Bab01YbXd3eituUT09Cg==).

## Bill Of Materials

[BOM.xls](fabrication/BOM.xls) specifies the surface-mount components.

Budget-friendly through-hole components to complete the build and some sourcing suggestions:

| QTY | SOURCE URL | DESCRIPTION | NOTES |
| :---: | :--- | :--- | :--- |
| 2 | [Tayda SKU: A-1310](https://www.taydaelectronics.com/20-pin-2-54-mm-single-row-female-pin-header.html) | 20 Pin 2.54mm Single Row Female Pin Header | |
| 3 | [Tayda SKU: A-3670](https://www.taydaelectronics.com/mini-toggle-switch-1m-series-spdt-on-off-on-short-lever.html) | Toggle SPDT On-Off-On Short Lever | |
| 2 | [Tayda SKU: A-4807](https://www.taydaelectronics.com/spst-momentary-soft-touch-push-button-stomp-foots-pedal-switch-on-off-b.html) | SPST Momentary Soft Touch Push Button Stomp Foots / Pedal Switch OFF-(ON) | |
| 6 | [Tayda SKU: A-2969](https://www.taydaelectronics.com/b10k-ohm-linear-taper-potentiometer-round-shaft-pc-mount-l.html) | 10K OHM Linear Taper Potentiometer PCB Mount Round Shaft Dia: 6.35mm | |
| 3 | [Tayda SKU: A-5527](https://www.taydaelectronics.com/dust-seal-covers-for-potentiometer.html) | Dust Seal Cover For Potentiometer | Could also use electrical tape |
| 2 | [Tayda SKU: A-261](https://www.taydaelectronics.com/led-3mm-red.html) | LED 3mm Red | |
| 1 | [Tayda SKU: A-4118](https://www.taydaelectronics.com/dc-power-jack-2-1mm-barrel-type-pcb-mount.html) | DC Power Jack 2.1mm Barrel-Type PCB Mount | |
| 6 | [Tayda SKU: A-932](https://www.taydaelectronics.com/91640-dup-knob-davies-1900h-clone-black.html) | Knob DAVIES 1900H CLONE Black | Or anything that fits the 6.35mm pot shafts |
| 1 | [Tayda SKU: A-6628](https://www.taydaelectronics.com/matte-white-sand-texture-125b-style-aluminum-diecast-enclosure.html) | 125B Style Aluminum Diecast Enclosure MATTE WHITE SAND TEXTURE | Colour isn't important; the commercial Hothouse artwork is not included in this repo |
| 1 | [Tayda SKU: A-5165-CST-DR1](https://www.taydaelectronics.com/125b-custom-drill-enclosure-service.html) | 125B ENCLOSURE CUSTOM DRILL SERVICE | Optional |
| 1 | [Tayda SKU: A-5165-CST-UV1](https://www.taydaelectronics.com/125b-uv-printing-service.html) | 125B ENCLOSURE FACE UV PRINTING SERVICE | Optional |
| 1 | [Stompbox Parts SKU: RIB-6P-1](https://stompboxparts.com/cables-wire-plugs/ribbon-cable-6-pin-1-prebond/) | Ribbon Cable - 6 pin - 1" - Prebond | _Prebond_ is important! |
| 1 | [Stompbox Parts SKU: RIB-6P-2](https://stompboxparts.com/cables-wire-plugs/ribbon-cable-6-pin-2-prebond/) | Ribbon Cable - 6 pin - 2" - Prebond | _Prebond_ is important! |
| 2 | [Mouser PN: 568-NRJ6HM1](https://www.mouser.com/ProductDetail/568-NRJ6HM1)| Neutrik NRJ6HM-1 1/4" Stereo Audio Connector | [Tayda SKU: A-6446](https://www.taydaelectronics.com/6-35mm-1-4-stereo-insulated-switched-cylindrical-socket-jack-pcb-pins.html) also works in a pinch |
| 2 | [Mouser PN: 568-NRJ6HM1](https://www.mouser.com/ProductDetail/568-NRJ-NUT-MN)| Neutrik NRJ-NUT-MN Mounting Nut for NRJ6HM-1 | |
| 1 | [Mouser PN: 667-EEU-FR1E101B](https://www.mouser.com/ProductDetail/667-EEU-FR1E101B)| Panasonic EEU-FR1E101B Aluminum Electrolytic Capacitors - Radial Leaded 25VDC 100uF 6.3x11.2mm LS 5.0mm | Use whatever low-ESR capacitor you prefer |

