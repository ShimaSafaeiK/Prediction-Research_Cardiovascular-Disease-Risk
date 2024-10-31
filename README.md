# Prediction-Research_Cardiovascular-Disease-Risk
Machine learning project predicting cardiovascular disease risk using genetic and health data, leveraging TensorFlow for AI-driven insights into cardiovascular health.
### Summary of Steps and Improvements
#In this project, I aimed to predict cardiovascular disease risk using the UCI heart disease dataset. 
#Below is an overview of how we tackled various issues and improved our model in multiple iterations:

#1. **Initial Handling of Missing Values:**
   #- I initially removed four columns with the most missing values to ensure a more complete dataset for training.
   #- Later, I revised this approach by filling missing values with the median to retain more information.

#2. **One-Hot Encoding and Feature Selection:**
   #- I applied one-hot encoding to categorical features, such as 'sex', 'thal', and 'slope'. Initially, I dropped the 'id' column and selected key features.
   #- I continuously refined which features were selected to ensure that the model used the most relevant data.

#3. **Normalization of Features:**
   #- Continuous features were normalized to improve model convergence during training.
   #- I used `StandardScaler` to standardize features like 'age', 'cholesterol', and 'thalch'.

#4. **Feature Engineering Attempts:**
     #- I tried several feature engineering strategies:
     #- Removing less important columns to handle missing values.
     #- Filling missing values with the median.
     #- Normalizing features to reduce the influence of outliers.
     #- Finally, I chose to retain most features while filling missing values to preserve as much data as possible.

#5. **Neural Network Model Iterations:**
   #- Initially, I used a simpler neural network model which had fewer units in each layer.
   #- I iterated by adding more layers, units, and batch normalization. This increased the model’s complexity to improve its learning capability.
   #- I added dropout layers to prevent overfitting, which is when a model performs well on training data but poorly on unseen data.

#6. **Random Forest and XGBoost Models:**
   #- I later incorporated two other powerful models: RandomForest and XGBoost.
   #- These models were trained alongside our neural network to understand their performance on the same dataset.

#7. **Model Evaluation and Comparison:**
   #- I evaluated each model using metrics such as accuracy, F1 score, precision, recall, and ROC-AUC.
   #- I compared the three models: Neural Network, RandomForest, and XGBoost.
   #- Feature importance plots were created to understand which features most influenced the RandomForest and XGBoost models.

### Project Steps in Bullet Points

#1. **Import Libraries**: Loaded necessary Python libraries for data handling, model training, visualization, and evaluation.

#2. **Load and Preview Dataset**: Loaded the UCI heart disease dataset and conducted an initial exploration.

#3. **Visualize Missing Data**: Created a heatmap to visualize missing values in the dataset.

#4. **One-Hot Encoding**: Encoded categorical features using one-hot encoding to convert them into numerical data for modeling.

#5. **Feature Selection**: Selected features for the model based on relevance while excluding unnecessary columns like 'id'.

#6. **Normalization**: Applied normalization to continuous features to bring them to the same scale.

#7. **Handle Missing Values**: Dropped columns with the most missing values and filled other missing values with the median.

#8. **Reload Data and Redefine Target**: Reloaded and reprocessed the dataset for consistency, ensuring target and features were correctly defined.

#9. **Split Data**: Divided the data into training and test sets to evaluate model performance effectively.

#10. **Build Neural Network**: Created an improved neural network with dropout and batch normalization to prevent overfitting.

#11. **Train Neural Network**: Trained the model with callbacks for early stopping and learning rate reduction.

#12. **Model Evaluation**: Evaluated the model using accuracy, F1 score, precision, recall, ROC-AUC, and confusion matrix.

#13. **RandomForest and XGBoost Models**: Trained two additional models (RandomForest and XGBoost) to compare their performance with the neural network.

#14. **Compare All Models**: Compared accuracy and F1 scores for all three models.

#15. **Feature Importance Visualization**: Visualized feature importance for RandomForest and XGBoost.

