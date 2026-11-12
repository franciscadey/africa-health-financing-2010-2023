# Health financing and population health in Africa, 2010–2023

**Completed WDI comparison (11 November 2026):** all 84 values for mortality and life expectancy in CAF, Somalia and South Sudan, 2010–2023, match the newly supplied WDI extract exactly. Retain the source values. This resolves consistency with WDI for these records, not independent validation of the underlying demographic estimates. See `SOURCE_VERIFICATION.md`.


**Source-check update (11 November 2026):** the newly supplied WDI extract also reports CAF 2022 under-five mortality as 424.6. This observation matches the current supplied WDI download and was not introduced by cleaning. Other flagged observations and underlying-provider validation remain open. See `SOURCE_VERIFICATION.md`.


## Question and design
This capstone examines associations between health financing and UHC service coverage, life expectancy at birth and under-five mortality. It uses the supplied country-level export for 2010–2023. The descriptive panel contains 53 countries and 742 country-year observations. The common complete-case sample has 52 countries and 713 observations. This is a selected export rather than complete coverage of Africa; Djibouti is absent and the selection rationale remains undocumented.

Nine ordinary least-squares models include country and year indicator terms, log GDP per capita, and one financing measure at a time: log health spending per capita, government health expenditure as a percentage of GDP, or out-of-pocket expenditure as a percentage of current health spending. Country-clustered standard errors use finite-sample correction and t inference with 51 degrees of freedom. All comparisons are exploratory and unadjusted for multiple testing.

## Descriptive findings
Within the common sample, unweighted country means show overall increases in UHC coverage and life expectancy and a decline in under-five mortality between 2010 and 2023. Financing trends fluctuate. Nominal per-capita spending and government spending as a share of GDP finish above their 2010 levels; the out-of-pocket share finishes below its 2010 level. These are country averages, not population-weighted regional estimates. There are 51 countries in each annual mean except 2012, which has 50. Membership changes across years.

## Main regression findings
All nine financing confidence intervals include zero. The spending-per-capita coefficients are:

| Outcome | Coefficient | 95% confidence interval | p-value |
|---|---:|---:|---:|
| UHC index | −0.3845 | −2.2773 to 1.5083 | .6851 |
| Life expectancy | −1.6405 | −3.6856 to 0.4046 | .1135 |
| Under-five mortality | 7.3335 | −8.8229 to 23.4898 | .3664 |

Full results for all indicators are in results/tables/main_regression_results.csv. These estimates do not provide clear evidence of a financing association under these specifications. They do not demonstrate that financing has no effect or is unimportant. The level-outcome spending coefficients are per one-unit increase in natural-log spending; for a 10% spending increase, multiply by log(1.10).

## Sensitivity
The historical exclusion of CAF 2014/2019/2021/2022 and SLE 2010 changes the mortality spending coefficient from +7.3335 to −0.4913, with the sample falling from 713 to 708. The exclusion estimate has p=.8609 and interval −6.0932 to 5.1107. Both intervals include zero, but the sign and magnitude change substantially. Thus the magnitude and direction are sensitive to those observations. The exclusion is an influence check, not a correction of confirmed errors.

With log under-five mortality as the outcome, the spending elasticity is .0305 (p=.6189; 95% interval −.0918 to .1528; 713 observations). Changing the outcome scale does not establish the validity of the source values.

## Data quality and limitations
The workbook contains CAF mortality of 424.6 per 1,000 and life expectancy of 18.818 years in 2022, and other unusual paired observations in CAF, Somalia and South Sudan. They are retained unchanged. All 84 checked values for these three countries and two outcomes match the new WDI extract exactly. This verifies WDI consistency while independent validation or explanation of the underlying demographic estimates remains outside the completed check. The five-record sensitivity does not cover all unusual records or test life-expectancy sensitivity. Some extreme source records are already absent from the common sample because financing or GDP is missing.

The analysis cannot identify causality. Country effects remove time-invariant country differences and year effects absorb common shocks, but time-varying confounding, reverse causation, measurement error and cross-country dependence remain possible. Current-dollar spending is affected by inflation and exchange rates. A declining out-of-pocket share does not prove lower absolute household payments or reduced financial hardship. Complete-case selection and modeled health estimates constrain interpretation. Broader functional-form, residual and influence diagnostics have not been completed in this fresh notebook.

## Conclusion
The prior statistical findings have been reproduced in the new Colab run. The requested WDI consistency check is complete and the organized notebook has now executed successfully in a fresh kernel with unchanged result tables. The source values are retained. Findings remain exploratory and limited by the unusual underlying estimates, sample selection and observational design. The documented project is ready for repository review and upload; causal or strong policy claims are not supported.
