# Snapshot Validation

Checked October 17, 2026 using **KiCad 10.0.3**. These results describe the packaged BinaryClock3 snapshot under its saved project rules. They are not an independent electrical review or a manufacturing sign-off. Ignored checks and severity settings are recorded in the JSON reports.

| Check | Result |
|---|---:|
| ERC errors | 5 |
| ERC warnings | 2 |
| DRC errors | 17 |
| DRC warnings | 127 |
| Unconnected items reported by DRC | 0 |
| Schematic-to-PCB parity findings | 0 |

## Electrical Checks

[ERC.json](reports/ERC.json) reports three undriven power-pin findings, one undriven input, one power-output-to-power-output connection, and two labels connected to only one pin. Inspect their exact locations in KiCad; the repository packaging task did not resolve or waive them.

## Board Checks

[DRC.json](reports/DRC.json) reports clearance, copper-edge clearance, solder-mask bridging, connection-width, dangling track/via, library-footprint mismatch, and silkscreen/text findings. DRC ran with schematic parity checking. Copper zones were not refilled or saved as part of this packaging operation.

## Part and Manufacturing Details to Review

- U4 is labeled BQ25186DLHR, but its symbol and footprint identifiers name BQ25185. This naming discrepancy is not proof of compatibility or incompatibility; check the actual device pin mapping and land pattern.
- The plotted board outline is approximately 60 × 30 mm, exceeding the initial 50 × 30 mm target.
- The saved stackup is four-layer, 1.6 mm, with white front and blue back mask and no copper finish specified.
- The exact battery and its temperature-sensor implementation remain to be confirmed.
- The exported BOM lists generic passive values and several generic symbol values. It is not ready for direct procurement without a part-selection review.
- Firmware, charging tests, assembled-board behavior, and enclosure fit were not validated in this task.
