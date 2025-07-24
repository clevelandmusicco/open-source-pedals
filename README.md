# Cleveland Music Co. Open Source Pedals

Here you can find the design files used in the production of [Cleveland Music Co.](https://clevelandmusicco.com) pedals. This includes schematics, PCB layouts, Gerber/BOM/CPL files for PCB fabrication and assembly, templates for enclosure drilling, and more. In addition to the sources we use for our retail pedals and kits, there are several DIY projects for popular so-called "clones" you can modify and/or fabricate on your own. All of these materials are made available as [Open Source Hardware](https://oshwa.org/resources/open-source-hardware-definition/) distributed under a [Creative Commons Attribution-ShareAlike 4.0 International license](https://creativecommons.org/licenses/by-sa/4.0/).

<img height="100" alt="cleveland" src="https://github.com/user-attachments/assets/f5b442f6-08ab-48fc-8a97-a49fcd0cf47f" />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img height="100" alt="cle_" src="https://github.com/user-attachments/assets/47aedd84-2b1f-429c-9b37-d9c4e3cbcf66" />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img height="100" src="https://resources.oshwa.org/files/assets/oshw-logo-filled-color.svg" />

## What is here and how do I view or use it?

The directory structure is self-explanatory.

* Most schematics and PCB layouts were created with [Eagle 9.6.2](https://eagle-updates.circuits.io/downloads/latest.html), which is free for personal use (but not open source). Designs added in the future will likely be created in [KiCad](https://www.kicad.org/).
* The zipped Gerber files, BOM, and CPL files can be used as-is at [JLCPCB](https://jlcpcb.com/).
* Drill layouts for enclosures are formatted for use and stored at [Tayda Electronics](https://drill.taydakits.com/).

If there are any deviations from the above, the README file for each pedal points that out.

>[!IMPORTANT]
>All Cleveland Music Co. logos and trademarks have been removed from these source files. The artwork we use for our commercial products is also omitted. This is conventient as it provides a clean starting point for modification, but it also helps to avoid potential branding conflicts or confusion. 
>
>TL;DR: **USE OF CLEVELAND MUSIC CO. TRADEMARKS, LOGOS, OR BRANDING ON ANY HARDWARE, SOFTWARE, OR DOCUMENTATION (INCLUDING DESIGN FILES) DERIVED FROM THESE MATERIALS WITHOUT EXPRESS CONSENT FROM CLEVELAND MUSIC CO. IS NOT PERMITTED.**

### `eagle` directory files

The `.sch` and `.brd` (schematic and board) files are included. Additionally, there is an `.lbr` (library) containing only the footprints required to view and manipulate the `.brd` layout.

**The PCB layouts mostly use SMD components, with a few exceptions:** As a rule of thumb, aluminum electrolytic capacitors used for power filtering are through-hole, as are potentiometers, LEDs, switches, and trimmers. Some designs include through-hole pads for silver mica "tone capacitors" or similiar. This is pointed out in each pedal's README file and component suggestions are provided.

<img width="1469" height="522" alt="superior-design" src="https://github.com/user-attachments/assets/db2d9888-23b9-46b4-9465-0cdb986911c2" />

_The Superior Overdrive `.brd` file loaded in Eagle. Note the Cleveland Music Co. branding and trademarks have been removed from the source files._

### `fabrication` directory files

The `.zip` containing Gerber files is ready-to-use at [JLCPCB](https://jlcpcb.com/). It might be compatible with other services, but we haven't tested it. Also included are verified and tested `BOM.csv` and `CPL.csv` files for PCBA (Printed Circuit Board Assembly) services at JLCPCB.

The BOMs follow a few general guidelines:

1. High-quality component manufacturers like TDK, onsemi, Texas Instruments, Murata, Samsung, and others are favored wherever possible.
2. Audio signal path capacitors use C0G or NP0 MLCC capacitors from JLCPCB's parts library wherever possible.
3. As C0G/NP0 SMD capacitors tend to be larger than their X7R equivalents, 1206 and 0805 footprints are common for audio signal path capacitors in the PCB layouts.
4. Some of the BOMs can get expensive at JLCPCB due to the use of many so-called ["extended" components](https://jlcpcb.com/help/article/pcb-assembly-faqs). Our retail pedals and kits always use the highest-quality available components where it makes sense. If you want less expensive PCBs, use less expensive "basic" parts from the JLCPCB parts library, or source and solder the components yourself.

<img width="1421" height="604" alt="superior-fab-tilt" src="https://github.com/user-attachments/assets/65f20d46-1bf6-4561-bd96-d2c82cdcbe58" />

_Rendering of a Superior Overdrive PCB fabricated with these files. Note the Cleveland Music Co. branding and trademarks have been removed from the source files._

There is also a `.url` file with a link to the Drill Template at Tayda. These templates have been verified and tested. For example, [here is the Superior Overdrive Drill Template](https://drill.taydakits.com/box-designs/new?public_key=SVhxKzdDNXZjeXVUNXpSM1phNTFkdz09Cg==).

<img width="1522" height="885" alt="image" src="https://github.com/user-attachments/assets/39448fab-f5ef-4988-9663-e2599d316544" />

_The Superior Overdrive Drill Template at Tayda Electronics._

## What is [Open Source Hardware](https://oshwa.org/resources/open-source-hardware-definition/)?

Open source hardware is hardware whose design is made publicly available so that anyone can study, modify, distribute, make, and sell the design or hardware based on that design. The hardware’s source, the design from which it is made, is available in the preferred format for making modifications to it. Ideally, open source hardware uses readily-available components and materials, standard processes, open infrastructure, unrestricted content, and open-source design tools to maximize the ability of individuals to make and use hardware. Open source hardware gives people the freedom to control their technology while sharing knowledge and encouraging commerce through the open exchange of designs.

## In a nutshell, what is the [Creative Commons Attribution-ShareAlike 4.0 International license](https://creativecommons.org/licenses/by-sa/4.0/)?

### You are free to:

* **Share** — copy and redistribute the material in any medium or format for any purpose, even commercially.
* **Adapt** — remix, transform, and build upon the material for any purpose, even commercially.

### Under the following terms:

* **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests Cleveland Music Co. endorses you or your use.
* **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
* **No additional restrictions** — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

We cannot revoke these freedoms as long as you follow the license terms, even if we decide to stop distributing these materials under the terms at a later date.

>[!WARNING]
>No warranties are given. The license may not give you all of the permissions necessary for your intended use. For example, other rights such as publicity, privacy, or moral rights may limit how you use these materials.

>[!CAUTION]
>This description highlights only some of the key features and terms of [the actual license](https://creativecommons.org/licenses/by-sa/4.0/). It is not a license and has no legal value. You should carefully review all of the terms and conditions of [the actual license](https://creativecommons.org/licenses/by-sa/4.0/) before using the contents of this repository.

## Why would a for-profit company do this? Are you worried about people "ripping you off"?

Basically, two ideas we fiercely support:

1. Sharing designs promotes innovation. Designers don't waste brain power "reinventing the wheel" when they can freely reuse and improve upon public designs.
2. People should have the right to study, modify, AND REPAIR the physical devices they own. And if people do not or cannot buy our hardware products for any reason, the should have _permission_ to make, sell, and distribute new designs or hardware derived from ours, as long as their work is also publicly shared.

We're not worried about people "ripping us off". Practically speaking, even with access to a product’s design, it's not trivial for someone else to make and sell it. They still need to source components, manufacture and/or assemble parts, design and implement a testing strategy, create distribution and commerce channels, and much more. We have a head start doing all of this while offering our products at prices low enough that it's likely not worth undercutting us. And frankly, if people really wanted to rip us off, they would reverse engineer and reproduce our products _whether they were open source or not_, selling them at higher "prestige" prices. Legally speaking, this would not make them criminals; it would just make them assholes.

So, as a matter of principle, we're happy to accept the risks posed by bad actors as the price to make knowledge and freedoms available to the good ones (such as yourself).
