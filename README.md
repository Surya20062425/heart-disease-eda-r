# Heart Disease EDA & Regression (R — Base R)

Complete exploratory data analysis and regression pipeline for a heart-disease dataset (**10,000 rows × 21 columns**), written in **base R only** — no external packages required.

## Features

- **Dataset View** — shape, columns, types, unique value counts
- **Summary Statistics** — numerical summaries, categorical summaries, key metrics
- **Missing Values** — total + per-column counts, rows with NA, imputation (mean / mode)
- **Duplicate Records** — count + dedup summary
- **Descriptive Stats** — target prevalence, age/BMI ranges, correlation with target
- **Correlation** — top 10 feature–target correlations + numeric correlation heatmap
- **Histograms** — distributions of all numeric features
- **Boxplots** — numeric features grouped by heart-disease status
- **Scatter Plots** — Age vs BMI and Cholesterol vs BMI, colored by target
- **Outliers** — IQR 1.5×IQR rule detection per feature
- **Frequency Tables** — value counts for categorical features
- **Unique Values** — per-column unique-count summary
- **Linear Regression** — single feature → target
- **Multiple Linear Regression** — all numeric features → target

## Prerequisites

- **R 4.0+** — [Download from CRAN](https://cran.r-project.org/)
- **IRkernel** (for Jupyter Notebook support) — one-time setup:

```r
install.packages("IRkernel")
IRkernel::installspec()
```

## Installation

1. **Clone the repository:**

```bash
git clone https://github.com/Surya20062425/heart-disease-eda-r.git
cd heart-disease-eda-r
```

2. **Open the notebook in Jupyter:**

```bash
jupyter notebook heart_disease_eda_R.ipynb
```

Or open it in **VS Code** with the R extension, **RStudio**, or any Jupyter-compatible environment.

## Data

The notebook automatically searches for `heart_disease.csv` in common locations relative to the notebook:

- `heart_disease.csv`
- `heart.csv`
- `heart_disease_data.csv`
- `data/heart_disease.csv`
- `../heart_disease.csv`
- `../heart.csv`

**To use your own data:** Set `DATA_PATH` in Code Cell 2 to point at your CSV file:

```r
DATA_PATH <- "path/to/your/heart_data.csv"
```

**If no CSV is found**, a synthetic dataset with the same schema (10,000 × 21) is generated automatically so every section stays runnable.

### Expected Schema (21 columns)

| Column | Type | Description |
|--------|------|-------------|
| Age | numeric | Age in years |
| Sex | character | Male / Female |
| BMI | numeric | Body Mass Index |
| Cholesterol | numeric | Total cholesterol |
| Triglycerides | numeric | Triglycerides |
| SystolicBP | numeric | Systolic blood pressure |
| DiastolicBP | numeric | Diastolic blood pressure |
| Glucose | numeric | Blood glucose |
| PhysicalHealth | numeric | Days of poor physical health (0-30) |
| MentalHealth | numeric | Days of poor mental health (0-30) |
| SleepTime | numeric | Average hours of sleep |
| Smoking | character | Yes / No |
| AlcoholDrinking | character | Yes / No |
| Stroke | character | Yes / No |
| DiffWalking | character | Yes / No |
| Diabetes | character | Yes / No |
| PhysicalActivity | character | Yes / No |
| Asthma | character | Yes / No |
| KidneyDisease | character | Yes / No |
| SkinCancer | character | Yes / No |
| HeartDisease | character | **Target** — Yes / No |

## Usage

1. Open `heart_disease_eda_R.ipynb` in Jupyter
2. Select the **IRkernel** (R kernel) for the notebook
3. Run cells sequentially (Cell → Run All) or step through each section
4. All outputs (tables, plots, model summaries) render inline

### Key Variables

- `TARGET_COL` — auto-detected target column (defaults to `HeartDisease`)
- `RANDOM_STATE` — seed for reproducibility (default: 42)

## Outputs

The notebook produces:
- Summary tables (dimensions, missingness, duplicates, statistics)
- Visualizations (histograms, boxplots, scatter plots, correlation heatmap)
- Outlier detection reports (IQR method)
- Linear regression summaries (single & multiple features)
- Frequency tables for all categorical features

## License

MIT License — feel free to use, modify, and distribute.