### Cleaner
This notebook takes the .csv file produced in the Scraper and cleans it such that it can be used without any further changes for the actual analysis

The code does the following transformations:

- Extracts country code from the name column, than using an auxiliary web-downloaded file  provides the full name of the country based on the country code. The country codes used by organizer seems to be a combination of two formats, thus the unmatched codes are changed manually.

- From the category column the gender (first letter) and age range (last 2 digits or 1 letter, i this case we substitute it for the corresponding age).

- Times are transformed to the seconds/minutes, such that they can be treated as numeric in the analysis. The missing value is denoted by dash, for easier transformation, this is replaced by zeros in the appropriate format and be treated later on in the analysis.

First dataframe produced is the `marathon_clean.csv` which serves as a general datasource for the further analysis.

Additionally, `pace_table.csv` is created with a pace on each segment of a course for each runner. This dataframe is transformed to long format such that it is ready for visualisations.