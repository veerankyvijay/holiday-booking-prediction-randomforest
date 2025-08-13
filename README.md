# holiday-booking-prediction-randomforest
✈️ Holiday Booking Prediction using Random Forest This project builds a machine learning model to predict whether a customer will book a holiday package based on their booking and travel behavior. The dataset contains historical customer booking data, and the aim is to help travel/airline companies identify potential customers
# ✈️ Holiday Booking Prediction using Random Forest

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-1.3+-yellow.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

## 📌 Project Overview
This project predicts whether a customer will **book a holiday** based on their booking and travel behavior.  
Using historical customer booking data, the model helps travel and airline companies **identify potential customers before they make a purchase decision**.

We implemented a **Random Forest Classifier** for prediction and evaluated the model using metrics like **Accuracy, Precision, Recall, F1-score**, and a **Confusion Matrix**.

---

## 🎯 Objectives
- Preprocess and clean raw customer booking data.
- Train and evaluate a Random Forest model.
- Interpret results and draw actionable insights.
- Visualize performance metrics and feature importance.

---

## 📂 Dataset
The dataset contains customer booking records with features like:
- Demographic details
- Travel dates
- Booking patterns
- Destination preferences

*(Dataset is available in `/data` folder — `customer_booking.csv`)*

---

## 🛠 Tech Stack
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
- **Model:** Random Forest Classifier  

---

## 📊 Results & Insights
- Model is **more accurate in detecting non-buyers** than buyers.
- **High false positives** → potential for marketing budget waste.
- Good **recall for buyers** → fewer missed potential customers.
- Accuracy can be improved with:
  - **Hyperparameter tuning**
  - **Feature engineering**
  - **Balancing the dataset**

---

## 📈 Model Performance

| Metric        | Score |
|---------------|-------|
| Accuracy      | 0.70  |
| Precision     | 0.93  |
| Recall        | 0.71  |
| F1-score      | 0.42  |



---

## 📊 Visualizations
- Confusion Matrix  
- Feature Importance Plot  
- Accuracy/Recall Comparison  

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/holiday-booking-prediction-randomforest.git
   cd holiday-booking-prediction-randomforest
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run the Jupyter Notebook:

bash
Copy
Edit
jupyter notebook holiday_booking_prediction.ipynb
📌 Future Improvements
Add more features from external data sources.

Experiment with Gradient Boosting, XGBoost, and LightGBM.

Use cross-validation for more robust performance metrics.
