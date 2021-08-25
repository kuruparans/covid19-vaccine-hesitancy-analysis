# Data Dictionary
We collated together several different datasets together from various sources in our project. The vast majority were from official government sources, namely census surveys and models. All raw data is available under the `datasets/raw/` folder. We combined and cleaned these into a single file for ease of use, available in the `datasets/clean/` folder.

A listing of all available fields in our clean dataset is as follows:

| Column Name | Type | Description | Source |
| --- | --- | --- | --- |
| `fips` | Integer | 5 digit numeric unique code to identify each county | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `county_name` | String | County Name | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `state` | String | State | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `division` | String | Division | [Census](https://www2.census.gov/geo/pdfs/maps-data/maps/reference/us_regdiv.pdf) |
| `region` | String | Region | [Census](https://www2.census.gov/geo/pdfs/maps-data/maps/reference/us_regdiv.pdf) |
| `vaccine_hesitant` | Float | Decimal percent of county population that identifies as vaccine hesitant, 2021 | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `vaccine_hesitant_strong` | Float | Decimal percent of county population that identifies as strongly vaccine hesitant, 2021 | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `vaccine_hesitant_category` | String | Low, Medium, High categorization of `vaccine_hesitant` value, 2021 | via [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `social_vulnerability_index` | Float | CDC/ATSDR Social Vulnerability Index, 2018 | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `ethnicity_hispanic` | Float | Decimal percent of Hispanic, 2019 | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `ethnicity_native` | Float | Decimal percent of non-Hispanic Native Hawaiian/Pacific Islander, 2019 | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `ethnicity_asian` | Float | Decimal percent non-Hispanic Asian, 2019 | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `ethnicity_black` | Float | Decimal percent of non-Hispanic Black, 2019 | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `ethnicity_white` | Float | Decimal percent of non-Hispanic White, 2019 | [CDC](https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw) |
| `population` | Integer | Population of county, 2019 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `birth_rate` | Float | Birth rate of county, 2016-19 | [CDC](https://wonder.cdc.gov/natality.html) |
| `unemployment` | Float | Decimal percent of unemployed, 2019 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `poverty` | Float | Decimal percent of population living in poverty, 2019 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `median_income` | Integer | Median income of county, 2019 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `rural_urban_code` | Integer | Categorization on 1-9 scale of Rural Urban Continuum Code, 2013 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `urban_influence_code` | Integer | Categorization on 1-12 scale of Urban Influence Code, 2013 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `education_high_school_less` | Integer | Decimal percent of population that has less than a high school degree, 2019 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `education_high_school_only` | Integer | Decimal percent of population that has only a high school degree, 2019 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `education_degree_some` | Integer | Decimal percent of population that has some post-secondary degree, 2019 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `education_bachelors_degree` | Integer | Decimal percent of population that has a Bachelors degree, 2019 | [USDA](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/) |
| `religion_total` | Integer | Rate of adherants of all religious denominations per 1k pop, 2010 | [ARDA](https://www.thearda.com/Archive/Files/Descriptions/RCMSCY10.asp) |
| `religion_evangelical` | Integer | Rate of Evangelical Protestant adherants per 1k pop, 2010 | [ARDA](https://www.thearda.com/Archive/Files/Descriptions/RCMSCY10.asp) |
| `religion_mainline_protestant` | Integer | Rate of of Mainline Protestant adherants per 1k pop, 2010 | [ARDA](https://www.thearda.com/Archive/Files/Descriptions/RCMSCY10.asp) |
| `election_democrat_wins` | Integer | Number of Democrat wins from 2008-2020 presidential elections | via [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_republican_wins` | Integer | Number of Republican wins from 2008-2020 presidential elections | via [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_total_2008` | Integer | Number of total votes from 2008 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_dem_2008` | Integer | Number of Democrat votes from 2008 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_gop_2008` | Integer | Number of Republican votes from 2008 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_oth_2008` | Integer | Number of other votes from 2008 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_total_2012` | Integer | Number of total votes from 2012 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_dem_2012` | Integer | Number of Democrat votes from 2012 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_gop_2012` | Integer | Number of Republican votes from 2012 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_oth_2012` | Integer | Number of other votes from 2012 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_total_2016` | Integer | Number of total votes from 2012 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_dem_2016` | Integer | Number of Democrat votes from 2012 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_gop_2016` | Integer | Number of Republican votes from 2012 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_oth_2016` | Integer | Number of other votes from 2012 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_total_2020` | Integer | Number of total votes from 2020 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_dem_2020` | Integer | Number of Democrat votes from 2020 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |
| `election_gop_2020` | Integer | Number of Republican votes from 2020 presidential election | [@tonmcg](https://github.com/tonmcg/US_County_Level_Election_Results_08-20) |


