# Data Dictionary

| Field | Description | Type |
|---|---|---|
| listing_id | Project-assigned row identifier; not an original advert ID | Text |
| make | Vehicle manufacturer | Text |
| model | Vehicle model | Text |
| year | Advertised model year | Integer |
| price | Advertised asking price | Numeric |
| currency | Currency shown in the listing | Text |
| mileage_km | Advertised mileage in kilometres | Numeric |
| transmission | Advertised transmission; blank when not stated | Text |
| fuel_type | Advertised fuel type; blank when not stated | Text |
| body_type | Advertised body category | Text |
| location | Location shown in the source result | Text |
| date_collected | Date the observation was transcribed | Date |
| source_name | Website from which the observation was collected | Text |
| listing_url | Source results/category page; not necessarily an individual advert | URL |
| notes | Additional context or caveats captured during transcription | Text |

Blank transmission and fuel fields mean the detail was not available in the captured result. Potential duplicate observations are flagged for manual review and are not automatically removed. Prices are asking prices, not verified transaction values.
