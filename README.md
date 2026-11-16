# PPG Signal Regression and Classification

## Overview
An exploratory Machine Learning project focused on analyzing Photoplethysmography (PPG) signals through regression and classification techniques.

The project investigates the relationship between statistical features extracted from PPG signals and glucose measurements using multiple machine learning algorithms.

## Dataset Information
- Number of participants: 18
- Original signal recordings: 18
- Samples per recording: 21,900
- Segmentation window sizes: 250, 500 and 1,000 samples
- Window overlap: 50%
- Extracted statistical features: 12

## Technologies Used
- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- SciPy

## Methodology

### 1. Signal Exploration and Preprocessing
- Inspected raw PPG recordings.
- Examined signal characteristics and statistical properties.
- Explored different signal segmentation window sizes.

### 2. Signal Segmentation
- Divided recordings into windows of 250, 500 and 1,000 samples.
- Applied 50% overlap between consecutive windows.

### 3. Feature Extraction
Extracted 12 statistical features:
- Mean, Standard Deviation and Variance
- Minimum, Maximum and Median
- Range and Root Mean Square (RMS)
- Interquartile Range (IQR)
- Skewness and Kurtosis
- Mean Absolute Difference

### 4. Regression
Implemented and compared:
- Linear Regression
- Support Vector Regression (SVR)
- Decision Tree Regressor
- Random Forest Regressor

### 5. Classification
Implemented and compared:
- Logistic Regression
- Support Vector Machine (SVC)
- Decision Tree Classifier
- Random Forest Classifier

Glucose categories were assigned using predefined project thresholds:
- Normal: Glucose ≤ 125
- Prediabetic: 125 < Glucose ≤ 175
- Diabetic: Glucose > 175

Classification experiments used the categories represented in the available dataset.

### 6. Model Evaluation
Used Leave-One-Out Cross-Validation (LOOCV).

Regression metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

Classification metrics:
- Accuracy
- Macro Precision
- Macro Recall
- Macro F1-score
- Balanced Accuracy
- Confusion Matrix

## Experimental Findings
- SVR achieved the lowest MAE among the tested regression configurations with a 250-sample window using PPG-only features.
- Random Forest Classifier achieved the highest classification accuracy of 77.78% with 250- and 500-sample windows.

## Limitations
- The dataset contains only 18 participant-level recordings.
- Classification results are affected by class imbalance.
- The project-defined glucose thresholds are experimental and are not intended for clinical diagnosis.
- The models have not been clinically validated.

## Project Structure
- `PPG_Regression_and_Classification_Project.ipynb` – Main notebook containing signal analysis, feature extraction, model implementation and evaluation.

## Execution
1. Open the notebook in Google Colab.
2. Connect or upload the required dataset.
3. Install the necessary dependencies.
4. Execute the notebook cells sequentially.


## Project Visualizations

### 1. Glucose Level Distribution
This histogram illustrates the distribution of glucose measurements across the participants.

![Glucose Level Distribution](images/glucose-distribution.png)

### 2. Raw PPG Signal
Visualization of the complete raw PPG signal recording.

![Raw PPG Signal](images/raw-ppg-signal.png)

### 3. Detailed PPG Signal
A closer view of the first 2,000 samples of the PPG signal.

![Detailed PPG Signal](images/detailed-ppg-signal.png)

## Author

**Vinita Sharma**

- GitHub: [@vinitasharma15](https://github.com/vinitasharma15)

This repository documents my implementation and exploration of PPG signal analysis using Machine Learning.
