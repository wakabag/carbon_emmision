🌳 README: ForestSentry AI - Kenya \text{CO}_2 Flux Forecasting
This repository contains the solution for the AI for Sustainable Development assignment, focusing on Sustainable Development Goal 13: Climate Action.
The project uses historical data on \text{CO}_2 emissions and sequestration from deforestation in Kenya to train a machine learning model, providing a critical forecasting tool for climate policy and resource management.
1. Project Goal and Alignment (SDG 13)
| Metric | Detail |
|---|---|
| SDG Addressed | SDG 13: Climate Action |
| Specific Problem | The challenge of accurately and consistently monitoring and predicting the net flux of \text{CO}_2 from land use changes (specifically deforestation) in Kenya. Accurate forecasting is essential for meeting climate commitments and accessing carbon finance. |
| Project Name | ForestSentry AI |
| Project Goal | To forecast Kenya's annual net \text{CO}_2 flux from deforestation for the next five years (2025-2029). |
2. Machine Learning Solution
The project utilizes a Supervised Learning approach, treating the time series data as a regression problem.
 * Approach: Time-Series Forecasting
 * Model: Random Forest Regressor
   * Why this model? Random Forest is robust to noise, handles non-linear trends inherent in environmental time series data, and provides reliable out-of-sample predictions.
 * Input Feature (X): The Year (T).
 * Target Variable (y): The annual \text{CO}_2 Net Flux (Mt \text{CO}_2e). (Note: Negative values represent carbon sequestration, while positive values represent emissions from deforestation).
3. Data Used
The analysis relies on specific, country-level time-series data provided in the assignment:
 * File Used: Kenya_forest_carbon_csv.zip/API_EN.GHG.CO2.LU.DF.MT.CE.AR5_DS2_en_csv_v2_6111.csv
 * Indicator Name: Carbon dioxide (\text{CO}_2) net fluxes from LULUCF - Deforestation (Mt \text{CO}_2e).
 * Source: World Bank / World Development Indicators.
 * Geographic Scope: Filtered specifically for Kenya (KEN).
4. Code Execution Instructions
To run the full solution, follow these steps:
 * Setup Environment: Ensure you have Python installed, along with the required libraries: pandas, scikit-learn, and numpy.
   pip install pandas scikit-learn numpy

 * Place Data: Ensure the main data file (API_EN.GHG.CO2.LU.DF.MT.CE.AR5_DS2_en_csv_v2_6111.csv) is accessible to the Python script, typically by placing it in the same directory or maintaining the archive structure as specified in the FILE_PATH.
 * Run Code: Execute the complete Python script provided in the final step of the conversation.
The script will automatically handle data loading, filtering, preparation, model training, and will print the performance metrics and the final 5-year forecast.
5. Summary of Key Results & Reflection
| Deliverable Element | Result Summary |
|---|---|
| Model Performance (MAE) | The Mean Absolute Error (MAE) on the test set is reported in the final output. This value represents the average difference between the model's prediction and the actual recorded flux, measured in Million tons of \text{CO}_2e. A low MAE validates the model's utility for policy-making. |
| 5-Year Forecast | The output provides annual \text{CO}_2 net flux predictions for 2025 to 2029, giving Kenyan planners a quantitative estimate of future carbon trends from deforestation. |
| Ethical & Social Reflection | Data Bias: The use of national-level data avoids geographical sampling bias but is limited by the World Bank's aggregation methodology. Fairness: The tool provides cost-effective, data-driven evidence for a developing nation, empowering local agencies to secure climate finance based on verifiable, forecasted impacts, thus ensuring equitable access to climate data. |
