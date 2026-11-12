# Main analytical variables

| Variable | Export code | Unit / interpretation |
|---|---|---|
| uhc_service_coverage | SH_UHC_SCI | UHC service coverage index, 0–100 |
| life_expectancy | SP.DYN.LE00.IN | Life expectancy at birth, years |
| under5_mortality | SH.DYN.MORT | Under-five mortality per 1,000 live births |
| gdp_per_capita | NY.GDP.PCAP.CD | Current US$ per person |
| health_expenditure_per_capita | SH.XPD.CHEX.PC.CD | Current US$ per person |
| government_health_expenditure_gdp | SH.XPD.GHED.GD.ZS | Domestic general government health spending, % GDP |
| out_of_pocket_expenditure | SH.XPD.OOPC.CH.ZS | Out-of-pocket spending, % current health expenditure |
| log_gdp_per_capita | Derived | Natural log, only for positive GDP |
| log_health_expenditure_per_capita | Derived | Natural log, only for positive spending |

Country Code and Year identify a unique observation. Unrenamed source indicator columns remain in the processed panel but are not model regressors. Maternal mortality is not a project outcome and has only 47 available observations out of 742. Population and urban population are counts. PPP GDP in the source is current international dollars and is not used in the primary models. No inflation or currency conversion adjustment was applied.
