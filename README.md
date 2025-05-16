
This repository contains code and analysis for **Fairness in Machine Learning**, specifically targeting **Demographic Parity** and **Balance metrics** in classification tasks across different groups.

🔗 **Colab Notebook**: [Click here to view and run the notebook](https://colab.research.google.com/drive/1GoahZGnvwsEuBjTycdsamWYyILTsBoj3?usp=sharing)

---

## 📊 Dataset Summary

- **Total Samples**: 500
  - **Selection Class (y = 1)**: 250
  - **Rejection Class (y = 0)**: 250
- **Group A**
  - Selection: 175
  - Rejection: 70
- **Group B**
  - Selection: 75
  - Rejection: 180

---

## ✅ Initial Model Performance

- **Training Accuracy**: `100.00%`

---

## 📈 Fairness Metrics (Before Dataset Modification)

### 🔹 Demographic Parity
- P(ŷ = 1 | Group A) = 0.714
- P(ŷ = 1 | Group B) = 0.294
- **Demographic Parity Difference** = `0.420`

### 🔸 Balance Metric
- **Balance Score** = `0.5767`

---

## 🔁 Dataset Update (Fairness Optimization)

- Removed 50 samples (10% of data) to improve group balance.
- No impact on model accuracy: **100.00%**
  
### 🔹 Updated Fairness Metrics
- **New Demographic Parity Difference**: `0.3469`
- **New Balance Score**: `0.5190`

> ⚖️ **Interpretation**: The dataset was adjusted to reduce overrepresentation in Group A's selection and Group B's rejection. This led to a fairer outcome **without sacrificing model accuracy**.

---

## 📌 Key Takeaways

- Simple dataset rebalancing improved fairness without compromising separability or accuracy.
- Fairness metrics such as **Demographic Parity Difference** and **Balance** are useful to quantify and guide dataset-level interventions.
- No label flipping or complex debiasing was needed — just careful sample removal.

---

## 🛠 Technologies Used

- Python
- Google Colab
- Basic NumPy/Pandas operations
- Manual fairness metric calculations

---

## 📁 Files

- `fair_ml_hw1.ipynb`: Code notebook for all calculations
- `README.md`: Project overview and summary (this file)

---

## 📬 Contact

For questions or collaborations, feel free to reach out via GitHub or email.

---

