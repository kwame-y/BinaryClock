---
title: Pocket Binary Clock
author: Kwame
description: A compact rechargeable clock displaying HH:MM:SS with 20 LEDs.
modified_at: 2026-10-17
---

# Design history

This entry summarizes the project discussion. It does not represent a new inspection of the current hardware files, and no time-spent estimates have been added.

The project started with a 50 × 30 mm target, KiCad 10, twenty LEDs, three buttons, USB-C charging, and a transparent enclosure. The main devices selected were the ATtiny1616, IS31FL3239, RV-3028-C7, and BQ24074.

Battery-temperature limits led to a proposal to add a hardware interlock to the BQ24074 design. That approach increased the component count. A later simplification proposal used the BQ25186, with charger configuration handled through firmware. The battery, connector, and thermistor arrangement still need to be finalized together.

The workflow then changed to manually connecting and routing the design, using a parts list and connection guide. The earlier generated schematic should be treated as a separate draft until reconciled with that manual work.

# October 17th, 2026

The current project was located in BinaryClock3 and packaged using PCBCard's repository organization. The board is branded TickTock REV 1.0 and includes routing and front/back silkscreen artwork.

The current schematic labels the charger BQ25186DLHR. Its custom symbol and footprint names still reference BQ25185, which remains a verification item. The earlier BQ24074 draft was not imported into this snapshot.

The package now contains the KiCad 10 project, project-specific libraries, available custom 3D models, a schematic-derived BOM, schematic/layer exports, and front/back 3D renders. Model paths were made portable in the packaged copy; the original design files were not edited.

KiCad 10.0.3 reports 5 ERC errors and 2 warnings, and 17 DRC errors and 127 warnings. It reports zero unconnected items and zero schematic-to-PCB parity findings. These checks establish the draft's current state; they do not make it fabrication-ready.

The saved design is approximately 60 × 30 mm, with four copper layers and a 1.6 mm board setting. This differs from the initial width target. The production folder currently contains a draft BOM only.
