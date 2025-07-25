# Capstone\_2\_IMDB\_reviews

Movie Dataset data analysis





\# 🎬 Movie Voting Average Prediction - Capstone Project 2



\## 📌 Objective

To build a machine learning model that predicts the voting average of movies using data from TMDB, based on features such as genres, actors, directors, popularity, vote\_count, etc.



\## 🧩 Dataset

\- Source: The Movie Database (TMDB)

\- ~10,000 movies with features like genres, cast, director, and more



\## 🧹 Data Wrangling

\- Parsed stringified columns (`genres`, `actors`, etc.)

\- Handled missing values and dropped irrelevant columns

\- Extracted `release\_year` and dropped release\_date



\## 📊 EDA

\- Visualized voting\_average vs runtime

\- Checked genre frequency, top directors, top actors, etc.

\- Detected weak or no correlation between voting\_average and other variables, hence moved onto tree based models.



\## 🛠 Preprocessing

\- Log transformed `vote\_count`, `popularity`, and `runtime`

\- One-hot encoded categorical columns

\- Removed outliers using standard deviation method

\- Feature Engineered num\_genres, main\_genres, num\_actors, main\_actors



\## 📈 Modeling

\- Tried: Linear Regression, Decision Tree, Random Forest, Gradient Boosting, XGBoost.

\- Final Model: XGBoost (after hyperparameter tuning using RandomizedSearchCV)



\## 🧪 Results

| Model              | R²     | MAE   | RMSE |

|-------------------|--------|-------|------|

| Linear Regression | 0.19   | 0.53  | 0.78 |

| Decision Tree     | 0.08   | 0.63  | 0.79 |

| Random Forest     | 0.42   | 0.48  | 0.66 |

| Gradient Boosting | 0.40   | 0.50  | 0.67 |

| \*\*XGBoost (Tuned)\*\* | \*\*0.46\*\* | \*\*0.46\*\* | \*\*0.65\*\* |



\## Conclusion

\- XGBoost achieved the best results.

\- Feature engineering and handling data irregularities significantly improved performance.

\- Future improvement: merge another dataset that has reviews of the movie, budget and relevant information that can boost performance.

