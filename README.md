# Traffic_Volume_Prediction
Traffic Volume Prediction; is a Data Science project that forecasts hourly traffic counts using weather and time features. It combines LightGBM and XGBoost with feature engineering and is deployed via Gradio for interactive real‑time predictions.

## 📌 Overview
This project predicts hourly traffic volume using weather and time features.  
We built an ensemble model (**LightGBM + XGBoost**) with feature engineering, hyperparameter tuning, and deployment via Gradio.

---

## 📂 Dataset
- **Source:** Metro Interstate Traffic Volume dataset  
- **Features:** Hour, day of week, temperature, rain, snow, holiday/weekend indicators  
- **Target:** Traffic volume (vehicle count per hour)

---

## ⚙️ Workflow
1. **Data Preprocessing**
   - Missing value handling  
   - Feature scaling and encoding  

2. **Exploratory Data Analysis (EDA)**
   - Traffic trends by hour/day  
   - Weather impact on traffic  

3. **Feature Engineering**
   - Lag features (lag_1, lag_2, lag_3)  
   - Rolling mean & std  
   - Cyclical time features (hour_sin, hour_cos)  

4. **Model Building**
   - LightGBM and XGBoost models  
   - Ensemble blending (55% LightGBM, 45% XGBoost)  

5. **Hyperparameter Tuning**
   - Optuna optimization for best parameters  

6. **Evaluation**
   - Metrics: R², MAE, RMSE  
   - Plots: Actual vs Predicted, Residuals, Feature Importance  

7. **Deployment**
   - Gradio app in Google Colab  
   - Interactive UI for predictions  

---

## 📊 Results
| Metric   | Value   |
|----------|---------|
| R² Score | 0.986   |
| MAE      | 150.9   |
| RMSE     | 229.8   |

- **Actual vs Predicted:** Strong alignment  
- **Residuals:** Centered around zero, no bias  
- **Feature Importance:** Lag features and cyclical encodings were most influential  

---

## 🚀 Deployment
-Originally, the project deliverables mentioned a Flask web application.  
However, since Flask servers face tunneling and blocking issues in Google Colab, we deployed the model using **Gradio** instead.  

Gradio provides:
- An interactive web interface directly in Colab.
- A shareable `.gradio.live` link for testing and demonstration.
- Simplified integration without additional server setup.
- **Gradio App:** Interactive interface for predictions  
- **Demo Link:** [https://06be4e819d29486a7b.gradio.live](https://06be4e819d29486a7b.gradio.live)  

---

## 📈 Insights
- Peak traffic occurs during morning and evening rush hours.  
- Weather (rain/snow) reduces traffic volume.  
- Lag features capture temporal dependencies effectively.  

---

## 🔮 Future Improvements
- Flask/REST API deployment on cloud (Heroku/Render).  
- Real‑time data ingestion from sensors.  
- Dashboard integration for visualization.
