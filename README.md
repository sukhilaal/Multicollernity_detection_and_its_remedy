# California Housing Dataset: Correlation & Multicollinearity Analysis

An exploratory data analysis (EDA) Jupyter Notebook using Python, Pandas, and Seaborn to inspect the **California Housing dataset** and visualize pairwise feature correlations as a foundational step toward understanding **multicollinearity**.

---

## 📌 Project Overview

In regression and predictive modeling, understanding how independent features relate to one another—and to the target variable—is essential. This notebook loads the classic California Housing dataset from `scikit-learn`, constructs a structured Pandas DataFrame, and uses annotated correlation heatmaps to examine linear relationships among housing attributes.

### Key Concepts Covered
* **Pairwise Correlation:** Measuring linear relationships between two variables using Pearson's correlation coefficient.
* **Multicollinearity:** Understanding the distinction between two-variable correlation and multicollinearity (where one predictor variable is linearly explained by two or more other predictor variables).
* **Heatmap Visualization:** Using `matplotlib` and `seaborn` to generate readable, annotated correlation matrices.

---

## 📊 Dataset Information

The dataset is fetched directly via `sklearn.datasets.fetch_california_housing()` and is derived from the **1990 U.S. Census** (one row per census block group).

* **Total Instances:** 20,640
* **Features:** 8 numeric predictive attributes
* **Target Variable:** `Price` (Median house value in hundreds of thousands of dollars)
* **Missing Values:** None

| Feature | Description |
| :--- | :--- |
| **`MedInc`** | Median income in block group |
| **`HouseAge`** | Median house age in block group |
| **`AveRooms`** | Average number of rooms per household |
| **`AveBedrms`** | Average number of bedrooms per household |
| **`Population`** | Block group population |
| **`AveOccup`** | Average number of household members |
| **`Latitude`** | Block group latitude |
| **`Longitude`** | Block group longitude |
| **`Price`** *(Target)* | Median house value for California districts |

---

## 🛠️ Tech Stack & Dependencies

* **Python 3.x**
* **Pandas** – Data manipulation and DataFrame creation
* **NumPy** – Numerical operations
* **Scikit-Learn** – Loading the California Housing dataset
* **Matplotlib & Seaborn** – Statistical data visualization and correlation heatmaps

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install Required Libraries
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Run the Notebook
Open the notebook in Jupyter Notebook, JupyterLab, or Google Colab:
```bash
jupyter notebook your_notebook_name.ipynb
```

---

## 🔍 Key Takeaways from the Heatmap

* **`MedInc` vs. `Price`:** Median income shows the strongest positive correlation with median house value.
* **`AveRooms` vs. `AveBedrms`:** Average rooms and average bedrooms exhibit strong positive correlation with each other, making them primary candidates to monitor for multicollinearity.
* **`Latitude` vs. `Longitude`:** Strong negative correlation reflecting California's northwest-to-southeast geographic orientation.

---

## 🔮 Future Enhancements

* Add `sns.clustermap()` to hierarchically group correlated feature clusters.
* Compute **Variance Inflation Factor (VIF)** scores to formally quantify multicollinearity across all predictors.
* Build baseline regression models (OLS, Ridge, Lasso) to compare coefficient stability before and after handling correlated features.
<img width="596" height="487" alt="image" src="https://github.com/user-attachments/assets/ca394ce9-a1fe-45cd-84eb-0809cecaecf2" />
<img width="983" height="667" alt="image" src="https://github.com/user-attachments/assets/c04e439f-2c44-4982-bc3b-f0ab3041838f" />




