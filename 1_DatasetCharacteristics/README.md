# Dataset Characteristics

**[Notebook](exploratory_data_analysis.ipynb)**

## Dataset Information

### Dataset Source
- **Dataset Link:** [Provide a direct link to your dataset. If the dataset is private, explain the reason and provide contact information for the dataset owner] The date is part of a challenge on the https://challengedata.ens.fr website.
- **Dataset Owner/Contact:** [[[If applicable, provide contact information for private datasets] https://challengedata.ens.fr/participants/challenges/163/

### Dataset Characteristics
- **Number of Observations:** 6,076,546 (Training samples) + approx. 2,028,750 (Test samples). Total: approx. 8.1 million records.
- **Number of Features:** 6 base features (plus derived features such as One-Hot Encodings).

### Target Variable/Label
- **Label Name:** invalid_ratio
- **Label Type:** Regression (Continuous value in the interval [0, 1])
- **Label Description:** This label represents the ratio of parking violations in a specific zone at a specific time.
- It is a ratio value:
    0.0 means: No parking violations (0%).
    1.0 means: Exclusively parking violations (100%). The task is to predict this proportion based on location and time.
- **Label Values:**[0.0 to 1.0] (Float). Common values are fractions resulting from raw counts (e.g., 1/3 ≈ 0.333, 1/2 = 0.5), as well as the extremes 0.0 and 1.0.
- **Label Distribution:** The distribution is strongly "bimodal" at the edges and generally widely distributed:
    The mean is approx. 0.502.
    A large portion of the data consists of extreme values: approx. 27% of the data are exactly 1.0 (only violations) and approx. 16% are exactly 0.0 (no violations).
    The rest is distributed across the entire spectrum in between.
### Feature Description
[Provide a brief description of each feature or group of features in your dataset. If you have many features, group them logically and describe each group. Include information about data types, ranges, and what each feature represents.]

**Example format:**
Spatio-Temporal Features This group defines where and when the measurement took place.
  -  Feature 1 (longitude / longitude_scaled): [Geographic longitude of the location. Data type: Float. Represents the East-West position of the parking zone.]
   - Feature 2 (latitude / latitude_scaled): [Geographic latitude of the location. Data type: Float. Represents the North-South position of the parking zone.]
   - Feature 3 (hour): [Hour of the day (0-23). Data type: Integer/Categorical. Critical for identifying daily patterns (e.g., rush hour, night time).]
   - Feature 4 (day_of_week): [Day of the week (e.g., 0=Monday to 6=Sunday). Data type: Integer/Categorical. Distinguishes between weekdays and weekends.]
   - Feature 5 (month_of_year): [Month of the year (1-12). Data type: Integer/Categorical. Captures seasonal effects.]
Contextual Features Additional information regarding the measurement context.
   - Feature 6 (total_count): [The total number of vehicles detected in this zone at this time. Data type: Integer. Serves as a weighting factor for the significance of the invalid_ratio (e.g., a ratio derived from total_count=100 is statistically more significant than one derived from total_count=1).]

## Exploratory Data Analysis

The exploratory data analysis is conducted in the [exploratory_data_analysis.ipynb](exploratory_data_analysis.ipynb) notebook, which includes:
- Data loading and initial inspection
- Statistical summaries and distributions
- Missing value analysis
- Feature correlation analysis
- Data visualization and insights
- Data quality assessment
