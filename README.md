# Python Templates for Marketing Analytics – Project Overview
In this project, I built a modular, Python‑driven reporting suite that automatically turns Google Analytics 4 (GA4) and Google Search Console (GSC) exports into polished, stakeholder‑ready reports—eliminating manual spreadsheet work and repetitive slide‑building.


## Background & Objectives
- Pulling GA4 and GSC metrics each month often means copy‑pasting CSVs, wrangling formulas, and formatting slides—work that steals hours from actual analysis.
- My goal was to compress that workflow to a single click: mount Drive, run the notebook, and receive three PDF reports (channel, page group, keyword) that mirror the questions executives ask most.

## Feature Highlights
| Template                     | Key Questions Answered                           | Outputs                                                 |
| ---------------------------- | ------------------------------------------------ | ------------------------------------------------------- |
| **GA4 Channel Group Report** | Which traffic sources are growing or shrinking?  | MoM / YoY tables, bar charts, all‑channel summary       |
| **GSC Page‑Group Report**    | How are language or content clusters performing? | Fiscal‑year‑aligned pivots, custom month order, visuals |
| **GSC Keyword Report**       | Which queries drive clicks—and how do we rank?   | AI‑translated keyword list, click‑rank‑CTR matrices     |

### Additional capabilities:
- Instant deltas: automatic vs. Last Month & vs. Last Year columns for every metric.
- AI translation: top Japanese queries are translated to English via LangChain + GPT‑4o, so global teams can follow along.
- PDF compilation: cover page, auto‑generated TOC, side‑by‑side tables & charts, all embedded with Japanese fonts for bilingual clarity.

## Typical Use Cases
- Monthly KPI Review – Replace slide decks with auto‑generated PDFs sent to leadership.
- Content Gap Analysis – Spot under‑performing page groups or keywords in seconds.
- International SEO Alignment – Share AI‑translated keyword trends with non‑Japanese stakeholders.

## Technical Stack
- Data: Google Sheets + gspread (raw GA4 & GSC exports)
- Processing: Pandas, NumPy, fiscal‑year logic in Python
- Visualisation: Matplotlib + japanize‑matplotlib for Japanese labels
- AI layer: LangChain + GPT‑4o‑mini (OpenAI) for keyword translation
- Reporting: ReportLab with GenShin Gothic fonts → multi‑section PDF
- Execution: Runs locally or in Google Colab; Drive mounted for seamless file I/O

This project turns hours of data grunt work into minutes of automated insight—freeing marketers to focus on strategy, not spreadsheets.
