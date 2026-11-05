# Zimbabwe Used Vehicle Market Analysis

**Author:** Tatenda Alistair Gonzo  
**Project type:** Exploratory Data Analysis (EDA)  
**Tools:** Python, Pandas, Matplotlib, Jupyter/Google Colab  
**Data snapshot date:** 5 November 2026

## Project overview
This project explores publicly advertised used-vehicle listings in Harare, Zimbabwe. It examines asking prices, vehicle age, mileage, make/model mix and listing characteristics.

The aim is to demonstrate a practical data analytics workflow: data sourcing, documentation, cleaning, exploratory analysis, visualisation and communication of limitations.

## Dataset
The initial dataset is in `data/used_vehicles.csv`. It contains 21 listing observations sourced from:
- [AutoTrader Zimbabwe – Toyota Axio listings in Harare](https://www.autotrader.co.zw/cars/for-sale/harare/toyota/axio)
- [Classifieds.co.zw – used Toyota Axio listings](https://www.classifieds.co.zw/zimbabwe-cars/Toyota/axio/used)
- [Zimbabwe Marketplace – motor vehicles in Harare](https://www.zimbabwemarketplace.co.zw/motor-vehicles/harare)

Each row includes the source page URL and a collection date. Some records were captured from search-result pages rather than individual advert pages; this is documented in the `notes` field. Some attributes were not visible in the search result and are intentionally left blank rather than guessed.

## Important data limitations
- This is a small, non-random convenience sample, not a representative census of Zimbabwe's vehicle market.
- The sample is heavily weighted toward Toyota Axio listings; comparisons across makes should therefore be treated cautiously.
- Asking prices are not confirmed transaction prices.
- Listings may be duplicated across websites or may change/disappear. Cross-platform duplicates should be reviewed during further cleaning.
- Vehicle attributes not displayed in the source result are left missing.
- All listed prices in this starter dataset are denominated in USD. Currency is retained as a separate field for validation.
- This dataset is a point-in-time snapshot and should be refreshed before drawing current market conclusions.

## Research questions
1. What is the distribution of advertised asking prices in this sample?
2. How do asking prices vary by model year and mileage?
3. Which makes and models appear most frequently?
4. How complete are the available listing attributes?
5. What additional data would be required for stronger market conclusions?

## Repository structure
```text
.
├── data/
│   └── used_vehicles.csv
├── notebooks/
│   └── vehicle_market_analysis.ipynb
├── reports/
│   └── preliminary_findings.md
├── visuals/
│   └── (generated charts saved here)
├── requirements.txt
└── README.md
```

## How to run
1. Open `notebooks/vehicle_market_analysis.ipynb` in Google Colab or Jupyter.
2. If using Colab, upload `data/used_vehicles.csv` when prompted, or mount your Google Drive/repository.
3. Run the notebook cells from top to bottom.

## Ethics and responsible use
Only publicly visible listing information is included. Personal contact details are excluded. Listing URLs are retained for traceability. Respect source website terms and do not use the data to imply seller endorsement or verified vehicle condition.
