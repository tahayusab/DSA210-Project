# Does Discrimination Make Countries Less Happy? A Data-Driven Analysis
## DSA210 Final Project Report

### Abstract
This study investigates the relationship between societal discrimination and national happiness levels across 57 countries. Motivated by an apparent contradiction—Finland's top happiness ranking despite reports of prevalent racism—I explored whether various forms of discrimination correlate with national well-being. Using data from the World Happiness Report, World Values Survey, European Social Survey, World Bank, and Freedom House, I analyzed the impact of five types of discriminatory attitudes (toward LGBTQ+ individuals, immigrants, racial and religious minorities, and linguistic minorities) on happiness scores.

Results reveal a strong negative association between discrimination and happiness, with LGBTQ+ discrimination showing the strongest correlation (**r = -0.76, p < 0.001**). Machine learning models, particularly **Random Forest**, were able to predict whether a country fell into the "high" or "low" happiness category with **83% accuracy** based solely on discrimination indicators. These findings suggest that reducing discrimination may not only promote social justice but also contribute to improved collective well-being.

---

## 1. Introduction

### Motivation and Background
This research was inspired by a widely circulated meme highlighting Finland’s simultaneous ranking as the world’s happiest country and one of the most racist toward Black individuals. This apparent paradox prompted a deeper inquiry into whether such a contradiction is unique or part of a broader global pattern. Could societal discrimination undermine national happiness, even if economic and political indicators are strong?

### Research Questions
This project seeks to address the following questions:

- Is there a statistically significant relationship between discrimination levels and national happiness?
- Which forms of discrimination are most strongly associated with lower happiness scores?
- Can discrimination data alone accurately predict a country's happiness level?
- Does this relationship hold after controlling for economic development?

### Hypothesis
I hypothesize that **higher levels of societal discrimination are associated with lower national happiness**. Discrimination may erode social cohesion, trust, and psychological well-being, affecting the broader population—not just marginalized groups.

---

## 2. Data Collection and Preparation

### Data Sources
The analysis draws from multiple reputable sources:

- **World Happiness Report**: Provides happiness scores based on national surveys.
- **World Values Survey and European Social Survey**: Capture social attitudes toward various minority groups.
- **World Bank**: Offers GDP per capita as an economic control variable.
- **Freedom House**: Scores countries based on political freedom and civil liberties.

### Final Dataset Composition
After standardizing country names and removing entries with missing data, the final dataset included **57 countries** with the following variables:

- **Happiness Score (0–10 scale)**
- **Five Discrimination Indicators** (percent of respondents unwilling to have certain groups as neighbors):
  - LGBTQ+ individuals
  - Immigrants
  - People of different races
  - People of different religions
  - People who speak a different language
- **GDP per capita**
- **Freedom Score**

### Data Cleaning Process
Significant preprocessing was required to reconcile inconsistencies in country naming conventions across datasets. Missing values were handled through **listwise deletion** to preserve analytical integrity, resulting in a final sample of **57 countries** with complete data.

---

## 3. Methodology

### Statistical Analysis
- **Correlation Analysis**: Pearson and Spearman coefficients were calculated to assess the strength and direction of relationships between discrimination and happiness.
- **Hypothesis Testing**: Significance of correlations was tested using p-values (**< 0.05 considered statistically significant**).

### Machine Learning Techniques
Several **supervised and unsupervised learning methods** were implemented:

#### Classification Models
Countries were labeled as **"high" or "low" happiness** based on median split of happiness scores.

#### Algorithms Used
- k-Nearest Neighbors (**k-NN**)
- Decision Trees
- Random Forest

#### Clustering
- **K-means clustering** identified natural groupings among countries based on discrimination and happiness profiles.

### Rationale for Machine Learning
Machine learning methods can capture **non-linear and multi-dimensional relationships** that traditional statistical techniques may overlook. High classification accuracy would further support the hypothesis that **discrimination patterns are strong indicators of national happiness levels**.

---

## 4. Results

### Correlation Analysis

| Type of Discrimination | Pearson Correlation (Happiness) | p-value |
|-----------------------|------------------------------|--------|
| LGBTQ+               | -0.76                         | <0.001 |
| Racial               | -0.47                         | <0.001 |
| Religious            | -0.46                         | <0.001 |
| Language             | -0.43                         | <0.001 |
| Immigration          | -0.35                         | <0.01  |

All five forms of discrimination were **significantly negatively correlated** with happiness. LGBTQ+ discrimination exhibited the strongest relationship.

### Machine Learning Classification Performance
Using only the five discrimination indicators as features, the **Random Forest classifier achieved 83% accuracy** in predicting whether a country was "high" or "low" in happiness.

### Feature Importance (Random Forest)
1. LGBTQ+ discrimination
2. Racial discrimination
3. Religious discrimination
4. Immigration discrimination
5. Language discrimination

### Cluster Analysis
Unsupervised clustering identified two primary groups of countries:

- **Cluster 1**: Low discrimination, high happiness (e.g., Nordic countries)
- **Cluster 2**: High discrimination, lower happiness (e.g., some Eastern European and Middle Eastern nations)

### Controlling for GDP
Multivariate analysis **confirmed that the discrimination-happiness relationship persisted independently of economic status**.

---

## 5. Discussion

### Interpretation of Findings
Societal discrimination is inversely related to national happiness. This likely reflects broader social dynamics—such as trust, inclusion, and community cohesion—that influence overall life satisfaction.

### Significance of LGBTQ+ Discrimination
High LGBTQ+ acceptance may serve as a **proxy for societal openness, progressive policies, human rights, and social trust**—all of which contribute to happiness.

### Policy Implications
Reducing discrimination may serve as a **low-cost, high-impact strategy** for enhancing national well-being.

---

## 6. Limitations

### Data Limitations
- Sample size limited to **57 countries**
- **Survey biases** (self-reported attitudes may not fully reflect behaviors)
- **Temporal mismatches** (data collected across different years)

### Methodological Limitations
- **Causality not established** (correlation ≠ causation)
- **Confounding variables** (education, historical context)
- **Reverse causality** (lower happiness may increase intolerance)

---

## 7. Future Directions
Future research should:

- Expand country coverage.
- Conduct longitudinal analysis.
- Investigate **regional trends**.
- Explore **causal relationships**.

---

## 8. Conclusion

### Key Findings
Discrimination is strongly linked to **lower national happiness**, with LGBTQ+ discrimination showing the strongest negative correlation.

### Implications
Inclusivity is **not only morally right**—it is **statistically associated** with greater national happiness.

### Final Thought
Reducing societal discrimination may **enhance both equity and collective well-being**.

---

This should fit well with a GitHub-style markdown format. Let me know if you need any refinements!
