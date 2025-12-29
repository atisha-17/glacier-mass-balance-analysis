# Global versus Indian Glacier Mass Balance Trends: A WGMS-Based Assessment

**Submitted by:** Atisha Mehta

**Project Supervisor:** Mr. Manoj Kumar

**Case Study:** Chhota Shigri Glacier, India

## Project Overview
This research investigates glacier mass balance trends across continents and India using datasets from the **World Glacier Monitoring Service (WGMS)** and **The Cryosphere**. The study performs a quantitative analysis of long-term data to detect patterns of accelerated melting, with a specific focus on the vulnerability of the **Chhota Shigri Glacier** in the Himalayas.

## Key Objectives
* **Comparative Analysis:** Analyze and compare mass balance trends between global and Indian datasets.
* **Vulnerability Mapping:** Identify regions most susceptible to accelerated glacier melting.
* **Predictive Modeling:** Utilize Machine Learning (XGBoost and LSTM) to capture temporal trends and non-linear variations in glacier melt.
* **Resource Management:** Provide insights for sustainable glacier and water resource management.

## Data Acquisition & Preprocessing
The study utilizes two primary data sources:
1. **WGMS Dataset:** Global historical records from 1880 to recent years, covering 800+ glaciers.
2. **Chhota Shigri Dataset:** Reanalysis of the longest mass balance series in the Himalayas (2002–2023).

### Preprocessing Steps:
* **Handling Missing Data:** Linear interpolation was used to handle missing values.
* **Stationarity Testing:** Performed the Augmented Dickey-Fuller (ADF) test (Statistic: -2.0088, p-value: 0.2827).
* **Feature Engineering:** Calculated lag features, rolling means, and standard deviations to capture historical influence on mass balance.
* **Differencing:** Applied first-order differencing to remove seasonality and make the series stationary.

## Machine Learning Models
Two primary models were implemented and compared:
* **XGBoost (Extreme Gradient Boosting):** Efficiently handles non-linear relationships and multivariate time-dependent variables.
* **LSTM (Long Short-term Memory):** Specifically built to capture long-term temporal dependencies and sequential patterns in time-series data.
**Training Configuration:** Models were trained for 100 epochs using the **Adam optimizer** with adaptive learning rates.

## Results & Performance Evaluation
The performance was evaluated using Mean Squared Error (MSE) and Mean Absolute Error (MAE). **LSTM** consistently outperformed XGBoost across all datasets.

### Model Comparison Table
| Dataset | Best Model | MSE | MAE |
| --- | --- | --- | --- |
| **Chhota Shigri (Local)** | LSTM | 0.0510 | 0.1840 |
| **Regional (India & Neighbors)** | LSTM | 0.0510 | 0.1840 |
| **Global Dataset** | LSTM | 0.2862 | 0.3383 |

### Final Analysis
* **Global Trend:** Shows a gradual decline, smoothed by averaging various climates worldwide.
* **India Trend:** Displays a steeper decline than global averages, reflecting the vulnerability of Himalayan glaciers.
* **Chhota Shigri:** Exhibits the sharpest and most volatile decline due to local climatic sensitivity (monsoon and temperature rise).

## Conclusion
This study confirms accelerated glacier mass loss at global, national, and regional scales. While global trends show a steady decline, the Himalayan region—specifically Chhota Shigri—shows a much sharper and erratic decrease. These findings highlight the urgent need for climate adaptation strategies and sustainable tourism practices to preserve vital water resources.

## Technologies Used
* **Languages:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, TensorFlow, Keras.
* **Environment:** Google Colab.
  
## References
1. M. F. Azam et al., "Reanalysis of the longest mass balance series in Himalaya using a nonlinear model: Chhota Shigri Glacier (India)," *Cryosphere*, 2024.
2. L. Jakob and N. Gourmelen, "Glacier Mass Loss Between 2010 and 2020 Dominated by Atmospheric Forcing," *Geophys. Res. Lett.*, 2023.
3. World Glacier Monitoring Service (WGMS).
