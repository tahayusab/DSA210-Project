# 📊 DSA210-Project: **Happiness & Racism Analysis**  

## 🌍 Project Overview  

This project explores the **relationship between national happiness levels and discrimination**, focusing on racism, religious bias, and other social exclusion factors.  

By analyzing global happiness rankings alongside discrimination-related statistics, we aim to uncover patterns highlighting how **inclusivity affects societal well-being**.  

---

### 🔍 Key Questions  

- Does higher discrimination correlate with lower happiness levels?(changed because of the results)  
- What are the strongest factors influencing this relationship?  
- Are there **regional differences** in the impact of racism on well-being?  
- Can we build a **predictive model** to estimate happiness using inclusivity metrics?  

These insights can inform **policymakers, educators, and social organizations** seeking to foster more inclusive societies.  

---
## 📈 Analysis Plan  

1. **Data Collection & Cleaning**  
   - Load and preprocess happiness and discrimination datasets.  
   - Handle missing values and harmonize country names for merging.  

2. **Feature Engineering**  
   - Normalize discrimination percentages.  
   - Create regional groups or clusters if applicable.(tried and shown a relation)   

3. **Exploratory Data Analysis (EDA)**  
   - Visualize distributions and outliers.  
   - Use heatmaps, bar charts, and scatter plots to show relationships.
   

4. **Statistical Testing**  
   - Use Pearson & Spearman correlation to test significance.  
   - Run permutation tests to validate results.  
   - Make randomise testing to say if data shows refuse H0 or unable to refuse H0
   - 
5. **Modeling & Prediction**  (possible future research)
   - Train regression or classification models to predict happiness from exclusion metrics.  
   - Evaluate model accuracy and feature importance.

---
## 📌 Hypothesis  

- **Null Hypothesis (H₀):** There is no significant relationship between discrimination levels and the **World Happiness Index**.  
- **Alternative Hypothesis (Hₐ):** Higher discrimination correlates with **lower** happiness levels, indicating a negative relationship.

change **Alternative Hypothesis (Hₐ)** because the relation was there but it was negative unlike previous **Alternative Hypothesis (Hₐ):** which was positive relation
Statistical tests will determine whether we can reject the null hypothesis and establish a measurable impact of racism on national well-being.  

---

## 🎯 Objectives  

- **Analyze correlations** between discrimination factors and happiness scores.  
- **Identify trends** among countries with high/low discrimination levels.  
- **Explore confounding factors** (GDP, education, governance).  
- **Develop a predictive model** estimating happiness based on inclusivity indicators.  
- **Provide insights** on how inclusivity policies affect national well-being.  

---

## 📊 Dataset  

### Primary Data Sources  

1. **World Happiness Index** – [World Happiness Report](https://worldhappiness.report/)  
2. **Discrimination Data:**  
   - [Europa Racism Data](https://data.europa.eu/data/datasets/s193_53_0_ebs138?locale=en)  
   - [Eurobarometer Discrimination Report](https://europa.eu/eurobarometer/surveys/detail/2972)  
   - [World Values Index](https://www.worldvaluessurvey.org/WVSOnline.jsp)  

---

## 🛠️ Tools & Technologies  

- **Programming Language:** Python  
- **Data Libraries:** Pandas, NumPy, SciPy  
- **Visualization:** Matplotlib, Seaborn  
- **Analysis:** Pearson & Spearman Correlation, Regression Modeling  

---

## 📈 Analysis Summary  

### 📌 Descriptive Statistics  

| Metric       | Mean  | Std Dev | Min  | Max   |
|--------------|-------|---------|------|-------|
| Happiness    | 5.68  | 0.88    | 3.88 | 7.38  |
| Homosexuals  | 46.17 | 26.90   | 3.00 | 93.80 |
| Immigrants   | 22.77 | 14.65   | 2.60 | 72.80 |
| Race         | 17.12 | 13.76   | 0.60 | 70.40 |
| Religion     | 18.22 | 15.61   | 1.60 | 71.20 |
| Language     | 15.85 | 13.34   | 2.00 | 70.80 |

---

### 🔗 Correlation Analysis  

**Pearson Correlation Matrix** (Linear Relationships):

| Variable      | Happiness | Homosexuals | Immigrants | Race  | Religion | Language |
|---------------|-----------|-------------|------------|-------|----------|----------|
| **Happiness** | **1.00**  | -0.757      | -0.352     | -0.472| -0.462   | -0.429   |
| Homosexuals   | -0.757    | **1.00**    | 0.473      | 0.490 | 0.427    | 0.402    |
| Immigrants    | -0.352    | 0.473       | **1.00**   | 0.841 | 0.624    | 0.730    |
| Race          | -0.472    | 0.490       | 0.841      | **1.00**| 0.797  | 0.888    |
| Religion      | -0.462    | 0.427       | 0.624      | 0.797 | **1.00** | 0.732    |
| Language      | -0.429    | 0.402       | 0.730      | 0.888 | 0.732    | **1.00** |

![download](https://github.com/user-attachments/assets/d68ba48d-58e7-4777-b031-fcbe630672d1)



📌 **Spearman Correlation Matrix** also shows similar patterns.

![download](https://github.com/user-attachments/assets/c08a5401-b768-494c-a628-65c5c7bba926)



🧠 **Observation:**  
- Negative correlations between **discrimination and happiness** across all categories.  
- Strongest negative correlation: **Homosexuals (-0.757)** → LGBTQ+ exclusion has the highest impact.  
- Race (-0.472) and Religion (-0.462) also show strong negative relationships.  
- High inter-correlation between discrimination factors (e.g., Race & Language: **0.888**) suggests overlapping exclusions.  

---

## 📌 Hypothesis Testing  

All **traditional p-values < 0.05**, indicating **statistically significant** correlations.  
However, **permutation test p-values ≈ 1.00**, which suggests that these relationships are likely **not random**.

### ❌ Null Hypothesis Rejected  
✅ Discrimination significantly affects happiness.  
⚠️ But the **correlations are negative**, contradicting any assumption that these exclusions boost happiness.

---

### 📉 Individual Results  

#### Homosexuals  
- Observed correlation: **-0.757**  
- Traditional p-value: **0.0000**  
- Permutation p-value: **1.0000**  
- ✅ Significant, ❌ Correlation is negative.

   
    ![download](https://github.com/user-attachments/assets/3ec2076d-78c6-4aec-b462-33b213f8130e)


#### Immigrants  
- Observed correlation: **-0.352**  
- Traditional p-value: **0.0071**  
- Permutation p-value: **0.9956**  
- ✅ Significant, ❌ Correlation is negative.

  
   ![download](https://github.com/user-attachments/assets/15c14bbe-2112-45cc-813a-12e799015a49)


#### Race  
- Observed correlation: **-0.472**  
- Traditional p-value: **0.0002**  
- Permutation p-value: **1.0000**  
- ✅ Significant, ❌ Correlation is negative.

  
   ![download](https://github.com/user-attachments/assets/fb49efd4-7d86-4091-b7fe-494b777fccb9)


#### Religion  
- Observed correlation: **-0.462**  
- Traditional p-value: **0.0003**  
- Permutation p-value: **1.0000**  
- ✅ Significant, ❌ Correlation is negative.


   ![download](https://github.com/user-attachments/assets/893844a1-8079-43e8-a015-8288559a33e5)


#### Language  
- Observed correlation: **-0.429**  
- Traditional p-value: **0.0009**  
- Permutation p-value: **0.9997**  
- ✅ Significant, ❌ Correlation is negative.


   ![download](https://github.com/user-attachments/assets/ea4a95d2-ef9c-43ec-a96f-1ff9244973a5)
---
## 🤖 Machine Learning Models

This section explores several supervised and unsupervised learning techniques used to understand the relationship between happiness and various discrimination metrics across countries.

---

### 📌 K-Nearest Neighbors (KNN)

KNN is a simple, instance-based learning algorithm that classifies a data point based on the majority label among its k nearest neighbors in the feature space.

**🔍 Model Performance**
- **Accuracy**: `0.83`
- **Classification Report**:
  ```
               precision    recall  f1-score   support

           0       0.83      0.83      0.83         6
           1       0.83      0.83      0.83         6

    accuracy                           0.83        12
   macro avg       0.83      0.83      0.83        12
weighted avg       0.83      0.83      0.83        12
  ```

**📉 Bias-Variance Tradeoff**
| k  | Bias     | Variance | Error Rate |
|----|----------|----------|-------------|
| 3  | 0.178    | -0.011   | 0.167       |
| 5  | 0.178    | -0.011   | 0.167       |
| 7  | 0.222    | -0.056   | 0.167       |
| 10 | 0.222    | -0.056   | 0.167       |
| 15 | 0.244    | 0.006    | 0.250       |

✅ **Best k:** 3 (Lowest MSE: `0.3452`)

![KNN Accuracy](https://github.com/user-attachments/assets/7dd169a1-46c5-4ce2-8c6b-501194740104)
![Bias-Variance](https://github.com/user-attachments/assets/4b4aae45-8820-4e2e-ae14-b707f7d7d1ac)
![Error vs K](https://github.com/user-attachments/assets/6d9f4aab-96da-48b4-bffd-e9e3980c5c10)

---

### 🌳 Decision Tree

Decision Trees split the dataset based on feature values to learn simple, interpretable rules.

- **Best Depth Chosen**: `9`

![Best Depth](https://github.com/user-attachments/assets/e8edc228-c9bf-4ff4-bde4-748cd8d9a57b)

**📈 Visualization of Tree (Depth = 9):**
![Tree Diagram](https://github.com/user-attachments/assets/eeb5c75a-afb1-4684-824e-4660fea4eb8c)

---

### 🌲 Random Forest

Random Forest builds an ensemble of decision trees using bootstrapped data and feature randomness.

- **Best Parameters**:
  - `max_depth`: 9
  - `n_estimators`: 100
- **Best Cross-Validated MSE**: `0.7588`

![Random Forest Feature Importances](https://github.com/user-attachments/assets/8e5210b4-d845-4af4-9c68-6e4181bc2598)

> 📝 Note: Although homosexuality showed the strongest relationship, the negative correlation suggests **lower tolerance is associated with lower happiness**, which visually appears as a reverse effect in the graph.

---

### 🧠 PCA + Random Forest

- **Optimal PCA Components**: `4`
- **Random Forest with PCA - CV MSE**: `0.3768`

![PCA Scree Plot](https://github.com/user-attachments/assets/8ec4a99d-10d9-45b3-bf5a-507618e59948)
![PCA Biplot](https://github.com/user-attachments/assets/8eb85a99-78d8-4218-be2f-3f4715a39151)

---

## 📊 Clustering (Unsupervised Learning)

To find structure in the data without labels, various clustering techniques were used.

---

### 🔗 Hierarchical Clustering

Uses distance-based dendrograms to iteratively merge similar countries.

![Dendrogram 1](https://github.com/user-attachments/assets/028f0fce-fad4-410c-aad1-5ce8a85b91ff)
![Dendrogram 2](https://github.com/user-attachments/assets/42ac5d91-0ed8-4d90-a236-058c96f27911)
![Cluster Map](https://github.com/user-attachments/assets/9d831dcb-f2f2-4502-973f-11e4e9450643)

**Cluster Sizes**
```
3    18
5    14
4    14
2     8
1     2
6     1
```

---

### 📍 K-Means Clustering

K-Means partitions data into `k` groups by minimizing intra-cluster variance.

![KMeans Clusters](https://github.com/user-attachments/assets/74756bf8-bf93-4d2f-b130-fb4457c8aa24)

**Cluster Optimization**
- **Elbow Method:** k = 2
- **Silhouette Score:** k = 7
- **Chosen k:** `5` (based on visualization & outlier detection)

> 👀 Data point 20 appeared distant in hierarchical clustering and was best isolated using `k=5`.

---

### 🔻 Divisive Clustering

This top-down approach begins with all data in one cluster and recursively splits.

![Divisive Clustering](https://github.com/user-attachments/assets/14fa1465-55ff-4fb4-9aba-36b15216ac07)

---

## ➕ Enriching the Dataset

To strengthen the analysis, additional economic and freedom indicators were introduced.

### 🧮 GDP and Freedom Indices

These were tested to enhance correlations and provide broader context:

- **Freedom vs Happiness**  
  ![Freedom Graph](https://github.com/user-attachments/assets/f36d19bd-a9c4-48b9-bfa7-b9838b4a6d95)

- **GDP vs Happiness**  
  ![GDP Graph](https://github.com/user-attachments/assets/a250a722-be21-40d5-acbc-b7c6ba3f3a35)

> 💡 Note: These features made the correlation plots more dense and did not improve model performance significantly, so were not included in final models.


## 📊 Visualizations  
![download](https://github.com/user-attachments/assets/50ae71e6-35a8-4584-95b9-9c9659af7abe)


![download](https://github.com/user-attachments/assets/2fc762ac-f4d8-4899-b6d9-25d631505a3f)
![download](https://github.com/user-attachments/assets/c621d1bd-0524-4f32-bd31-1c00cd56f123)
![download](https://github.com/user-attachments/assets/469102e5-e869-424e-b3e4-2d49cfa6f876)
![download](https://github.com/user-attachments/assets/56f3e0c4-0b4a-4017-b825-b364f88f1ec8)
![download](https://github.com/user-attachments/assets/249df4e7-629e-4efa-b383-1ec8fdf165e7)

k-means methods
![image](https://github.com/user-attachments/assets/e7313d9a-46b1-4f3d-8e6b-2c1d68a7423e)
![image](https://github.com/user-attachments/assets/55d3b2f6-60ec-4306-824a-b85d5f2d68b6)


---

## 🎯 Conclusion  

- **Higher discrimination = Lower happiness levels**  
- **LGBTQ+ exclusion shows the strongest negative impact**  
- Countries with **inclusive policies** score higher on the happiness index  

---

## 🌍 Implications  

These findings support global initiatives to:  
- Reduce exclusionary behaviors and policies  
- Promote inclusivity and equal rights  
- Foster well-being through social cohesion  

---

## 🔮 Next Steps  

- 🔎 Explore **confounding variables** like GDP, education, governance  
- 🌐 Conduct **regional-focused** analysis  
- 🤖 Build a **predictive ML model** using inclusivity as a feature  

---
