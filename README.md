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
