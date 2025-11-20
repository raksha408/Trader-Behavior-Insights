# Trader Behavior Insights — Data Science Assignment

This project analyzes the relationship between **Bitcoin market sentiment** (Fear–Greed Index) and **trader performance** using Hyperliquid historical trade data.  
The goal is to uncover patterns between trader PnL, trading activity, and market emotion.

---

##  Datasets Used

### 1. Bitcoin Market Sentiment Dataset  
- Columns: `date`, `fear_greed_value`, `fear_greed_label`  
- Source: Internshala assignment link  
- Represents daily market psychology (Fear → Greed → Extreme Greed)

### 2. Hyperliquid Historical Trader Data  
- Columns include:  
  `Execution Price`, `Size USD`, `Side`, `Fee`, `Closed PnL`, `Timestamp`, etc.  
- Used to calculate daily trader activity and performance.

---

##  Steps Performed

### **1. Data Cleaning**
- Converted timestamps to proper datetime format  
- Extracted date for each trade  
- Filtered relevant columns  
- Renamed columns for readability  

### **2. Feature Engineering**
Created daily metrics:
- `daily_pnl` → sum of Closed PnL  
- `daily_volume` → sum of USD traded  
- `avg_price` → mean execution price  
- `daily_fees` → total fees paid  

### **3. Merging Both Datasets**
- Joined Hyperliquid data with Market Sentiment data  
- Merge key: `date`

---

## 📊 Visual Outputs

Below are the key charts generated from the analysis:

### **1️⃣ Daily Trader PnL vs Fear–Greed Index**
<p align="center">
  <img src="https://github.com/your-username/Trader-Behavior-Insights/blob/main/plots/Daily%20Trader%20PnL%20vs%20Fear%E2%80%93Greed%20Index.png" width="700">
</p>

### **2️⃣ Daily Trading Volume vs Market Sentiment**
<p align="center">
  <img src="https://github.com/your-username/Trader-Behavior-Insights/blob/main/plots/Daily%20Trading%20Volume%20vs%20Market%20Sentiment.png" width="700">
</p>

### **3️⃣ Time-Series Comparison**
<p align="center">
  <img src="https://github.com/your-username/Trader-Behavior-Insights/blob/main/plots/Time-Series%20Comparison.png" width="700">
</p>

### **4️⃣ Performance & Sentiment Metrics**
<p align="center">
  <img src="https://github.com/your-username/Trader-Behavior-Insights/blob/main/plots/Performance%20%26%20Sentiment%20Metrics.png" width="700">
</p>

---
##  Project Structure

This repository is organized into clear, modular folders to make the analysis easy to follow and reproduce:

### **1. README.md**
Contains the full project explanation, methodology, insights, visualizations, and instructions for running the notebook.

### **2. requirements.txt**
A list of Python libraries required to run the notebook without errors.  
Includes packages like pandas, numpy, matplotlib, seaborn, etc.

### **3. notebook/**
This folder contains the main analysis notebook:
- **trader_behavior_analysis.ipynb**  
  The complete end-to-end workflow including:
  - Data loading  
  - Cleaning & preprocessing  
  - Feature engineering  
  - Sentiment merging  
  - Visualizations  
  - Correlation and insights  

### **4. data/**
Contains sample reference datasets:
- **fear_greed_index_sample.csv**  
  Represents the Bitcoin market sentiment dataset.
- **historical_data_sample.csv**  
  Represents sample Hyperliquid trader transaction data.

*(Note: Actual raw datasets are large and not included. Only small samples are provided to illustrate structure.)*

### **5. plots/**
Includes all visual outputs generated in the notebook:
- **pnl_vs_sentiment_scatter.png** – Daily PnL vs Fear–Greed Index  
- **volume_vs_sentiment_scatter.png** – Volume vs Sentiment  
- **timeseries_pnl_sentiment.png** – Time-series comparison of PnL & sentiment  
- **correlation_heatmap.png** – Heatmap of PnL, volume, price, sentiment correlations  

Each plot directly supports insights in the analysis.

---

##  Key Insights

### **1. Sentiment and Profitability**
- Daily PnL has a **moderate negative correlation (-0.45)** with the Fear–Greed Index.  
- This suggests traders performed **better during Fear periods** than during Greed periods.

### **2. Sentiment and Trading Volume**
- Volume shows a **strong negative correlation (-0.57)** with sentiment.  
- Traders tend to take **larger positions when the market is fearful**.

### **3. Sentiment vs Avg Price**
- A mild positive correlation (+0.19) shows prices rise slightly in greed phases.

### **4. Behavioral Pattern**
- Extreme Greed days tend to coincide with **lower trading activity**.  
- Fear periods show **higher volume and sometimes higher profits**, suggesting contrarian behavior.

---

##  Tools Used
- Python  
- Pandas  
- Matplotlib  
- Seaborn  
- Google Colab  

---

---

## 📊 Visual Outputs

Below are the key charts generated from the analysis:

### **1️⃣ Daily Trader PnL vs Fear–Greed Index**
![Daily Trader PnL vs Fear–Greed Index](https://github.com/your-username/Trader-Behavior-Insights/blob/main/plots/Daily%20Trader%20PnL%20vs%20Fear%E2%80%93Greed%20Index.png)

### **2️⃣ Daily Trading Volume vs Market Sentiment**
![Daily Trading Volume vs Market Sentiment](https://github.com/your-username/Trader-Behavior-Insights/blob/main/plots/Daily%20Trading%20Volume%20vs%20Market%20Sentiment.png)

### **3️⃣ Time-Series Comparison**
![Time-Series Comparison](https://github.com/your-username/Trader-Behavior-Insights/blob/main/plots/Time-Series%20Comparison.png)

### **4️⃣ Performance & Sentiment Metrics (Correlation Heatmap)**
![Performance & Sentiment Metrics](https://github.com/your-username/Trader-Behavior-Insights/blob/main/plots/Performance%20%26%20Sentiment%20Metrics.png)

---

##  How to Reproduce
1. Clone repository  
2. Open the `Trader-Behavior-Insights.ipynb` notebook  
3. Upload both datasets to Colab  
4. Run all cells  
5. Charts and insights will be generated automatically  

---

##  Author
Shriraksha Kulkarni

  
