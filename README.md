# Trader-Sentiment-Performance-Analysis

### 📊 **Trader Performance vs Bitcoin Market Sentiment**

This project analyzes the relationship between trader behavior and Bitcoin market sentiment using historical execution data and the Fear-Greed Index.

---

### 📁 **Datasets Used**

1. **Bitcoin Market Sentiment**

   * Columns: `timestamp`, `value`, `classification`, `date`
   * Source: Fear-Greed Index for Bitcoin

2. **Hyperliquid Historical Trader Data**

   * Columns: `account`, `coin`, `execution price`, `size tokens`, `side`, `timestamp ist`, `closed pnl`, `fee`, `start position`, etc.

---

### 🔧 **Project Objective**

To explore how market sentiment (Fear/Greed) impacts:

* 📈 Trader profitability (Closed PnL)
* ⚖️ Leverage usage
* ✅ Win rate
* 💰 Trading fees

---

### 🧠 **Steps Performed**

1. **Data Preprocessing**

   * Converted date/time columns to datetime format
   * Merged both datasets on date

2. **Feature Engineering**

   * Calculated custom `leverage = abs(start_position) / execution_price`
   * Generated binary win/loss flag from `Closed PnL`

3. **Exploratory Data Analysis**

   * Plotted:

     * Average PnL by sentiment
     * Win rate by sentiment
     * Avg leverage by sentiment
     * Avg trading fee by sentiment
     * Number of trades per sentiment

---

### 📊 **Key Insights**

* 🟢 Traders tend to have **higher PnL and win rates during Greed/Extreme Greed**.
* 🔴 Leverage usage remains high during both Fear and Greed.
* ⚖️ Average fee doesn’t vary much across sentiment types.

---

### 💻 **Technologies Used**

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Jupyter Notebook

---

### 📂 **How to Run**

1. Clone or download the repository.
2. Place both CSV files in the working directory.
3. Run `trader_sentiment_analysis.ipynb` in Jupyter.
4. All plots and outputs will be generated in the notebook.

---
