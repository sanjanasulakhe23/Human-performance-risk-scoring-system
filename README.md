# 🧠 Human Performance Risk Scoring System

_Modeling performance breakdown risk using lifestyle, stress, and behavioral stability signals_

---

## 📌 Project Overview

This project builds an **interpretable risk scoring system** to identify individuals at risk of performance breakdown using real-world lifestyle and stress data.

Instead of predicting outcomes with a black-box model, the project focuses on **risk modeling**, similar to systems used in credit risk, health risk, and churn analytics.

The system answers:
> **Who is at risk, why are they at risk, and how severe is the risk?**

---

## 🎯 Outcome

### ✅ Final Outcome
- Each individual is assigned a **Performance Risk Score (0–1)**
- Individuals are segmented into **Low, Medium, and High Risk**
- The system explains risk using **pressure, recovery, and behavioral volatility**

This makes the results **actionable and interpretable**, not just analytical.

---

## 📂 Data Used

- **Sleep Health and Lifestyle Dataset (Kaggle)**
- Lifestyle and physiological indicators such as:
  - stress level
  - sleep duration and quality
  - physical activity
  - heart rate

---

## 🧠 Conceptual Framework

Human performance risk is modeled as:
-risk =Pressure -Recovery+ Volatility

Where:

- **Pressure** → mental and physiological demand  
- **Recovery** → ability to absorb demand  
- **Volatility** → instability in behavior  

This mirrors real-world risk systems where instability amplifies failure probability.

---

## 📐 Signal Design

### 🔴 Pressure Signals
Represent demand placed on an individual.

Derived from:
- Stress level
- Heart rate (physiological stress proxy)

Pressure Score (normalized 0–1):
-Pressure = 0.7 × Stress + 0.3 × Heart Rate


---

### 🟢 Recovery Signals
Represent capacity to handle pressure.

Derived from:
- Sleep duration
- Sleep quality
- Physical activity

Recovery Score (normalized 0–1):
Recovery = 0.4 × Sleep Duration+ 0.3 × Sleep Quality + 0.3 × Physical Activity

---

### 🟡 Volatility Signals (Advanced Component)
Volatility captures **instability**, not absolute level.

Derived from:
- Deviation of stress from the population mean

Higher volatility indicates unstable behavior, which increases breakdown risk.

---

## 🧮 Performance Risk Score

### Raw Risk Formula
Performance Risk = 0.5 × Pressure − 0.3 × Recovery + 0.2 × Volatility

- Pressure increases risk  
- Recovery reduces risk  
- Volatility amplifies risk  

The final score is normalized to a **0–1 range** for interpretability.

---

## 🏷️ Risk Segmentation

Risk scores are converted into actionable categories using quantile-based bucketing:

- **Low Risk**
- **Medium Risk**
- **High Risk**

This ensures balanced and meaningful groupings suitable for decision-making.

---

## 📊 Model Validation & Interpretation

### 1️⃣ Risk Score Distribution by Category
**What it shows:**  
Clear separation between Low, Medium, and High risk groups.

**Why it matters:**  
Confirms that the risk score meaningfully differentiates individuals.

---

### 2️⃣ Pressure vs Recovery (Colored by Risk)
**What it shows:**  
- High risk → high pressure & low recovery  
- Low risk → low pressure & high recovery  

**Why it matters:**  
Visually validates the core logic of the model.

---

### 3️⃣ Volatility vs Risk Score
**What it shows:**  
Higher behavioral volatility corresponds to higher risk.

**Why it matters:**  
Demonstrates that instability amplifies performance breakdown risk, making the system more realistic and advanced.

---

## ✅ Sanity Check Summary

| Risk Group | Pressure | Recovery | Volatility |
|-----------|----------|----------|------------|
| Low | Low | High | Low–Moderate |
| Medium | Moderate | Moderate | Lower |
| High | High | Low | High |

This confirms that the system behaves logically and consistently.

---

## 🏁 Key Takeaways

- Performance breakdown risk is driven by **multiple interacting factors**
- Recovery can buffer pressure, but instability amplifies risk
- Rule-based risk systems can be powerful, interpretable, and actionable
- This framework can be extended to HR analytics, health risk screening, and productivity analysis

---

## 🚀 Future Improvements

- Incorporate time-series data for dynamic volatility
- Optimize weights using statistical learning
- Extend framework to multi-dataset signal fusion
- Deploy as an interactive dashboard

---

## 📎 Why This Project Is Strong

- End-to-end system design
- Custom risk modeling (not given by data)
- Interpretable logic
- Validated with evidence
- Suitable for real-world analytics use cases





