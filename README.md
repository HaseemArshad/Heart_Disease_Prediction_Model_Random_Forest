# Heart Disease Prediction using Random Forest

## Overview
This project utilizes a Random Forest Classifier to predict heart disease based on patient data. The dataset used comes from the Cleveland Heart Disease dataset and includes various patient attributes such as age, cholesterol levels, and exercise-induced angina. The model is trained and evaluated to provide insights into the most important factors contributing to heart disease.

## Dataset
The dataset consists of the following key features:
- **age**: Age of the patient
- **sex**: Gender (0 = Female, 1 = Male)
- **cp**: Chest pain type
- **trestbps**: Resting blood pressure
- **chol**: Cholesterol level
- **fbs**: Fasting blood sugar (1 = True, 0 = False)
- **restecg**: Resting electrocardiographic results
- **thalach**: Maximum heart rate achieved
- **exang**: Exercise-induced angina (1 = Yes, 0 = No)
- **oldpeak**: ST depression induced by exercise
- **slope**: Slope of the peak exercise ST segment
- **ca**: Number of major vessels colored by fluoroscopy
- **thal**: Thalassemia
- **condition**: Target variable (0 = No heart disease, 1 = Heart disease)

## Data Analysis
### Exploratory Data Analysis (EDA)
- **Correlation Analysis**: A heatmap is generated to analyze feature correlations.
- **Feature Distributions**: Boxplots and histograms visualize the distribution of key features.
- **Feature Engineering**: Age groups were created to assess trends.

## Model Training
### Preprocessing Steps
- One-hot encoding applied to categorical variables.
- Dataset split into training (80%) and testing (20%) sets.

### Model
A **Random Forest Classifier** is trained using the following hyperparameters:
- **n_estimators**: 100 (number of trees in the forest)
- **max_depth**: Tuned using GridSearchCV
- **min_samples_split**: Tuned using GridSearchCV

### Performance Metrics
- **Accuracy Score**: Measures overall model correctness.
- **Confusion Matrix**: Evaluates false positives and negatives.
- **ROC Curve & AUC Score**: Determines classification effectiveness.
- **Feature Importance**: Analyzes the most significant features in predicting heart disease.

## Results
- The model achieved an **accuracy of 0.73**.
- The most important features contributing to heart disease prediction include:
  - thal
  - thalach
  - oldpeak
  - ca
  - cp
  - trestbps
  - age
  - chol
  - exang
  - sex
  - slope
  - restecg
  - fbs
  - age_group_60-80
  - age_group_40-60
- The AUC Score is **0.84**, indicating good predictive ability.

## How to Run the Project
### Requirements
Ensure you have the following dependencies installed:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
```

### Running the Script
1. Clone the repository:
   ```bash
   git clone <repository_link>
   cd <repository_folder>
   ```
2. Place the dataset (`heart_cleveland_upload.csv`) in the project directory.
3. Run the script:
   ```bash
   python heart_disease_prediction.py
   ```
4. The trained model will be saved as `random_forest_heart_disease_model.pkl`.

## Future Improvements
- Implement deep learning models for improved predictions.
- Collect a larger dataset for better generalization.
- Deploy the model as a web application for real-world usability.

## Conclusion
This project demonstrates the effectiveness of machine learning in medical diagnosis. The Random Forest model provides a reliable method to predict heart disease, potentially aiding in early diagnosis and treatment planning.

