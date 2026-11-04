# Track 1: BA Labor Market in China (2026 A2)

## Project overview
This repository contains the pilot data, updated raw and cleaned datasets, codebooks, collection protocol, automated extraction scripts, and validation notebooks for our study of the 2026 Business Analytics (BA) job market in China. This builds upon our A1 pilot data.

## Research question
In 2026, what core and AI-related skills are demanded for BA-related roles in China, and how
do these skill requirements correlate with salary levels across different role families and city tiers?

## Data & Deliverables
- **Source**: BOSS Zhipin public search pages (manual collection).
- **Collection period**: 2026-09-27 to 2026-11-02.
- **Record count**: 194 eligible postings (from 234 raw records).
- **Raw data**: `data/raw/boss_pilot_A2_raw_merged.csv`
- **Cleaned data**: `data/cleaned/boss_pilot_A2_cleaned.csv`
- **Analysis-ready data**: `data/cleaned/clean_pool_for_gold_set.csv`

### Measurement & Validation (A2 Core)
- **Codebook**: `data/documentation/codebook_A2.docx`
- **Machine Extraction Results**: `data/documentation/machine_extraction_results_A2.csv`
- **Human Gold Set**: `data/documentation/Goldset_Coder_B_150.csv` and `Goldset_Coder_C_50.csv`
- **Validation Notebook**: `notebooks/03_Validation.ipynb` (Produces F1-Score = 0.414 and Cohen's Kappa = 0.408).

### Code & Notebooks
- `notebooks/01_cleaning.ipynb`: Data cleaning pipeline.
- `notebooks/02_M6_M8_Analysis.ipynb`: Automated skill extraction (Regex) and EDA figures.
- `notebooks/03_Validation.ipynb`: Model validation and inter-coder agreement.

## How to reproduce
1. Clone this repository.
2. Install dependencies: `pip install pandas numpy matplotlib seaborn scikit-learn openpyxl`.
3. Run the Jupyter Notebooks in the `notebooks/` directory in order (01 -> 02 -> 03).

## Known gaps and biases
- Manual convenience sample, not a random sample.
- Automated extraction (Regex) struggles to distinguish between "must-have" and "nice-to-have" AI skills, resulting in an F1-score of 0.414.
- Human coders had a moderate agreement (Kappa = 0.408) on ambiguous AI requirements in the JDs.

## Contributors
- Yingqi Liu (Data Collection, Cleaning, Analysis, Validation)
- Sitong Guo (Data Collection, Codebook Design, Human Coding)
- Wenqian Li (Data Collection, Human Coding, Report Writing)