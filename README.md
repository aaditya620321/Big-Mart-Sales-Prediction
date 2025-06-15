# 🛒 Big Mart Sales Prediction Using Machine Learning

A complete end-to-end Machine Learning project that predicts the sales of various products across Big Mart outlets. It includes data preprocessing, model building, evaluation, feature importance analysis, deployment using Joblib, and a GUI application using Tkinter.

---

## 📌 Project Overview

This project aims to predict the **sales of products** at different Big Mart outlets using historical data. The pipeline involves:

- Data cleaning & preprocessing  
- Handling missing values & outliers  
- Feature engineering  
- Machine learning model building  
- Evaluation & optimization  
- GUI-based prediction tool using Tkinter  

---

## 📊 Dataset

The dataset used is `big_mart_Train.csv`, containing 8523 records and 12 features such as:

- Item Identifier  
- Item Weight  
- Item Visibility  
- Item MRP  
- Outlet Size  
- Outlet Type  
- Item Outlet Sales (Target)

---

## 🧹 Data Preprocessing Steps

- Checked and handled **missing values** using:
  - Mean/Median imputation  
  - Interpolation  
  - KNN Imputer  
- Encoded categorical variables using **Ordinal Encoding**  
- Created new features like **Outlet Age**  
- Normalized and replaced inconsistent values (e.g., "Low Fat", "low fat" → "LF")  
- Removed irrelevant features based on feature importance  

---

## ⚙️ Models Used

| Model                   | R² Score (Cross-Validation) |
|-------------------------|-----------------------------|
| Random Forest Regressor | 0.55                        |
| XGBRF Regressor         | **0.59** (Best Model)       |

---

## 📈 Feature Importance (XGBoost)

- Outlet_Type → 39.5%  
- Outlet_Identifier → 20.5%  
- Item_MRP → 14.8%  
- Outlet_Age → 13.8%  
- Outlet_Size → 7.7%  
- Others (very minimal)

---

## 🖥️ GUI Implementation

The final model is deployed with a **Tkinter-based GUI** where users can input:

- Item MRP  
- Outlet Identifier  
- Outlet Size  
- Outlet Type  
- Outlet Establishment Year  

🧮 The GUI calculates and predicts the **estimated sales value range** in real-time.

---

## 💾 Model Deployment

Model saved using `joblib` for fast loading and inference:

```python
import joblib
model = joblib.load('bigmart_model')
```

---

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/yourusername/big-mart-sales-prediction.git
```

2. Install requirements:
```bash
pip install -r requirements.txt
```

3. Run the GUI:
```bash
python gui_app.py
```

---

## 🧠 Skills Demonstrated

- Data Cleaning & Preprocessing  
- Exploratory Data Analysis (EDA)  
- Feature Engineering  
- Regression Modeling  
- GUI Development  
- Model Deployment  

---

## 📁 Project Structure

```
├── big_mart_Train.csv  
├── data_preprocessing.ipynb  
├── model_training.py  
├── bigmart_model (saved model)  
├── gui_app.py  
└── README.md
```

---

## 🏁 Output Example

📷 *[Insert GUI screenshot or prediction output image here]*

---

## 🧑‍💻 Author

**Aaditya Raj Pandey**   
📍 Data Science Enthusiast | Python Developer  

---

⭐ *If you liked this project, feel free to star it on GitHub and share your feedback!*
