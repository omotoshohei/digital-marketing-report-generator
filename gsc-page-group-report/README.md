

| Step                | Purpose                                          | Key function(s)                                   |
| ------------------- | ------------------------------------------------ | ------------------------------------------------- |
| **1. Authenticate** | Mount Drive & authorise Google Sheets API        | `initialize_colab_and_gsheets()`                  |
| **2. Load data**    | Pull raw GSC exports (one worksheet per group)   | `load_dataframes()`                               |
| **3. Pre-process**  | Clean dates/numbers, add fiscal labels (FY24/25) | `df_preprocess()` → `preprocess_all_dataframes()` |
| **4. Aggregate**    | Build month-level tables with YoY & MoM deltas   | `generate_monthly_table()`                        |
| **5. Visualise**    | Create bilingual bar charts (日本語 labels ready)   | `generate_monthly_graph()`                        |
| **6. Package**      | Assemble cover, TOC, charts & tables into PDF    | `generate_pdf()`                                  |
