# Nevermore Activated Carbon Filters - Micro Edition

<div align="center">Nevermore Micro V5 Duo (dual fan)</div>

![Nevermore Activated Carbon Filter Micro V5 Duo](images/DUO_COMBINED_render.png "Nevermore Activated Carbon Filter Micro V5 Duo")

Originally intended as a carbon fume filter for Voron V2, it has found its way into a multitude of other machines. Let yours be the next! Bad smells or fumes, or complaints thereof, should not keep you from being a maker!

- [Nevermore Activated Carbon Filters - Micro Edition](#nevermore-activated-carbon-filters---micro-edition)
- [About The Nevermore Micro](#about-the-nevermore-micro)
  - [Why The Nevermore?](#why-the-nevermore)
  - [Nevermore Background](#nevermore-background)
  - [Nevermore V5 Duo](#nevermore-v5-duo)
- [FAQs](#faqs)
  - [What fans should I use?](#what-fans-should-i-use)
  - [How do I make a suggestion/report a bug/find out more?](#how-do-i-make-a-suggestionreport-a-bugfind-out-more)
- [Getting Started](#getting-started)
  - [SOURCING THE PROPER ACID-FREE CARBON](#sourcing-the-proper-acid-free-carbon)
  - [NEVERMORE 3D PRINTER CARBON](#nevermore-3d-printer-carbon)
  - [BOM (V5)](#bom-v5)
  - [Assembly](#assembly)
    - [Instructions for V5](#instructions-for-v5)
    - [Instructions for V4](#instructions-for-v4)
  - [Final Thoughts on Usage](#final-thoughts-on-usage)
    - [Back: Voron V2.4R2 kit by Lecktor](#back-voron-v24r2-kit-by-lecktor)
- [Sources:](#sources)

# About The Nevermore Micro

[VOCs (Volatile Organic Compounds)](https://en.wikipedia.org/wiki/Volatile_organic_compound) are common in daily life but VOCs generated from 3D printing are known to cause severe health issues and even cause cancer in some cases.

![Emitted VOCs](images/emitted-voc.jpg "Emitted VOCs")

A study from 2013 of [ultrafine particle emissions from desktop 3D printers (2013)](https://www.sciencedirect.com/science/article/pii/S1352231013005086) is a good start to understand the importance of your filament choices and the printer's environment.

![Characterization of volatile organic compound emissions from consumer level material extrusion 3D printers (2019)](images/emitted-voc2.jpg "Characterization of volatile organic compound emissions from consumer level material extrusion 3D printers (2019)")
_(credit: [Characterization of volatile organic compound emissions from consumer level material extrusion 3D printers (2019)](https://www.sciencedirect.com/science/article/pii/S0360132319304196))_

![Characterization of particulate and gaseous pollutants emitted during operation of a desktop 3D printer (2019)](images/emitted-voc3.jpg "Characterization of particulate and gaseous pollutants emitted during operation of a desktop 3D printer (2019)")
_(credit: [Characterization of particulate and gaseous pollutants emitted during operation of a desktop 3D printer (2019)](https://www.sciencedirect.com/science/article/pii/S0160412018323663))_

## Why The Nevermore?

At the end of the day, a fresh single-pass filtered exhaust (at brand new) has perhaps 70% VOC removal efficiency while still exhausting 30% of the nasty. A worn-in 50% efficiency recirculation filter achieving four passes would still remove 94% of the bad stuff. Or 99% at six passes!

The number of passes you get all depends on how well you can seal your build chamber.

Some will have a hard time achieving a good chamber seal, which creates the biggest drawback of recirculation filters - _they're air flow neutral_. Meaning, as nothing pulls air into the chamber, air can diffuse freely to the outside through any remaining gaps. And that air could be _zero-per-cent_ cleaned...

If you plan on using only a Nevermore - be sure to seal your chamber as good as possible to prevent diffusing.

## Nevermore Background

There are many options for 3d printing air filters. Here’s a short list, and why I eventually settled on creating Nevermore:

**1. Home air purifiers**

**PRO:** Plug and play! High air flow (mostly). Will filter most particles a 3d printer produces.

**CON:** ABS headaches are not from particles, but Volatile Organic Compounds (VOCs), that are two orders of magnitude smaller than any particles a HEPA or ULPA could trap - they’re essentially gasses.

While home purifiers typically also contains carbon filtration and/or photocatlytic UV filtration stages, they will still not be suitable for 3d printing. Why? Efficient carbon adsorption in sufficient amount and stages is an absolute airflow killer, so most purifiers contain only a thin layer of carbon mesh/pellets that will be fully adsorbed within days or weeks at full power. And even if the filter is not used, contact with air saturates the carbon in 1-2 months. Yet they’re advertised as lasting for 6 months – that's only true for the HEPA component, not the VOC adsorbant carbon we're after.

And replacement filters typically run 20-60 USD a pop. Quite a lot for changing every few weeks when the carbon component depletes.

UV photocatalyst activity can last though; however, breakdown is slow and inefficient with voc halflives of several hours. The TiO2 layer reacting to the UV will also easily get irreversibly blocked by silicates (of which there are a lot in peoples homes, in everything from sink and bathroom sealants to plaster walls). And breakdown will many times be incomplete. Styrene passing a PCO filter might get turned to even more dangerous benzene, for instance.

**2. Carbon/HEPA filter combinations like the Zortrax M Series HEPA Filters**

Same as above. The HEPA component will keep working, but the carbon is just a few pebbles per hex. It could provide partial VOC clearance when fresh, but will quickly deplete with air flow. Then you need to replace it for 36 USD after a week of printing.

**3. Wet scrubber**

Awesome for both particles and VOCs, but its an industrial solution with any smaller home versions plagued by loud noise, water leakage and mechanical issues. It's not a solution for the masses.

**So, how about Nevermore?**

Well, the carbon in those filters mentioned above, costing a lot for little duration is actually dirt cheap. Whereas you get 20 grams for 36 USD with a zortax filter, **you can get 5000 grams for 36 USD in bulk**.

And with an enclosed chamber, you don't need the air flow of a room-size air purifier. Even a 350mm V2 Voron only holds about 5cf, meaning even a partial flow from a 5015 fan of 0.5-2cfm is enough to filter the fumes efficiently at the source.

So what are we waiting for? We got lots of cheap carbon. We can replace is easily. We don't need high airflow to clean a small chamber. We deal with poor efficiency of one-pass carbon filters by multiplying the amount and recirculate the air.

Enter, _The Nevermore_.

## Nevermore V5 Duo

Following the V4, the V5 Duo was released that changes the direction of air flow, better suited for when the Nevermore Micro would be placed flat on the bottom or top of the printer. Though there are other "outlet" options, like for the V1.8/Trident style that blows outwards and not up.

The V5 Duo also adds a 2nd additional 5015.

![Nevermore Micro V5 Duo](images/nevermore-micro-duo.jpg "Nevermore Micro V5 Duo")

![Nevermore Micro V5 Duo](images/nevermore-micro-duo-opened.jpg "Nevermore Micro V5 Duo")

_(Nevermore V5 Duo. used with permission from Tightwad(JT)#6055)_

This repository hosts both versions, as they the same in design and function.

# FAQs
## What fans should I use?

Aim for any 5015 blower with a rating above 200Pa / 20mmH2O / 1 inH2O.

Since the fan (probably) cant be reused for other projects and will function in a high temp environment affecting its lifetime, go for budget. The Sunon Maglev MF50151VX (12V) / MF50152VX (24V) (high speed version, 6000 rpm) is good but unfortunately almost impossible to find as most are fakes. The GDStime 6000rpm Dual Ball bearing is another good option, but quality may vary. The Delta BFB0524HH is a gucci option, as is the special micro versions made for the papst rlf-35 which is an equally awesome and expensive fan. Any fan that works well for stealthburner should be a good option for nevermore micro as well.

See the BOM below for more details.

## How do I make a suggestion/report a bug/find out more?

- [The Nevermore Micro](https://github.com/nevermore3d/Nevermore_Micro)
  - [Report a Bug](https://github.com/nevermore3d/Nevermore_Micro/issues)
  - [Request a Feature](https://github.com/nevermore3d/Nevermore_Micro/issues)
- [Explore all Nevermore Activated Carbon Filters](https://github.com/nevermore3d)

# Getting Started

You're ready to build a Nevermore Micro? Cool!

> **_NOTE:_** MADE FOR ABS/PC/PETG - USE A DECENTLY HEAT RESISTANT FILAMENT !!

> **_NOTE:_**: Since you are committing to fan dissection, be aware a 5015 used for a NM Micro will most likely never find a different purpose!

## SOURCING THE PROPER ACID-FREE CARBON

**IMPORTANT!** Since first release the varying quality carbon out there has become increasingly evident. Users has both gotten bad carbon as well as outright dangerous stuff (in one case oxidizing most metal surfaces in a new voron in minutes. Be sure to vet your carbon supplier! You do not want your printer to look like this.

![Acid residue on end-stop switch oxidizing](images/endstop-switch-acid-residue.jpg "Acid residue on end-stop switch oxidizing")

_(z end-stop switch after using acid residue carbon for 30 minutes, oxidizing)_

![Acid residue on rails and screws oxidizing](images/voron2-oxidation1.png "Acid residue on rails and screws oxidizing")

_(oxidation on rails and screws after using acid residue carbon. used with permission from Zeptron#8880)_

![Acid residue on filament tension spring oxidizing](images/voron2-oxidation2.png "Acid residue on filament tension spring oxidizing")

_(oxidation on filament tension spring after using acid residue carbon. used with permission from Zeptron#8880)_

![Acid residue on bolts and washers oxidizing](images/voron2-oxidation3.png "Acid residue on bolts and washers oxidizing")

_(oxidation on bolts and washers after using acid residue carbon. used with permission from Zeptron#8880)_

Optimal carbon for 3D printer VOC adsorption is sourced from **virgin coconut**, not wood/bitumen/charcoal/bamboo/lignin/etc. The porosity for each and every source will vary greatly.

For example, for aquarium or moonshine use you want large macroporosity to filter larger impurities, like oils. For that reason, water/liquid-use carbon has a large macropore area, defined as >100nm. 3D Printer VOCs are generally less than 0.5 nm, meaning that **for optimal capture rate and efficiency we want carbon with a high microporosity ratio, defined as <1nm**. A higher iodine count >1000 usually indicates at least some micro/mesoporosity, and a higher hardness (>95%) will create less dust in air filtration. CTC number doesn't translate well to our VOCs; however, toluene adsorption - which sometimes is available - is a good metric.

**Avoid acid washed carbon at all costs**. Residues have oxidized printers! Go for steam activated, non acid-washed. A blend of neutral carbon and alkaline KOH carbon might be the best blend in the future, but impossible to currently source from trustworthy manufacturers.

Finding carbon that fills all criteria is hard. Look around, ask suppliers about the carbon, hear what others recommend. 

## NEVERMORE 3D PRINTER CARBON
**Nevermore offers its own premium carbon of unmatched specifications through selected voron resellers.** Its the best activated carbon for 3D printer use we have found after speaking to most major, vetted suppliers, offering benzene adsorbtion of up to 48 wt%, surface area of 1250 and CTC value of 80. It doesn't come cheap compared to bulk carbon from amazon, but its safe, has unbeatable performance, and every purchase supports the nevermore project by at least a dollar, see [Lecktor listing](https://lecktor.com/en/nevermore/870-nevermore-carbon.html)

## BOM (V5)

- 2x 5015 blowers (rating above 200Pa / 20mmH2O / 1 inH2O)
  - Sunon Maglev MF5015VX (high speed version, 6000 rpm. NOTE: There are A LOT of fake sunons out there, even from usually reputable sources. Blantant examples include 24V versions. Also, Sunon does not officially reecommend PWM:ing this fan, so while its still perfectly doable it can have unintended consequences later on) (There is no 24V version for this fan only comes in 12 V)
  - GDStime 6000rpm Dual Ball bearing on Aliexpress (This is 12V rated fans)
  - Delta BFB0524HH (This is 24V rated fans)
  - Avoid mechatronics fans for this purpose.
- 5x M3x0.5mm Heatset inserts (standard voron issue)
  - 2 for seating plenum to base
  - 2 for seating plenum lid to plenum
- 8x 6x3mm cylindrical magnets
- 1x 2 pin JST header
- 4x M3x16 BHCS
  - for heat inserts that go into the four fan tabs
- 1x M3x18 BHCS
  - ONLY for delta and v1.8 variants
- 1x M3x6 BHCS
- 1x M3x4 BHCS
  - for the extra hole in the plenum@lid for symmetry (it doesn’t attach to anything and is totally optional)

Acid-free Activated Carbon

- 4mm Active Carbon Air Filter Pellets

Optional for the cartridge closure

- 1x M3x0.5mm Heatset inserts
- 1x M3x6 BHCS

Optional for Vorons or any printer with 2020 extrusions

- 2x M3x12 SHCS
- 2x M3 2020 T-Nuts

Optional for Vorons or any printer using 24PSU
- 24 to 12 buck converter

## Assembly

Check out assembly images (**take note at how the fans are cut!**) here: [Nevermore V5 Plenum Assembly Album](https://ibb.co/album/0BN405?sort=name_asc&page=1&params_hidden%5Blist%5D=images&params_hidden%5Bfrom%5D=album&params_hidden%5Balbumid%5D=0BN405)

### Instructions for V5

_Coming soon... Similar to V4 though._

### Instructions for V4

Start by cutting up the 5015 so just the center remains. Take off the top half, cut the bottom piece circular along the fan blades. We aim for removing the focused air stream and instead achieve an even pressure across all of the filter medium.

The Nevermore Micro has three main parts: **Base**, **Plenum**, and **Cartridge** (plus lids for the plenum/cartridge).

- **Base** is mounted in the 130mm space between the bottom extrusions found on many vorons (designed for v2 originally). It’s seated with one m3 on each side, that screws into to a receiving 2020 M3 T-nut.

- **Plenum** holds the cut up 5015 fan, and is seated with two m3 screws into the base (base has two recieving m3 4mm heat inserts) on each side.

- **Cartridge** holds the filter medium of your choice (made for 4mm air filter active carbon pellets, but feel free to filter with what you think works best!). It snaps onto the Plenum piece for easy and quick removal.

For wiring, you are free to connect however works with your printer. If you do not have any direct controls on your MCU (controller board), then directly wiring may be your only option (with an inline switch).

However, if your MCU does have an additional fan output, then it is recommended to connect to it. If you are using Klipper on a Raspberry Pi, you have the option of using PWM fans and connecting the control wire to one of your PWM outputs on the RPi 40-pin header.

## Final Thoughts on Usage

**PID tune AGAIN if a Nevermore Micro is installed right beneath a heated bed, or draws/exhausts air over the bed thermistor. This is important, as worst case it could cause the bed to overheat, and/or make the heater adhesive burn (this will smell worse than any ABS printing!), and/or possibly even damage the bed heater.**

The Nevermore Micro's activated carbon will not filter Ultra-Fine Particulates (UFP). This is what the HEPA filter does in the Nevermore Mini (not released yet) and [Nevermore Max](https://github.com/nevermore3d/Nevermore_Max) variants. Those also have built-in negative-pressure fans.

However, you can achieve the same results with the Nevermore Micro by using a HEPA filter of your own and creating slightly negative air-pressure within your build chamber, exhausting air outwards at a slow pace. Since you are filtering with the Nevermore, the vast majority of VOCs will be filters by the active carbon filtration, leaving the HEPA filter to capture the remaining UFPs. This also greatly extends the live of your HEPA filter as the Nevermore Micro will be accumulating the larger particulates.

To create a negative pressure within your build chamber, simply install a fan to slowly draw air out of your build chamber and our through a HEPA filter. Voron machines already have such a design with their rear exhaust housing for HEPA filters.

The negative pressure will also eliminate diffusion, especially if your build chamber is not completely sealed.

---
### Back: [Voron V2.4R2 kit by Lecktor](../Readme.md)

# Sources:
[Nevermore Github](https://github.com/nevermore3d/Nevermore_Micro)