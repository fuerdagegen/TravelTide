# TravelTide – Customer Segmentation and Rewards Program Analysis

## Project description
This project analyzes user behavior at **TravelTide**, an e-booking startup, to help the marketing team design a personalized **rewards program**.  
The goal is to identify distinct customer personas and assign them perks they are most likely to value, improving retention and engagement.

The analysis combines **SQL**, **Python**, and **machine learning** to uncover behavioral patterns, validate marketing personas, and suggest data-driven campaign strategies.

---

## Project summary

### 🎯 Objective
Support TravelTide’s Marketing Team in building a personalized rewards program by:
1. Understanding customer behavior and preferences.  
2. Identifying behavioral segments (personas).  
3. Assigning each customer a likely favorite perk for targeted marketing.

---

### 🧭 Approach
The project follows a structured four-stage workflow:

1. **Exploratory data analysis (EDA)** – Cleaned and explored customer, session, flight, and hotel data from PostgreSQL.  
2. **Feature engineering** – Created user-level behavioral and value metrics (e.g., RFM, discount use, travel patterns).  
3. **Customer segmentation** – Combined **descriptive statistics** (RFM + personas) with **unsupervised ML** (K-Means, DBSCAN).  
4. **Supervised modeling** – Built **Random Forest** and **Decision Tree** classifiers to validate and operationalize personas.

---

### 💡 Key insights
- Travel behavior varies along continuous dimensions — customers rarely fit into rigid clusters.  
- Descriptive segmentation (RFM + personas) gives greater interpretability than K-Means alone.  
- Supervised ML validated that manual personas reflect measurable differences in user behavior.  
- The **decision tree** revealed interpretable, high-level rules that can directly guide marketing segmentation.  
- Iterating between **manual persona definition → ML validation → rule extraction** enables continuous improvement.

---

### 📈 Outcomes
- Around 6,000 user profiles aggregated and cleaned  
- 16 engineered features including recency, frequency, and monetary value  
- 5 RFM-based segments mapped to **8 behavioral personas**  
- Random Forest accuracy: **93%**  
- Decision Tree accuracy: **70%**, offering clear, human-readable segmentation rules  

---

### 📂 Links to key files
- Executive Summary (PDF)  
- [EDA Notebook](https://github.com/fuerdagegen/TravelTide/blob/main/notebooks/Travel_Tide_%E2%80%93_EDA.ipynb)  
- [Aggregated Analysis and Feature Engineering Notebook](https://github.com/fuerdagegen/TravelTide/blob/main/notebooks/Travel_Tide_%E2%80%93_Aggregated_Analysis_and_Feature_Engineering.ipynb)
- [Machine Learning Notebook](https://github.com/fuerdagegen/TravelTide/blob/main/notebooks/Travel_Tide_%E2%80%93_Machine_Learning.ipynb)
- [User Aggregated Dataset](data/traveltide_user_agg_features.csv)

---

## 🧱 Directory structure
```
TravelTide/
├── data/
│   └── traveltide_user_agg_features.csv
├── notebooks/
│   ├── TravelTide_-_EDA.ipynb
│   ├── TravelTide_-_Aggregated_Analysis_and_Feature_Engineering.ipynb
│   └── TravelTide_-_Machine_Learning.ipynb
├── reports/
│   └── Aggregated Analysis and Feature Engineering/
├── scripts/
└── README.md
```

---

## ⚙️ Installation
```bash
git clone https://github.com/<yourusername>/TravelTide.git
cd TravelTide
pip install -r requirements.txt
```

---

## ▶️ Usage

Run each notebook in order to reproduce the analysis:
1.	```TravelTide_-_EDA.ipynb```
2.	```TravelTide_-_Aggregated_Analysis_and_Feature_Engineering.ipynb```
3.	```TravelTide_-_Machine_Learning.ipynb```

---

## 🧩 Dependencies
-	pandas
-	numpy
-	matplotlib
-	seaborn
-	scikit-learn
-	scipy
-	sqlalchemy / psycopg2 (for PostgreSQL connection)

---

## 🗝️ Example usage
```
import pandas as pd

# Load aggregated user-level data
df = pd.read_csv('data/traveltide_user_agg_features.csv')

# Display key metrics
df[['ltv_usd', 'recency_days', 'frequency_trips_per_day']].describe()
```
---

## 🧠 Author

Pino Bonetti
Marketing strategist & data analyst — Berlin
Project completed as part of the Masterschool Data Analytics Program
