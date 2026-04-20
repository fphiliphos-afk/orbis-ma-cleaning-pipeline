# orbis-ma-cleaning-pipeline
*“Mock Orbis M&amp;A data cleaning pipeline for a family ownership &amp; acquisition study (Continental Europe, 2005–2026). Includes BVD‑ID linking, currency conversion to EUR, construction of family_owned, diversification, n_acq, total_value, and firm‑year panel. Fully reproducible Python + Stata code.”*
# Orbis M&A Cleaning Pipeline – Family Ownership & Acquisitions

**Purpose:** Demonstrate a reproducible data cleaning pipeline for a study on how family ownership influences acquisition activity in Continental Europe (2005–2026), using Moody’s Orbis / Orbis M&A data.

## Files

| File | Description |
|------|-------------|
| `clean_orbis_mock.py` | Full cleaning script: loads raw mock data, cleans BVD-IDs, converts currency using ECB rates, constructs `family_owned`, `diversification`, `n_acq`, `total_value`, and outputs deal-level + firm-year panel. |
| `present_clean_data_updated.py` | Generates quality report, summary stats, frequency tables, histograms, yearly trends, correlation heatmap. |
| `sample_clean_deals.csv` | First 20 rows of final deal-level dataset. |
| `sample_clean_panel.csv` | First 20 rows of final firm-year panel. |
| `data_dictionary.csv` | Variable definitions, sources, transformations. |
| `reproducibility_log.txt` | Step-by-step log from raw to clean data. |

## Key Features

- BVD‑ID linking across years (fuzzy matching demo)
- Daily ECB exchange rates → real EUR
- Family ownership flags (threshold‑based)
- Diversification (NACE 2‑digit comparison)
- Firm‑year panel with acquisition counts and total values

## Requirements

- Python 3.8+
- pandas, numpy, matplotlib, seaborn

## How to Run

1. Place your raw Orbis M&A export (CSV) on your Desktop as `raw_deals.csv`.
2. Run `python clean_orbis_mock.py`
3. Run `python present_clean_data_updated.py`

## Author

[Feleke Philiphos] – prepared for Upwork proposal demonstration.
