# Hothouse Digital Signal Processing Pedal (125B)

The Hothouse is a compact effect pedal for the [Electrosmith Daisy Seed](https://electro-smith.com/products/daisy-seed). You can use it to easily get Daisy Seed DSP projects off the breadboard and onto your pedalboard, either by compiling and flashing any of the code in [the official repository](https://github.com/clevelandmusicco/HothouseExamples), or by using the [Daisy Web Programmer](https://electro-smith.github.io/Programmer/) with the [pre-compiled binaries](https://github.com/clevelandmusicco/HothouseExamples/releases). And of course, you can also [write your own DSP code for the Hothouse](https://github.com/clevelandmusicco/HothouseExamples/wiki/Creating-your-own-effects). Basically, anything that runs on the Daisy Seed will run on the Hothouse.

This directory contains the open source hardware files for the [Cleveland Music Co. Hothouse DSP Pedal Kit](https://clevelandmusicco.com/hothouse-diy-digital-signal-processing-platform-kit/). Included are the gerber, BOM, and CPL files required to fabricate your own PCBs at JLCPCB. Also included are suggestions for the various through-hole components and other hardware required.

>[!NOTE]
> No step-by-step tutorial for having the boards fabricated is provided. It's assumed that anyone interested in using these files is already familiar with the fabrication process at their provider of choice. However, the files in this repo have only been tested with JLCPCB.

>[!IMPORTANT]
> Remember that all of these materials are made available as [Open Source Hardware](https://oshwa.org/resources/open-source-hardware-definition/) distributed under a [Creative Commons Attribution-ShareAlike 4.0 International license](https://creativecommons.org/licenses/by-sa/4.0/). Before using these materials, be sure to follow the links above and read the [main repo README](/README.md) and [LICENSE](/LICENSE) files.

## Overview

The Hothouse design is comprised of three PCBs:

1. The Main PCB,
2. A Switching & LED daughterboard,
3. A Power & Audio I/O daughterboard.

<img width="777" height="735" alt="hothouse-main-pcb" src="https://github.com/user-attachments/assets/b5803595-6ba8-4069-90f4-6c0f93129d8f" />  

_The Main PCB_

<img width="753" height="327" alt="hothouse-switching-pcb" src="https://github.com/user-attachments/assets/63a6cf0d-6b2d-43e2-865a-e12a12d27876" />  

_The Switching & LED Daughterboard_

<img width="679" height="327" alt="hothouse-io-pcb" src="https://github.com/user-attachments/assets/dca83c48-911c-4e4a-9941-9cd11f6b637e" />   

_The Power & Audio I/O Daughterboard_

The main PCB is designed for a mix of through-hole and surface-mount components, while the two daughterboards use only through-hole components. The three PCBs are connected by 6-pin ribbon cables. Refer to [the commercial product build docs](https://github.com/clevelandmusicco/HothouseExamples/wiki/Cleveland-Music-Co.-Hothouse-DIY-Digital-Signal-Processing-Pedal-Kit-Build-Guide-(Stereo-Version)) for more information.

All commercial branding (Cleveland Music Co.-specific stuff) has been removed from the PCBs and files in this repository.

### eagle Directory

For each of the three boards, you will find four files:

* An Eagle schematic (`.sch`)
* An Eagle board (`.brd`)
* An Eagle library (`.lbr`) for the devices and footprints specific to the board layout
* A PDF schematic

All the files were created with Eagle 9.6.2 "free". Having separate files for each board provides flexibility; not everyone will want to modify or fab all three PCBs.

### fabrication Directory

There is a zip of the gerber files for each board following the same naming convention as the `eagle` directory. A BOM and CPS file in `.csv` and `.xls` formats is provided for use with `hothouse-no-branding.zip`. You'll also find a DIY drill template in `.pdf` format for those wanting to drill their own 125B enclosures.

## Resources

* [HothouseExamples GitHub repo](https://github.com/clevelandmusicco/HothouseExamples) - The official code examples repo with effects created in C++, Puredata/Plugdata, and Max.
* [Cleveland Music Co. Hothouse DSP Pedal Kit](https://clevelandmusicco.com/hothouse-diy-digital-signal-processing-platform-kit/) - A retail example of a pedal created from the files in this directory. _The chicken or the egg?_ and all that ...
* [Cleveland Music Co. Hothouse Build Guide](https://github.com/clevelandmusicco/HothouseExamples/wiki/Cleveland-Music-Co.-Hothouse-DIY-Digital-Signal-Processing-Pedal-Kit-Build-Guide-(Stereo-Version)) - The build documentation for the retail kit.
* [DIY 125B enclosure drill template](fabrication/hothouse-drill-template.pdf) - For those wanting to drill their own 125B enclosures. It assumes you assemble everything according to the build guide above for proper fit.
* [Tayda 125B drill template](https://drill.taydakits.com/box-designs/new?public_key=Q2luT1FRTVZRM3Bab01YbXd3eituUT09Cg==) - For custom-machined enclosures from Tayda. Highly-recommended if you don't have a drill press or some other way to accurately drill holes in the TOP and SIDES of an enclosure. (You'll need to sign up for an account; FWIW, I've never recieved a single spam email from them.)

## Bill Of Materials

`BOM.xls` (or `BOM.csv`) specifies the surface-mount components. It is adapted from a late-2025 fabrication run used for the commercial kits. "Adapted" because some of the parts used aren't always in stock at JLCPCB publicly (they are stocked in my personal parts library); several components have been swapped out here for purposes of general availability.

Budget-friendly through-hole components to complete the build and some sourcing suggestions:

| QTY | SOURCE URL | DESCRIPTION | NOTES |
| :---: | :--- | :--- | :--- |
| 2 | [Tayda SKU: A-1310](https://www.taydaelectronics.com/20-pin-2-54-mm-single-row-female-pin-header.html) | 20 Pin 2.54mm Single Row Female Pin Header | |
| 3 | [Tayda SKU: A-3670](https://www.taydaelectronics.com/mini-toggle-switch-1m-series-spdt-on-off-on-short-lever.html) | Toggle SPDT On-Off-On Short Lever | |
| 2 | [Tayda SKU: A-4807](https://www.taydaelectronics.com/spst-momentary-soft-touch-push-button-stomp-foots-pedal-switch-on-off-b.html) | SPST Momentary Soft-Touch Push-Button Stomp Switch OFF-(ON) | |
| 6 | [Tayda SKU: A-2969](https://www.taydaelectronics.com/b10k-ohm-linear-taper-potentiometer-round-shaft-pc-mount-l.html) | 10K OHM Linear Taper Potentiometer PCB Mount Round Shaft Dia: 6.35mm | Use whatever 16mm pot you prefer |
| 3 | [Tayda SKU: A-5527](https://www.taydaelectronics.com/dust-seal-covers-for-potentiometer.html) | Dust Seal Cover For Potentiometer | Could also use electrical tape |
| 2 | [Tayda SKU: A-261](https://www.taydaelectronics.com/led-3mm-red.html) | LED 3mm Red | |
| 1 | [Tayda SKU: A-4118](https://www.taydaelectronics.com/dc-power-jack-2-1mm-barrel-type-pcb-mount.html) | DC Power Jack 2.1mm Barrel-Type PCB Mount | The retail kits use a Kobiconn jack, but this works fine |
| 6 | [Tayda SKU: A-932](https://www.taydaelectronics.com/91640-dup-knob-davies-1900h-clone-black.html) | Knob DAVIES 1900H CLONE Black | Or anything that fits the shafts of the pots you're using |
| 1 | [Tayda SKU: A-6628](https://www.taydaelectronics.com/matte-white-sand-texture-125b-style-aluminum-diecast-enclosure.html) | 125B Style Aluminum Diecast Enclosure MATTE WHITE SAND TEXTURE | Colour or finish isn't important; this is just what the retail kits use |
| 1 | [Tayda SKU: A-5165-CST-DR1](https://www.taydaelectronics.com/125b-custom-drill-enclosure-service.html) | 125B ENCLOSURE CUSTOM DRILL SERVICE | Optional |
| 1 | [Tayda SKU: A-5165-CST-UV1](https://www.taydaelectronics.com/125b-uv-printing-service.html) | 125B ENCLOSURE FACE UV PRINTING SERVICE | Optional |
| 1 | [Stompbox Parts SKU: RIB-6P-1](https://stompboxparts.com/cables-wire-plugs/ribbon-cable-6-pin-1-prebond/) | Ribbon Cable - 6 pin - 1" - Prebond | _Prebond_ is important! But you could also simply "fly" 6 hookup wires the olde fashioned way |
| 1 | [Stompbox Parts SKU: RIB-6P-2](https://stompboxparts.com/cables-wire-plugs/ribbon-cable-6-pin-2-prebond/) | Ribbon Cable - 6 pin - 2" - Prebond | Ditto above|
| 2 | [Mouser PN: 568-NRJ6HM1](https://www.mouser.com/ProductDetail/568-NRJ6HM1)| Neutrik NRJ6HM-1 1/4" Stereo Audio Connector | [Tayda SKU: A-6446](https://www.taydaelectronics.com/6-35mm-1-4-stereo-insulated-switched-cylindrical-socket-jack-pcb-pins.html) also works in a pinch; but the Neutrik part is recommended |
| 2 | [Mouser PN: 568-NRJ6HM1](https://www.mouser.com/ProductDetail/568-NRJ-NUT-MN)| Neutrik NRJ-NUT-MN Mounting Nut for NRJ6HM-1 | |
| 1 | [Mouser PN: 667-EEU-FR1E101B](https://www.mouser.com/ProductDetail/667-EEU-FR1E101B)| Panasonic EEU-FR1E101B Aluminum Electrolytic Capacitors - Radial Leaded 25VDC 100uF 6.3x11.2mm LS 5.0mm | Use whatever low-ESR capacitor you prefer |

