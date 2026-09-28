# Track 1: BA Labor Market in China (2026 Pilot)

## Project overview
This repository contains the A1 pilot data, coding sheet, collection protocol, and cleaning scripts for a study of BA/DA/BI job postings in mainland China in 2026.

## Research question
In publicly visible BOSS Zhipin Business Analytics-related job postings collected between 2026-09-27 and 2026-09-28, what skills do they require, and how are salary levels related to role type, city, industry, and AI-related skills?

## Data
- Source: BOSS Zhipin public search pages, manual collection.
- Collection period: 2026-09-27 to 2026-09-28.
- Record count: 110 postings (clean sample: 91 eligible records).
- Raw data: `data/raw/job_data.csv`
- Cleaned data: `data/cleaned/boss_pilot_cleaned.csv`
- Codebook: `data/documentation/codebook.md`
- Collection protocol: `data/documentation/collection_protocol.md`

## How to reproduce the pilot
1. Clone this repository.
2. Install dependencies: `pip install pandas openpyxl numpy matplotlib`
3. Run `python run_cleaning.py` to produce the cleaned dataset and figures.

## Known gaps and biases
- This is a manual convenience sample, not a random sample.
- BOSS Zhipin search ranking may affect which postings are visible.
- Some salary fields are missing or ambiguous.

## Contributors
- Yingqi Liu
- Sitong Guo
- Wenqian Li