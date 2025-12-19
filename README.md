# NUPAT AI Fellowship – Stage Two Case Study

This repository contains my submission for the **NUPAT AI Fellowship (Stage Two) Case Study Assessment**.

The objective of this assessment is to analyze trading and user activity data, extract meaningful business insights, and build a fraud detection model based on user behavior.

---

## 📁 Project Structure


├── NUPAT_Case_Study.ipynb ├── trades.csv ├── user_activitycsv.csv └── README.md
## 📊 Part 1: Exploratory Data Analysis & Market Insights

### Market Dynamics
- Identified the **top 3 most traded pairs by USD volume** using a fixed conversion rate of **1500 NGN/USD**.

### Volatility Analysis
- Calculated **daily price volatility** for the BTCNGN pair.
- Applied a **7-day rolling average** to observe volatility trends.

### User Behavior
- Analyzed deposit patterns by:
  - Day of the week
  - Hour of the day
- Identified peak deposit periods to understand user activity behavior.

---

## 🔐 Part 2: Fraud Detection Model

### Feature Engineering
User-level features were created using both datasets, including:
- Deposit and withdrawal frequency
- Withdrawal-to-deposit ratio
- Time between first and last activity
- Total trading volume in USD
- Number of unique assets and trading pairs

### Target Labeling
Since no fraud label was provided, a **rule-based approach** was used to flag suspicious users who:
- Withdraw most of their deposited funds
- Perform minimal trading activity
- Exit the platform within 24 hours

### Model
- A **Random Forest Classifier** was trained to predict suspicious users.
- **Recall** was prioritized during evaluation to minimize missed fraudulent cases.

---

## 🧠 Key Assumptions
- Timestamps were provided in ISO format rather than UNIX.
- All fiat currencies were converted using a fixed rate of **1500 NGN/USD**.
- Fraud detection labels are heuristic-based due to lack of ground truth.

---

## 📌 How to Run
1. Clone the repository
2. Open `NUPAT_Case_Study.ipynb`
3. Ensure `trades.csv` and `user_activitycsv.csv` are in the same directory
4. Run all cells from top to bottom

---

## 👤 Author
**Ayobami Akande**



## 🛠️ Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
w
