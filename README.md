# Electricity Access and GDP per Capita

Homework 2: Collaborative Data Wrangling & EDA
DSE 511 – Fall 2026

---

## Dataset Information

* **Sources:** [World Bank – Access to Electricity](https://data.worldbank.org/indicator/EG.ELC.ACCS.ZS) and [World Bank – GDP per Capita](https://data.worldbank.org/indicator/NY.GDP.PCAP.KD)
* **Date accessed:** September 2, 2026
* **Description:** The first dataset reports the percentage of each country’s population with access to electricity. The second dataset reports GDP per capita in constant 2015 US dollars.
* **Years used:** 2000–2023
* **Raw file sizes:** Electricity access is about 166 KB, and GDP per capita is about 367 KB.
* **Final size:** 4,914 rows and 5 columns
* **Countries and territories:** 211
* **License:** Creative Commons Attribution 4.0 (CC BY 4.0)

---

## Methods

### Data Cleaning – Teliyah Jackson

The datasets were cleaned and combined using Python and pandas. The cleaning steps included:

* Removed metadata columns that were not needed.
* Kept data from 2000 to 2023.
* Changed both datasets from wide format to long format.
* Renamed columns to make them easier to understand.
* Changed the year and measurement columns to numeric data types.
* Combined the datasets using country code and year.
* Removed rows with missing electricity or GDP values.
* Removed regional and income-group totals.
* Checked for duplicate country-year rows.
* Checked the electricity and GDP value ranges.
* Sorted the final data by country and year.
* Saved the cleaned data as `Data/cleaned/electricity_gdp_cleaned.csv`.

### Exploratory Data Analysis – Ben

The datasets were transformed and analyzed also using Python and pandas. Pandas was also used to generate a scatterplot.

* Imported the combined and cleaned file, courtesy of Teliyah.
* Transformed the data into per-country averages.
* Calculated the summary statistics prior to per-country and after per-country averaging.
	** Statistics used include mean, standard deviation, min, max, 25th, 50th, and 75th percentiles, as these are included in the "describe()" package.
* Calculated the correlation between electricity_access and gdp_per_capita
* Scatter plotted the result. Terminated analysis when it became clear that the two variables have an incredibly strong near step-wise relationship.



---

## Results

The final cleaned dataset contains 4,914 complete country-year records from 211 countries and territories. It has no missing measurements or duplicate country-year rows.

The exploratory data analysis results and representative figure will be added after the analysis is completed.

The correlation between electrification and GDP per capita was about 0.4.

Electrification per capita was heavily clustered around 100%; the median country had 99% electrification, but the mean country had 81% electrification.

Most interestingly, there was a break point at about $15k in GDP per capita. All countries with a GDP per capita greater than approximately that value had full electrification.

---

## Collaboration Notes

* **Teliyah Jackson:** Created the repository, cleaned and combined the data, and documented the cleaning process.
* **Ben:** Calculated summary statistics, transformed data, created scatterplot.
* **Both partners:** Documented results in the README, prepared documents for submission.

---

## Reproducibility Instructions

1. Clone or download this repository.

2. Install the required Python package:

   `pip install -r requirements.txt`

3. Open `Notebooks/data_cleaning.ipynb` in Jupyter Notebook or VS Code.

4. Run the notebook cells from top to bottom.

5. An internet connection is needed when the notebook requests country information from the World Bank API.

6. The cleaned dataset will be saved in `Data/cleaned`.

---

## Merge Conflict Reflection

Coming soon