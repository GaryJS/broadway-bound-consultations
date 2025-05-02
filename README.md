# Broadway Bound Consultations

## Metadata Overview
This dataset contains weekly Broadway show performance data spanning from 1985 to 2022.

## Data Source
- **Source:** [Kaggle.com](https://www.kaggle.com/datasets/praveensh/broadway-shows-data/data)
- **Collected by:** Praveen Shahani
- **Data Format:** `.csv`

## Data Collection and Extraction
- Data was webscraped by the original uploaded and made available on Kaggle.
- Downloaded from Kaggle as a `.csv` file.
- No major transformations occurred during extraction.

## Data Cleaning Process
- Data was cleaned using Python, primarily utilizing the pandas library for data manipulation.
- Column names were reformatted for SQL-friendly conventions (lowercase, underscores instead of spaces, removal of special characters).
- Data types were corrected (e.g., numeric types for financial field)
- Missing show names were replaced with "Unknown".
- Duplicate rows were removed.
- Dates were standardized, and new fields for year, month, and day were extracted from the date field.
- Cleaned data was saved into a new Data Frame and imported into a MySQL relational database.

## Data Units and Column Definitions

| Column Name             | Description                                              | Data Type          |
|--------------------------|----------------------------------------------------------|--------------------|
| `year`                   | Year of the Broadway performance (extracted from date)   | Integer (`int32`)  |
| `showname`               | Name of the Broadway show                                | String (`object`)  |
| `potentialgross`         | Total gross revenue from ticket sales ($)                | Float (`float64`)  |
| `difference`             | Difference between potential gross and actual gross ($) | Float (`float64`)  |
| `averageticket`          | Average price of a ticket ($)                            | Float (`float64`)  |
| `seatssold`              | Number of seats sold for the performance                 | Integer (`int64`)  |
| `seatsintheater`         | Number of seats available in the theater                 | Integer (`int64`)  |
| `previews`               | Number of preview performances before official opening  | Integer (`int64`)  |
| `cap`                    | Percentage of seating capacity sold (%)                 | Float (`float64`)  |
| `diffcap`                | Change in seating capacity percentage from previous week | Float (`float64`)  |
| `date`                   | Full date of the performance (YYYY-MM-DD)                | DateTime (`datetime64[ns]`) |
| `month`                  | Month of the performance                                | Integer (`int32`)  |
| `day`                    | Day of the performance                                  | Integer (`int32`)  |

## Data Validation and Regulations
- Data was cross-checked against Playbill.com.
- This data set is for **educational purposes only**.
- Playbill.com usage policies but be followed (if applicable).

## References
- [Original Dataset on Kaggle](https://www.kaggle.com/datasets/praveensh/broadway-shows-data/data)
- [Playbill official Website](https://playbill.com/grosses)

---
- **Authors** Gary San Angelo, Robert Clemens
- **Date** 04/28/2025
