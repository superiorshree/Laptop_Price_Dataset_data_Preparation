# Laptop Price Dataset: Data Preparation

Machine Learning, Activity 1 (Unit I: Foundations & Data Preparation).

This project takes a raw, messy laptop dataset and prepares it for a future machine learning task. No prediction model is trained here. The whole workflow is in one Jupyter notebook.

## Dataset

- **Name:** Laptop Price dataset (`laptopData.csv`)
- **Source:** <paste the link you downloaded the file from>
- **Size:** 1,303 rows x 12 columns (raw file)
- **What it contains:** laptop specifications (brand, type, screen size, CPU, RAM, storage, GPU, operating system, weight) and the price
- **Target for a future task:** `Price`

## What the notebook does

| Step | Work done |
|---|---|
| 1-2 | Select, load and inspect the dataset |
| 3 | Find data types, summary statistics and suspicious values |
| 4 | Count missing values (including hidden `?` placeholders) |
| 5 | Handle missing values (median for numbers, mode for text) |
| 6 | Remove duplicate rows and fix inconsistent labels |
| 7 | EDA: summary statistics, frequency counts and 4 graphs |
| 8 | One-hot encoding of the categorical columns |
| 9 | Train/test split and standardisation (`StandardScaler`, fitted on training data only) |
| 10 | Save the prepared dataset and write a conclusion |

## Problems found in the raw data

- 30 rows were completely empty
- `?` used as a hidden missing value in `Inches`, `Weight` and `Memory`
- 9 impossible screen sizes (above 20 inches) and 9 impossible weights
- 29 exact duplicate rows (hidden by a row-number column)
- Numbers stored as text with units (`8GB`, `1.37kg`), and `macOS` / `Mac OS X` used for the same operating system

## Result

The prepared file `laptop_prepared.csv` has **1,244 rows and 43 columns** and no missing values. The `split` column marks each row as `train` or `test`.

## Files

| File | Description |
|---|---|
| `ML_Activity1_Laptop_Data_Preparation.ipynb` | The full notebook with outputs and graphs |
| `laptopData.csv` | Original raw dataset (unchanged) |
| `laptop_cleaned.csv` | Cleaned data, before encoding and scaling |
| `laptop_prepared.csv` | Final data: encoded, split and scaled |
| `requirements.txt` | Python libraries needed |

## How to run

```bash
pip install -r requirements.txt
jupyter notebook ML_Activity1_Laptop_Data_Preparation.ipynb
```

Keep `laptopData.csv` in the same folder as the notebook. You can also open the notebook in Google Colab and upload the CSV using the Files panel. Running every cell recreates `laptop_cleaned.csv` and `laptop_prepared.csv`.

## Libraries

pandas, numpy, matplotlib, scikit-learn

## Author

Shreeyansh Mahamuni
