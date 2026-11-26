# TS808 Clone — Bill of Materials

> Pricing in Iranian Toman, based on a domestic parts order that covered several projects at once. Some parts — especially the capacitor variety — were bought in bulk rather than priced exactly one-per-position, so treat this as a **rough estimate of real build cost**, good enough to show the savings vs. a retail Ibanez pedal, not a lab-exact parts list.

| Component | Spec | Qty | Unit price (Toman) | Line total |
|---|---|---|---|---|
| Op-amp | RC4558 DIP | 1 | 73,100 | 73,100 |
| Transistor | 2SC1815, NPN TO-92 | 1 | 12,400 | 12,400 |
| Clipping diode | 1N4148 | 2 | 7,200 | 14,400 |
| DC power jack | 2.0mm barrel, DC005 | 1 | 52,900 | 52,900 |
| Mono 1/4" jacks | Input + output | 2 | 39,500 | 79,000 |
| 3PDT footswitch | FS5700-style, imported from Turkey | 1 | 900,000 | 900,000 |
| Pot — Drive | 500K standard | 1 | 150,000 | 150,000 |
| Pot — Tone | 20K standard | 1 | 196,000 | 196,000 |
| Pot — Level | 100K long-shaft | 1 | 213,000 | 213,000 |
| Knob caps | Colored 3AG-style, 1 per pot | 3 | 47,300 | 141,900 |
| Resistor | 100K standard | 1 | 29,000 | 29,000 |
| Resistor | 470KΩ (gain-network resistor — see Known Issues) | 1 | negligible | ~0 |
| Other resistors + battery clip + LED | Negligible cost, rolled in as misc | — | — | ~0 |
| Heat-set insert | For enclosure assembly (PETG) | 8 | 6,400 | 51,200 |
| Film cap, propylene audio | 47nF / 630V axial | 1 | 279,000 | 279,000 |
| Film cap, propylene audio (OXO) | 22nF / 250V axial | 1 | 141,400 | 141,400 |
| Electrolytic, RUBYCON | 100µF / 10V | 1 | 15,800 | 15,800 |
| Electrolytic, ELNA SILMIC (non-polar) | 10µF / 16V | 1 | 162,000 | 162,000 |
| Electrolytic, ELNA | 0.22µF / 50V | 1 | 4,500 | 4,500 |
| Electrolytic, ELNA (non-polar) | 0.22µF / 16V | 1 | 4,600 | 4,600 |
| Electrolytic, Panasonic audio (non-polar) | 1µF / 50V | 2 | 116,000 | 232,000 |
| Electrolytic, Panasonic audio | 47µF / 10V | 1 | 33,400 | 33,400 |
| Ceramic disc | 100nF | 1 | 5,800 | 5,800 |
| Multilayer ceramic | 100nF | 1 | 9,100 | 9,100 |
| Multilayer ceramic | 51pF | 1 | 13,900 | 13,900 |
| Film cap, AD Electronics | 0.047µF / 250V | 1 | 64,800 | 64,800 |
| **Parts subtotal** | | | | **≈2,879,100** |
| PCB fabrication | CheapPCB, single unit (board >100cm²) | — | — | 2,615,480 |
| Enclosure — bottom | PETG, FDM, 50% infill, print-service quote | 1 | — | 1,628,328 |
| Enclosure — lid | PETG, FDM, 50% infill, print-service quote | 1 | — | 758,787 |
| **Running total** | | | | **≈7,881,695** |

At recent free-market rates, the toman/USD rate has been swinging roughly between 210,000 and 272,000 toman per dollar over the last couple of months.[^1] At that range, ≈7,881,695 toman works out to roughly **$29–38** — up from the original "$15–20" guess, mostly due to a few items that aren't pocket-change local parts: the imported footswitch (900,000), the PCB fab run (2,615,480), and the enclosure print-service cost (2,387,115 combined). Still well under a third of what a new Ibanez TS808 costs.

[^1]: Shafaq News reporting on Iran's free-market USD/toman rate: [above 230,000](https://shafaq.com/en/Economy/Iranian-currency-falls-as-USD-tops-230K-tomans-in-free-market), [above 236,000](https://shafaq.com/en/Economy/US-dollar-tops-236-000-Iranian-tomans), [243,550 one-year high](https://shafaq.com/en/Economy/US-Dollar-hits-one-year-high-in-Iran), [272,200](https://shafaq.com/en/Economy/Iranian-toman-weakens-against-US-dollar-5).

---

## Known Issues (v1)

Current, known limitations of the v1 build:

- **Gain-network resistor bug:** the resistor network was meant to total roughly 510KΩ, but was accidentally wired using a 470KΩ and a 47KΩ resistor in parallel instead of the intended configuration. The pedal didn't work correctly until the 47KΩ resistor was isolated and removed; the 470KΩ alone (not an exact 510KΩ) was kept in the final build rather than sourcing the precise value.
- **Potentiometer mounting holes too small** for the threaded metal pot bushings — had to be worked around during assembly.
- **Audio jack footprint inaccuracy:** the 3D-printed footprints for the jacks came out slightly off-center, preventing all four PCB mounting screws from fitting at once. Worked around by using 2 of the 4 screws plus mounting the footswitch itself to the enclosure body for extra rigidity.
- **Two lid standoffs needed hand-sanding** to fit, as a side effect of the jack alignment issue above.
- **Knob/label overlap:** the knobs on the pots are large enough to cover part of the engraved labels on the enclosure surface.
- Power source: tested and confirmed working on a 9V battery.

The PCB came out to ~82×126mm (≈103cm²), consistent with it needing a panelized fabrication run.
