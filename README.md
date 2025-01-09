# Stock Price Performance of Pharmaceutical Companies during COVID-19 in the US

**Link to archival record:**  
https://sandbox.zenodo.org/records/140733  
**DOI:** 10.5072/zenodo.140733

**Contributors**  
Irith Chaturvedi  
Thomas Jiang

## Summary
The COVID-19 pandemic presented unprecedented challenges worldwide, deeply affecting public health and economic systems. This project investigates the correlation between U.S. COVID-19 death rates and the stock price performance of major pharmaceutical companies involved in vaccine development. The goal is to uncover whether significant pandemic-related events influenced the financial markets, focusing on AstraZeneca (AZN), Johnson & Johnson (JNJ), and Pfizer (PFE). This analysis will focus on the period from 2020 to 2021, capturing the timeline when the pandemic was at its absolute peak.

**Important dates we consider for our project:**  
March 19, 2020: California issued the first statewide stay-at-home order in the U.S. to curb the spread of the virus.  
January 8, 2021: The U.S. reported its highest single-day number of new COVID-19 cases, with over 300,000 new infections.  
January 12, 2021: The U.S. recorded its second-highest single-day number of new cases, with approximately 250,000 new infections.  
January 6, 2021: The U.S. reported its third-highest single-day number of new cases, with around 240,000 new infections.  
January 12, 2021: The U.S. experienced its highest single-day death toll from COVID-19, with over 4,400 deaths.  
January 13, 2021: The U.S. recorded its second-highest single-day death toll, with more than 4,300 deaths.  
December 11, 2020: The U.S. Food and Drug Administration (FDA) granted Emergency Use Authorization (EUA) for the Pfizer-BioNTech COVID-19 vaccine, the first COVID-19 vaccine approved in the U.S.

## Research Question
How did fluctuations in U.S. COVID-19 death/case rates correlate with changes in the stock prices of major pharmaceutical companies during the pandemic?

## Objectives
- Analyze COVID-19 death and case data alongside stock price fluctuations for selected companies.  
- Identify trends around significant pandemic-related events such as vaccine approvals, the advent of major Covid-19 outbreak waves, etc.  
- Provide actionable insights for stakeholders, creating an automated workflow and a reproducible package.

## Approach
The analysis involves:  
Cleaning, curating, and managing COVID-19 and stock price data using Python.  
Generating visualizations to understand trends and correlations.  
Automating workflows for reproducibility using Snakemake.

The project delves into the characteristics of the dataset, source of retrieval, cleaning, integration and analysis. It highlights trends such as increased stock prices during vaccine approvals, signaling positive market responses to public health advancements. Conversely, stock prices demonstrated instability during periods of pandemic-related uncertainty. It also provides the steps to rerun and reproduce our analysis using workflow automation and documentation.

## Data Profile
This project incorporates datasets on COVID-19 statistics and stock prices.

### 1. COVID-19 Data
**Source:** Johns Hopkins University GitHub Repository GitHub Repository.  
**Description:** Daily COVID-19 cases, deaths, and recovery data from U.S. states.  
**Data information:** 5 CSV files covering key dates from 2020 to 2021.

**Processing:**  
Filtered for U.S. state and territory data. Datasets had fields grouped for each State within the United States to have aggregate statistics for each state.  
This provides a comprehensive analysis that tackles the countrywide effect of the pandemic on the livelihoods of the masses.  
All 5 cleaned datasets were combined or concatenated into a master dataset to perform a singular analysis.  
Metrics such as Incident Rate and Case Fatality Ratio were averaged for each state to create cumulative visualizations. Bar charts were used to portray state-wise data, while Line Graphs were used to make a Time-Series Analysis.

**Files downloaded from source:**  
01-06-2021.csv  
01-08-2021.csv  
01-12-2021.csv  
01-13-2021.csv  
12-11-2020.csv

**License and terms of use:**  
This data set is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0) by Johns Hopkins University on behalf of its Center for Systems Science in Engineering. Copyright Johns Hopkins University 2020.

### 2. Stock Price Data
**Source:** Alpha Vantage API API Documentation.  
**Description:** Weekly stock prices for AstraZeneca, Johnson & Johnson, and Pfizer from December 2019 to January 2021.  
**Dataset information:** 3 CSV files, filtered and adjusted for weekly high, low, and volume metrics.

**Processing:**  
Adjusted weekly stock data was aligned with COVID-19 significant dates.  
Stock identifiers were added for easier differentiation in integrated files.  
Files were then integrated into a master data source by concatenating data frames to perform a singular analysis of all data.  
Visualizations for Time series analysis on weekly Highest stock price for each company along with volume of stock were created.

**Files retrieved from source using API:**  
PFE_weekly_adjusted.csv  
JNJ_weekly_adjusted.csv  
AZN_weekly_adjusted.csv

**License and Terms of Use:**  
Alpha Vantage provides a free API service for retrieving stock data, governed by specific terms and conditions. By default, users are granted a non-exclusive, non-sublicensable, non-transferable, non-assignable, revocable license to access and utilize the Alpha Vantage Platform for personal, non-commercial use. It is safe to assume that Research and Academic use, as in our case, follows the Personal, Non-Commercial License.

## Findings

### COVID-19 Trends
The U.S. experienced peaks in case numbers and deaths in January 2021. For instance, the highest single-day case count occurred on January 8, 2021, exceeding 300,000 cases.  
States with higher population densities exhibited higher incident rates and case fatality ratios. For example, states like California and New York showed significant spikes in both metrics, interestingly North and South Dakota, comparatively less populated states were outliers for Incident Rates.

### Stock Price Trends
All company stocks surged following the advent of COVID - 19 as pandemic in March 2020 reflecting market optimism.  
The stock market demonstrated volatility during early 2020, coinciding with global uncertainty and lockdown announcements.

## Analysis
From the visualizations:  
**Case Fatality Ratios:** The COVID-19 visualizations aim to show the dire situations of individual states in the USA, painting a grim picture during one of the hardest times faced by human civilization. Ratios for Illinois and New York were the highest, signifying more COVID cases leading to deaths per person in comparison to other states.  
**Incident Rates:** All states with the highest populations within the USA such as California, New York, Illinois, Texas had high incident rates. However less populated states like South and North Dakota, and Tennessee, had high incident cases too, which was anomalous, to say the least.  
**Stock Trends:** Our weekly high results from the data visualizations show a sharp increase in the stock price for Johnson and Johnson when COVID-19 hit its peak number of cases and deaths in a day in the USA, while AstraZeneca and Pfizer's prices stabilized immediately during the same time.  
Interestingly all three companies saw a steady increase in their stocks up until the time they released their vaccines. Pfizer and AstraZeneca, who released their vaccines in November and December 2020, saw a decrease in their stock price. This could be attributed to the early misconceptions and ineffectiveness of vaccines leading to uncertainty amongst the masses during that period. Johnson and Johnson, who released their vaccine later in March of 2021, saw its stock price increase during November and December 2020. This could have happened due to people putting their trust in the effectiveness of a vaccine taking longer to develop than its competitors. At an average for the three companies, however, the stock prices seem to have balanced out when the largest COVID-19 wave hit.  
All companies diluted large volumes of stock on the onset of COVID-19 in the USA, this could mean that companies were anticipating an increase in their valuation during a worldwide health crisis. The volume of stock seems to have reduced when the pharmaceutical companies introduced their vaccines.

## Future Work

### Lessons Learned
**Data Integration Complexity:** Aligning datasets with differing time granularities required significant preprocessing. In the future to integrate datasets from different sources, there needs to be some commonality between them, such as a common column to join datasets on. This is something we would take into consideration while choosing problems to answer.

### API Limitations
The limitations of the stock data APIs, such as those from Alpha Vantage, were another significant hurdle. The free API tier only allowed for a limited number of retrievals per day (in our case, just 5). This restriction slowed down the data-gathering process, especially when dealing with large-scale datasets. Additionally, the free tier only provided weekly stock data, which, while useful for some analyses, lacked the granularity needed for a more precise investigation of how stock prices reacted to daily changes in COVID-19 metrics. A possible workaround in future work would be to either upgrade to a premium account to access daily stock data or consider alternative stock data providers that may offer more flexible retrieval policies or better access at a similar cost. Exploring methods to automate the retrieval of data in batches could also optimize the time and effort spent on API requests.

### Potential Directions
**Extend Analysis to Include Other Companies**  
While our analysis focused on major pharmaceutical companies like Pfizer, AstraZeneca, and Johnson & Johnson, the pandemic also saw significant contributions from companies such as Moderna and Novavax, both of which played pivotal roles in COVID-19 vaccine development. Including these companies in future analyses would provide a more comprehensive view of the pharmaceutical industry’s response to the pandemic and its correlation with stock performance. By comparing the stock price trajectories of these additional companies, we could gain deeper insights into the competitive dynamics within the pharmaceutical sector and how individual company developments (e.g., vaccine approvals, partnerships, or regulatory hurdles) affected their stock performance.

**Broaden the Geographic Scope**  
The scope of our analysis was limited to the United States, focusing on the relationship between U.S. COVID-19 death rates and the stock price performance of major pharmaceutical companies. However, the global nature of the pandemic means that different countries had varying levels of impact, vaccine distribution strategies, and public health policies, all of which could have influenced stock prices in diverse ways. Expanding the geographic scope to include data from other countries, such as the United Kingdom, India, and Brazil, would allow for cross-country comparisons. This could help to identify broader trends, such as how stock prices responded to government responses in different regions or how the varying progression of the pandemic affected the stock performance of companies operating internationally.

## Reproducing the Analysis
**Prerequisites:**  
Python 3 environment  
Dependencies listed in requirements.txt (Pandas, Matplotlib, Requests, Snakemake)

**Steps to Reproduce:**
1. **Clone Repository:**  
   `git clone https://github.com/illinois-data-curation/is477-fa24-cosco`

2. **Install Dependencies:**  
   `pip install -r requirements.txt`

3. **Fetch Data:**  
   Go over to https://www.alphavantage.co/support/#api-key and create your API key, you will use this to fetch the stock data from the source.  
   Use the DataAcquisitionCleaning_stocks.py, within the ‘scripts’ folder to change the provided API key to your API key.  
   Run DataAcquisitionCleaning_stocks.py to collect and clean stock price data and put it in the Data folder.  
   Go over to https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports and download the following CSV files into the folder CasesData, also create an empty folder called "Cleaned":  
   01-06-2021.csv  
   01-08-2021.csv  
   01-12-2021.csv  
   01-13-2021.csv  
   12-11-2020.csv  
   Run data_cleaning_covid.py within the scripts folder to clean COVID-19 data. This puts all cleaned and filtered CSV COVID data files into `Cleaned`.

4. **Integrate Data:**  
   Run Dataintegration_Covid.py within the scripts folder to combine the cleaned COVID-19 datasets. This creates a file combined_covid_data.csv.  
   Run DataintegrationStocks.py within the scripts folder to integrate stock price datasets This creates a file Combined_weekly_filtered.csv.

5. **Generate Visualizations:**  
   Run covid_analysis.py present in the Analysis folder for COVID-19 trend visualizations. This uses the newly created combined_covid_data.csv to create visualizations in the Covid_Graphs folder.  
   Run stocks_analysis.py present in the Analysis folder for stock performance plots. This uses the newly created Combined_weekly_filtered.csv to create visualizations in the Stocks_Graphs folder.

6. **Automate Workflow:**  
   Execute Snakefile using Snakemake to automate the entire workflow. Remember to use your API key instead of the one provided by default.
   `snakemake --cores 1`
   *or*
   `python -m snakemake --cores 1`

7. **BOX Link**
    https://uofi.box.com/s/e6e7kanvgmgmiu38dos6g9fvqdj1om3k

## Compliance & Licensing
**Compliance with Licenses:**  
COVID-19 data from JHU: CC BY 4.0.  
Stock data from Alpha Vantage: Non-commercial, personal/research use allowed.

**Code and Documentation:**  
MIT License.  
Scripts and analysis steps are clearly cited and documented.

**Citations:**
- Johns Hopkins University COVID-19 Datasets: GitHub Repository
- Alpha Vantage API: API Documentation
- Python Libraries:
  - Pandas: McKinney, W. (2010). Data Structures for Statistical Computing in Python.
  - Matplotlib: Hunter, J. D. (2007). Matplotlib: A 2D Graphics Environment.
  - Requests: Kenneth Reitz. (2011). Requests: HTTP for Humans.
- Snakemake: Mölder, F., et al. (2021). Sustainable data analysis with Snakemake. F1000Research, 10, 33.

## FAIR Principles and Archival Repository
**Findable & Accessible:** Project is deposited in Zenodo with DOI: 10.5072/zenodo.140733  
**Interoperable & Reusable:**  
Clear metadata (DataCite XML, JSON-LD) and documentation provided.  
Code and data in non-proprietary formats.  
**GitHub Repository:** https://github.com/illinois-data-curation/is477-fa24-cosco

## Development Details & Key Features
**Language:** Python 3  
**Development Status:** Completed

**Core Features:**
- Data Acquisition & Cleaning Scripts:
  - DataAcquisitionCleaning_stocks.py
  - data_cleaning_covid.py

- Data Integration & Analysis Scripts:
  - Dataintegration_Covid.py
  - DataintegrationStocks.py
  - covid_analysis.py
  - stocks_analysis.py

- Workflow Automation:
  - Snakefile for end-to-end reproducibility

- Cleaned Datasets & Outputs:
  - Cleaned COVID-19 data in Cleaned folder
  - Filtered stock data in Data_Stocks folder
  - Visualizations in CovidGraphs and StocksGraphs folders

## Metadata for Zenodo Deposit
**Title:** Stock Price Performance of Pharmaceutical Companies during COVID-19 in the US  
**Description:** This repository contains datasets, scripts, and documentation for analyzing correlations between U.S. COVID-19 metrics and the stock prices of key pharmaceutical companies during the pandemic.  
**Resource Type:** Project Deliverable  
**Creators:**
- Irith Chaturvedi (Project Member)
- Thomas Jiang (Project Member)
**License:** MIT License  
**Date:** 2024-12-07  
**Files:** is477-fa24-cosco-releaseformetadata.zip

**Related Work:**  
Relation: Is metadata for  
Identifier: https://github.com/illinois-data-curation/is477-fa24-cosco  
Resource Type: Publication / Project Deliverable

**Export Metadata**  
DataCite XML: MetaData/140733.xml  
JSON-LD: MetaData/140733

**Persistent Identifier**  
DOI: 10.5072/zenodo.140733
