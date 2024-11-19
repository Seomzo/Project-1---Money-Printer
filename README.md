# Money-Printer

In today's volatile cryptocurrency market, understanding trends and making accurate predictions are invaluable for investors and analysts alike. This project aims to develop an application for analyzing and predicting cryptocurrency trends by performing correlation analysis and predictive modeling.

![Cryptocurrency Trends](images/cryptocurrency_trends.png)

## Table of Contents

- [Money-Printer](#money-printer)
  - [Business Understanding](#business-understanding)
  - [Data Understanding](#data-understanding)
  - [Data Analysis](#data-analysis)
    - [Correlation Analysis](#correlation-analysis)
  - [Predictive Modeling](#predictive-modeling)
    - [Data Segmentation](#data-segmentation)
    - [Model Testing](#model-testing)
    - [Future Predictions](#future-predictions)
  - [Visualization](#visualization)
  - [Conclusion and Future Work](#conclusion-and-future-work)
  - [Project Presentation](#project-presentation)
    - [Team Members (Slide 1)](#team-members-slide-1)
    - [Project Overview (Slide 2)](#project-overview-slide-2)
    - [Goals and Questions Addressed (Slide 3)](#goals-and-questions-addressed-slide-3)
    - [Data Analysis Requirements (Slide 4)](#data-analysis-requirements-slide-4)
    - [Approach Taken to Achieve Goals (Slide 5)](#approach-taken-to-achieve-goals-slide-5)
    - [Results and Conclusions](#results-and-conclusions)
      - [Phase 1: Price Prediction Dashboard (Slide 6)](#phase-1-price-prediction-dashboard-slide-6)
      - [Phase 2: Correlation Analysis (Slide 7)](#phase-2-correlation-analysis-slide-7)
      - [Accuracy Testing (Slide 8)](#accuracy-testing-slide-8)
    - [Summary of Key Questions Answered (Slide 9)](#summary-of-key-questions-answered-slide-9)
    - [Problems Encountered (Slide 10)](#problems-encountered-slide-10)
    - [Future Considerations (Slide 11)](#future-considerations-slide-11)
  - [For More Information](#for-more-information)
  - [Repository Structure](#repository-structure)

---

## Business Understanding

The cryptocurrency market is known for its high volatility and the complex interplay between different coins. By identifying correlations and applying predictive models, we can gain insights into market dynamics and potentially forecast future trends. This application will enable users to analyze relationships between cryptocurrencies and make informed predictions about their prices.

## Data Understanding

To conduct a thorough analysis, reliable and comprehensive data is essential. We will collect historical data on various cryptocurrencies, including price, trading volume, and market capitalization, from reputable sources such as [CoinMarketCap](https://coinmarketcap.com/) and [CoinGecko](https://www.coingecko.com/). The data will be cleaned and preprocessed to ensure consistency and accuracy for analysis.

## Data Analysis

### Correlation Analysis

We will perform correlation analysis by comparing data from two or more cryptocurrencies to identify potential relationships. This involves:

- **Calculating correlation coefficients** (e.g., Pearson or Spearman) between cryptocurrency price movements.
- **Analyzing lagged correlations** to see if movements in one coin predict movements in another.
- **Visualizing** the correlations using heatmaps and interactive graphs to identify significant relationships.

![Correlation Heatmap](images/correlation_heatmap.png)

## Predictive Modeling

### Data Segmentation

To assess the predictive power of our models, we will:

- **Split historical cryptocurrency data** into training and validation sets.
- **Use the training set** to build and train machine learning models.
- **Validate the models** by comparing predictions against the validation set.

### Model Testing

We will experiment with various machine learning models suitable for time series forecasting, such as:

- **Linear Regression**
- **ARIMA (AutoRegressive Integrated Moving Average)**
- **LSTM (Long Short-Term Memory) neural networks**
- **Transformer models**

We will evaluate the models using metrics like **RMSE (Root Mean Squared Error)** and **MAE (Mean Absolute Error)** to determine their accuracy.

### Future Predictions

If the models demonstrate acceptable accuracy, we will use them to predict future cryptocurrency prices. We will also provide confidence intervals to represent prediction uncertainty.

![Prediction vs Actual](images/prediction_vs_actual.png)

## Visualization

Visualization plays a crucial role in understanding data and communicating insights. We will develop interactive dashboards and charts to:

- **Display correlation heatmaps** between different cryptocurrencies.
- **Show historical trends** using line graphs and candlestick charts.
- **Compare model predictions with actual data** using overlay plots.
- **Visualize prediction confidence intervals**.
- **Allow users to interact with the data** by selecting date ranges, coins, and other parameters.

![Interactive Dashboard](images/interactive_dashboard.png)

## Conclusion and Future Work

This project aims to provide a powerful tool for analyzing and predicting cryptocurrency trends. By combining correlation analysis with predictive modeling, users can gain valuable insights into market dynamics. In the future, we plan to:

- **Incorporate more advanced models** and techniques to improve prediction accuracy.
- **Expand the application** to include real-time data updates.
- **Integrate additional features** such as sentiment analysis from social media.

---

## Project Presentation

### Team Members (Slide 1)

- **Avineet Sharma**
- **Omar Alsadoon**
- **Vinayak Grover**
- **Natasha Anghelescu**
- **Daniel Levy**

### Project Overview (Slide 2)

#### Money-Printer: Cryptocurrency Correlation & Prediction Tool

**Objective**:

To uncover meaningful patterns in cryptocurrency price movements through predictive modeling and correlation analysis, enabling data-driven trading decisions.

**Unique Value Proposition**:

- Simplifies complex cryptocurrency market data into clear predictions and correlations.
- Empowers users with actionable insights derived from advanced data analytics.
- Reduces trading uncertainty by leveraging historical trends for informed decision-making.
- Intuitive interface for users to analyze asset interactions and make better investment choices.

_"Transforming complex data into actionable trading strategies."_

### Goals and Questions Addressed (Slide 3)

1. **Can a simple machine learning model leverage historical price data to accurately forecast future cryptocurrency prices?**
2. **Do cryptocurrency prices show a correlation, and to what degree do they move together?**

### Data Analysis Requirements (Slide 4)

#### Data Sources

- **Yahoo Finance API**: Real-time cryptocurrency data, including price, volume, and market cap.

#### Correlation Metrics

- **Pearson/Spearman correlation**
- **Thresholds for significance and lagged correlations**

### Approach Taken to Achieve Goals (Slide 5)

The project was divided into two main components:

#### 1. Price Prediction Model

- Users input a cryptocurrency, start date, and slice date.
- Utilized regression analysis to predict future prices based on historical trends.
- Generated actionable buy/sell recommendations to inform user decisions.

#### 2. Correlation Analysis

- Allowed users to input two cryptocurrencies and a specific time frame.
- Performed correlation analysis to measure and interpret the degree of relationship between the selected assets.

### Results and Conclusions

#### Phase 1: Price Prediction Dashboard (Slide 6)

- **Result**: The regression model successfully predicted cryptocurrency prices with good accuracy.
- **Visualization**: A line graph showing the current price of Bitcoin (BTC).
- **Visualization**: A Prophet model predicting BTC's future price up to 3 years.

#### Phase 2: Correlation Analysis (Slide 7)

- **Result**: Identified meaningful correlations between cryptocurrencies.
- **Visualization**: Heatmap displaying correlation coefficients between selected cryptocurrencies and index funds.
- **Visualization**: Line graph showing side-by-side normalized price trends of two cryptocurrencies.

#### Accuracy Testing (Slide 8)

- **Result**: Tested the accuracy of the Prophet Model on historical data, effectively predicting historical price movements.

### Summary of Key Questions Answered (Slide 9)

1. **Can a machine learning model predict cryptocurrency prices?**

   - **Answer**: Yes, with good accuracy for shorter time frames.

2. **Are cryptocurrency prices correlated?**

   - **Answer**: Yes, but results improved after resolving an issue with the `.pct_change()` function.

   **Problem**: Initial correlation data was less correlated than expected.

   **Solution**: Removed the duplicate `.pct_change()` function to get more realistic results.

### Problems Encountered (Slide 10)

1. **Prediction Uncertainty**:

   - **Problem**: Predictions became more uncertain the further out the model forecasted.
   - **Solution**: Limited predictions by adding a slice date window for better accuracy.

### Future Considerations (Slide 11)

1. **Dynamic Model Inputs**:

   - Make the model more dynamic by allowing user inputs for cryptocurrency and date range.

2. **Advanced Predictive Algorithms**:

   - Use a more advanced predictive algorithm that incorporates more variables than just price points.

Additional questions and research plans could include further optimization of correlation metrics and predictive modeling.

---

## For More Information

For any inquiries or further information about the project, please contact the team members or visit our repository.

## Repository Structure

- `data/`: Contains the datasets used for analysis.
- `notebooks/`: Jupyter notebooks with data analysis and modeling code.
- `images/`: Visual assets used in the README and documentation.
- `src/`: Source code for the application and models.
- `README.md`: Project documentation and overview.

---

By adding slide numbers to each relevant section in the "Project Presentation," we've aligned the README with your presentation slides for better reference and coherence.

