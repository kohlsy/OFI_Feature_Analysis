# OFI_Feature_Analysis

## Requirements
See `requirements.txt` for Python dependencies:

Install them via `pip install -r requirements.txt`.

## Steps to Run
1. Clone the repo
2. In `scripts/multi_stock_ofi.py`, set your `API_KEY`.
3. Run `python scripts/multi_stock_ofi.py`.
   - This will pull 1 week of MBP-10 data for each stock, compute OFI/PCA/returns, and save pickled data in `/data`.
4. For cross-impact, load the 5 pickled DataFrames, merge them, and run a multi-variate regression using the cross-impact notebook.
5. Plots and tables can be seen in `project/results/`.
6. Summaries go in `notebooks/` or PDF for the final report.

## Notebook Descriptions

Filename: multi_stock_ofi.py

Description:
  Pulls 1 week of MBP-10 data for each of the 5 specified stocks,
  computes multi-level OFI (top 5 levels), aggregates to 1-minute,
  runs PCA to create OFI_PCA, computes mid-price & 1-minute returns,
  saves the final DataFrame to /data/<symbol>_1m_aggregated.pkl.

Filename: multi_stock_crossimpact.py

Description: 
- Analyze Cross-Impact (merges all 5 pickled dataframes,runs cross-impact regressions for contemporaneous and 1-min-lag).
- Quantify Results (print regression stats, compare self vs. cross-impact).
- Visualization and Reporting (heatmaps, scatter, etc., saved to /results).
