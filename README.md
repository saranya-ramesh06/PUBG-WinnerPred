#  PUBG Winner Placement Prediction  

This project focuses on predicting a player’s winning placement percentage (winPlacePerc) in the popular battle royale game PlayerUnknown’s Battlegrounds (PUBG). Using data from over *4.4 million* player stats, we apply data preprocessing, feature engineering, EDA, and various machine learning models to build an accurate prediction model.

---

##  Dataset Information

*Dataset Used:* pubg.csv  
Contains detailed stats of players in each match.

###  Key Features:

| Feature         | Description                                |
|-----------------|--------------------------------------------|
| Id            | Unique player ID                           |
| groupId       | Unique team ID                             |
| matchId       | Unique match ID                            |
| assists, kills, headshotKills, killPoints, damageDealt | Combat statistics |
| boosts, heals, revives | Healing & utility stats |
| walkDistance, rideDistance, swimDistance | Movement stats |
| matchDuration, matchType | Game configuration |
| winPlacePerc  | 🎯 *Target* – Normalized placement percentage (0 to 1) |

---

##  Exploratory Data Analysis (EDA)

-  Verified data types and handled any format issues  
-  Handled *missing values*  
-  Removed *outliers* (e.g., zero movement + zero kills = probable bot)  

###  Visual Analysis:
- Distribution plots for numerical features  
- Correlation heatmaps for multicollinearity detection  
- Boxplots to compare winPlacePerc across match types and player groups  

---

##  Feature Engineering

- Created new metrics:
  - killPerDistance (kills per walk distance)
  - damagePerKill (average damage per kill)
- Aggregated *team-level features* like:
  - avgKills, totalDistance
- Encoded matchType using Label Encoding & One-Hot Encoding

---

##  Machine Learning Models Used

| Model                        | Description |
|-----------------------------|-------------|
| Linear Regression           | Baseline model |
| Decision Tree Regressor     | Tree-based non-linear model |
| Random Forest Regressor     | Ensemble of decision trees |
| XGBoost Regressor           | Advanced boosting model |
| Gradient Boosting Regressor | Boosting with shallow trees |
| K-Nearest Neighbors         | Distance-based prediction |

---

##  Model Evaluation Metrics

- *Mean Absolute Error (MAE)*
- *Mean Squared Error (MSE)*
- *Root Mean Squared Error (RMSE)*
- *R² Score (Coefficient of Determination)*

###  Best Models:
- *Random Forest Regressor*
- *XGBoost Regressor*

---

##  Hyperparameter Tuning

- Used GridSearchCV and RandomizedSearchCV for tuning  
- Optimized parameters to *improve accuracy* and *reduce overfitting*

---

## Conclusion 
- The project successfully built a model to predict win placement percentages in PUBG. By leveraging combat, movement, and support features, the model offers insights into what gameplay aspects lead to better performance. These findings can help players refine strategies and help game developers understand engagement patterns.

