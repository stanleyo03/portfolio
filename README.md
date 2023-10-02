![pfp](/images/pfp_me.JPG)

My name is Stanley and I'm studying Statistics, Machine Learning, and Computer Science at Carnegie Mellon Univeristy. I am passionate about statistics and data science and am constantly learning new skills to deepen my understanding and knowledge of data science. Here are two of the projects I have worked on in the past. 

# Project 1: Stock Portfolio Tracker and Predictor
This Python project offers a comprehensive stock portfolio tracker with visualization and predictive capabilities. The project utilizes the Yahoo Finance API (yfinance) to fetch historical stock data for a given ticker. The system allows users to input stocks in the format "Ticker Share_Count YYYY-MM-DD" and tracks their portfolio's performance over time. Key features include:

**Portfolio Tracking:** The system keeps track of each stock's performance in the portfolio, including initial investment value, current value, and net profit/loss.

**Portfolio Visualization:** The system provides visualization tools to showcase the performance of individual stocks and the entire portfolio over time. It plots both actual and predicted stock prices, helping users gauge the effectiveness of the predictive model.

**Predictive Modeling:** The project implements a neural network predictive model using TensorFlow and LSTM layers to forecast future stock prices. The model takes historical data as input and provides predictions for the next day's closing price.

**Interactive Interface:** The program offers an interactive command-line interface where users can request stock predictions, view transaction history, calculate total net profit, and visualize portfolio profits.

**Limitations:** The current version has limitations, such as the inability to add more shares to an existing stock and removing stock shares.

The project aims to provide users with insights into their stock portfolio's performance, predictions, and trends using historical data and predictive modeling. The code is organized into classes for Stocks and Portfolios, promoting modularity and scalability.

For example , the following stocks were added to the portfolio in the form of 'ticker num_shares date_added': 
aapl 1 2020-01-01
tsla 2 2022-02-02
lcid 10 2021-12-20
nvda 1 2023-01-01
amzn 2 2021-12-31

Here is a visualization of the portfolio's profits over time.
![image](https://github.com/StanO1225/Stanley_Portfolio/assets/115967184/f5298ba3-6d23-421b-be8e-7f832fde84e4)

Here is a visualization for predicted stock prices for Nvidia.
![image](https://github.com/StanO1225/Stanley_Portfolio/assets/115967184/7fd0474f-5033-40b6-9e27-3b64d91774f5)

# Project 2: Predicting NBA Career Outcomes

This project involves building a Random Forest Classification model to predict the career outcomes of NBA players based on their performance during their first four seasons in the league. 

## Frameworks Used:
- Pandas
- Matplotlib/Seaborn
- Sklearn: train_test_split, RandomForestClassifier, GridSearchCV

## Project Steps:

### Data Cleaning: 
- Read in the two datasets: 'awards_data.csv' containing awards/accolades information and 'player_stats.csv' containing player statistics. Merged them on player/season to get overall dataframe.
- Performed EDA on the loaded data to understand its structure and contents.
- Conducted data imputation by replacing null values with the mean and transforming categorical variables into numerical representations.

### Data Engineering
- Define the outcome classes for both season and career outcomes based on predefined guidelines (Elite, All-Star, Starter, Rotation, Roster, Out of the League).
- Split the data into two sets based on players' draft years: pre-2015 and post-2015 based on the requirements in our definition of career outcome.
- Aggregated player statistics over the first four seasons in the league to create features and training set for the model.

### Model Selection, Training, and Evaluation:
- Select a RandomForestClassifier as the model due to its ability to handle feature selection and thresholds effectively.
- Split the dataset into training and test sets for model evaluation.
- Use GridSearchCV for hyperparameter optimization to find the best model configuration.
- Train the RandomForestClassifier using the training data with the optimized hyperparameters.
- Evaluate the model's performance on both the training and test sets using accuracy metrics: training set accuracy > 90% while testing set accuracy is ~60%
- Prepared a dataset of post-2018 drafted players and predicted the probabilities each of their careers fell into each of the categories.

![image](/images/feature_importance_bar.JPG)
### Conclusion
This project demonstrates the application of a Random Forest Classification model to predict NBA players' career outcomes based on their first four seasons' performance. By carefully preprocessing the data, selecting relevant features, and optimizing the model, we achieved a ~60% accuracy in predicting career outcomes. The insights gained from this project can provide valuable information for NBA teams and analysts in making strategic decisions about player development and team building. Future improvements to the model involve using a larger training dataset, more selective feature selection, and other data engineering techniques to reduce the possibilities of overfitting.
