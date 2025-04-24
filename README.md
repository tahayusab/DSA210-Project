# 📊 DSA210-Project: **Happiness & Racism Analysis**  

## 🌍 Project Overview  

This project explores the **relationship between national happiness levels and discrimination**, focusing on racism, religious bias, and other social exclusion factors.  

By analyzing global happiness rankings alongside discrimination-related statistics, we aim to uncover patterns highlighting how **inclusivity (or lack thereof) affects societal well-being**.  

### 🔍 Key Questions  
- Does higher discrimination correlate with lower happiness levels?  
- What are the strongest factors influencing this relationship?  
- Are there **regional differences** in the impact of racism on well-being?  
- Can we build a **predictive model** to estimate happiness using inclusivity metrics?  

These insights can inform **policymakers, educators, and social organizations** seeking to foster more inclusive societies.  

---

## 📌 Hypothesis  

- **Null Hypothesis (H₀):** There is no significant relationship between discrimination levels and the **World Happiness Index**.  
- **Revised Alternative Hypothesis (Hₐ):** Higher discrimination correlates with **lower** happiness levels, indicating a negative relationship.  

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

### **Primary Data Sources:**  
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

### 📌 **Descriptive Statistics**  

| Metric      | Mean  | Std Dev | Min | Max |
|------------|-------|---------|-----|-----|
| Happiness  | 5.68  | 0.88    | 3.88 | 7.38 |
| Homosexuals | 46.17 | 26.90   | 3.00 | 93.80 |
| Immigrants  | 22.77 | 14.65   | 2.60 | 72.80 |
| Race        | 17.12 | 13.76   | 0.60 | 70.40 |
| Religion    | 18.22 | 15.61   | 1.60 | 71.20 |
| Language    | 15.85 | 13.34   | 2.00 | 70.80 |

### 🔗 **Correlation Analysis**  

**Pearson Correlation Matrix** _(linear relationships)_:

| Variable      | Happiness | Homosexuals | Immigrants | Race | Religion | Language |
|--------------|-----------|-------------|------------|------|----------|----------|
| **Happiness** | **1.00**  | -0.757  | -0.352  | -0.472  | -0.462  | -0.429 |
| **Homosexuals** | -0.757 | **1.00** | 0.473 | 0.490 | 0.427 | 0.402 |
| **Immigrants** | -0.352 | 0.473 | **1.00** | 0.841 | 0.624 | 0.730 |
| **Race** | -0.472 | 0.490 | 0.841 | **1.00** | 0.797 | 0.888 |
| **Religion** | -0.462 | 0.427 | 0.624 | 0.797 | **1.00** | 0.732 |
| **Language** | -0.429 | 0.402 | 0.730 | 0.888 | 0.732 | **1.00** |


![download](https://github.com/user-attachments/assets/fbca9169-2b4e-43d6-b856-f3f3a37bae95)

![download](https://github.com/user-attachments/assets/c0d0a0f2-fbec-4c79-861f-9c81ae63b723)


Observations:  
- **Negative correlations between discrimination and happiness** across all categories.  
- Strongest negative correlation: **Homosexuals (-0.757)** → LGBTQ+ exclusion significantly impacts happiness.  
- **Race (-0.472) & Religion (-0.462) also show strong negative relationships**.  
- **High correlation between discrimination factors** (e.g., Race vs. Language: **0.888**), indicating overlapping exclusion patterns.  

**Spearman Correlation Matrix** _(rank-based relationships)_ shows similar trends, reinforcing findings.

### 📌 **Hypothesis Testing Results**  

All **traditional p-values < 0.05**, indicating **statistically significant correlations**.  
However, **permutation test p-values ≈ 1.00**, suggesting correlations might not be purely random.  

✅ **Null Hypothesis Rejected** → **Discrimination significantly affects happiness**.  
❌ **Contradicts Initial Hₐ** → Racism **reduces** happiness rather than increasing it. 

Homosexuals:
  Observed correlation = -0.7572
  Traditional p-value = 0.0000
  Permutation test p-value = 1.0000
  ❌ H₀ rejected, but correlation is negative (contradicts Hₐ).

  
![download](https://github.com/user-attachments/assets/9a66fcf5-a617-4736-adbe-eb983cfdad88)


Immigrants:
  Observed correlation = -0.3528
  Traditional p-value = 0.0071
  Permutation test p-value = 0.9956
  ❌ H₀ rejected, but correlation is negative (contradicts Hₐ).

  
![download](https://github.com/user-attachments/assets/254cba7e-38a3-402c-bb3e-45accf723a37)


Race:
  Observed correlation = -0.4726
  Traditional p-value = 0.0002
  Permutation test p-value = 1.0000
  ❌ H₀ rejected, but correlation is negative (contradicts Hₐ).

  
![download](https://github.com/user-attachments/assets/e23ff8fd-ea81-4b5c-a23f-e761253051c9)


Religion:
  Observed correlation = -0.4625
  Traditional p-value = 0.0003
  Permutation test p-value = 1.0000
  ❌ H₀ rejected, but correlation is negative (contradicts Hₐ).

  
   ![download](https://github.com/user-attachments/assets/8a81433a-16c8-496f-8e5e-121bbba3baa7)


Language:
  Observed correlation = -0.4293
  Traditional p-value = 0.0009
  Permutation test p-value = 0.9997
  ❌ H₀ rejected, but correlation is negative (contradicts Hₐ).

  
   ![download](https://github.com/user-attachments/assets/6e6b4127-f594-428a-a6e5-05e58c11d4ed)


  
---

## 📊 Visualizations  


![download](https://github.com/user-attachments/assets/1d783f60-bf81-4d6f-a9bc-88e34bcc3cc5)

 

---

## 🎯 Conclusion  

Based on our findings:  
- **Higher discrimination is strongly linked to lower happiness levels**.  
- **LGBTQ+ discrimination has the strongest negative impact** on happiness.  
- Countries with **higher inclusivity policies** tend to have **higher happiness rankings**.  

### 🌍 **Implications**  
Reducing social exclusion could lead to **increased well-being**, reinforcing the need for **anti-discrimination policies** globally.  

---

## 🔮 Next Steps  
🔹 **Investigate confounding factors** like GDP, education, governance.  
🔹 **Expand analysis** to regional studies.  
🔹 **Develop a predictive machine learning model**.  



---
