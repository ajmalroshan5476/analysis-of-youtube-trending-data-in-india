# 📊 Analysis of YouTube Data
*Views, Likes, and Stardom: Insights from YouTube Trending Categories*

---

## 📌 Table of Contents
- [Business Problem](#-business-problem)
- [Objectives](#-objectives)
- [Dataset](#-dataset)
- [Tools & Techniques](#-tools--techniques)
- [Analysis & Findings](#-analysis--findings)
- [Final Conclusions](#-final-conclusions)
- [Engagement Index](#-engagement-index)
- [Future Work](#-future-work)
- [Project Links](#-project-links)

---

## 🎯 Business Problem
YouTube engagement metrics are heavily influenced by a small group of **star creators**, making it difficult to determine if a category’s performance reflects **genuine audience interest** or the impact of a few popular channels.

This project analyzes engagement both **with and without star bias** to:
- Help **platforms** improve recommendations
- Guide **advertisers** in better budget allocation
- Support **new creators** in finding sustainable growth categories

---

## 🔍 Objectives
- Identify categories driven by **authentic audience interest** vs. star dominance  
- Provide **actionable insights** for advertisers  
- Guide **emerging creators** toward organic growth opportunities  

---

## 📚 Dataset
- **Source**: [YouTube Trending Dataset – Kaggle](https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset)  
- **Scope**: 200,000+ trending videos (2017 onwards, India focus)  
- **Granularity**: Each row = one video’s daily performance on trending  

---

## 🛠 Tools & Techniques
- 🐍 **Python** → Core analysis  
- 🗄 **DuckDB** → SQL-style queries  
- 🧹 **Pandas & NumPy** → Data cleaning & wrangling  
- 📊 **Matplotlib & Seaborn** → Visualization  
- 📈 **SciPy & Statsmodels** → ANOVA & Tukey HSD tests  
- ☁️ **Google Colab** → Interactive workflows  

---

## 📊 Analysis & Findings

### 1. Skewed Views → Log Transformation  
- Large deviation between **mean vs. median views**  
- Applied **log transformation** → reduced outlier impact  

### 2. Category Distribution  
- **Entertainment & Music** dominate trending content  
- Small niches (Nonprofits, Pets & Animals) underrepresented  

### 3. ANOVA Test on Views  
- **F-statistic: 231.66, p-value: 0.0** → Categories differ significantly  
- Music, Entertainment, Gaming, Film & Animation attract **much higher views**  

### 4. Tukey HSD Post-hoc Test  
- Music significantly outperforms nearly every other category  
- Education, News, Travel, Nonprofits lag behind  

### 5. Stardom Concentration  
- 4 categories (Music, Entertainment, Gaming, Film & Animation) account for:  
  - **75.46% of views**  
  - **73.51% of engagement (likes + comments)**  

### 6. Engagement Patterns  
- **Star-driven** → High visibility, lower engagement ratio  
- **Non-star** → Lower reach, higher engagement per viewer  

---

## 📌 Final Conclusions
- 🎬 **Stardom dominates** → ~75% of views & engagement in 4 categories  
- 📊 **Significant differences** → Music videos lead consistently  
- ❤️ **Engagement trade-off** → Non-star categories foster deeper interactions despite lower reach  

---

## 🕵 Engagement Index
Formula:
```text
Engagement Index = (Total Likes / Total Views) + (Total Comments / Total Views)
