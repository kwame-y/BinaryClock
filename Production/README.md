# Production

**Draft only: no fabrication release is included.**

`BOM.csv` was exported from the current schematic using KiCad 10.0.3, grouped by value and footprint. It includes 52 component instances plus 4 test points. External battery and thermistor selection is still pending. Complete manufacturer part numbers, ratings, and sourcing before ordering.

The schematic and PCB still have ERC/DRC findings; see [validation details](../Hardware/VALIDATION.md). Gerbers and placement files have deliberately not been issued as a production release.

When the design is ready, export revision-matched Gerbers for all copper and required fabrication layers, drill files, an assembly BOM, component placement data, and manufacturing notes. Record the source commit, KiCad version, and validation results with that release.
