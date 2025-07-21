# Failed-Insights

# Failed Orders Insights – Gett Matching Analysis

This project analyzes “failed” orders in the Gett ride-hailing system to uncover patterns in cancellations and rejections. Gett (formerly GetTaxi) is a corporate transportation management platform where clients request rides and drivers accept offers. Here we focus on orders that never completed—either cancelled before or after driver assignment, or outright rejected by drivers.

## 📁 Dataset

- Source: Internal Gett ride logs used in their Data Science take-home assignment  
- Format: CSV with order records, timestamps, failure reasons, driver assignment status, etc.

## 🔍 Analysis Tasks

1. **Failure Reason Distribution**  
   - Categorize each failed order as:  
     - Cancelled **before** driver assignment  
     - Cancelled **after** driver assignment  
     - Driver **rejection**  
   - Plot counts and highlight the category with the highest failures.

2. **Hourly Failure Trends**  
   - Aggregate failed orders by hour of day  
   - Visualize which hours see spikes in particular failure types  
   - Interpret patterns (e.g., peak commute times, late-night cancellations)

3. **Average Time to Cancellation**  
   - Compute time from order creation to cancellation for with-driver vs. without-driver cases  
   - Compare mean/median times and test for significance

## 🧹 Data Cleaning & Preparation

- Parsed timestamps into datetime and extracted `order_hour`  
- Dropped incomplete or malformed records  
- Standardized failure reason labels  
- Handled missing driver assignments by flagging “no-driver” cancellations

## 🛠️ Skills & Tools

Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook, Exploratory Data Analysis

## 📦 Outputs

- Cleaned dataset: `failed_orders_cleaned.csv`  
- Plots:  
  - Bar chart of failure reason counts  
  - Line plot of hourly failure distribution  
  - Boxplots/comparison of cancellation times  

## 📈 Next Steps

- Drill into geographic or client-level patterns  
- Build a predictive model to flag high-risk orders in real time  
- Integrate driver availability data to optimize matching algorithms  
