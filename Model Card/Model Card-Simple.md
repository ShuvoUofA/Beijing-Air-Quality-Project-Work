# Model Card: Beijing Air Quality Prediction Model

## Model Details
- **Model Name**: Beijing Air Quality Prediction Model
- **Model Version**: Initial Feasibility Stage
- **Model Type**: Regression
- **Developers**: Shuvo Biswas, Nasim Zaman Piyas, Maryum Ali, Izuchukwu Ogbuigbo, Manjot Singh
- **Release Date**: Not yet released

## Intended Use
- **Primary Use**: Predicting air pollution levels in Beijing based on weather and pollutant data.
- **Intended Users**: Public health authorities, environmental researchers, urban planners, and policymakers.
- **Out-of-Scope Use Cases**: Real-time applications and predictions for regions outside Beijing or data outside the training time period (2013–2017).

## Model/Data Description
- **Data Used**: 
  - Air quality data from Beijing Municipal Environmental Monitoring Center.
  - Weather data from China Meteorological Administration.
  - Covers hourly data (March 2013–February 2017) from 12 monitoring stations.
  - Features include pollutant concentrations (e.g., PM2.5, SO2), weather variables (e.g., temperature, pressure), and temporal features.
- **Features**: Pollutant levels, meteorological data, temporal patterns.
- **Model Architecture**: TensorFlow-based regression model leveraging Python for preprocessing (Pandas, NumPy) and visualization (Matplotlib/Seaborn).

## Training and Evaluation
- **Training Procedure**: Includes handling missing values, encoding wind direction as categorical features, and applying normalization techniques.
- **Evaluation Metrics**: Correlation analysis and other regression metrics (e.g., mean squared error) on test data.
- **Baseline Comparison**: Not included in the feasibility report but will be established during subsequent phases.

## Ethical Considerations
- **Fairness and Bias**: Addressed geographic, temporal, and data quality biases by normalization and testing for balanced representation.
- **Privacy**: Data is non-personal but must be transparently used for public communication.
- **Security**: Secure storage of data with access restrictions.

## Limitations and Recommendations
- **Known Limitations**: 
  - Limited time period (2013–2017) may not reflect current trends.
  - Seasonal variations add modeling complexity.
  - Geographical biases due to uneven data collection across stations.
- **Recommendations for Use**: Use the model as a decision-support tool, not for critical real-time actions.

## Additional Information
- **References**: [World Health Organization](https://www.who.int), [Bekkar et al., 2021](https://journalofbigdata.springeropen.com/articles/10.1186/s40537-021-00548-1)
- **License**: TBD
- **Contact Information**: Group members or the course instructor.
