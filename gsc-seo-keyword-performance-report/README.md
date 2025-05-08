# GSC SEO Keyword Performance Report

This project builds a **monthly SEO keyword performance report** from Google Search Console (GSC) data stored in Google Sheets.  
The workflow runs completely in **Google Colab**, translates top‑performing Japanese keywords to English with **LangChain + OpenAI**, calculates month‑over‑month and year‑over‑year deltas, and outputs a multi‑section **PDF** ready for stakeholders—complete with Japanese fonts and metric definitions.

---

## Key Features

- **Zero‑setup Colab Notebook**  
  Authenticates Google Drive & Sheets (`gspread`) with two lines—no local installs.

- **Automated Google Sheets Ingestion**  
  Reads every worksheet in the spreadsheet `gsc-seo-keyword-performance-report`, skipping the target‑keyword tabs (`df_kw_target_jp`, `df_kw_target_en`).  
  All sheets are concatenated into a single DataFrame for analysis.

- **Clean & Enrich Data**  
  - Removes commas/percent signs and converts columns to `int`/`float`.  
  - Generates pivot tables for **Clicks**, **Impressions**, **CTR**, and **Average Position**.  
  - Adds _vs. Last Month_ and _vs. Last Year_ columns for instant trend spotting.

- **AI‑powered Keyword Translation**  
  Uses **LangChain** with **GPT‑4o‑mini** to translate the top 55 Japanese queries into clean English equivalents—perfect for international teams.

- **Category Merging Helper**  
  `merge_category_data()` smart‑merges click & rank tables with your target keyword lists, then auto‑adds **average** and **total** summary rows.

- **Professional PDF Output**  
  Styled with **ReportLab** and Japanese **GenShin Gothic** fonts:  
  - Cover page & auto‑generated Table of Contents  
  - Eight tables (Clicks, Impressions, CTR, Rankings + JP/EN target sections)  
  - Appendix with metric definitions & licence note

---

## Process

1. **Open in Colab**  

2. **Mount Drive & authenticate**  
   Run the first cell—Colab will guide you through OAuth for Drive & Sheets.

3. **Prepare your spreadsheet**  
   - File name **`gsc-seo-keyword-performance-report`**  
   - Worksheets:  
     - Monthly GSC exports (e.g., `202402`, `202403`, `202502`, `202503` …)  
     - Target lists: `df_kw_target_jp`, `df_kw_target_en`  
   - Share the sheet with your Colab e‑mail / service‑account.

4. **Set your OpenAI key**  
   In Colab:  
   ```python
   from google.colab import userdata
   userdata.set('OPENAI_API_KEY', 'sk‑...')

5. **Run all cellst**
The notebook will:
   - Load & clean data
   - Translate keywords
   - Build pivot tables and category summaries
   - Save gsc-keyword_performance_report_monthly-YYYY-MM-DD.pdf to your /content and Drive.

