# Predicting Dropout Rates: A Study of Equity and Bias

## Overview
This project investigates the use of machine learning models to predict student dropout rates while addressing fairness and equity. Using the Students Performance dataset, the study examines how socially relevant features like gender and ethnicity influence model predictions and subgroup disparities. The results highlight the importance of designing ethical and unbiased ML systems for educational applications.

## Key Features
- **Dataset Analysis**: Utilizes a balanced dataset of high school students with diverse demographic and academic attributes to predict dropout risk.
- **Fairness Evaluation**: Assesses model fairness by analyzing the impact of including or excluding demographic features (e.g., gender, ethnicity) on subgroup accuracy and F1 scores.
- **Feature Importance**: Investigates the influence of key features like absences, highlighting their predictive power and potential biases.
- **Intersectional Bias**: Explores disparities in predictions for intersectional groups, identifying challenges for underrepresented demographics.

## Project Structure
- `data`: Students Performance dataset and preprocessing scripts for stratified train-test splits
- `models`: Logistic Regression, Random Forest, and Multilayer Perceptron (MLP) models with optimized hyperparameters
- `evaluation`: Computed accuracy, F1 scores, and feature importance across demographic subgroups
- `results`: Performance metrics and visualizations of subgroup disparities under different feature inclusion scenarios

## Methodology
1. **Dataset and Preprocessing**:
   - Used the Students Performance dataset from Kaggle.
   - Converted target variable into a binary classification task to identify students at risk of dropout.
   - Created intersectional groups by combining gender and ethnicity to analyze fairness.
2. **Model Training**:
   - Trained three ML models: Logistic Regression, Random Forest, and MLP.
   - Evaluated model performance with and without demographic features (gender, ethnicity).
3. **Feature Analysis**:
   - Assessed the importance of key features, particularly absences, using feature importance metrics in Random Forest.
   - Analyzed the impact of removing absences on model accuracy and fairness.

## Results
- Models with the **Absences** feature demonstrated high accuracy (~91–93%) and balanced subgroup performance.
- Excluding **Absences** resulted in significant performance drops (~48–64%), highlighting its predictive importance.
- Intersectional biases were observed for underrepresented groups (e.g., "Other" ethnicity and African-American demographics), particularly in the MLP model when gender was excluded.
- Fairness trade-offs:
  - Logistic Regression offered more equitable outcomes across demographics with minimal accuracy trade-offs compared to MLP.

## Contributions
- **Ananya Kulshrestha**: Developed the MLP model, led initial data preprocessing, and authored the first half of the report.
- **Ronak Saluja**: Trained Random Forest and Logistic Regression models, contributed to evaluation scripts, and authored the second half of the report.

## Takeaways
1. **A Model is Only as Good as its Data**: Bias in datasets strongly influences model performance and fairness.
2. **Performance and Fairness Must Coexist**: Prioritizing fairness may require small trade-offs in accuracy but ensures equitable outcomes.
3. **Every Decision Counts**: Even minor adjustments in feature selection or architecture can significantly impact subgroup fairness and accuracy.

## Future Work
- Address class imbalances using techniques like undersampling, oversampling, or synthetic data generation.
- Evaluate the impact of diverse datasets and additional fairness-aware algorithms.
- Explore real-world datasets while ensuring data privacy and ethical considerations.

## Ethical and Societal Risks
This study emphasizes the need for ethical handling of sensitive data and fairness-aware designs in ML systems. Future implementations should avoid deploying models that perpetuate social biases and ensure rigorous testing to address intersectional disparities.

## Acknowledgements
Special thanks to Professor Hadfield-Menell, Professor Wilson, TA Stephen Casper, and the 6.3950 course staff for their guidance and support.

## References
For detailed citations, refer to the final project report. Dataset available on [Kaggle](https://www.kaggle.com/ds/5195702).
