# Completed WDI consistency check

Compared on 11 November 2026. The supplied P_Data_Extract_From_World_Development_Indicators (2).xlsx contains the requested three countries, two indicators and 14 years. Footer rows were excluded. Source files remain unchanged.

## Result
**All 84 values match the original workbook** (absolute tolerance 1e-10; no missing values in either side). Maximum absolute difference is zero.

| Country | Under-five mortality, 2010–2023 | Life expectancy, 2010–2023 |
|---|---:|---:|
| Central African Republic | 14 / 14 match | 14 / 14 match |
| Somalia | 14 / 14 match | 14 / 14 match |
| South Sudan | 14 / 14 match | 14 / 14 match |

This includes CAF 2022 mortality of 424.6 per 1,000 and life expectancy of 18.818 years; CAF's other flagged years; Somalia 2011; and the flagged South Sudan years. The values were not introduced by notebook cleaning. Detailed comparison is in results/tables/source_verification_84_observations.csv.

## Analytical decision
Retain the original WDI values in the primary models. No data correction, imputation or new exclusion is supported by this comparison. Main results and figures therefore remain unchanged. The historical five-record exclusion remains an influence sensitivity rather than an alternative corrected dataset. It includes SLE 2010, which is outside this three-country verification extract and is not an established source error.

## What this establishes and what it does not
The requested WDI source-consistency check is complete for these 84 observations. This is not an independent validation of the demographic estimates: both files derive from WDI. Understanding the extreme estimates would require underlying UN IGME/UN population documentation or provider clarification. Their magnitude and the mortality coefficient's sensitivity should remain in the limitations, without describing the values as confirmed mistakes.

This extract does not validate other countries, indicators or years, and the full original workbook's acquisition date/URL and country-selection rationale remain undocumented. The supplied filename and source metadata were retained; the actual browser download URL and date were not independently captured. The review date above is not a claimed acquisition date.

## Suggested capstone wording
The unusual mortality and life-expectancy observations for Central African Republic, Somalia and South Sudan were compared with a newly downloaded WDI extract for 2010–2023. All 84 values matched the original workbook and were retained in the primary analysis. This establishes consistency with WDI rather than independent validation of the underlying estimates. A historical five-record exclusion showed sensitivity of the mortality spending coefficient and is reported as an influence check.

Earlier one- and two-observation extracts are preserved in data/verification. This full comparison supersedes their limited coverage.
