# Airbnb Data Cleaning

This project uses a Jupyter notebook to inspect and clean the Airbnb listings dataset. It demonstrates basic data preparation with pandas and exports the resulting data to CSV and Excel formats.

## Files

- `Airbinb.ipynb` — notebook for inspecting and cleaning the data.
- `Airbnb_Open_Data.csv` — source dataset required by the notebook.
- `Cleaned_data_csv` — cleaned CSV output created when the notebook runs.
- `Excel_cleaned_data.xlsx` — cleaned Excel output created when the notebook runs.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- pandas
- openpyxl (for Excel export)

Install the Python packages if needed:

```bash
python -m pip install pandas openpyxl jupyter
```

## Run the notebook

Open a terminal in this project folder and start Jupyter:

```bash
jupyter notebook
```

Open `Airbinb.ipynb` and run the cells in order. The notebook reads `Airbnb_Open_Data.csv` using a relative path, so keep the notebook and source CSV in the same folder.

## What the notebook does

1. Loads the dataset and inspects its columns, structure, and sample rows.
2. Selects or removes columns to reduce the dataset.
3. Removes duplicate rows.
4. Cleans selected values, including uppercasing host identity verification and converting instant-bookable values to `1` or `0`.
5. Removes currency symbols and commas from prices, drops rows without a price, and converts prices to integers.
6. Exports the resulting data to `Cleaned_data_csv` and `Excel_cleaned_data.xlsx`.

The notebook also explores column-name changes and missing values. Its `dropna()` call is not assigned back to the data, so it does not remove all rows with missing values; only rows missing a price are explicitly dropped before export.
