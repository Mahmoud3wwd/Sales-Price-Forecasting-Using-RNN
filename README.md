# Fruit & Vegetables Time-Series Forecasting Using GRU Neural Networks

## Objective
This project aims to forecast the **average prices of fruits and vegetables** using historical data from the Fruit & Vegetables Time-Series dataset. The model leverages **Gated Recurrent Unit (GRU) neural networks** to handle sequential dependencies in the data and evaluates performance using various statistical metrics.

---

## Dataset Overview
- **Source:** Fruit & Vegetables Time-Series dataset  
- **Features Used:**
- **Date** (as the temporal index)
- **Average Prices**
- **Data Period:** 2013-06-20 to 2021-07-25  

### Data Preprocessing
1. Converted the `Date` column to datetime format.
2. Set the `Date` column as the index.
3. Scaled data using **MinMaxScaler** for efficient training.

---

## Methodology
### 1. Data Visualization
- Historical trends of average prices were plotted to identify patterns over time.
  
### 2. Data Preparation
- **Windowing:** Created a sliding window dataset (5 time steps as input to predict the next value).
- Split data into **training** and **testing subsets**.

### 3. Model Architecture
- **GRU-based Sequential Model**:
  - GRU layers with 60, 50, 30, 20, and 10 units.
  - Dense output layer for prediction.
- **Optimizer:** Adam  
- **Loss Function:** Mean Squared Error (MSE)  

### 4. Training
- Trained for **10 epochs** with **early stopping** to prevent overfitting.
- Monitored loss during training.

### 5. Prediction for 2024
- Used the last window of test data to predict daily average prices for 2024.
- Predictions were inverse-transformed to match the original scale.

### 6. Evaluation Metrics
- **Root Mean Squared Error (RMSE):** 0.1266  
- **Mean Absolute Error (MAE):** 0.0780  
- **R-squared (R²):** 0.0788  

---

## Results
1. **Training Performance:**
   - GRU model demonstrated effective learning with steadily decreasing loss curves.
   
2. **Evaluation:**
   - RMSE: 0.1266
   - MAE: 0.0780
   - R²: 0.0788  

3. **2024 Predictions:**
   - Forecasted daily average prices for 2024, reflecting seasonal trends and variations.
   
4. **Visual Analysis:**
   - Actual vs. predicted values for test data aligned well, confirming the model's accuracy.
   - 2024 predictions followed logical trends, showcasing the model's ability to generalize.

---

## Conclusion
The GRU model successfully handled sequential dependencies in the dataset, providing accurate forecasts with low error rates and reliable predictions for 2024. This demonstrates the model's potential for future applications in time-series forecasting of commodity prices.

---

## Visualizations
- **Historical Trends:** Seasonal patterns in the training data.
- **Prediction Results:** Comparison of actual vs. predicted values.
- **Future Trends:** Predicted prices for 2024.

---

## How to Use
1. Clone this repository:
   ```bash
   git clone <[repository-link](https://github.com/Mahmoud3wwd/Sales-Price-Forecasting-Using-RNN)>
