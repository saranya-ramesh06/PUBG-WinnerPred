Project Overview

This project focuses on predicting a player's winning placement percentage (winPlacePerc) in the popular game PlayerUnknown's Battlegrounds (PUBG). The dataset comprises over 4.4 million observations with 28 variables, capturing various performance metrics across match types. The project applies data preprocessing, feature engineering, exploratory data analysis (EDA), and machine learning to develop an accurate predictive model.

Dataset Information
Dataset Used:

pubg.csv – Contains detailed stats of players in each match.

Key Features:

Id: Unique player ID

groupId: Unique team ID

matchId: Unique match ID

assists, kills, killPoints, headshotKills, damageDealt: Combat statistics

boosts, heals, revives: Healing/utility stats

walkDistance, rideDistance, swimDistance: Movement features

matchDuration, matchType: Game configuration

winPlacePerc: Target – Normalized placement percentage (0 to 1)

Exploratory Data Analysis (EDA)
Data Cleaning:
Verified data types and converted dates if necessary.

Checked for and addressed missing values.

Removed outliers that could skew model predictions (e.g., zero movement + zero kills).

Feature Engineering:
Created features representing player efficiency and aggression (e.g., killPerDistance, damagePerKill).

Aggregated team-level stats for better prediction (e.g., average kills, total distance).

Encoded matchType using label encoding or one-hot encoding.

Visualizations:
Distribution plots for numerical variables.

Correlation heatmaps to identify multicollinearity.

Boxplots to examine differences in winPlacePerc across match types and player groups.

Machine Learning Models Used
Several models were trained and evaluated:

Linear Regression

Decision Tree Regressor

Random Forest Regressor

XGBoost Regressor

Gradient Boosting Regressor

K-Nearest Neighbors Regressor

Model Evaluation Metrics
Used standard regression metrics to compare models:

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

R² Score

Hyperparameter Tuning
Performed hyperparameter tuning using GridSearchCV and RandomizedSearchCV.

Tuned models to improve performance and avoid overfitting.

How to Run the Project
1️ Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
2️ Run the Jupyter Notebook
bash
Copy
Edit
jupyter notebook PRCP-1012-GameWinnerPred.ipynb
Key Insights
Kills, walk distance, and damage dealt are strong predictors of a player’s final placement.

Match type and match duration significantly influence player behavior and outcome.

Healing and boosting are more common in matches with longer durations.

Players with no movement and no kills are likely bots or disconnected players, and negatively affect model performance.

Random Forest and XGBoost produced the most accurate predictions, due to their robustness against non-linear relationships and outliers.

Conclusion
The project successfully built a model to predict win placement percentages in PUBG. By leveraging combat, movement, and support features, the model offers insights into what gameplay aspects lead to better performance. These findings can help players refine strategies and help game developers understand engagement patterns.

