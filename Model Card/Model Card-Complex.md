# Model Card: Preferred Model for Air Quality Prediction

## Model Details

- **Model Name:** Deep neural network designed for time-series forecasting, combining recurrent layers 
- **Model Version:** 1.0
- **Model Type:** Time-Series Regression Model using RNN
- **Developers:** Shuvo Biswas, Nasim Zaman Piyas, Maryum Ali, Izuchukwu Ogbuigbo, Manjot Singh
- **Release Date:** 10th December 2024

---

## Intended Use

- **Primary Use:** Predicting air pollution levels in Beijing based on weather and pollutant data.
- **Intended Users:** Public health authorities, Healthcare Providers, Smart City Developers, and Environmental & Health Researchers who are interested to work with air quality data.
- **Out-of-Scope Use Cases:** Real-time applications and predictions for regions outside Beijing or data outside the training time period (2013–2017).

---

## Model/Data Description

- **Data Used**: 
  - Air quality data from Beijing Municipal Environmental Monitoring Center.
  - Weather data from China Meteorological Administration.
  - Covers hourly data (March 2013–February 2017) from 12 monitoring stations.
  - Features include pollutant concentrations (e.g., PM2.5, SO2), weather variables (e.g., temperature, pressure), and temporal features.

- **Features**: Pollutant levels (PM2.5, PM10, CO, NO2, SO2, O3), meteorological data (Temperature, Pressure, Wind Direction etc.), temporal patterns (Time of day, Day of week).

- **Model Architecture:** 
  - A deep neural network (DNN) combining sequential and dense layers to capture complex nonlinear time-series relationships. The architecture includes the Key hyperparameters:
    - **Number of features:** 16
    - **Train, Validation & Test data ratio:** 7:2:1
    - **Number of Hidden Layers:** 2
    - **1st hidden layer:** 64
    - **2nd Hidden Layer:** 128
    - **Activation Functions:** ReLu
    - **Optimizer:** Adam
    - **Epochs: 100**

## Training and Evaluation

- **Training Procedure:**
  - The model was trained using historical air quality data from Beijing, with the dataset split into 70% training, 20% validation, and 10% testing. The training process utilized Python and key libraries such as pandas, scikit-learn, and TensorFlow.

- **Evaluation Metrics:**
  - The model is evaluated using common regression metrics:
    - Mean Absolute Error (MAE) : **0.302**
    - Root Mean Squared Error (RMSE) : **0.536**
    - R-squared (R²) Score : **0.947**
  - The evaluation is conducted on the held-out test dataset to assess how well the model generalizes to unseen data.

- **Baseline Comparison:**
  - The model was compared against more complex architectures like LSTM, Bi-LSTM, and GRU, as well as simpler regression models, to assess accuracy and computational efficiency.

## Ethical Considerations

- **Fairness and Bias**: Normalization and balanced representation were applied to address geographic, temporal, and data quality biases. Measures were taken to mitigate biases and handle outliers caused by unforeseen impacts at monitoring stations, ensuring fairness and robustness.
- **Privacy**: The non-personal training data is anonymized and compliant with privacy regulations, ensuring transparent use for public communication.
- **Security**: Data is encrypted, access is controlled, and secure storage practices are used to prevent unauthorized access to sensitive air quality data.

## Limitations and Recommendations

- **Known Limitations:**
  - Performance may degrade on long-term predictions (e.g., 24+ hours) as the model's accuracy tends to decrease over longer forecasting windows, though improvements are anticipated by exploring advanced time-series architectures (e.g., LSTM, GRU).

- **Recommendations for Use:**
  - The model is best suited for short-term (1-3 hours) air quality predictions.


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

