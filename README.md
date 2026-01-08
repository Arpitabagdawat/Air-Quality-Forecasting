# Air Quality Index Prediction & Forecasting

This project analyzes and forecasts air quality data using the **UCI Air Quality Dataset**.  
The dataset contains hourly averaged responses from an array of chemical sensors deployed in an Italian city.

The main objective of this project is:
- To clean and preprocess real-world air quality data
- Handle missing values correctly
- Perform time-series forecasting using **Facebook Prophet**

---

## 📊 Dataset Information

- **Source:** UCI Machine Learning Repository  
- **Dataset Name:** Air Quality Dataset  
- **Time Period:** March 2004 – April 2005  
- **Frequency:** Hourly data  

### Important Dataset Characteristics
- Values are separated using `;`
- Decimal values use **comma ( , )** instead of dot
- Missing values are encoded as **-200**
- Last rows contain only null values

---

## 🧹 Data Preprocessing Steps

1. Loaded dataset using:
   - `sep=';'`
   - `decimal=','`
2. Removed extra empty columns
3. Removed trailing rows containing only null values
4. Replaced `-200` with `NaN`
5. Filled missing values using **column-wise mean**
6. Converted `Date` and `Time` into a single **datetime column**
7. Prepared dataset in Prophet-compatible format:
   - `ds` → datetime
   - `y` → target variable (Relative Humidity)

---

## 🕒 Time-Series Preparation

- Converted date format from `DD/MM/YYYY` to `YYYY-MM-DD`
- Converted time from `HH.MM.SS` to `HH:MM:SS`
- Combined Date and Time into a single datetime column
- Final dataframe structure:

  ds → DateTime
y → Relative Humidity (RH)


---

## 🤖 Forecasting Model

- **Algorithm Used:** Facebook Prophet
- **Forecast Horizon:** 365 hours (hourly frequency)
- **Target Variable:** Relative Humidity (RH)

### Model Steps
1. Trained Prophet model on historical data
2. Generated future timestamps
3. Predicted future RH values
4. Visualized:
 - Forecast trend
 - Seasonality components

---

## 📈 Results & Visualization

The model outputs:
- `yhat` → Predicted value
- `yhat_lower` → Lower confidence interval
- `yhat_upper` → Upper confidence interval

Visualizations include:
- Overall forecast plot
- Trend, daily and yearly seasonality components

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Facebook Prophet

---

## 📂 Project Structure


---

## 🚀 Future Enhancements

- Forecast other air quality parameters (CO, NOx, NO2)
- Use advanced imputation techniques
- Compare Prophet with ARIMA / LSTM models
- Deploy the model as a web application

---

## 👩‍💻 Author

**Arpita Bagdawat**  
Data Science & Analytics Enthusiast  

---

## ⭐ Acknowledgements

- UCI Machine Learning Repository  
- Facebook Prophet Documentation

 
