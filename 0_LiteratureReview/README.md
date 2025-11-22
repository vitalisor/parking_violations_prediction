# Literature Review

Approaches or solutions that have been tried before on similar projects.

**Summary of Each Work**:

- **Source 1**: [Predicting the spatiotemporal legality of on-street parking using open data and
machine learning]

  - **[[Link](https://www.tandfonline.com/doi/epdf/10.1080/19475683.2019.1679882?needAccess=true)]()**
  - **Objective**:The objective was to propose a data-driven framework using NYC open data (parking tickets, POIs, human mobility) to understand and predict the spatiotemporal legality of on-street parking, while also examining the impact of different spatial scales on model performance.

  - **Methods**:The study aggregated multi-source data into four spatial units (point, street, census tract, and grid) and applied various machine learning models—including Random Forest, SVM, and DNN—as both a regression problem (predicting ticket counts) and a binary classification problem (legal vs. risky).
  - **Outcomes**:The results showed that the Random Forest model performed best across all spatial scales for both regression and classification , that finer spatial resolutions generally produced less error , and that POIs like retail and food services were positively associated with parking violations.
  - **Relation to the Project**:

- **Source 2**: [Predicting on-street parking violation rate using deep residual neural networks]

  - **[[Link](https://www.sciencedirect.com/science/article/abs/pii/S0167865522002938)]()**
  - **Objective**:The objective of the work was to develop a deep learning system capable of predicting fine-grained on-street parking violation rates by using indirect data instead of expensive sensors.
  - **Methods**:The authors used a deep residual neural network trained on features like time, weather, sector capacity, and geographical distances to "Points of Interest" (PoIs) , supplemented by a novel Gaussian smoothing method to handle sparse data.
  - **Outcomes**:The results demonstrated that the model can accurately predict parking violation rates on a large-scale dataset (MAE 0.169) , with the data smoothing technique significantly improving accuracy and the approach outperforming a related method.
  - **Relation to the Project**:

- **Source 3**: [Parking Ticket Analysis using Machine Learning]

  - **[[Link](https://github.com/tadowney/ticket_analysis)]()**
  - **Objective**:The project's goal is twofold: first, to conduct an exploratory data analysis of the extensive New York City parking violation dataset, and second, to test and compare various machine learning models for predicting a ticket characteristic.
  - **Methods**:
Python (Pandas, Matplotlib, Seaborn) was used for the analysis; for the prediction, three specific classification models were trained and compared: a Deep Feedforward Neural Network, K-Nearest Neighbor (KNN), and a Decision Tree Classifier.
  - **Outcomes**:
The project provides a Jupyter Notebook with exploratory visualizations of the NYC data and a performance comparison of the prediction models, which shows relatively low accuracy for all models (e.g., the Neural Network at 45.40% and Decision Tree at 33.98%) alongside significant differences in training runtime
  - **Relation to the Project**:
