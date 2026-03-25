# Daily Commute Stress Analysis using KNN 🚗📉

This project is an end-to-end Data Science assignment focused on analyzing how daily commuting affects stress levels. [cite_start]The study is based on primary data collected through a survey of 80 individuals [cite: 3-25].

## 📌 Project Overview
The goal is to predict whether a person feels "Highly Stressed" (Target Variable) based on their commute logistics like distance, cost, and time spent traveling.

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** Pandas, NumPy, Seaborn, Matplotlib, Scikit-learn
- **Algorithm:** K-Nearest Neighbors (KNN)

## 📊 Dataset Details
- [cite_start]**Total Responses:** 80 [cite: 3-25]
- **Key Attributes:**
  - [cite_start]`Distance`: Commute distance in Kilometers [cite: 1]
  - [cite_start]`Cost`: Average daily travel cost [cite: 1]
  - [cite_start]`Time`: Duration of the commute [cite: 1]
  - [cite_start]`Transport Mode`: Primary mode of transport (Bus, Car, Walking, etc.) [cite: 1]
  - [cite_start]**Target:** `Stress` (Yes/No) [cite: 1]

## 🚀 Workflow

### 1. Data Wrangling & Cleaning
- [cite_start]Handled duplicate records (e.g., duplicate email entries)[cite: 4, 6].
- Cleaned numerical strings (extracted numbers from "20km", "Rs. 500").
- Filled missing values using median/mode strategies.

### 2. Exploratory Data Analysis (EDA)
- Performed statistical analysis and created visualizations (Bar charts, Heatmaps).
- Analyzed class balance to check the distribution of stressed vs. non-stressed individuals.

### 3. Feature Engineering
- **Encoding:** Used Label Encoding for ordinal data (Time) and One-Hot Encoding for nominal data (Transport Mode).
- **Correlation:** Used **Pearson Correlation** to select features most related to stress.
- **Scaling:** Applied `StandardScaler` to normalize data for the KNN algorithm.

### 4. Model Training & Testing
- **Split Strategy:** - 80% Training, 20% Testing.
  - 30% of the Training set was used for **Validation** to tune the model.
- **Algorithm:** K-Nearest Neighbors (KNN) with `Random_state=0`.

## 📈 Results (Accuracy Comparison)
| Metric | Training Accuracy | Testing Accuracy |
| :--- | :--- | :--- |
| **Euclidean** | 75.00% | 64.71% |
| **Manhattan** | 75.00% | 58.82% |
| **Minkowski** | 75.00% | 64.71% |

### Key Observation:
The **Euclidean Distance** metric provided the highest test accuracy, proving to be more effective for this dataset than Manhattan distance.

## 🏁 Conclusion
The project successfully classifies commute stress levels. The slight gap between training and testing accuracy suggests a minor overfitting, which could be improved with a larger dataset.
