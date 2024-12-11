# General Overview of the Project

The **Predicting Air Quality: An Applied AI Approach to Beijing's Pollution Data** is a machine learning-based project aimed at predicting air quality health index in Beijing using data on pollutants and weather variables. The project focuses on developing accurate models that can forecast air quality  and air quality health index over time, helping stakeholders such as policymakers, public health authorities, and environmental researchers make informed decisions to mitigate air pollution's harmful effects on human health and the environment.

Beijing faces significant air quality challenges, especially during certain seasons when pollutants like PM2.5, NO2, and SO2 can reach hazardous levels. With the help of machine learning models, we aim to create predictive tools that can:
- Provide early warnings on air quality trends.
- Assist in making evidence-based decisions regarding urban planning and public health interventions.
- Support research efforts focused on pollution control and environmental sustainability.

### Project Map
1. **Data Collection:** Data is sourced from Beijing's Municipal Environmental Monitoring Center and China Meteorological Administration. This includes hourly measurements of pollutant concentrations and weather variables like temperature, humidity, and wind direction. The dataset would be found here https://www.kaggle.com/datasets/sid321axn/beijing-multisite-airquality-data-set. It has also been uploaded in the Dataset folder.
2. **Feature Engineering:** The data is processed to extract features that capture temporal patterns in air quality and meteorological conditions. These features are designed to enhance the model's ability to predict AQHI accurately by considering both historical data and seasonal trends. Key features include:
  - **Pollutant Concentrations:** Levels of pollutants such as PM2.5, PM10, CO, NO2, SO2, and O3.
  - **Weather Variables:** Meteorological data, including temperature, pressure, wind speed and direction, and humidity.
  - **Temporal Features:** Variables representing the time of day, day of the week, and seasonal patterns that influence air quality.
  - **Lag Features:** Past values of pollutants and weather variables (e.g., pollutant levels from the previous hour) to capture time-dependent trends and dependencies.
  - **Rolling Features:** Moving averages or rolling window statistics (e.g., 3-hour or 24-hour rolling mean) to smooth out fluctuations and highlight broader trends in air quality.
  - **New Features:** Additional features, such as the interaction between weather variables and pollutants like AQI (air quality index) that provide deeper insights into pollution patterns. Also features like weekends, hoildays and seasons which help in understanding the pattrens.

4. **Model Training:** The dataset is split into training and testing sets, and various models are trained to predict future air quality. Advanced models like deep neural networks (DNN) and recurrent neural networks (RNN) are considered for their ability to capture complex time-series dependencies.
5. **Evaluation:** The model’s accuracy is evaluated using metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared to determine how well the model predicts future pollution levels.

### Expected Outcomes
- **Short-term Predictions:** The model will provide reliable short-term (1-24 hour) predictions of air quality health index in Beijing.
- **Health Impact Forecasts:** The predictions can be used to assess health risks, such as respiratory issues and cardiovascular diseases, that are exacerbated by poor air quality.
- **Urban Policy Support:** The model will help inform public health policies, such as issuing air quality advisories, optimizing traffic patterns, and identifying areas requiring pollution mitigation measures.
- **Sustainability and Environmental Management:** The project will support efforts to reduce pollution and improve the quality of life for Beijing residents by providing data-driven insights into pollution control and environmental policies.

### Map of Stakeholders
- **Public Health Authorities**: Use air quality forecasts to warn the public and healthcare providers of health risks.
- **Government Officials**: Use predictions to enforce regulations and optimize urban planning for cleaner air.
- **Environmental NGOs**: Rely on predictions for advocacy and policy change.
- **Residents**: Receive early warnings about pollution levels and their health risks.
- **Researchers**: Access data for further studies on pollution trends, environmental sustainability, and health impacts.

The overall goal is to create a robust and scalable prediction model that can enhance Beijing's air quality management efforts, reduce health-related costs, and improve the city’s livability.

# Repository Structure

The repository is organized into the following folders and files:

### Folders:

- **Dataset files**: Contains the raw data used for training and evaluation. This folder includes all the necessary datasets required for the project.
- **Model Card**: Contains the model card for describing the architecture, use cases, limitations, and other details about the model.
- **Notebooks**: Holds Jupyter notebooks or other similar files used for exploratory data analysis (EDA), model training, and other research tasks.
- **Project Report**: This folder includes the final project report documenting the methodology, results, and analysis performed throughout the project.

### Files:

- **Architecture Diagrams**: A file containing visual representations of the model architecture, which helps in understanding the flow of data and the components involved.
- **README.md**: The README file that provides an overview of the project, instructions for running the code, and other relevant information.

# Project Breakdown
1. **Pre-Processing**
2. **Initial Data Exploration (EDA)**
3. **Feature Engineering**
4. **Training and Evaluation Pipeline**
   -**Simple Models**
   
### 1. Preprocessing
 - Load the dataset using your preferred library (e.g., pandas for CSV files).
 - Check for missing values with data.isnull().sum() and handle them using imputation or removal techniques.
 - Detect and handle outliers using methods like Z-scores or the IQR rule.
 - Normalize numerical features using tools like StandardScaler or MinMaxScaler from sklearn.
 - Encode categorical variables with one-hot encoding or label encoding (LabelEncoder).

### 2. Initial EDA
 - Inspect the dataset's structure using data.info() and data.describe().
 - Visualize feature distributions using histograms or KDE plots (seaborn.distplot).
 - Identify correlations using a heatmap (seaborn.heatmap).
 - Plot pairwise relationships between numerical variables using seaborn.pairplot.

### 3. Feature Engineering
 - Extract new features, such as datetime attributes.
 - Combine or split columns as needed (e.g., extract prefixes, create ratios).
 - Perform feature selection using methods like correlation thresholds or sklearn.feature_selection. 
 - Save the transformed dataset for consistency across steps.

### 4. Training and Evaluation Pipeline
 - Split the dataset into training and testing subsets using train_test_split.
 - Train a baseline model to establish a benchmark.
 - Train advanced models, optimizing their hyperparameters with tools like GridSearchCV.
 - Evaluate model performance on the test set using metrics like accuracy or RMSE.
 - Save the best-performing model for deployment (joblib.dump or pickle).

### Simple Models
We explore basic regression models, including:
- Linear Regression
- Lasso Regression
- PCA-based Regression
- Random Forest
- XGBoost, and Support Vector Regressors
  
**Steps for Simple Models:**
 - Import libraries and upload the dataset.
 - Perform feature engineering and break down the time series.
 - Use Grid Search with Cross-Validation for tuning.
 - Apply PCA and compare model performance.

### Dataset
All the training and test sets, both X nad Y can be downloaded from the dataset folder.

### Evaluation
All models are evaluated using RMSE, MAE, and R² to measure their predictive accuracy.


