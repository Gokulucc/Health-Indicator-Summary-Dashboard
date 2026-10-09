Global Life Expectancy and Between-Country Inequality, 1950–2023

A reproducible descriptive epidemiology project in R, examining how life expectancy at birth has changed across 237 countries since 1950, and whether the gap between countries has narrowed.

Key findings
Life expectancy rose substantially. Mean life expectancy across countries increased from 49.7 years in 1950 to 74.1 years in 2023, a gain of over 24 years.
Between-country inequality narrowed. The gap between the 90th and 10th percentile countries fell from 30.4 to 18.8 years, driven by faster gains among countries with the lowest life expectancy (+28.4 years at the 10th percentile vs +16.9 years at the 90th).
Large inequalities remain. In 2023, life expectancy ranged from 54.5 years (Nigeria) to 86.4 years (Monaco). The distribution was negatively skewed (median 75.3 years), with the lowest values concentrated in sub-Saharan Africa.
COVID-19 is visible. A temporary decline in mean life expectancy occurred in 2020–2021.

Methods

Data source: Life expectancy at birth from Our World in Data. Full source details are in life-expectancy/readme.md.

Data cleaning

Started with 21,565 country-year records.
Removed regional, continental and income-group aggregates (e.g. "Africa", "High-income countries") to avoid double counting.
Removed sub-national entities (England and Wales, Scotland, Northern Ireland), since the United Kingdom is included, and the historical USSR, since its successor states are included.
Retained Kosovo, which has a non-standard OWID country code.
Restricted the analysis to 1950–2023, because pre-1950 estimates were available only for a small number of high-income, mainly European countries.
Result: a balanced panel of 237 countries × 74 years (17,538 observations), with no missing country-years.

Analysis

Descriptive statistics (mean, median, SD, range) for 2023.
Annual mean, 10th and 90th percentiles across countries, 1950–2023.
Inequality measured as the 90/10 percentile gap, chosen because it is robust to single extreme values.

Data quality checks and sensitivity analysis

Extreme low values were investigated. North Korea in 1950 (14.2 years) reflects mortality during the Korean War.
Estimates for the Central African Republic showed implausible year-to-year volatility from 2009 onwards (e.g. 18.8 years in 2022 and 57.4 in 2023), consistent with modelled crisis mortality in a country with limited vital registration.
Re-running the inequality analysis excluding the Central African Republic did not change the results.



Limitations
Estimates are unweighted by population: each country counts equally, so results describe the typical country rather than the typical person.
Life expectancy at birth is a period measure, reflecting mortality in a given year rather than the actual lifespan of any cohort.
Estimates for countries with limited vital registration are modelled and carry substantial uncertainty that is not shown here.
The analysis is descriptive and does not examine causes of the


Tools

R · tidyverse (dplyr, ggplot2, readr) · Quarto · renv · Git/GitHub

Author

Gokulraj Venkatesan, MPH (University College Cork)
