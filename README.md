# TS808 Tube Screamer Clone

![Altium Designer](https://img.shields.io/badge/Altium%20Designer-PCB%20Design-E6007E)
![SolidWorks](https://img.shields.io/badge/SolidWorks-CAD%20%26%20Simulation-ED1C24)
![PETG](https://img.shields.io/badge/3D%20Printing-PETG%2FFDM-00599C)
![License: CC BY--NC--SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey)

A hand-built clone of the Ibanez TS808 Tube Screamer overdrive pedal — designed, fabricated, and assembled from scratch, and now gigging regularly with my band.

<p align="center">
  <img src="docs/photos/final TS808 clone.jpg" alt="Finished TS808 clone pedal" width="500">
</p>

## Why build one

A genuine Ibanez TS808 typically retails around $170–180 (sometimes higher), and even the cheaper TS9 model runs $99–170 new, or roughly $80–100 used. Rather than pay that, I designed and built my own from published schematics — and ended up learning PCB design, enclosure design, and mechanical/structural simulation along the way.

## How it was built

1. **Circuit** — Sourced a TS808-style schematic and built it around a classic RC4558 dual op-amp and a 2SC1815 transistor.
2. **PCB** — Designed the schematic and board layout in Altium Designer (final board ≈82×126mm, >100cm²).
3. **Fabrication** — Ordered through [CheapPCB](https://www.cheappcb.ir) ([@CheapPCB](https://t.me/CheapPCB) on Telegram), a service that panelizes multiple customers' boards together into one production run, which brings the cost down since you're not paying for a full minimum-size (100cm²+) board on your own.
4. **Assembly** — Hand-soldered every component.
5. **Enclosure** — Modeled the enclosure and lid in SolidWorks, including mounting for the PCB, pots, jacks, footswitch, and battery. Used SolidWorks Simulation to study how the mechanical load from stomping the footswitch travels through the board and enclosure, and added two types of standoffs specifically to help direct that stress away from the board.
6. **Printing** — 3D printed the enclosure in PETG via FDM (200µm layer height, 50% infill).
7. **Final assembly & tuning** — Assembled, fine-tuned, and it's now in regular use at band rehearsals and shows.

## Repository contents

- `hardware/pcb/` — Altium schematic, PCB layout, and fabrication Gerbers
- `hardware/enclosure/` — SolidWorks part/assembly files, STEP, STL, and renderings
- `docs/photos/` — build photos (bare PCB, soldering, enclosure printing, final assembly)
- `BOM.md` — full bill of materials and real cost breakdown

## Cost

The original back-of-envelope estimate was "$15–20," but once every real cost is accounted for — including an imported footswitch, the actual PCB fabrication run, and the enclosure print-service cost — the realistic total comes to about **7.9 million toman (~$29–38 at current free-market rates)**. See [`BOM.md`](./BOM.md) for the full breakdown. Note that some parts (especially a few of the capacitors) were bought in bulk alongside other projects, so treat the BOM as a solid *estimate* of real cost rather than a lab-exact accounting — it's still well under a third of what a new Ibanez TS808 costs, and most of the gap from the original estimate comes from one-time fabrication/import costs that wouldn't repeat on a second build.

## Build photos

<p align="center">
  <img src="docs/photos/enclosure parts arrived 1.jpg" alt="Enclosure parts arrived" width="250">
  <img src="docs/photos/enclosure part arrived bubble wrap.jpg" alt="Enclosure parts in packaging" width="250">
  <img src="docs/photos/bare PCB.jpg" alt="Bare PCB fresh from fabrication" width="250">
</p>
<p align="center">
  <img src="docs/photos/after soldering.jpg" alt="PCB after hand-soldering" width="250">
  <img src="docs/photos/how top of the enclosure came out.jpg" alt="Printed enclosure lid" width="250">
  <img src="docs/photos/3d assembled side view.jpg" alt="3D-printed enclosure assembled, side view" width="250">
</p>
<p align="center">
  <img src="docs/photos/fully assembled .jpg" alt="Fully assembled pedal" width="250">
  <img src="docs/photos/first test and actual playing.jpg" alt="First test and actual playing" width="250">
  <img src="docs/photos/tube screamer.jpg" alt="Tube Screamer clone" width="250">
</p>

## Known issues (v1)

This is a first, working build — not a finished commercial product. Current known issues:

- **Gain-network resistor error:** the resistor network was meant to total roughly 510KΩ, but was accidentally wired as a 470KΩ and 47KΩ resistor in parallel instead of the intended value. The pedal didn't work correctly until the 47KΩ resistor was isolated and removed; the remaining 470KΩ (not an exact 510KΩ) was kept rather than sourcing the precise part.
- **Potentiometer mounting holes** in the enclosure are slightly too small for the threaded metal pot bushings.
- **Audio jack footprint misalignment:** the 3D-printed footprints for the jacks came out slightly off-center, which prevents all four PCB mounting screws from being used at once. Currently held with 2 of 4 screws, plus the footswitch mounted to the enclosure body for extra rigidity.
- Two of the lid standoffs needed hand-sanding to fit properly as a result of the above.
- **Knob/label overlap:** the knobs installed on the pots are large enough to cover parts of the engraved labels on the enclosure surface (e.g. part of the "Distortion" label is obscured once the knob is on).

## License

This project is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) — you're free to build, use, study, and modify this design (including for your own non-commercial projects), as long as you give credit and share any derivatives under the same license. Commercial use (selling built units, kits, or the design itself) is not permitted without separate permission.

## Credits

Designed and built by Arshak Khoshnevis.
