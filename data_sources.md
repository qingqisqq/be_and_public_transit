# Data Sources

All raw data stored in `raw_data/` and never modified.

---

## 1. My Daily Travel Survey

- **Provider:** Chicago Metropolitan Agency for Planning (CMAP)
- **Used for:** Trip records, sociodemographics, mode choice outcome
- **Notes:** Home-based trips filtered; trip mode recoded to binary
  transit vs. private vehicle
- **URL** https://datahub.cmap.illinois.gov/documents/2e0719dce2c34eeea81039eca35def80/about

---

## 2. EPA Smart Location Database

- **Provider:** U.S. Environmental Protection Agency
- **Variables used:** Population density, employment density (D1C),
  employment entropy
- **URL** https://www.epa.gov/smartgrowth/smart-location-mapping#SLD

---

## 3. OpenStreetMap

- **Provider:** OpenStreetMap contributors
- **Variables used:** Intersection density, road network complexity,
  amenity / POI density

---

## 4. Chicago Open Data Portal

- **Provider:** City of Chicago
- **URL:** https://data.cityofchicago.org
- **Datasets used:** parks, CTA stops

---

## 5. Satellite Imagery (Mapbox Static API)

- **Provider:** Mapbox
- **Access:** Requires API token (stored in `.env`, not committed)
- **Coverage:** 1,148 census tracts
- **Notes:** Image extent adaptive to tract size

---


