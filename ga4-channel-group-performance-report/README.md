# GA4 Channel Group Report

This repository contains a Google Colab project for generating monthly channel group reports using data exported from Google Analytics 4. The project reads data from a Google Spreadsheet, processes and aggregates metrics on a monthly basis, generates informative tables and graphs, and finally compiles everything into a polished PDF report using ReportLab.

## Key Features

- **Google Colab Integration:**  
  The code is designed to run seamlessly in Google Colab, so you don't need to install complex packages locally.

- **Google Sheets Data Pipeline:**  
  Automatically reads and processes data from your Google Spreadsheet.  
  *(For the data table, download the Excel file, update it as needed, then upload and convert it to a Google Spreadsheet.)*

- **Data Preprocessing:**  
  Converts raw data to numeric values and datetime objects, extracts the year and month, and assigns fiscal years based on custom logic.

- **Visualization:**  
  Generates monthly bar graphs with customizable colors for each fiscal year.

- **Comprehensive Reporting:**  
  Aggregates individual channel data (including an "All Channel" summary that sums up all channels by month) and creates tables with Year-over-Year (YoY) and Month-over-Month (MoM) comparisons.

- **PDF Report Generation:**  
  Combines tables and graphs into a final PDF report complete with a cover page, table of contents, and metric explanations.

## Getting Started

1. **Open the Notebook in Google Colab:**  
   Simply open the provided Colab notebook.

2. **Connect Your Google Drive:**  
   Mount your Google Drive in Colab to access your files.

3. **Update Your Data:**  
   Download the Excel file for the data table, update it as needed, then upload and convert it to a Google Spreadsheet.

4. **Run the Cells:**  
   Execute the cells in order to generate your reports.

## Contributing

Feel free to contribute to this project by submitting pull requests, opening issues, or providing feedback. Your contributions are welcome!
