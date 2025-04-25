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

## 📊 Visualizations  
![download](https://github.com/user-attachments/assets/50ae71e6-35a8-4584-95b9-9c9659af7abe)


![download](https://github.com/user-attachments/assets/2fc762ac-f4d8-4899-b6d9-25d631505a3f)
![download](https://github.com/user-attachments/assets/c621d1bd-0524-4f32-bd31-1c00cd56f123)
![download](https://github.com/user-attachments/assets/469102e5-e869-424e-b3e4-2d49cfa6f876)
![download](https://github.com/user-attachments/assets/56f3e0c4-0b4a-4017-b825-b364f88f1ec8)
![download](https://github.com/user-attachments/assets/249df4e7-629e-4efa-b383-1ec8fdf165e7)


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
