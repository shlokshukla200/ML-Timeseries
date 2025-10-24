# ⏳ Time Series Decomposition & Moving Averages using Python

📈 **A hands-on demonstration of time series analysis techniques — including additive decomposition, trend extraction, and moving averages (SMA & EMA) — using Python and Statsmodels.**  
This project uses a synthetic dataset to showcase how trends and seasonality can be separated from noise.

---

## 🧩 What is Time Series Decomposition?

**Time Series Decomposition** is a statistical method that breaks down a time series into three components:
1. **Trend** 📉 — Long-term movement or direction of data  
2. **Seasonality** 🔁 — Regular patterns repeating over fixed intervals  
3. **Residuals** 🔍 — Random noise or irregular fluctuations  

This helps better understand and model temporal data.

---

## 🏗️ Project Structure

├── time_series_decomposition.py # Main script
├── README.md # Project documentation

yaml
Copy code

---

## ⚙️ Libraries Used

- 🧮 **NumPy** — for mathematical operations  
- 📊 **Pandas** — for time series data manipulation  
- 🎨 **Matplotlib** — for data visualization  
- 🧠 **Statsmodels** — for time series decomposition  

---

## 🚀 Implementation Overview

### 1️⃣ Generate Synthetic Time Series
A daily dataset is created for one year, combining a **sinusoidal seasonal pattern** with random noise:
```python
data = np.sin(np.arange(365) * 2 * np.pi / 365) + np.random.normal(0, 0.5, 365)
2️⃣ Visualize the Time Series
Plot the generated series to observe the overall pattern and noise:

python
Copy code
plt.plot(ts, label='Original Time Series')
3️⃣ Apply Additive Decomposition
Use seasonal_decompose from Statsmodels to separate trend, seasonality, and residual components:

python
Copy code
result_add = seasonal_decompose(ts, model='additive')
4️⃣ Plot Components
Visualize the trend and seasonal components individually for deeper insights.

5️⃣ Compute Moving Averages
Simple Moving Average (SMA) — 7-day rolling mean

Exponential Moving Average (EMA) — 30-day weighted moving mean
Both are plotted alongside the original data.

💻 Example Visualization
The plots generated include:

🟢 Original Time Series

🔵 Additive Trend

🟠 Seasonal Component

🔴 7-Day SMA and 30-Day EMA

Each reveals a unique perspective of how the time series behaves over time.
