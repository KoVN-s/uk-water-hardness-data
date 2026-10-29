# 💧 UK Water Hardness by Postcode Dataset (2026 Edition)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://waterhardness.uk)
[![Data Format](https://img.shields.io/badge/Format-CSV%20%7C%20JSON-blue.svg)](https://waterhardness.uk/outcodes)
The most comprehensive, granular open dataset of tap water hardness across the United Kingdom. Covers over **11,000+ UK postal sectors** and all **2,977 postal districts (outcodes)** across England, Scotland, Wales, and Northern Ireland.
> 🌐 **Official Interactive Directory & Live Postcode Checker:**  
> **[https://waterhardness.uk](https://waterhardness.uk)** — Check official Drinking Water Inspectorate (DWI) PPM ratings, water suppliers, and appliance salt settings by UK postcode.
---
## 📊 Dataset Schema
The main dataset is available in [`uk_water_hardness_by_postcode.csv`](./uk_water_hardness_by_postcode.csv):
| Column Header | Data Type | Description | Example |
| :--- | :--- | :--- | :--- |
| `sector` | String | Full UK Postal Sector | `YO19 6` |
| `outcode` | String | Postal District (Outcode) | `YO19` |
| `latitude` | Float | Geographic Latitude (WGS84) | `53.86613` |
| `longitude` | Float | Geographic Longitude (WGS84) | `-1.02924` |
| `elevation` | Integer | Elevation above sea level (meters) | `263` |
| `water_company` | String | Regional Water Wholesaler | `Yorkshire Water` |
| `ppm_reading` | Integer | Hardness in Parts Per Million (CaCO3) | `110` |
| `clark_degrees`| Float | Hardness in English Clark Degrees (°e) | `7.7` |
| `hardness_level`| String | Classification (Soft / Moderate / Hard / Very Hard) | `Moderately Hard` |
| `dishwasher_setting`| String | Recommended Dishwasher Salt Calibration Code | `H01` |
---
## 🚀 Quick Start / Usage
### Python (Pandas)
```python
import pandas as pd
# Load dataset directly from raw GitHub
url = "https://raw.githubusercontent.com/PHONGUIT22/uk-water-hardness-dataset/main/uk_water_hardness_by_postcode.csv"
df = pd.read_csv(url)
# Filter all postcodes with Very Hard water (> 200 PPM)
hard_water_areas = df[df['ppm_reading'] >= 200]
print(f"Total hard water sectors: {len(hard_water_areas)}")
```
### cURL / Bash
```bash
curl -O https://raw.githubusercontent.com/PHONGUIT22/uk-water-hardness-dataset/main/uk_water_hardness_by_postcode.csv
```
---
## 🗺️ Key Regional Insights
- **Soft Water Zones (< 100 PPM):** Scotland (Edinburgh, Glasgow), North West England (Manchester, Lake District), Wales (Cardiff, Swansea), and parts of the South West (Devon, Cornwall). See the [UK Soft Water Areas Directory](https://waterhardness.uk/guides/soft-water-areas-in-the-uk).
- **Aggressively Hard Water (> 280 PPM):** London, Thames Valley (Reading, Oxford), East Anglia (Norwich, Cambridge), and South East England (Brighton, Southampton). Check the [London Postcode Hardness Guide](https://waterhardness.uk/guides/london-water-hardness-by-postcode).
- **Interactive Heatmap:** Explore the [UK Water Hardness Map](https://waterhardness.uk/guides/uk-water-hardness-map-guide).
---
## 📜 Attribution & Citation Policy
This dataset is licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.
If you use this dataset in your research, academic papers, commercial products, or web applications, you **MUST** provide attribution with a backlink to the primary project homepage:
```text
Source: WaterHardness.uk - Official UK Water Hardness & Postcode Directory
URL: https://waterhardness.uk
```
