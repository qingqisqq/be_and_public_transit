# Data Sources

All raw data stored in `raw_data/` and never modified.

---

## 1. My Daily Travel Survey

- **Provider:** Chicago Metropolitan Agency for Planning (CMAP)
- **Used for:** Trip records, sociodemographics, mode choice outcome
- **Notes:** Home-based trips filtered; trip mode recoded to binary
  transit vs. private vehicle

> [TBC: exact URL, version/date, license]

---

## 2. EPA Smart Location Database

- **Provider:** U.S. Environmental Protection Agency
- **Variables used:** Population density, employment density (D1C),
  employment entropy
- **License:** Public domain (U.S. federal government)

> [TBC: exact version and download date]

---

## 3. OpenStreetMap

- **Provider:** OpenStreetMap contributors
- **License:** Open Database License (ODbL)
- **Variables used:** Intersection density, road network complexity,
  amenity / POI density

> [TBC: download date / snapshot]

---

## 4. Chicago Open Data Portal

- **Provider:** City of Chicago
- **URL:** https://data.cityofchicago.org
- **Datasets used:** Building footprints, parks, CTA stops, land use

> [TBC: exact dataset names and download dates]

---

## 5. Satellite Imagery (Mapbox Static API)

- **Provider:** Mapbox
- **Access:** Requires API token (stored in `.env`, not committed)
- **Coverage:** 1,148 census tracts
- **Notes:** Image extent adaptive to tract size

> [TBC: exact API endpoint, access date]

---

## 6. VLM Model Weights

Models used (loaded from HuggingFace / official releases):
- CLIP (ViT-B/32, ViT-L/14, ViT-H/14)
- RemoteCLIP (ViT-B/32, ViT-L/14)
- DINOv3 (Sat-B, Sat-L, Sat-H)
- InternVL3-78B (used for Tier 3 phrase generation)

> [TBC: exact model checkpoints / commit hashes]

Model weights are **not** stored in this repository.
