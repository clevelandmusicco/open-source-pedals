# The 'Why'

The 'Why' is an adaptation of the venerable Electro-Harmonix (EHX) Big Muff circuit. All components are surface mount (SMD) except for the power filtering capacitor and three board-mounted pots. So, assembly is as simple as soldering these four parts to the PCB.

## Big Muff Circuit Variation

The Big Muff is famous for having been made in many different variants over the years, each having a unique sound due to its mix of component values, transistor types and current gain (hFE), and even the dielectrics of the capacitors used. Since the topology of the schematic is consistent, the same PCB layout can be used to make (almost) any variant. So, making a "Ram's Head" as opposed to a "Green Russian", for example, is a matter of editing the BOM. I have made no fewer than five great-sounding Big Muffs using the files in this directory, with some of them being mashups of values from several different variants (the [Cleveland Music Co. Smuffle Fuzz](https://clevelandmusicco.com/pedals/smuffle-fuzz/) is one such example).

The canonical source for Big Muff schematics has to be [Kit Rae's Big Muff Page](https://www.kitrae.net/music/music_big_muff.html). Here you can find a schematic for every known variant of the Big Muff circuit with consistent part identifiers and notes about capacitor dialectrics, transistors, etc.

To make it easy to try different variants, I have used the same identifiers Kit uses on his website. The schematic in the `eagle` directory is from [the David Gilmour Big Muff](https://www.kitrae.net/music/David_Gilmour_Big_Muff.html) (which Kit calls "Version 2 Big Muff 1973 #3), and `BOM_gilmour.csv` specifies JLC part numbers that match this schematic. If you want to make a different variant, simply create a new BOM selecting parts that match the schematic you want to make.

>[!NOTE]
> I'll probably add more BOMs in the future. Pull requests are also welcome!

You may occasionally need to tweak a capacitor footprint to use the part number you want (C8 is probably the leading candidate here). The largest footprint in `the-why.lbr` is 1206; there's plenty of space on the board to make all capacitors 1206 if you wanted to. You won't even need to change the CPL coordinates if you're careful.

## A Few Words About SMD/SMT Hate

Get over it. If you want to make an exact clone of a 1969 Big Muff Pi V1, best of luck to you ... for many reasons; The 'Why' is probably not a project for you. The 'Why'is for people who want to learn about SMT PCBA, or just aren't very interested in sourcing and soldering through-hole components.

Sure, SMT is more difficult (if not impossible) to repair sometimes. And, yeah, such tiny parts must _sound different_ than big, magical, 'mojo' parts, right? Of course they do. But the same could be said for every part in every version of the Big Muff that ever used different capacitor dielectrics or resistor material or paint colour or whatever. An NP0 SMD capacitor is different than a polyester film cap. Obviously. But different isn't the same as inferior.

You also have to consider that component tolerances can make ten Big Muffs that came off the line back-to-back in 1974 all sound slightly different, even brand new. Going by the values on a schematic will not get you an exact copy of the holy grail sound you might think you're seeking. Many of the critical components used were often well out of the specified tolerance in the first place, and as the parts age, those values drift even more.

(Let's not talk about 'fidelity', either. The purpose of distortion devices like the Big Muff is literally to _distort (pull or twist out of shape)_ an audio signal. Come on, man.)

So, if you know what you're doing and you select capacitor dialectrics that make sense, pay attention to transistor current gain, and so on, you can make a perfectly-legitimate, excellent-sounding (and often far less noisy) Big Muff with SMT.