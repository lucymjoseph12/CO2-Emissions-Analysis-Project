# CO2 Emissions Analysis

In this project, I tried to analyze the CO2 and Greenhouse Gases Emissions dataset provided by *Our World in Data* using Python packages like Pandas, Numpy and Plotly for visualization. To view the plotly graphs in the notebook, [click here](https://nbviewer.org/github/lucymjoseph12/Projects/blob/main/CO2%20Emissions%20Analysis/CO2%20Emissions%20Analysis.ipynb)

## Data

The descriptions for the columns used in this analysis are as follows:

* **country**              : Geographic location.	
* **year**                 : Year of observation.	
* **iso_code**             : ISO 3166-1 alpha-3, three-letter country codes.
* **co2**                  : Annual production-based emissions of carbon dioxide (CO2), measured in million tonnes.
* **coal_co2**             : Annual production-based emissions of carbon dioxide (CO2) from coal, measured in million tonnes.
* **gas_co2**              : Annual production-based emissions of carbon dioxide (CO2) from gas, measured in million tonnes.
* **oil_co2**              : Annual production-based emissions of carbon dioxide (CO2) from oil, measured in million tonnes.
* **share_global_co2**     : Annual production-based emissions of carbon dioxide (CO2), measured as a percentage of global       production-based emissions of CO2 in the same year.
* **share_global_cumulative_co2**: Cumulative production-based emissions of carbon dioxide (CO2) since the first year of data availability, measured as a percentage of global cumulative production-based emissions of CO2 since the first year of data availability.


The full list of columns and their descriptions can be found [here](https://github.com/owid/co2-data/blob/master/owid-co2-codebook.csv).

## Analysis

The data starts from 1750. To deal with the missing values, we filtered out the first quartile for **'year'** and dropped columns with more than 80% missing values. For the purpose of this analysis, we will restrict the analysis to the time period 1920 to 2020.

**Global Emissions Trend**

<img width="763" alt="image" src="https://user-images.githubusercontent.com/104146102/212789019-16e761c3-c108-4650-b04d-ccbfa7feb41b.png">

Interestingly, the low points coincide with economic crises and major events - COVID 19 pandemic in 2020, global financial crisis and oil crisis in 2008, Soviet Union collapse, Gulf war and Indian economic crisis in 1991

**Emissions due to Gas, Oil and Coal**

<img width="795" alt="image" src="https://user-images.githubusercontent.com/104146102/212789223-e53c7c82-4868-4d03-b243-5da381d09990.png">

**Analyzing top contributors to global emissions**

The dataset contains the data for categories like continents, income categories etc. These records will not have iso codes as they are not countries. We create a list of entities that are not countries so that we can exclude them if needed.

<img width="794" alt="image" src="https://user-images.githubusercontent.com/104146102/212789479-068961c3-3692-4eed-a5b9-15b01c0949df.png">

Russia's sudden decline in emissions since 1991 may be attributed to the collapse of the Soviet Union.
The increase of CO2 emissions in China through out the 2000's may be attributed to its fast economic growth during the time and focus on manufacturing.

**Global Share of the Top 10 Contributors**

<img width="762" alt="image" src="https://user-images.githubusercontent.com/104146102/212789738-bca4bcb1-e074-4082-96bc-7f28db6a9273.png">

China and India's shares of global emissions in 2020 are more than their share of cumulative emissions - China's being 16 points ahead. The United States on the other hand had a lower share in 2020 compared to their share of cumulative emissions.
