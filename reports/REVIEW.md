# Final reproducibility review

Completed 11 November 2026. The received Colab notebook and exported results are preserved. Repeated reconstruction in the older notebook reflected recovery from expired Colab sessions; consolidation is a reproducibility improvement rather than a judgment on that working process.

## Completed checks
- The exact supplied workbook was loaded, footer rows removed and country-year data reconstructed. The 713-row exported sample matches all columns from the received Colab run.
- The organized notebook was executed from its first cell through its last in a newly started Python kernel. All 17 code cells completed without saved errors. Notebook schema validation passed.
- The six final CSVs for the nine main regressions, two mortality sensitivity tables, annual outcome/financing means and annual country counts match the prior Colab exports within absolute/relative tolerance 1e-8.
- All 84 mortality and life-expectancy observations for CAF, Somalia and South Sudan, 2010–2023, match the supplied new WDI extract exactly. See SOURCE_VERIFICATION.md.
- Both regenerated figures were visually reviewed for titles, units, labels, clipping and layout. The two notes explain sample composition, weighting and nominal spending.
- The input hash, software versions, exact validation package set and executed notebook are saved. ZIP integrity was checked.

## Organized notebook changes
Added section explanations, local loading with a Colab fallback, source-value checks, a source hash and package manifest, consolidated exports and model interpretation. Removed checkpoint downloads and the separately demonstrated first UHC model, which is already included in the nine-model loop. Retained original sample, estimators, source values, historical five-record sensitivity and figure definitions. No imputation, replacement data or unrequested new model search was introduced.

## Results and scope
The panel contains 742 country-years; the common sample has 713 observations in 52 countries, with 51 annual countries except 2012 (50). All nine financing intervals include zero. The mortality spending coefficient changes sign after the historical five-record exclusion, and the log-mortality coefficient also has an interval spanning zero. These are imprecise observational estimates, not evidence that financing is irrelevant.

The newly supplied notebook does not include the older pooled OLS, correlation and VIF analyses. They are not claimed as reproduced components of this edition. Broader residual, influence and functional-form diagnostics were not added.

## Remaining limitations
WDI consistency is verified for the requested 84 values; independent validation or explanation of the underlying demographic estimates is separate and has not been established. The historical SLE 2010 exclusion is outside that verification scope and is not a confirmed error. The original acquisition date/URL and reason for omitting Djibouti remain undocumented. Model sensitivity, complete-case selection, nominal currencies, changing annual membership and possible time-varying confounding remain substantive limitations.

The local fresh-kernel run tests file loading on Windows/Python 3.12, not the Colab upload fallback. Source-provider data versions may change in future. No source-value correction is justified by the completed comparison. No GitHub upload or project code license selection was performed.
