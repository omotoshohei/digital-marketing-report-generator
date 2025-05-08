# Google Search Console Page-Group Monthly Report

This repository contains a Google Colab project (and standalone Python script) for generating monthly page-group performance reports using data exported from Google Search Console. The notebook/script reads data from a Google Spreadsheet, cleans and aggregates metrics by fiscal month, renders informative tables and graphs, and compiles everything into a polished PDF report via ReportLab.

## Key Features

- **Google Colab Integration**  
  Run end-to-end in Colab—no local install needed. Includes auth helper for Drive & Sheets.

- **Google Sheets Data Pipeline**  
  Automatically reads one worksheet per page-group.  
  *(For local CSV backups, drop them in `data/`, or point the script to any folder of CSV exports.)*

- **Data Preprocessing**  
  - Drops unused columns (`CTR`, `Position`)  
  - Parses `Date` to datetime, cleans numeric columns  
  - Extracts year/month/week and assigns custom fiscal years (FY23–FY25)

- **Aggregation & Comparison**  
  - Pivots metrics by fiscal month  
  - Computes Year-over-Year (YoY) and Month-over-Month (MoM) deltas

- **Visualization**  
  Bilingual bar charts (日本語 labels supported) comparing FY24 vs. FY25, saved automatically under `images/`.

- **PDF Report Generation**  
  Combines cover page, table of contents, side-by-side tables & charts, and an appendix of metric/page-group explanations into a single PDF.

## Process

1. **Open the Colab notebook**  

2. **Authenticate & mount Drive**  
   Run the first cell to mount Google Drive and authenticate with Google Sheets API.

3. **Prepare your Sheets**  
   - Create three Google Sheets named exactly:  
     - `1_df_heysho.com_gsc_daily_total`  
     - `2_df_heysho.com_gsc_daily_jp`  
     - `3_df_heysho.com_gsc_daily_en`  
   - Share each with your Colab service-account email (or your own Google account).

4. **Run all cells**  
   Execute through to the end. The script will:  
   - Load and preprocess data  
   - Generate monthly tables & charts  
   - Assemble and save `gsc-page-group-report-monthly-simple-YYYY-MM-DD.pdf`

## Contributing
Contributions welcome! Feel free to open issues, suggest enhancements, or submit pull requests for:

- Supporting additional page-groups
- Custom fiscal-year logic
- Alternative output formats (CSV, Excel)
- Styling tweaks to charts or PDF layout
