# Financial Market Prediction and Investment Strategy Optimization Using Machine Learning

<img width="861" alt="image" src="https://github.com/user-attachments/assets/a266f09c-1eb3-40ab-8089-9f7d2e70a87c" />

A Data-Driven Approach to Financial Market Prediction and Investment Strategy Optimization

# 🧠 Project Overview

This project combines technical stock analysis and fundamental financial assessment using advanced machine learning techniques. By analyzing past market performance, financial statements, and risk profiles, we aim to:

* Forecast future stock price movement (one-step and multi-step horizons).

* Provide actionable investment recommendations based on model outputs.

* Support Prime INC's shift toward automated, data-driven decision-making.
  

# 🏢 Business Context

A globally recognized investment firm known for its strategic interest in emerging markets delivers flexible and technology-driven investment solutions tailored to diverse client profiles. However, after missing key investment opportunities in the previous quarter due to delayed and inefficient decision-making, Prime INC is looking to integrate machine learning to drive predictive insights and optimize stock portfolio strategies.

# 🎯 Business Problem
Prime INC seeks to overcome limitations in traditional investment analysis by embracing data-driven methods. The key challenge is:

**"How can we accurately predict the direction of stock prices to identify profitable investment opportunities and reduce risk?"**

❗Specific Obstacles
 * **Missed Opportunities:** Delayed analysis led to lost high-return opportunities.

 * **Lack of Predictive Models:** No reliable mechanism to forecast stock price direction.

 * **Complex Financial Interpretation:** Difficulty extracting insight from financial statements.

 * **Unquantified Risks:** Limited understanding of volatility and exposure in prospective assets.

# 📌 Project Objectives

* Analyze high-potential stocks from Prime INC's portfolio.

* Benchmark these stocks against major indices such as S&P 500 and FTSE 100.

* Compare performance between NVDA (NVIDIA) and QUBT (Quantum Computing Inc.) — two firms under consideration for future investment.

* Measure:

  * 📊 Volatility & Risk

  * 🔄 Correlation with Market Indices

  * 💰 Market Capitalization

  * 📈 Stock Price Trend & Direction

# Data Description

* Data Sources: The Stock price data and the company Financials  were sourced from Yahoo Finance API (yfinance) which covered the period of 14 years (02/01/2010 to 30/12/2024).

These features are derived from historical stock prices;

* Date: Timestamp of the stock price data.
* Open Price: Opening price of the stock on a given day.
* High Price: Highest stock price during the trading day.
* Low Price: Lowest stock price during the trading day.
* Close Price: Final price of the stock at market close.
* Adjusted Close Price: Closing price adjusted for stock splits and dividends.
* Volume: Total number of shares traded in a day.

# Stock Market Analysis

An analysis of stock returns over time highlights significant differences in performance between NVDA and QUBT, including their return trends, stock movement distribution, and adjusted closing prices. Additionally, stock volatility and a comparative study with the S&P 500—using both correlation and regression analysis—offer deeper insights into how these stocks behave relative to the broader market.

  * **NVDA:**

 <img width="725" alt="image" src="https://github.com/user-attachments/assets/05502c86-9c17-4358-b595-10b6263bbb14" />


Figure 1. Nvidia Returns, Stock Direction Distribution and Adjusted Closing Prices 

  * **QUBT:**


    <img width="725" alt="image" src="https://github.com/user-attachments/assets/30e67002-4066-407e-b881-e8fe8491eba0" />

Figure 2. Quantum Returns, Stock Direction Distribution and Adjusted Closing Prices 


  <img width="502" alt="image" src="https://github.com/user-attachments/assets/88c09486-f13d-4b47-9764-f61110bce381" />

Figure 3. Stock Market Analysis Summary 


**🔍 Key Takeaways:**

 * **NVDA (NVIDIA Corporation):**

    * Profile: A stable, blue-chip growth stock with relatively low average volatility (2.62%), appealing to long-term investors.

    * Market Sensitivity: Strongly correlated with the S&P 500 (r = 0.62), making it responsive to macroeconomic conditions.

    * Predictability: Returns are more aligned with overall market trends, enhancing its suitability for predictable, steady growth strategies.

 * **QUBT (Quantum Computing Inc.)**

    * Profile: A highly volatile (16.93%) and speculative stock with weak correlation to the S&P 500 (r = 0.03), suggesting minimal market dependency.

    * Risk-Reward Nature: Ideal for high-risk, short-term traders aiming for potentially large gains from unpredictable price swings.

    * Diversification Potential: Due to its market independence, QUBT can serve as a portfolio diversifier when paired with more stable assets.

**Portfolio Strategy Implication** 

  * Balanced Exposure: Combining NVDA (for stability) with QUBT (for speculation) offers a blend of growth and diversification.

  * Risk Management: NVDA mitigates portfolio risk, while QUBT introduces upside potential for risk-tolerant segments.


# Predictive Modelling of Future Stock Direction

To forecast future stock movements, we will create technical indicators to analyze its stock price movement and enhance prediction accuracy and we employed various time series.

  * Technical Indicators:
    
    1. Relative Strength Index (RSI): Measures momentum to determine if a stock is overbought or oversold.

    2. Moving Average Convergence Divergence (MACD): Analyzes trend strength and momentum using moving averages.

    3. Price Rate of Change (ROC): Tracks the speed of price movements to gauge momentum.

## Features Selection and Dimensionality Reduction with PCA for Best Prediction:

   We used some models Correlation Matrix Heatmap and PCA to determine the best features to use for our prediction which are:- MACD, RSI, Price_ROC, Returns, Returns_sp500, Volatility, and Volume indicating they provide independent and useful information.

## Model Selection, Building, Training and Evaluation

Thereafter, we will use a combination of machine learning (ML) models, and deep learning (DL) models to predict stock price movements, for example,- KNN Classifier, Decision Tree, Random Forest, XGBoost, SVM (Support Vector Machine), Logistic Regression and LSTM (Long Short-Term Memory) and mlflow model tracking experiment to capture the metrics

The results are show below:

<img width="438" alt="image" src="https://github.com/user-attachments/assets/da8fe2d6-d4f4-4537-923d-d8d90cbea8b7" />

Figure 4. Models Evaluation Results 

Predicting stock movement is noisy and very hard, especially at daily resolution. A 50–55% accuracy is common baseline.

* Best Models: For this analysis, the two(2) models that did fairly well are: 
  
  * LSTM: Best accuracy (53.8%) but very low precision (29%). This means it predicts a lot of false positives.

  * SVC: 52.6% accuracy and highest precision. Best trade-off overall.
    
# Fundamental Analysis- NVIDIA

  * Profitability: Revenue & Net Income
    
<img width="734" alt="image" src="https://github.com/user-attachments/assets/e90f55e6-bc73-441c-8a3c-ebe0f05a5cbd" />

Figure 5. Revenue & Net Income

The Net profit margin recovered dramatically in 2024, showing strong earnings efficiency and growth and 2024 profit surge reflects its dominance in high-growth sectors like AI and data centers.

  * Leverage Risk: Capital Structure
    
<img width="770" alt="image" src="https://github.com/user-attachments/assets/a6d9ba7b-61f7-4414-a5e2-1680ce314cd3" />

Figure 5. Capital Structure

The Low and decreasing leverage indicates strong balance sheet and low financial risk.

# Reporting & Investment Strategy

Based on an integrated analysis of NVDA’s stock performance and financial fundamentals (2021–2024), the following strategic insights are recommended for Prime INC:

* Key Insights
1. Financial Turnaround in 2024
   NVIDIA delivered an extraordinary turnaround, growing revenue by ~4.8x and net income by over 14x from 2023 to 2024. Margins and efficiency ratios hit 
   historical highs.

2. Operational Efficiency & Low Leverage
   Consistently strong current ratios and declining debt-to-equity indicate robust liquidity and prudent capital management.

## Portfolio Recommendations

<img width="544" alt="image" src="https://github.com/user-attachments/assets/d905a82d-f938-40cb-97ed-89cf228d9e25" />

Figure 5. Portfolio Recommendations
