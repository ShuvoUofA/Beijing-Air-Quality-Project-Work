# Model Card: Advanced Model for Air Quality Prediction

## Model Details

- **Model Name:** Deep Neural Network with Time-Series Forecasting
- **Model Version:** 2.0
- **Model Type:** Regression (Deep Learning)
- **Developers:** Shuvo Biswas, Nasim Zaman Piyas, Maryum Ali, Izuchukwu Ogbuigbo, Manjot Singh
- **Release Date:** 10th December 2024

---

## Intended Use

- **Primary Use:** Time-series forecasting for air quality prediction in Beijing, with the capability to forecast multiple pollutants over time.
- **Intended Users:** Environmental researchers, data scientists, urban planners, and policymakers focusing on air quality management and health risk mitigation.
- **Out-of-Scope Use Cases:** Real-time operational monitoring systems and emergency response frameworks.

---

## Model/Data Description

- **Data Used:** Air quality data from the Beijing Municipal Environmental Monitoring Center, paired with meteorological data from the China Meteorological Administration.
  - Features include pollutant concentrations (e.g., PM2.5, PM10, CO, NO2, SO2, O3), weather variables (e.g., temperature, pressure, wind direction, humidity), and time-series components (e.g., time of day, day of the week).
  - Data spans from March 2013 to February 2017, collected at 12 monitoring stations across Beijing.

- **Features:**
  - **Input Features:** Hourly pollutant concentrations, weather variables, and temporal features (e.g., time of day, day of the week).
  - **Derived Features:** Lag features, rolling averages, seasonal components, and other time-series-specific transformations.

- **Model Architecture:** 
  - The model is a deep neural network (DNN) designed to capture complex nonlinear relationships in the time-series data.
  - The architecture includes multiple layers (e.g., dense layers, LSTM layers) for sequential pattern recognition.
  - Key hyperparameters:
    - Number of layers: 4
    - Units per layer: 128
    - Activation function: ReLU
    - Optimizer: Adam
    - Loss function: Mean Squared Error (MSE)

---

## Training and Evaluation

- **Training Procedure:**
  - The model is trained using the processed historical air quality data, which includes feature engineering such as lag and rolling features.
  - A supervised learning approach is used, with the model learning from historical pollutant levels and weather data to predict future air quality values.
  - **Training Environment:** Python with TensorFlow, Keras, and scikit-learn libraries. The model is trained on a machine with sufficient GPU resources (e.g., Tesla V100).

- **Training Dataset:**
  - The dataset includes hourly pollutant and weather data, split into training (80%) and testing (20%) datasets.
  - **Data Sources:**
    - All the date scource files for Train and Test are uploaded in the Dateset files folder.

- **Evaluation Metrics:**
  - The model is evaluated using common regression metrics:
    - Mean Absolute Error (MAE)
    - Root Mean Squared Error (RMSE)
    - R-squared (R²) Score
  - The evaluation is conducted on the held-out test dataset to assess how well the model generalizes to unseen data.

- **Baseline Comparison:**
  - The model's performance is compared to simpler models, such as Linear Regression and more complex models like Recurrent Neural Networks (RNNs), to assess both accuracy and computational efficiency.

---

## Ethical Considerations

- **Fairness and Bias:**
  - Efforts have been made to mitigate biases that may arise from data gaps or unequal representation of certain regions in the data collection process.
  - Bias correction techniques, including resampling and data normalization, are applied to ensure balanced model predictions across all data points.

- **Privacy:**
  - While the data is anonymized and does not contain personal information, transparency is essential in communicating the implications of model predictions for policy and health recommendations.
  - Any supplementary data used in the model is carefully handled in compliance with privacy regulations.

- **Security:**
  - All datasets are stored securely with encryption and access control measures in place to protect against unauthorized access.
  - Proper data handling practices are followed, ensuring compliance with relevant data security standards.

---

## Limitations and Recommendations

- **Known Limitations:**
  - The model's complexity means it may require significant computational resources, especially for training and hyperparameter tuning.
  - Performance may degrade on long-term predictions (e.g., 24+ hours) as the model's accuracy tends to decrease over longer forecasting windows, though improvements are anticipated by exploring advanced time-series architectures (e.g., LSTM, GRU).
  - Seasonal variations and extreme weather events may introduce noise that the model struggles to handle without further fine-tuning.

- **Recommendations for Use:**
  - The model is best suited for medium-term (1-24 hours) air quality predictions.
  - It is recommended to experiment with ensemble methods or hybrid models (e.g., combining DNN with RNN) for improved long-term forecasting.
  - Ideal for decision support in urban planning, environmental policy, and public health advisories.

---

## Additional Information

- **References:**
  - Zhang, Q. *Nature*, 2017. [Link](http://www.pku-atmos-acm.org/static/pdfs/Zhang%20Q%202017%20Nature_1.pdf)
  - *Environmental Health*, 2022. [Link](https://www.environmentalhealth.org/2022/05/13/we-must-act-on-air-pollution-to-prevent-climate-disaster/)
  - Guan, D. et al. *Environmental Science & Technology*, 2016. [Link](https://pmc.ncbi.nlm.nih.gov/articles/PMC7652049/)
  - Bekkar, A. et al. *Journal of Big Data*, 2021. [Link](https://journalofbigdata.springeropen.com/articles/10.1186/s40537-021-00548-1)
  - *World Health Organization*. Ambient (Outdoor) Air Pollution, 2018. [Link](https://www.who.int/news-room/fact-sheets/detail/ambient-(outdoor)-air-quality-and-health)
For further understanding, please see all the relevent references in the References folder.
- **License:** ENG M 680 - Adavance Topics in Engineering Management II
- **Contact Information:** Shuvo Biswas (shuvo.biswas@ualberta.ca), Nasim Zaman Piyas (nasim.piyas@ualberta.ca), Maryum Ali (maryum4@ualberta.ca)

