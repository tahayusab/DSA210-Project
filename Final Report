# Does Discrimination Make Countries Less Happy? A Data Analysis Project

**DSA210 Final Project Report**

---

## Abstract

I wanted to find out if there's a real connection between how much discrimination exists in a country and how happy that country is overall. I got this idea from a meme showing that Finland was both the happiest country and had high racism - which seemed weird. So I collected data on happiness scores and discrimination levels from 57 countries and used statistics and machine learning to see if there's a pattern.

My results show that countries with more discrimination are definitely less happy. The strongest connection was with discrimination against LGBTQ+ people (correlation of -0.76), but all types of discrimination were linked to lower happiness. I could even predict whether a country would be "high happiness" or "low happiness" with 83% accuracy just by looking at their discrimination data.

This matters because it shows that being inclusive isn't just the right thing to do - it actually makes entire countries happier.

---

## 1. Introduction

### Why I Chose This Topic

This whole project started because I saw a meme on social media showing that Finland was ranked as both the world's happiest country AND the most racist against Black people. That seemed really contradictory to me - how can a country be super happy but also really discriminatory?

I decided to dig deeper and see if this was just a weird coincidence or if there's actually a pattern across countries. Maybe discrimination and happiness are related in ways we don't usually think about.

### What I Wanted to Find Out

My main question was: **Do countries with more discrimination have lower happiness scores?**

I also wanted to know:
- Which types of discrimination affect happiness the most?
- Can I predict how happy a country is just by knowing how discriminatory it is?
- Do rich countries still show this pattern?

### My Hypothesis

I thought that countries with more discrimination would be less happy overall. My reasoning was that if people in a society are constantly dealing with prejudice and exclusion, that negative energy probably affects everyone's well-being, not just the people being discriminated against.

---

## 2. Data Collection

### Where I Got My Data

I used several different datasets to make sure my analysis was solid:

- **World Happiness Report**: This gives each country a happiness score from 0-10 based on surveys
- **European Social Survey**: Has data on discrimination attitudes in Europe  
- **World Values Survey**: Global survey asking people about their attitudes toward different groups
- **World Bank GDP data**: To control for how rich countries are
- **Freedom House**: Measures how free/democratic countries are

### What My Final Dataset Looked Like

After matching up all the data sources, I had complete information for 57 countries. For each country, I had:

- **Happiness score** (my main outcome variable)
- **5 types of discrimination** (% of people who wouldn't want these groups as neighbors):
  - LGBTQ+ people
  - Immigrants  
  - People of different races
  - People of different religions
  - People who speak different languages
- **GDP per capita** (economic control variable)
- **Freedom score** (political control variable)

### Data Cleaning Process

The hardest part was getting all the country names to match across different datasets. Some datasets used "United States" while others used "USA", etc. I also had to deal with missing data - some countries had happiness scores but no discrimination data, so I couldn't include them.

I ended up with 57 countries that had complete data for everything I needed.

---

## 3. Analysis Methods

### Basic Statistics

First, I did simple correlation analysis to see if discrimination and happiness were related. I used both Pearson correlation (for linear relationships) and Spearman correlation (for any monotonic relationships).

I also did hypothesis testing to make sure my results weren't just due to random chance.

### Machine Learning

Then I got more sophisticated and used machine learning to see if I could actually predict happiness from discrimination data:

- **Classification models**: I split countries into "high happiness" and "low happiness" groups and tried to predict which group a country belonged to
- **k-Nearest Neighbors**: Looks at similar countries to make predictions
- **Decision Trees**: Creates simple rules for classification
- **Random Forest**: Combines many decision trees for better accuracy
- **Clustering**: Groups countries with similar patterns together

### Why Machine Learning?

I used ML because it can find complex patterns that simple correlations might miss. Plus, if I can predict happiness from discrimination with high accuracy, that's stronger evidence that they're really connected.

---

## 4. Results

### Basic Statistics Results

The correlations were pretty shocking - every single type of discrimination was negatively correlated with happiness:

| Type of Discrimination | Correlation with Happiness | p-value |
|----------------------|---------------------------|---------|
| **LGBTQ+ discrimination** | **-0.76** | <0.001 |
| Racial discrimination | -0.47 | <0.001 |
| Religious discrimination | -0.46 | <0.001 |
| Language discrimination | -0.43 | <0.001 |
| Immigration discrimination | -0.35 | <0.01 |

**What this means**: Countries with more discrimination against any group tend to have lower happiness scores. The relationship with LGBTQ+ discrimination is especially strong.

All the p-values were way below 0.05, so I can be confident these aren't just random patterns.

### Machine Learning Results

#### Prediction Accuracy
My models could predict whether a country was "high happiness" or "low happiness" with **83% accuracy** just using discrimination data. That's pretty impressive!

#### Which Discrimination Matters Most?
The Random Forest model ranked the importance of different types of discrimination:

1. **LGBTQ+ discrimination** (most important)
2. Racial discrimination  
3. Religious discrimination
4. Immigration discrimination
5. Language discrimination (least important, but still matters)

#### Country Groupings
When I let the algorithm group countries naturally, it found that countries basically fall into two main groups:
- **Group 1**: Low discrimination, high happiness (like Nordic countries)
- **Group 2**: High discrimination, lower happiness

### What About Rich Countries?

Even when I controlled for GDP (how rich a country is), the discrimination-happiness relationship stayed strong. This means it's not just that poor countries happen to be both more discriminatory and less happy - there's something specific about discrimination that affects happiness beyond just economics.

---

## 5. What This All Means

### The Big Picture

My analysis shows that discrimination and happiness are definitely connected at the country level. This isn't just about individual people being unhappy when they face discrimination - it seems like discrimination creates a negative atmosphere that brings down everyone's happiness in a society.

### Why LGBTQ+ Discrimination Matters So Much

The fact that LGBTQ+ discrimination had the strongest relationship with happiness was surprising to me. I think this might be because:
- LGBTQ+ acceptance is often a sign of how generally open and tolerant a society is
- Countries that are inclusive toward LGBTQ+ people are probably inclusive in other ways too
- LGBTQ+ rights are a relatively recent social change, so countries that embrace them might be more progressive overall

### Practical Applications

**For governments**: If you want to make your country happier, working on reducing discrimination (especially against LGBTQ+ people) might be more effective than you'd think.

**For researchers**: Discrimination data could be used as an early warning system for declining national well-being.

**For advocates**: This gives concrete evidence that inclusive policies don't just help marginalized groups - they help everyone.

---

## 6. Limitations of My Study

I want to be honest about the problems with my analysis:

### Data Issues
- **Small sample**: Only 57 countries had complete data
- **Survey bias**: All my data comes from surveys, which might not capture real discrimination levels
- **Time periods**: My different datasets were from slightly different years
- **Cultural differences**: Survey questions might mean different things in different cultures

### Analysis Issues
- **Correlation ≠ Causation**: I can't prove that discrimination causes unhappiness, just that they're related
- **Confounding variables**: There might be other factors I didn't measure that affect both discrimination and happiness
- **Direction of causation**: Maybe unhappy countries become more discriminatory, rather than discrimination making countries unhappy

### Scope Issues
- **Mostly developed countries**: My sample was heavy on European and Western countries
- **Missing perspectives**: I didn't have good data from many African, Asian, or Latin American countries

---

## 7. Future Research Ideas

If I were to continue this project, here's what I'd want to do:

### Short-term improvements
- **Get more countries**: Try to find data sources that cover more of the world
- **Time series analysis**: Look at how countries change over time
- **Regional analysis**: See if the patterns are different in different parts of the world

### Longer-term projects
- **Causal analysis**: Try to figure out whether discrimination actually causes unhappiness or vice versa
- **Policy studies**: Look at specific anti-discrimination policies and see if they improve happiness
- **Mechanism research**: Try to understand WHY discrimination affects happiness (is it through social trust? economic effects? psychological stress?)

---

## 8. Conclusions

### What I Found

This project started with a meme about Finland, but it ended up revealing something pretty important: **discrimination and national happiness are strongly linked**. Countries with more discrimination tend to be less happy, and this relationship is strong enough that I can predict happiness levels with 83% accuracy just from discrimination data.

The strongest relationship was with LGBTQ+ discrimination, which suggests that acceptance of sexual and gender minorities might be a particularly important indicator of overall societal well-being.

### Why This Matters

These findings suggest that creating inclusive societies isn't just morally right - it's also practically beneficial for everyone's happiness. For policymakers trying to improve their country's well-being, focusing on reducing discrimination (especially against LGBTQ+ people) might be a surprisingly effective strategy.

### Personal Reflections

This project changed how I think about social issues. I used to think of discrimination as something that mainly affects the people being discriminated against. But my analysis suggests that discrimination creates a negative social atmosphere that brings everyone down.

It also made me appreciate how powerful data analysis can be for understanding social issues. What started as curiosity about a meme turned into evidence that could potentially influence policy decisions.

### The Bottom Line

**Countries that are more inclusive are measurably happier.** That's not just my opinion - it's what the data shows across 57 countries using multiple statistical methods. The evidence is pretty clear: if we want happier societies, we need more inclusive ones.
