# NHS Waiting List and Service Performance Analysis

An R Markdown portfolio project analysing NHS England
referral-to-treatment (RTT) waiting-list data for three London
trusts between April 2024 and March 2026.

## Aim

Explore changes in waiting-list size and waiting times,
compare selected specialties, and identify patterns that
warrant further investigation.

## Scope

- **Trusts:** Barts Health, Guy’s and St Thomas’, and
  Imperial College Healthcare.
- **Specialties:** General Surgery, Trauma and Orthopaedics,
  and Ophthalmology.
- **Data:** 24 monthly Excel workbooks, producing 216
  trust–specialty–month observations.

Counts represent incomplete pathways at month-end,
rather than unique patients.

## Tools and Methods

- **R:** readxl, dplyr, tidyr and ggplot2.
- **R Markdown:** reproducible HTML reporting.
- Automated workbook import and reporting-month extraction.
- Checks for missing records, duplicates, missing values,
  invalid measures and published 18-week proportion mismatches.
- Monthly and annual changes, trend charts and summary heatmaps.

## Key Findings

Between March 2025 and March 2026:

- Both the count and proportion waiting over 52 weeks
  decreased in all nine selected trust–specialty combinations.
- General Surgery at Guy’s and St Thomas’ recorded
  waiting-list growth of **90.03%**, alongside a
  **16.34 percentage-point decline** in the proportion
  within 18 weeks.
- Barts Health Ophthalmology recorded waiting-list growth
  of **21.82%**, alongside a **4.79 percentage-point decline**
  in the proportion within 18 weeks.
- Imperial College Healthcare recorded smaller waiting
  lists and improvements in both waiting-time proportions
  across all three selected specialties.

These findings identify investigation priorities.
They do not establish the causes of the changes.

## Project Files

- `NHS_RTT_Analysis.Rmd`: analysis code and commentary.
- `NHS_RTT_Analysis.html`: rendered report.
- `data/`: original monthly Provider workbooks.

To read the HTML report, download it and open it in a browser.

## Reproduce the Analysis

1. Download or clone this repository.
2. Place the 24 source workbooks in the `data` folder.
3. Open RStudio with the project folder as the working directory.
4. Install the required packages:

    install.packages(c(
      "readxl", "dplyr", "tidyr",
      "ggplot2", "knitr", "rmarkdown"
    ))

5. Open `NHS_RTT_Analysis.Rmd` and select **Knit to HTML**.

The exact source filenames and software environment are
recorded in Section 11 of the report.

## Data Sources

NHS England monthly Incomplete Provider RTT workbooks:

- [RTT data 2024–25](https://www.england.nhs.uk/statistics/statistical-work-areas/rtt-waiting-times/rtt-data-2024-25/)
- [RTT data 2025–26](https://www.england.nhs.uk/statistics/statistical-work-areas/rtt-waiting-times/rtt-data-2025-26/)

Results reflect the downloaded workbook versions.
Published historical data may subsequently be revised.

## Limitations

The analysis covers selected services and is not adjusted
for case complexity or differences in service provision.
Monthly snapshots cannot be summed to count unique patients
or used alone to explain changes in demand or treatment activity.

## Author

Asif Khandokar

Independent portfolio project using publicly available data.
This project is not an official NHS publication.