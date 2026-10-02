# Life expectancy - Data package

This data package contains the data that powers the chart ["Life expectancy"](https://ourworldindata.org/grapher/life-expectancy?v=1&csvType=full&useColumnShortNames=false) on the Our World in Data website. It was downloaded on October 2, 2026.

### Active Filters

A filtered subset of the full data was downloaded. The following filters were applied:

## CSV structure

Each row is an observation for an entity (usually a country or region) at a timepoint.

- "Entity" — the name of the entity, e.g. "United States".
- "Code" — our internal entity code. For most countries this is the [ISO alpha-3](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) code, e.g. "USA"; historical and other non-standard entities get a custom code.
- "Year" or "Day" — the timepoint. Annual data has a "Year" column holding an integer year; otherwise a "Day" column holds a date string in the form "YYYY-MM-DD".
- The final column is the data column — the time series that powers the chart. Downloaded with the "full data" option it corresponds to the time series below; with "only selected data visible in the chart" it is transformed depending on the chart type, so the correspondence may be less direct.


## Metadata.json structure

The .metadata.json file contains metadata about the data package. The "charts" key contains information to recreate the chart, like the title, subtitle etc. The "columns" key contains information about each of the columns in the csv, like the unit, timespan covered, citation for the data etc.

## How we process data at Our World in Data

Our World in Data is almost never the original producer of the data - almost all of the data we use has been compiled by others. If you want to re-use data, it is your responsibility to ensure that you adhere to the sources' license and to credit them correctly. Please note that a single time series may have more than one source - e.g. when we stitch together data from different time periods by different producers or when we calculate per capita metrics using population data from a second source.

Preparing this data involves several processing steps. Depending on the data, this can include standardizing country names and world region definitions, converting units, calculating derived indicators such as per capita measures, as well as adding or adapting metadata such as the name or the description given to an indicator.
[Read about our data pipeline](https://docs.owid.io/projects/etl/).

## Detailed information about the data


### Life expectancy – Long-run data – Riley; Zijdeman et al.; HMD; UN WPP
Period life expectancy is the number of years the average person born in a certain year would live if they experienced the same chances of dying at each age as people did that year.
Last updated: October 22, 2025  
Next expected update: October 2026  
Date range: 1543–2023  
Unit: years  
Source: Riley (2005); Zijdeman et al. (2015); HMD (2025); UN WPP (2024) – with major processing by Our World in Data  

#### How to cite this data

Riley (2005); Zijdeman et al. (2015); HMD (2025); UN WPP (2024) – with major processing by Our World in Data

#### What you should know about this data
- Across the world, people are living longer. In 1900, the global average life expectancy was 32 years. By 2023, this had more than doubled to 73 years.
- Countries around the world made big improvements, and life expectancy more than doubled in every region. This wasn’t just due to falling child mortality; people started living longer at all ages.
- Even after World War II, there have been large drops in life expectancy, such as during the Great Leap Forward famine in China, the HIV/AIDS epidemic in sub-Saharan Africa, the Rwandan genocide, or the COVID-19 pandemic.
- The UN counts crisis deaths in the year they happened, which can produce a sharp one-year fall. The Central African Republic reads 14.7 years in 2009 and 18.8 in 2022, against about 50 either side — the UN converted mortality surveys compiled by [Gang et al. (2023)](https://doi.org/10.1186/s13031-023-00514-z) into excess deaths for the years each survey was run, so these appear as isolated dips rather than the sustained gap the surveys point to.
- Period life expectancy is an indicator that summarizes death rates across all age groups in one particular year. It shows how long the average baby born in that year would be expected to live if they experienced the same chances of dying at each age as people did in that year.
- This chart shows long-run estimates of life expectancy compiled by our team from several data sources. Before 1950, for country-level data, we rely on the [Human Mortality Database (2025)](https://www.mortality.org/Data/ZippedDataFiles) combined with [Zijdeman (2015)](https://clio-infra.eu/Indicators/LifeExpectancyatBirthTotal.html). For regional data, we use [Riley (2005)](https://doi.org/10.1111/j.1728-4457.2005.00083.x). From 1950 onward, we use the [United Nations World Population Prospects (2024)](https://population.un.org/wpp/downloads).
- Detailed information on the source of each data point can be found on [this page](https://docs.google.com/spreadsheets/d/1LnrU1V3p2wq7sAPY4AHRdH1urol3cKev7prEvlLfSU4/edit?gid=0#gid=0).

#### Notes on our processing step for this indicator
This chart combines data from several sources. For country-level data before 1950, we use the Human Mortality Database (2025) data and Zijdeman et al. (2015). For country-years where these sources overlap, we use the Human Mortality Database.

For regional data, before 1950, we use Riley's (2005) estimates.

From 1950 onwards, we use the United Nations World Population Prospects (2024) for both country-level and regional data.

Detailed information on the source of each data point can be found on [this page](https://docs.google.com/spreadsheets/d/1LnrU1V3p2wq7sAPY4AHRdH1urol3cKev7prEvlLfSU4/edit?gid=0#gid=0).


## Sources

These are the sources behind the data in this package. Each time series above names the ones it draws on in its citation.

### Human Mortality Database

The Human Mortality Database (HMD) is a research resource that provides detailed mortality and population data for national populations with high-quality vital statistics. It includes original calculations of death rates and life tables, as well as the underlying data — such as birth counts, death counts, and census-based population estimates — used to produce these metrics.

Its scope is limited to countries with virtually complete death registration and census coverage, mostly wealthy and industrialized nations. The database’s core mission is to document the historical rise in human longevity and support research into its causes and implications. HMD follows a rigorous, uniform methodology focused on transparency, reproducibility, and comparability, while acknowledging limitations such as age misreporting and data coverage issues.

Each country’s dataset is curated and quality-checked by dedicated researchers, ensuring reliability for demographic and public health analysis.

Producer: Human Mortality Database  
Published: 2025-09-25  
Retrieved on: 2025-10-22  
Retrieved from: https://www.mortality.org/Data/ZippedDataFiles  
License: CC BY 4.0 (https://www.mortality.org/Data/UserAgreement)  

Citation: HMD. Human Mortality Database. Max Planck Institute for Demographic Research (Germany), University of California, Berkeley (USA), and French Institute for Demographic Studies (France). Available at www.mortality.org.

See also the methods protocol:
Wilmoth, J. R., Andreev, K., Jdanov, D., Glei, D. A., Riffe, T., Boe, C., Bubenheim, M., Philipov, D., Shkolnikov, V., Vachon, P., Winant, C., & Barbieri, M. (2021). Methods protocol for the human mortality database (v6). [Available online](https://www.mortality.org/File/GetDocument/Public/Docs/MethodsProtocolV6.pdf) (needs log in to mortality.org).

### United Nations – World Population Prospects

The World Population Prospects 2024 is the 28th edition of the official estimates and projections of the global population published by the United Nations since 1951. The estimates are based on all available sources of data on population size and levels of fertility, mortality, and international migration for 237 countries or areas.

For each revision, any new, recent, and historical, information that has become available from population censuses, vital registration of births and deaths, and household surveys is considered to produce consistent time series of population estimates for each country or areas from 1950 to today

For the estimation period between 1950 and 2023, data from 1,910 censuses were considered in the present evaluation, which is 79 more than the 2022 revision. In some countries, population registers based on administrative data systems provide the necessary information. Population data from censuses or registers referring to 2019 or later were available for 114 countries or areas, representing 48 percent of the 237 countries or areas included in this analysis (and 54 percent of the world population). For 43 countries or areas, the most recent available population count was from the period 2014-2018, and for another 57 locations from the period 2009-2013. For the remaining 23 countries or areas, the most recent available census data were from before 2009, that is more than 15 years ago.

Producer: United Nations  
Published: 2024-07-11  
Retrieved on: 2024-12-02  
Retrieved from: https://population.un.org/wpp/downloads/  
License: CC BY 3.0 IGO (https://population.un.org/wpp/downloads/)  

Citation: United Nations, Department of Economic and Social Affairs, Population Division (2024). World Population Prospects 2024, Online Edition.

### United Nations – World Population Prospects

The World Population Prospects 2024 is the 28th edition of the official estimates and projections of the global population published by the United Nations since 1951. The estimates are based on all available sources of data on population size and levels of fertility, mortality, and international migration for 237 countries or areas.

For each revision, any new, recent, and historical, information that has become available from population censuses, vital registration of births and deaths, and household surveys is considered to produce consistent time series of population estimates for each country or areas from 1950 to today

For the estimation period between 1950 and 2023, data from 1,910 censuses were considered in the present evaluation, which is 79 more than the 2022 revision. In some countries, population registers based on administrative data systems provide the necessary information. Population data from censuses or registers referring to 2019 or later were available for 114 countries or areas, representing 48 percent of the 237 countries or areas included in this analysis (and 54 percent of the world population). For 43 countries or areas, the most recent available population count was from the period 2014-2018, and for another 57 locations from the period 2009-2013. For the remaining 23 countries or areas, the most recent available census data were from before 2009, that is more than 15 years ago.

Producer: United Nations  
Published: 2024-07-11  
Retrieved on: 2024-12-17  
Retrieved from: https://population.un.org/wpp/downloads/  
License: CC BY 3.0 IGO (https://population.un.org/wpp/downloads/)  

Citation: United Nations, Department of Economic and Social Affairs, Population Division (2024). World Population Prospects 2024, Online Edition.

### United Nations – World Population Prospects

World Population Prospects 2024 is the 28th edition of the official estimates and projections of the global population that have been published by the United Nations since 1951. The estimates are based on all available sources of data on population size and levels of fertility, mortality and international migration for 237 countries or areas. If you have questions about this dataset, please refer to [their FAQ](https://population.un.org/wpp/faqs). You can also explore [data sources](https://population.un.org/wpp/data-sources) for each country or visit [their main page](https://population.un.org/wpp/) for more details.

Producer: United Nations  
Published: 2024-07-11  
Retrieved on: 2024-07-11  
Retrieved from: https://population.un.org/wpp/downloads/  
Direct download: https://population.un.org/wpp/assets/Excel%20Files/1_Indicator%20(Standard)/EXCEL_FILES/1_General/WPP2024_GEN_F01_DEMOGRAPHIC_INDICATORS_FULL.xlsx  
License: CC BY 3.0 IGO (https://population.un.org/wpp/downloads/)  

Citation: United Nations, Department of Economic and Social Affairs, Population Division (2024). World Population Prospects 2024, Online Edition.

### United Nations – World Population Prospects – Interim Update

World Population Prospects 2024 is the 28th edition of the official estimates and projections of the global population that have been published by the United Nations since 1951. The estimates are based on all available sources of data on population size and levels of fertility, mortality and international migration for 237 countries or areas. If you have questions about this dataset, please refer to [their FAQ](https://population.un.org/wpp/faqs). You can also explore [data sources](https://population.un.org/wpp/data-sources) for each country or visit [their main page](https://population.un.org/wpp/) for more details.

This is an interim update containing revised medium-variant estimates and projections for Togo.

Producer: United Nations  
Published: 2026-01-19  
Retrieved on: 2026-03-31  
Retrieved from: https://population.un.org/wpp/downloads/  
Direct download: https://population.un.org/wpp/assets/Excel%20Files/1_Indicator%20(Standard)/WPP2024_CSV_files_update.zip  
License: CC BY 3.0 IGO (https://population.un.org/wpp/downloads/)  

Citation: United Nations, Department of Economic and Social Affairs, Population Division (2024). World Population Prospects 2024, Online Edition.

### Zijdeman et al. – Life Expectancy at birth

This dataset provides the period Life Expectancy at birth per country and year. The overall aim of the dataset is to cover the entire world from 1500-2000.

This version (version 2) was built as part of the OECD "How was life" project. The dataset has nearly global coverage for the post-1950 period, while pre-1950 coverage decreases the more historic the period. Depending on sources, the data are annual estimates, five-yearly or decadal estimates.

  The sources used are:

  - [UN World Population Project](http://esa.un.org/wpp/).
  - [Human Mortality Database](http://www.mortality.org).
  - [Gapminder](http://www.gapminder.org).
  - [OECD](http://stats.oecd.org).
  - [Montevideo-Oxford Latin America Economic History Database](http://www.lac.ox.ac.uk/moxlad-database).
  - [ONS](http://www.ons.gov.uk/ons/datasets-and-tables/index.html).
  - [Australian Bureau of Statistics](http://www.abs.gov.au/ausstats/abs@.nsf/web+pages/statistics?opendocument#from-banner=LN).
  - Kannisto, V., Nieminen, M. & Turpeinen, O. (1999). Finnish Life Tables since 1751, Demographic Research, 1(1), DOI: 10.4054/DemRes.1999.1.1

  For specifics concerning (selections of) the sources, see the R code available in the working paper [here](https://clio-infra.eu/Indicators/LifeExpectancyatBirthTotal.html).

Producer: Zijdeman et al.  
Published: 2014-07-26  
Retrieved on: 2023-10-10  
Retrieved from: https://clio-infra.eu/Indicators/LifeExpectancyatBirthTotal.html  
Direct download: https://clio-infra.eu/data/LifeExpectancyatBirth(Total)_Broad.xlsx  
License: CC0 1.0 Universal (https://datasets.iisg.amsterdam/dataset.xhtml?persistentId=hdl:10622/LKYT53)  

Citation: Zijdeman, Richard and Filipa Ribeira da Silva (2015). Life Expectancy at Birth (Total). http://hdl.handle.net/10622/LKYT53, accessed via the Clio Infra website.

### James C. Riley – Estimates of Regional and Global Life Expectancy, 1800–2001

Historians and demographers have gone through considerable trouble to reconstruct life expectancy in the past in individual countries.

This overview collects information from a large body of that work and links estimates for historical populations to those provided by the United Nations, the World Bank, and other sources for 1950–2001. The result shows regional and global life expectancy at birth for selected years from 1800 to 2001. The bibliography of more than 700 sources is published separately on the web.

Producer: James C. Riley  
Published: 2005-10-21  
Retrieved on: 2023-10-10  
Retrieved from: https://doi.org/10.1111/j.1728-4457.2005.00083.x  
Direct download: https://u.demog.berkeley.edu/~jrw/Biblio/Eprints/%20P-S/riley.2005_estimates.global.e0.pdf  
License: JSTOR terms (https://about.jstor.org/terms/)  

Citation: Riley, J.C. (2005), Estimates of Regional and Global Life Expectancy, 1800–2001. Population and Development Review, 31: 537-543. https://doi.org/10.1111/j.1728-4457.2005.00083.x

    