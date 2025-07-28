# 🎓 Enhancing Student Success: Automated Probation Management System for Universities

**A powerful AI-driven recommendation system** that predicts student probation risk right after midterm exams—before it’s too late. It not only flags at-risk students but also delivers **personalized, actionable strategies** to boost performance and help them **avoid academic probation**. Built using a custom academic dataset and **dynamic machine learning pipelines**, this project is tailored for **real-world university environments**, enabling proactive intervention and smarter academic support.



---

## 📌 Project Objective

Universities often struggle to identify students at risk of academic probation. This system aims to:

- Predict student probation chance.
- Provide actionable recommendations to prevent academic failure.
- Support academic advisors and institutions in improving retention rates.

---

## ⚙️ Technologies Used

| Component          | Details                                |
|--------------------|----------------------------------------|
| Language           | Python                                 |
| ML Model           | Random Forest Regressor                |
| Dataset            | Custom-built academic performance data |
| Libraries          | Pandas, Scikit-learn, NumPy, Matplotlib|
| Model Training     | Dynamic / Real-time                    |

---

## 📂 Dataset Features

The dataset is tailored for academic probation prediction and contains real-world-inspired student attributes. Below is a sample of the key fields used in the recommendation system:

| **Feature**               | **Description**                                              |
|---------------------------|--------------------------------------------------------------|
| `Reg. No.`                | Unique student registration number                           |
| `Student Name`            | Full name of the student                                     |
| `Subjects`                | Courses enrolled during the current semester                 |
| `Previous Semester GPA`   | GPA achieved in the previous semester                        |
| `Current CGPA`            | Cumulative Grade Point Average up to the current semester    |
| `Current Probation Status`| Indicates whether the student is currently on probation      |
| `Probation Chance`        | Model-predicted probability of entering probation (in %)     |
| `Contacts`                | Contact details for academic advisor or student notification |

---

## 🔍 Model Prediction Categories

- 🟢 **Continue** – Performing well, no intervention needed.
- 🟡 **At Risk** – Performance dropping, needs attention.
- 🔴 **Withdraw** – High risk of probation or failure.

---

## 📊 Model Performance

| Metric           | Score     |
|------------------|-----------|
| R² Score         | 0.97      |
| MAE (Error)      | 28.29     |
| MSE              | 1.67      |
| Accuracy (Class) | 97%       |

> 📌 Note: These scores are based on validation from a custom-labeled dataset.

---

## 🧠 How It Works

1. User inputs academic data.
2. The system processes the input and predicts performance.
3. A recommendation is generated (Continue / At Risk / Withdraw).
4. The model dynamically learns from new entries (if enabled).

---

## 🧭 System Workflow

```mermaid
flowchart TD
    A[🎓 Student Academic Data]
    A1[📑 GPA, CGPA, Attendance, Quizzes, Assignments, Midterms]
    A --> A1

    A1 --> B[🧹 Preprocessing & Feature Engineering]
    B1[🔄 Data Cleaning & Normalization]
    B2[📐 Feature Selection & Extraction]
    B --> B1
    B --> B2

    B2 --> C[🧠 Model Training: Random Forest Regressor]
    C1[⚙️ Hyperparameter Tuning]
    C --> C1

    C1 --> D[📊 Probation Risk Prediction]
    D1[📈 Risk Score Generation]
    D2[🧾 Probation Classification]
    D --> D1
    D --> D2

    D2 --> E[🛠️ Personalized Recommendation Generator]
    E1[🎯 Strategy Based on Weak Areas]
    E2[📚 Suggested Study Actions]
    E3[📆 Weekly Progress Tracker]
    E --> E1
    E --> E2
    E --> E3

    E3 --> F[📈 Student & Advisor Dashboard]
    F1[👩‍🏫 Advisor View: Student Status + Risk]
    F2[👨‍🎓 Student View: Tips & Action Plan]
    F --> F1
    F --> F2
