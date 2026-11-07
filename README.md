# Zimbabwe Used Vehicle Market Analysis

**Author:** Tatenda Alistair Gonzo  
**Project:** Exploratory data analysis (EDA)  
**Snapshot date:** 5 November 2026  
**Tools:** Python, Pandas, NumPy, Matplotlib and Jupyter/Google Colab

## Project overview

This project explores a small snapshot of publicly advertised used-vehicle listings found on Zimbabwean listing websites. It demonstrates a basic analytics workflow: collecting and structuring observations, inspecting data quality, calculating descriptive statistics, identifying possible duplicates, visualising patterns and communicating limitations.

The project is exploratory and educational. It is not a valuation tool and does not estimate the price of every used vehicle in Zimbabwe.

## Questions explored

1. What does the asking-price distribution look like in this sample?
2. How do asking prices vary by model year?
3. What is the relationship, if any, between advertised mileage and asking price?
4. Which makes and models dominate the collected sample?
5. Which fields are missing, and are there possible duplicate advertisements?

## Dataset snapshot

The CSV contains **21 listing observations** collected on 5 November 2026:

- 18 Toyota Axio observations.
- 1 Honda Fit, 1 Nissan X-Trail and 1 Toyota Fortuner.
- All recorded asking prices are in USD.
- Transmission and fuel type are not stated for 3 observations.

The data was manually transcribed from public search/results pages. The `listing_url` field points to the relevant results/category page, not necessarily an individual advert. Some records therefore cannot be independently traced to a unique live advert from the CSV alone.

## Preliminary sample observations

- Median advertised asking price: **US$12,500**.
- Median advertised mileage: **71,000 km**.
- The sample is strongly concentrated in Toyota Axio listings.
- Two records (ZWV006 and ZWV016) share the same make, model, year, price and mileage. They are flagged for manual review, not automatically deleted.

These figures describe only the collected observations. They must not be presented as representative Zimbabwe-wide market prices.

## Repository structure

```text
.
├── data/
│   ├── used_vehicles.csv
│   └── DATA_DICTIONARY.md
├── notebooks/
│   └── vehicle_market_analysis.ipynb
├── reports/
│   ├── data_sources.md
│   └── preliminary_findings.md
├── visuals/
│   └── README.md
├── requirements.txt
└── README.md
```

## Run the analysis

### Option A — Google Colab

1. Open the notebook: [vehicle_market_analysis.ipynb](notebooks/vehicle_market_analysis.ipynb).
2. Select **Open in Colab** (or upload the notebook to Google Colab).
3. Run the cells from top to bottom.
4. If prompted, upload `data/used_vehicles.csv` from this repository.

### Option B — Local Jupyter

1. Download or clone this repository.
2. Install the packages:

   ```bash
   pip install -r requirements.txt
   ```

3. Start Jupyter from the repository's root folder:

   ```bash
   jupyter notebook
   ```

4. Open `notebooks/vehicle_market_analysis.ipynb` and run all cells.

The notebook saves generated charts in the `visuals/` folder.

## Data quality and limitations

- **Convenience sample:** observations were selected from visible search results, not a random sample.
- **Model imbalance:** Toyota Axio accounts for most records, limiting comparisons between models.
- **Possible duplicates:** ZWV006 and ZWV016 have matching make, model, year, price and mileage. The available source pages do not establish whether they are the same advert, so both are retained and flagged.
- **No individual advert URLs:** the stored URLs lead to source result/category pages. This reduces record-level traceability.
- **Asking prices only:** advertised prices are not confirmed sale prices and may be negotiable.
- **Snapshot only:** listings may be edited, removed or sold after collection.
- **Missing attributes:** unknown transmission and fuel values are left blank rather than guessed.
- **No causal claims:** this sample cannot establish that mileage or age causes a particular price.

## Responsible use

Only publicly visible vehicle listing attributes are included. Seller names, phone numbers and other personal contact details are excluded. Source links are provided for transparency. Respect the terms of the websites from which listing information is collected.

## Next improvements

1. Revisit each source and capture individual advert URLs and verification timestamps.
2. Review the two possible duplicate records manually.
3. Expand the sample across more makes, models, locations and price bands.
4. Record price conditions such as negotiable, duty paid or before duty consistently.
5. Refresh the dataset and compare snapshots over time.
6. Add a dashboard only after the underlying dataset is more complete.

## Visual previews

- [Asking-price distribution](visuals/price_distribution.svg)
- [Median asking price by model year](visuals/median_price_by_year.svg)
- [Mileage versus asking price](visuals/mileage_vs_price.svg)
- [Missing values](visuals/missing_values.svg)

[Open the notebook in Google Colab](https://colab.research.google.com/github/tatendagonzo/zimbabwe-used-vehicle-market-analysis/blob/main/notebooks/vehicle_market_analysis.ipynb).
