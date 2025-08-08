# Data Science Assignment - Web3 Trading Team

## Overview
This repository contains the analysis of trading behavior against market sentiment (Fear vs. Greed) for the Web3 Trading Team's data science assignment. The analysis is implemented in a Google Colab notebook (`notebook_1.ipynb`) and uses two datasets: the Bitcoin Market Sentiment Dataset and Historical Trader Data from Hyperliquid.

## Directory Structure
```
ds_<candidate_name>/
├── notebook_1.ipynb              # Main analysis notebook
├── csv_files/                   # Processed data outputs
│   └── sentiment_analysis.csv    # Sentiment analysis results
├── outputs/                     # Visual outputs
│   └── pnl_vs_sentiment.png     # Plot of closed PnL vs. sentiment
├── ds_report.pdf                # Summarized insights and explanations
└── README.md                    # Setup instructions and notes
```

## Setup Instructions
1. **Open Google Colab**:
   - Access [Google Colab](https://colab.research.google.com/) and open `notebook_1.ipynb` using the shared link (set to "Anyone with the link can view").

2. **Upload Datasets** (if using local files):
   - Download the datasets:
     - Fear/Greed: [https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf)
     - Historical: [https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs)
   - Upload to Colab:
     - Click the folder icon in Colab's left sidebar.
     - Upload `fear_greed_index.csv` and `historical_data.csv` to `/content/`.

3. **Alternative: Load from URLs**:
   - Use the provided CSV export URLs (ensure sheets are shared with "Anyone with the link can view"):
     - Fear/Greed: `https://docs.google.com/spreadsheets/d/1AuXwO80PNpP9SsUPe75tm7Sd4YTYneZCyjy-oXPI__o/export?format=csv&gid=0`
     - Historical: `https://docs.google.com/spreadsheets/d/1s8BBUJ-fzVNddmoW_V3NL7wFe-9m-lUselRKVFOCi1U/export?format=csv&gid=0`
   - Update the notebook's file paths to these URLs if preferred.

4. **Run the Notebook**:
   - Execute all cells in `notebook_1.ipynb`.
   - The notebook uses `pandas`, `matplotlib`, and `scipy`, which are pre-installed in Colab.
   - Verify column names and Bitcoin symbol (`@107`) using printed outputs.

5. **Save Outputs**:
   - The notebook saves:
     - Sentiment analysis table to `csv_files/sentiment_analysis.csv`.
     - Plot to `outputs/pnl_vs_sentiment.png`.
   - Download these files from Colab to include in the submission directory.

6. **GitHub Repository**:
   - Clone this repository: `git clone <repository_url>`.
   - Ensure the directory structure matches `ds_<candidate_name>/`.
   - Push updates to GitHub for submission.

## Notes
- **Column Names**: The Fear/Greed Dataset uses `date` and `classification` (lowercase). The Historical Trader Data uses `Timestamp`, `Coin`, `Size Tokens`, and `Closed PnL`. Verify these with `print(df.columns)` to avoid `KeyError`.
- **Bitcoin Symbol**: The code assumes `Coin == '@107'` for Bitcoin trades. Check `historical_df['Coin'].unique()` to confirm or adjust.
- **Data Loading**: Local files are used for simplicity, but URLs can be used if sheets are publicly accessible. Ensure proper sharing settings.
- **Submission**: Replace `<candidate_name>` with your name (e.g., `ds_johndoe`). Share the Colab notebook link and GitHub repository as instructed.
- **Extensions**: Consider adding leverage analysis (`Leverage` column, if available) or lagged sentiment effects for deeper insights.

For issues, refer to the notebook comments or contact [candidate email].