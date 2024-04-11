**Impact of Climate Change on Energy Consumption** 

**Team Introduction**

This project was successful due to the active participation of following team members:

- Adhithi Raghavan

- Amita Garad

- Loan Ho

- Tiffany Cheung

- Pallavi Deshmukh

**Overview**

In response to accelerating environmental changes, notably rising temperatures, sea levels, and shifting precipitation patterns, the relationship between these factors and energy consumption has become increasingly complex. This project aims to comprehensively analyze the impacts of environmental changes on energy consumption through comprehensive data analysis and machine learning techniques.

By undertaking this investigation, we seek to advance the collective understanding of climate-energy interactions and facilitate informed decision-making processes for policymakers, investors, and communities. Ultimately, this research endeavors to support the transition toward a more sustainable and resilient energy paradigm, capable of navigating the challenges posed by ongoing environmental transformations and contributing to global efforts to mitigate climate change impacts.

**Project Question**

Can we predict energy consumption in the United States using energy consumption data, temperature change data, sea-level change data, precipitation data and other variables through a machine learning model?

**Hypotheses**

Environmental changes, including rising temperatures, sea level rise, and changes in precipitation patterns, will have a significant impact on energy consumption.

- We hypothesize that as temperatures increase, there will be a corresponding rise in the demand for energy for cooling purposes.

- We hypothesize that sea level rise may lead to increased energy requirements for infrastructure maintenance and protection against coastal erosion and flooding.

- We hypothesize that changes in precipitation patterns may influence energy consumption in sectors such as agriculture, transportation, and hydroelectric power generation.

Overall, we expect to observe a positive correlation between environmental changes and energy consumption.

**Data Source** 

- [Energy Consumption Data](https://www.eia.gov/totalenergy/data/browser/index.php?tbl=T01.03#/?f=M\&start=200001) - The data was collected by the U.S. Energy Information Administration. The dataset is providing information on primary energy consumption by source in the US from 1949 - 2023.

- [Precipitation Data](https://www.epa.gov/climate-indicators/climate-change-indicators-us-and-global-precipitation) - The data was collected by the EPA United States Environmental Protection Agency. The dataset is providing information on the climate change indicators from the US and global precipitation from 1949 - 2023.

- [Temperature Change Data](https://www.fao.org/faostat/en/#data/ET) - The data was collected by the Food and Agriculture organization of the United Nations. The dataset is providing information on the temperature change on land from 1949 - 2023.

- [Sea Level Data](https://www.epa.gov/climate-indicators/climate-change-indicators-sea-level) ****-The data was collected by the EPA United States Environmental Protection Agency. The dataset is providing information on the climate change indicators on Sea Level from 1949 - 2023.

**Technologies Used** 

- Data Transformation: Python (pandas,) Jupyter Notebook, CSV file

- Data Visualization: Python (pandas, numpy, matplotlib, seaborn), Jupyter Notebook.

- Machine Learning Model: Python (pandas, numpy, matplotlib, seaborn, sci-kit learn, tensorflow), Jupyter Notebook, csv file

**Machine Learning Model** 

To find an answer to our project question, we tested out three different machine learning algorithms to see which one works best:

- Prophet

- Long Short-Term Memory (LSTM)

- LogisticRegression

- SARIMAX

- Random Forest Regression

- Neural Network Algorithm

**Project Outline**

1. **Data Collection**Our data collection process for a research project involves defining clear objectives and research question, identifying relevant data sources, selecting key variables, developing appropriate collection methods, establishing protocols for consistent and accurate data collection, implementing data collection procedures, verifying data quality, organizing and storing data accurately, documenting metadata information, and finally, conducting data analysis and interpretation to address the research objectives. This systematic approach ensures that researchers gather reliable and comprehensive data to support our analysis and contribute to advancing knowledge for the selected topic effectively.****

2. **Preprocessing**The energy consumption data was month-by-month or monthly data and needed to be aggregated on an annual basis. The various energy consumption types information was row by row instead of columns for each month and year. We used pivot table API from pandas to convert the row data to columnar data. This was a new technique that we learned in this data-cleaning process. The sea level data had different measurement techniques used over the years, and all the data was present in separate columns, so we had to merge them to get a single uniform measure. All the rest of the details like temperature and precipitation were merged with the energy consumption data to get all the data together in a single file so that further modeling and analysis can be done.

3) **Data Visualization**\
   ![](https://lh7-us.googleusercontent.com/BNfcO8YMPGZBrfibL_GqNcgr4-gw78J2C0GrzEaWSpC2qyqSgbLSJ-pMhJTfg1qg77zAo-1EUEPoEnD-kruEcCrKLRm6iaYffb4T1FNPwHjcaBk-KxafASOMoqC08Z_3dDSi6rtQNEiPemZSUwep4g)

This line chart provides a visual breakdown of energy consumption trends over time from various energy sources. This chart illustrates a clear shift towards clean energy.

![](https://lh7-us.googleusercontent.com/NHtYBfIMAdJiifLlgrkVibLE-qlNSRYf5HSF_HihwTEeziP0xdDjgYVOQBMlbey3GCMCC_wRjXoRN9341QqIgfq5hbF7IIdgzescHL0cnCy6a9lxSRT6c5HcxTmoVbJTsW2TL-NebI64aqIFzFFBDQ)

The area chart emphasizes the cumulative growth of renewable energy. The convergence of these two areas over recent years signals a significant shift in energy usage patterns.

![](https://lh7-us.googleusercontent.com/d0sXxVAwuFMIleMvcyPFtMA9tI2TbuVMSWVFq3npg9HtktAMnMmwnbkZunam8ftKeIW6-i55QpiAPDS1fAJdvDHBklGF-4jKmwrFIEZjl-OftmUdl2cvrET0VZs9fpdrFwAzKY6W8NHPEJkJNQWyzA)

This heatmap shows the correlation relationship between total primary energy consumption with sea level changes, precipitation changes, and temperature changes. This heatmap shows the positive correlation between energy consumption with the weather factors.

![](https://lh7-us.googleusercontent.com/Xezxiz-OGzSaufmctf-GSqPsHR7lRE9U0YdVyGnO588FWuIsnHpQQenqxp3UtMTgSSsidGEZPIc2EEe0QxnfH1rCvD-ZqrzxJF-4ZewWInSZpzMrYXAWMjq413VlhndgJVEf84mqmfCmmYJJ3UMLAA)

This line graph plots historical patterns between the energy consumption with the sea level changes, precipitation changes, and temperature changes. We see that the rising trend in total energy consumption aligns with increases in sea level and temperature. However, the relationship with precipitation changes is less consistent.

4. **Model Selection**

In order to determine which machine model will work for our dataset to predict energy consumption, we looked into 4 types of machine learning models. 

The first thing that we needed to determine is our target variable and feature variables. 

Linear Regression: 

- **Linear Regression** was performed to predict the total primary energy consumption based on the temperature change

- **Mean Squared Error**: 0.00037474

- **R-squared Score**: 0.999999

Logistic Regression

- Determined that this was not the most optimal model for our dataset as our target variable was continuous

Time Series Forecasting

- **Seasonal Autoregressive Integrative Moving Average** (SARIMA) Model

  - This model specifically uses forecasting to predict energy behavior and can be used to predict energy consumption 

  - This model assumes linearity as we are trying to forecast the variable of interest,  total energy consumption by using a linear combination of past values of that variable

- **Mean Squared Error: 65.092539**

- **R-squared**: -15.1692349

- The reason for a high mean-squared error is due to one of the following reasons:

  - Model complexity-as we have set the order parameters for non-seasonal and seasonal components to 0

  - Inappropriate model specification and insufficient data - not enough data to accurately capture the patterns and variability in energy consumption

- In order to better optimize this model, future exploration of incorporating additional features that may influence energy consumption

    \
Random Forest

- Random Forest was performed to predict the total primary energy consumption based on the historical year data

- **Best Model - Mean Squared:** 2.34652

- **Best Model - R-squared Score:** 0.99571

5. **Model Training**![](https://lh7-us.googleusercontent.com/WnEeq2JBvAsZUamW5ZqzBvmUdRrCOro1fFLmz_pp19UY3AHecK27m6eO04HHKBxA8jwasEWZklN-CJx7WOYxlqEUrhiZjiWHLLl7erGw6bkEizrREk1B4J_OuTgrJfbL7dkJi-QVHfT69Qa-6WK7RA)

This visualizes the relationship between the actual energy consumption values and the predicted energy consumption values generated by our model.

The blue dots represent the actual energy consumption values. 

Each dot's position on the y-axis corresponds to the actual energy consumption value, while its horizontal position represents the predicted energy consumption value.

The MSE is approximately 2.35. This indicates that, on average, the squared difference between the actual energy consumption values and the predicted values by the best model is around 2.35. 

Lower values of MSE indicate better model performance, as they suggest smaller prediction errors.

The R-squared score is approximately 0.996. This indicates that around 99.6% of the variance in energy consumption is explained by the independent variables included in the model. Higher R-squared values suggest a better model fit to the data.

****![](https://lh7-us.googleusercontent.com/C0qP3mN2JXHUb344nIdsHD9eWinwkzLwfJVmcEreya9IrwwKvObUGubI9FDt0Y2m9OHZCfam49wgvYRm5_-EFp-mUPPn6dMPpWLV8W5zkK5vFCYEQvaIyUWnjM2ln-UtkvpPj1VeUc8m9lEDDkSlMw)****

6. **Testing and Validation\
   **![](https://lh7-us.googleusercontent.com/1_1Ee7Kw4w9NLi8eg1bCwHauf1zKU2-kRXRtyH4C1bJHaUsw6a2g027mFZVxKR49eHQNLH2rD1AP4g-F0bhYxWMDZjaoyohyY-WxIrvzdPtC5at9rY_lTgWwzAyPVNa2NrZ10-QduE4p0_TuXd321Q)****

MSE is approximately 3.7421 which represents smaller differences between predicted and actual values. The standard deviation of the MSE scores is approximately 2.1402 and we can conclude that the model's performance is more consistent across. Overall, the cross-validation results indicate that the model performs reasonably well, with a low mean squared error on average.

7. **Model Prediction**

![](https://lh7-us.googleusercontent.com/OV0kDs886w-DpiiVLXIglFYRNlOAIUPOIVmNxKwOha0eXYNQUrfy6UBIUnJvEamvy6a4GpRrzStkkTd7IalebB0zw986DfGF-yft-ZMA-kimWFnuy48Se1-UcZi3GJUHGikYYUDIB3hZ4Vu5U-Z-PQ)

Our model predicted energy consumption for the next five future years (2024 to 2028). These values are the result of running the Random Forest Regressor model on the provided features.

**Limitations**As we are evaluating the accuracy and reliability of our model. We have identified the following challenges and limitations. 

1. **Spatial Heterogeneity:** Energy consumption patterns can vary significantly across different geographic regions due to variations in climate, population density, economic development, and infrastructure. Predictive models need to account for this spatial heterogeneity to ensure accuracy across diverse locations.

2. **External Shocks and Events:** Unforeseen events such as natural disasters, economic downturns, pandemics, or policy changes can have profound impacts on energy consumption patterns, rendering historical data less reliable for predictive purposes. Flexibility and adaptability in modeling approaches are essential to account for such external shocks.

3. **Behavioral Factors:** Human behavior plays a significant role in energy consumption, and it can be influenced by various socio-economic factors, cultural norms, technological advancements, and policy interventions. Incorporating these behavioral dynamics into predictive models adds another layer of complexity and uncertainty.

4. **Modeling Uncertainty:** Predictive models inherently involve uncertainty, particularly when dealing with complex systems like energy consumption influenced by environmental changes. Proper quantification and communication of uncertainty are crucial for decision-making and risk management based on model predictions.****

**Future use case**Our team has come up with the following use cases for our machine learning model.

1. **Renewable Energy Integration**: The model can assist in the integration of renewable energy sources like solar and wind power into the grid. By predicting energy consumption patterns and environmental conditions, stakeholders can better match renewable energy supply with demand, optimize energy storage solutions, and reduce reliance on fossil fuels.

2. **Smart Grid Optimization:** In the context of smart grids, the model can help improve grid stability, reliability, and efficiency. By anticipating fluctuations in energy demand and supply caused by environmental changes, grid operators can optimize grid operations, manage peak loads, and minimize system vulnerabilities.

3. **Urban Planning and Infrastructure Development:** City planners and developers can use the model to design sustainable urban environments and infrastructure. By predicting future energy demand patterns based on environmental factors, stakeholders can make informed decisions about building design, transportation systems, and land use planning to promote energy efficiency and resilience.

**Presentation**A Google Slides Presentation summarizing our project can be found ([here](https://docs.google.com/presentation/d/1sjgTIo9xpdLoaknargHoym5zLGCE3wr_UyG2ttY6YNM/edit?usp=sharing)).
