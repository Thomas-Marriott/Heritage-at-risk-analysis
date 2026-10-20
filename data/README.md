# Data

## Source
Historic England, **Heritage at Risk Register 2025** (published 6 November 2025).

File: `HAR_Register_2025_Entries_including_additions_and_removals.ods`
(listed on Historic England's site as "2025 entries, additions and removals").

## Where it came from
"Annual Heritage at Risk Registers and Maps" page on the Historic England website:
https://historicengland.org.uk/listing/heritage-at-risk/search-register/annual-heritage-at-risk-registers-and-maps/

Historic England asks that this data is taken from its published spreadsheets or Open Data Hub, not scraped from the website.

## Downloaded on
20 October 2026

## Licence and attribution
Copyright Historic England. Historic England publishes its open data under the Open Government Licence; the exact attribution wording for this file should be confirmed at the source page above.

## File format
OpenDocument Spreadsheet (`.ods`). To read it in Python with pandas:

```python
# pip install odfpy
import pandas as pd
sheets = pd.read_excel("data/HAR_Register_2025_Entries_including_additions_and_removals.ods",
                       sheet_name=None, engine="odf")
```

## Tabs in the file
| Tab | What it holds | Rows | Columns |
|---|---|---|---|
| `PLEASE_READ_How_to_use` | Introduction and notes from Historic England on how to use the data | n/a | n/a |
| `Entries_on_the_Register` | Every entry on the 2025 register | 4,891 | 28 |
| `Additions` | Entries added to the register this year | 138 | 28 |
| `Positive_Removals` | Entries removed for positive reasons, with a reason category | 129 | 23 |

The columns include region, local authority, heritage category, risk methodology, condition, vulnerability, trend and priority category. See the `PLEASE_READ_How_to_use` tab for Historic England's own definitions.

## Notes on use
- This is one year only. Earlier years (2013 to 2024) are published on the same page and may be added later.
- Cleaning decisions are recorded in the main project README and the notebooks, not here.
