# Cryptocurrency Market Analysis with Google Trends

This project explores the relationship between cryptocurrency market dynamics and Google Trends data, including exploratory data analysis (EDA), correlation studies, time lag analyses, and predictive modeling. Using various machine learning models, the project aims to identify patterns, predict trends, and provide insights into cryptocurrency market behavior.

---

## Approach

### 1. **Exploratory Data Analysis (EDA)**
   - Merged fragmented datasets (20 CSV files for trends and prices) into unified datasets.
   - Cleaned data by replacing values < 1 with 0 and extracting additional date information.
   - Visualized historical trends and highlighted key periods of activity.

### 2. **Correlation Analysis**
   - Examined correlations between token prices and Google Trends scores.
   - Identified strong relationships and evaluated the implications for market sentiment and trading strategies.

### 3. **Time Lag Analysis**
   - Investigated the optimal lag between search trends and price changes using Pearson correlation coefficients.
   - Highlighted immediate and delayed impacts of trends on prices.

### 4. **Machine Learning Models**
   - Developed predictive models for Google Trends data:
     - **ARIMA**: Best performance for capturing trends and noise.
     - **SARIMA**: Extended ARIMA with seasonal adjustments but less effective for this dataset.
     - **Prophet**: Robust for handling irregularities but not outperforming ARIMA.
     - **LSTM**: Struggled due to data complexity and tuning challenges.

### 5. **Token Patterns**
   - Analyzed relationships between different cryptocurrencies.
   - Explored interdependencies and identified key influencers in the market.

---

## Requirements

To run the analysis, the following dependencies and tools are required:

### Python Libraries
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `statsmodels`
- `fbprophet` (or `prophet` for updated installations)
- `tensorflow`
- `keras`

### Additional Tools
- Jupyter Notebook for running the analysis.
- Google Colab (optional): Some steps reference Colab links for execution.

### Data Sources
- CSV files for cryptocurrency trends and prices.
- External datasets for transaction volumes and counts (optional, included in the repository).

---

## Reproducing the Results

### 1. **Setup**
   - Clone the repository:
     ```bash
     git clone https://github.com/LoznianuAnamaria/challenges.git
     cd challenges/Crypto\ Market\ -\ Impact\ of\ Google\ Trends/
     ```
   - Install dependencies:
     ```bash
     pip install -r requirements.txt
     ```

### 2. **Data Preparation**
   - Place the trend and price CSV files in the `data/` folder.
   - Run the notebook `Crypto_Market.ipynb` to merge, clean, and preprocess the datasets.

### 3. **EDA and Visualization**
   - Execute the EDA sections in the notebook to generate insights and visualizations.
   - Review trend evolution by year, month, and week.

### 4. **Correlation and Time Lag Analysis**
   - Use the respective sections to compute correlations and identify optimal time lags.
   - Visualize results to understand the impact of trends on prices.

### 5. **Model Training and Evaluation**
   - Navigate to the machine learning model section of the notebook.
   - Train ARIMA, SARIMA, Prophet, and LSTM models for trend prediction.
   - Compare model performance using MAE, MSE, and RMSE.

---

## Insights

- Strong positive correlations exist between search trends and token prices for major cryptocurrencies.
- Time lags of 1 week are optimal for most tokens, with some exceptions showing delayed impacts.
- ARIMA models provide the best results for forecasting Google Trends data in this study.

---
