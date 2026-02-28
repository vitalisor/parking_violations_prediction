# Spatio-Temporal Prediction of Invalid Parking Ratios

## Repository Link

[(https://github.com/vitalisor/parking_violations_prediction)]

## Description

This project aims to predict the invalid parking ratio (`invalid_ratio`) for specific geographic zones and timeframes. 
The problem is to identify patterns in illegal parking based on spatio-temporal features such as location (latitude/longitude), 
traffic volume (`total_count`), and time (hour, day, month).

### Task Type

Regression (Tabular Data)

### Results Summary

#### Best Model Performance
- **Best Model:** CatBoost Regressor (Gradient Boosting with Native Categorical Support)
- **Evaluation Metric:** Spearman Rank Correlation (Primary) and Mean Squared Error (MSE)
- **Final Performance:** Spearman Correlation of **~0.545**, MSE of **~0.039**

#### Model Comparison
- **Baseline Performance:** Random Forest Regressor (Spearman: ~0.452, MSE: ~0.045)
- **Improvement Over Baseline:** ~0.093 increase in Spearman Correlation (+20.5% relative improvement)
- **Best Alternative Model:** Multi-Input Deep Neural Network with Spatial Embeddings via K-Means Clustering (Spearman: ~0.518, MSE: ~0.041)

#### Key Insights
- **Most Important Features:** 1. Geographic Location (Represented natively in CatBoost or via K-Means Zone_ID in the Neural Network)
  2. Traffic Volume (`total_count`)
  3. Time of Day (`hour`)
- **Model Strengths:** The CatBoost model effectively captures complex, non-linear patterns in tabular data and handles categorical features (like day, month, hour) natively, bypassing the massive memory overhead of one-hot encoding. It excels at ranking the relative risk of different zones.
- **Model Limitations:** While highly accurate on seen data distributions, tree-based models generally struggle to extrapolate outside the boundaries of the training data (e.g., predicting for a completely new, unseen city area).
- **Business Impact:** A high Spearman score indicates the model correctly ranks zones by their violation risk. This allows parking enforcement agencies to move away from random patrols and instead strategically prioritize high-risk areas, significantly optimizing resource allocation and patrol efficiency.

## Documentation

1. **[Literature Review](0_LiteratureReview/README.md)**
2. **[Dataset Characteristics](1_DatasetCharacteristics/exploratory_data_analysis.ipynb)**
3. **[Baseline Model](2_BaselineModel/baseline_model.ipynb)**
4. **[Model Definition and Evaluation](3_Model/model_definition_evaluation)**
5. **[Presentation](4_Presentation/README.md)**

## Cover Image

![Project Cover Image](CoverImage/cover_image.png)
