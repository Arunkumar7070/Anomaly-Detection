# Anomaly-Detection

## Project Team
- 22PW05 -> Arun Kumar
- 22PW34 ->Shree Vishal

## Objective
The main goal is to identify and flag anomalous user behavior in shared computer environments. Using the timing data of key holds, the system distinguishes between typical and atypical typing patterns, assisting in behavioral biometrics-based user identification.

## Dataset
The dataset contains 1,882 records with:
- **Timestamp**: A record of when each key was pressed.
- **Hold Time**: Duration each key was held down (in seconds).

## Methodology
### 1. **Data Preprocessing**
   - **Date Conversion**: Timestamps are converted into a `datetime` format for easier manipulation.
   - **Feature Scaling**: The `Hold Time` column is scaled for consistency.
   - **Invalid Entry Removal**: Entries with zero hold time are removed.

### 2. **Anomaly Detection Models**
   - **Isolation Forest**: An ensemble model that identifies anomalies by randomly isolating data points, making it effective for high-dimensional data.
   - **One-Class SVM**: A support vector machine model that detects anomalies by classifying points significantly deviating from the main distribution.
   - **Autoencoders**: Neural network-based models that reconstruct data patterns and identify anomalies when reconstruction errors are high.

### 3. **Rolling Statistics for Trend Analysis**
   - **Rolling Mean and Standard Deviation**: Calculated to monitor trends and highlight sudden deviations in hold times.

## Results
Each model was tested to assess its effectiveness in detecting typing pattern anomalies. Isolation Forest and One-Class SVM showed promising results for identifying behavioral deviations, while Autoencoders provided insight into subtle patterns via reconstruction errors.

## Technologies Used
- **Python Libraries**: `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`, `Scikit-learn`, `TensorFlow/Keras`
- **Framework**: Flask (for web application deployment)
