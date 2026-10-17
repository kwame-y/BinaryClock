# Hardware

Open `BinaryClock3.kicad_pro` in **KiCad 10**. This is a snapshot of the saved BinaryClock3 project supplied on October 17, 2026.

The source schematic and project settings were copied byte-for-byte. The packaged PCB differs only in four 3D model path strings, changed to `${KIPRJMOD}/3dmodels/...` so those models travel with the project. No electrical connections, geometry, routing, or placement were changed. The original files remain untouched.

`Custom_Libraries` includes the four custom symbol definitions extracted from this schematic's embedded symbol cache and five footprint files copied from the adjacent Custom Models folder. The project library tables use relative paths. These are packaging operations, not validation of the custom parts. The board's embedded footprints remain authoritative for the saved layout; DRC reports two library-footprint mismatches.

Install the standard KiCad 10 symbol, footprint, and 3D-model libraries as well. Model assignments are incomplete in the saved design, so the included renders omit some component bodies.

`source-sha256.json` records the original three source-file hashes. `reports` contains the checks run on this packaged snapshot. See [VALIDATION.md](VALIDATION.md) before using it for fabrication.
