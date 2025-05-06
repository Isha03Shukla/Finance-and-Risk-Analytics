**Part A** <br>
**Context** <br>
In the realm of modern finance, businesses encounter the perpetual challenge of managing debt obligations effectively to maintain a favorable credit standing and foster sustainable growth. Investors keenly scrutinize companies capable of navigating financial complexities while ensuring stability and profitability. A pivotal instrument in this evaluation process is the balance sheet, which provides a comprehensive overview of a company's assets, liabilities, and shareholder equity, offering insights into its financial health and operational efficiency. In this context, leveraging available financial data, particularly from preceding fiscal periods, becomes imperative for informed decision-making and strategic planning.<br>

**Objective**<br>
A group of venture capitalists want to develop a Financial Health Assessment Tool. With the help of the tool, it endeavors to empower businesses and investors with a robust mechanism for evaluating the financial well-being and creditworthiness of companies. By harnessing machine learning techniques, they aim to analyze historical financial statements and extract pertinent insights to facilitate informed decision-making via the tool. Specifically, they foresee facilitating the following with the help of the tool:

1. Debt Management Analysis: Identify patterns and trends in debt management practices to assess the ability of businesses to fulfill financial obligations promptly and efficiently, and identify potential cases of default.<br>
2. Credit Risk Evaluation: Evaluate credit risk exposure by analyzing liquidity ratios, debt-to-equity ratios, and other key financial indicators to ascertain the likelihood of default and inform investment decisions.<br>

They have hired you as a data scientist and provided you with the financial metrics of different companies. The task is to analyze the data provided and develop a predictive model leveraging machine learning techniques to identify whether a given company will be tagged as a defaulter in terms of net worth next year. The predictive model will help the organization anticipate potential challenges with the financial performance of the companies and enable proactive risk mitigation strategies.
Credit Default Prediction

---

The **objective** of this project is to develop a Financial Health Assessment Tool using machine learning techniques to evaluate the financial stability and creditworthiness of companies. By analyzing historical financial metrics, the tool aims to:
1. Predict potential defaulters in terms of net worth in the following year.
2. Facilitate debt management analysis by identifying patterns and trends in financial obligations and default risks.
3. Evaluate credit risk through key financial indicators such as liquidity ratios and debt-to-equity ratios.
The ultimate goal is to empower investors and businesses with actionable insights to support informed decision-making and proactive risk mitigation strategies.


My task was to:
1. Analyzing the provided financial data.
2. Imputing missing values - I used KNN imputer
3. Developing a machine learning model that can predict potential defaults by companies.
4. Evaluating model performance using standard classification metrics.
5. Drawing conclusions and recommending the best-performing model for deployment in a Financial Health Assessment Tool.

1. Data Loading and Cleaning:
    * The dataset was loaded using pandas.
    * Missing values and outliers were handle - KNN Imputer - 5 neighbors for KNN Imputer
    * Features and target variable (default) were clearly defined - 
2. Exploratory Data Analysis (EDA):
    * Correlation matrices and visualizations were used to understand relationships between financial metrics.
    * Key financial indicators such as liquidity ratio, debt-equity ratio, return on assets, etc., were examined.
3. Feature Scaling & Encoding:
    * StandardScaler or similar was used for numerical normalization.
    * Categorical variables (if any) were encoded.
4. Model Building: Several machine learning classification models were trained and evaluated, including:
    * Logistic Regression
    * Random Forest
Model Performance Improvement using VIF
Variance Inflation Factor (VIF) is a measure of multicollinearity in a set of multiple regression variables. A high VIF indicates that the associated independent variable is highly collinear with the other variables in the model.

1. Model Evaluation: Evaluation metrics included:
    * Accuracy
    * Precision, Recall, and F1-Score
    * ROC-AUC Score
    * Confusion Matrix

After evaluating various machine learning models on the classification task of predicting company defaults, the Random Forest models emerged as the most effective. While the untuned Logistic Regression model exhibited overfitting—with high performance on the training set but poor generalization to the testing set—the tuned Logistic Regression model showed improved performance but still fell short in comparison. Specifically, the tuned Logistic Regression achieved an accuracy of 0.789 and a recall of 0.981 on the test set. In contrast, both the basic and tuned versions of the Random Forest model achieved perfect scores across all key metrics (accuracy, precision, recall, and F1-score) on both training and testing sets. This indicates not only high predictive power but also strong generalization ability. Given their consistent and robust performance, the Random Forest models are the most suitable choice for the final classification task in this financial risk assessment project.

---

**Part B**<br>
**Context**<br>
Investors face market risk, arising from asset price fluctuations due to economic events, geopolitical developments, and investor sentiment changes. Understanding and analyzing this risk is crucial for informed decision-making and optimizing investment strategies.<br>

 

**Objective**<br>
The objective of this analysis is to conduct Market Risk Analysis on a portfolio of Indian stocks using Python. It uses historical stock price data to understand market volatility and riskiness. Using statistical measures like mean and standard deviation, investors gain a deeper understanding of individual stocks' performance and portfolio variability.<br>

Through this analysis, investors can aim to achieve the following objectives:<br>

1. Risk Assessment: Analyze the historical volatility of individual stocks and the overall portfolio.<br>
2. Portfolio Optimization: Use Market Risk Analysis insights to enhance risk-adjusted returns.<br>
3. Performance Evaluation: Assess portfolio management strategies' effectiveness in mitigating market risk.<br>
4. Portfolio Performance Monitoring: Monitor portfolio performance over time and adjust as market conditions and risk preferences change.<br>

---

**Stock Market Risk Analysis**

In the dynamic world of investing, market risk—driven by economic events, geopolitical changes, and investor sentiment—is a key concern for investors. To make informed decisions and optimize investment strategies, it’s essential to understand how individual assets and portfolios behave in terms of risk and return.

My objective in this project was to assess the market risk associated with a portfolio of five Indian stocks over an 8-year period. The goal was to:
* Quantify historical volatility and returns,
* Identify which stocks offer the best risk-reward balance,
* And provide actionable recommendations for both investors and businesses.

Here’s how I approached it:
1. Data Understanding & Preparation:
    * I worked with weekly stock price data for five Indian companies: ITC Limited, Bharti Airtel, Tata Motors, DLF Limited, and Yes Bank.
    * The data contained 418 rows and 6 columns, covering stock prices over 8 years.
    * I converted the 'Date' column to datetime for proper time series handling.
2. Stock Price Visualization:
    * I analyzed price trends over time. For example:
        * ITC was stable until 2020, then saw a strong rise.
        * Yes Bank peaked in 2018 and collapsed afterward.
        * DLF, Tata Motors, and Bharti Airtel all showed strong upward trends post-2021.
3. Returns Calculation:
    * I calculated logarithmic returns using the natural log of price ratios.
    * This helped normalize the data and make it suitable for volatility and return analysis.
4. Statistical Analysis:
    * I calculated average returns and standard deviation (volatility) for each stock.
    * Visualized these insights with a scatter plot of Return vs. Volatility, helping identify outliers and attractive opportunities.
5. Insights & Recommendations:
    * Yes Bank showed negative returns and the highest volatility, marking it high-risk, low-reward.
    * ITC had the lowest volatility with steady positive returns—ideal for risk-averse investors.
    * DLF Limited offered the highest returns with moderate volatility, suggesting a strong risk-reward profile.
    * Tata Motors and Bharti Airtel were moderately volatile with healthy returns, making them viable growth investments.
 

**Data Dictionary**<br>
The dataset contains weekly stock price data for 5 Indian stocks over an 8-year period. The dataset enables us to analyze the historical performance of individual stocks and the overall market dynamics.
