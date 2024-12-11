# Model Card: Beijing Air Quality Prediction Model

## Model Details
- **Model Name**: Beijing Air Quality Prediction Model
- **Model Version**: Initial Feasibility Stage
- **Model Type**: Regression
- **Developers**: Shuvo Biswas, Nasim Zaman Piyas, Maryum Ali, Izuchukwu Ogbuigbo, Manjot Singh
- **Release Date**: December 10, 2024 

## Intended Use
- **Primary Use**: Predicting air pollution levels in Beijing based on weather and pollutant data.
- **Intended Users**: Public health authorities, Healthcare Providers, Smart City Developers, and Environmental & Health Researchers who are interested to work with air quality data.
- **Out-of-Scope Use Cases**: Real-time applications and predictions for regions outside Beijing or data outside the training time period (2013–2017).

## Model and Data Insights
- **Data Used**: 
  - Air quality data from Beijing Municipal Environmental Monitoring Center.
  - Weather data from China Meteorological Administration.
  - Covers hourly data (March 2013–February 2017) from 12 monitoring stations.
  - Features include pollutant concentrations (e.g., PM2.5, SO2), weather variables (e.g., temperature, pressure), and temporal features.
- **Features**: Pollutant levels (PM2.5, PM10, CO, NO2, SO2, O3), meteorological data (Temperature, Pressure, Wind Direction etc.), temporal patterns (Time of day, Day of week).
- **Model Architecture**: A Python-based regression model using Pandas and NumPy for preprocessing, Matplotlib/Seaborn for visualization, and linear regression with backward elimination for feature selection and accuracy optimization.

## Training and Evaluation
- **Training Procedure**: Trained on Beijing air quality data with lag, rolling, and seasonal features. Preprocessing includes handling missing values, encoding wind direction, and normalization. Backward elimination refines features. Tools: Pandas, scikit-learn, and statsmodels in Python.Training and test files are stored in the Dataset Files folder.
- **Evaluation Metrics**: Model performance is assessed using correlation analysis, Mean Squared Error (MSE), Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE) on the test dataset for accurate regression evaluation.
- **Baseline Comparison**: The model's performance is compared against more complex models, such as Recurrent Neural Networks (RNN), to evaluate improvements in accuracy and computational efficiency.

## Ethical Considerations
- **Fairness and Bias**: Normalization and balanced representation were applied to address geographic, temporal, and data quality biases. Measures were taken to mitigate biases and handle outliers caused by unforeseen impacts at monitoring stations, ensuring fairness and robustness.
- **Privacy**: The non-personal training data is anonymized and compliant with privacy regulations, ensuring transparent use for public communication.
- **Security**: Data is encrypted, access is controlled, and secure storage practices are used to prevent unauthorized access to sensitive air quality data.

## Limitations and Recommendations
- **Known Limitations**: 
  - Limited time period (2013–2017) may not reflect current trends.
  - Seasonal variations and geographical biases due to uneven data collection add complexity.
  - Linear regression may be less accurate for long-term predictions compared to complex models like RNN.
- **Recommendations for Use**: Use the model for short-term (1-8 hour) forecasts as a decision-support tool, not for critical real-time actions.

## Additional Information
- **References**: [World Health Organization](https://www.who.int), [Bekkar et al., 2021](https://journalofbigdata.springeropen.com/articles/10.1186/s40537-021-00548-1)
- **License**: ENG M 680 (ADV TOPICS ENG MANAGEMENT II)
- **Contact Information**: Shuvo Biswas (shuvo.biswas@ualberta.ca), Nasim Zaman Piyas (nasim.piyas@ualberta.ca), Maryum Ali (maryum4@ualberta.ca)

