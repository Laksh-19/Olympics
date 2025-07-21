🏅 Olympic Medals Prediction using Linear Regression

This Google Colab notebook analyzes historical Olympic team performance data and builds a Linear Regression model to predict the number of medals a country may win based on available factors like the number of athletes and past medal performance.

📁 Dataset

We use the 'teams.csv' dataset containing:

team: Team name
country: Country name
year: Olympic year
athletes: Number of athletes sent
age: Average age of athletes
prev_medals: Number of medals won in the previous Olympics
medals: Actual medals won that year

📊 Project Overview

1. Data Preprocessing
Filtered essential columns
Removed null entries to ensure data consistency

2. Exploratory Data Analysis (EDA)
Correlation Analysis:
Found that athletes and prev_medals showed the strongest positive correlation with medal counts.
Visual Analysis:
Used Seaborn plots to visualize trends and relationships between medal counts and predictors.

3. Train-Test Split
Training Set: Data from Olympics before 2012
Test Set: Data from 2012 onwards
This ensures the model is trained on past data and tested on future events (following the 80:20 rule).

4. Model Building
Linear Regression using:
athletes
prev_medals
Model trained on historical data to predict future medal counts.

5. Evaluation
Mean Absolute Error (MAE):
The MAE was approximately 3.2986 medals, indicating the model was off by ~3 medals per team on average.
Post-processing:
Predictions were rounded and negative values were clipped to zero.
Error Analysis:
Created bar plots showing the difference between actual and predicted medals per country.
Prediction Accuracy:
While not perfect, the model provided reasonable estimates, especially for countries with consistent Olympic performance histories. It remained pretty accurate for countries with higher medal winning history eg. France, Canada, etc.

📦 Requirements

Python 3
pandas
numpy
seaborn
scikit-learn
matplotlib (optional, used via pandas plotting)

🚀 How to Run

Open the notebook in Google Colab
Upload the teams.csv dataset to the session
Run each cell step by step to reproduce the results

✅ Future Improvements

Try other models (e.g., Ridge, Random Forest, Gradient Boosting)
Include more features like:
Host country status
GDP or investment in sports
Gender ratio of athletes
Implement cross-validation for better generalization
