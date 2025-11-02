---
title: "Analyzing COVID-19 Data to Predict Death Rate"
output: github_document
---

# 📊 Analyzing COVID-19 Data to Predict Death Rate
**University of Kelaniya — Department of Statistics & Computer Science**  
**Course:** STAT 31631 – Statistical Modeling  
**Academic Year:** 2023/2024  
**Group 09**

---

## 👥 Group Members
- PS/2021/068 – MDDI Senadheera  
- PS/2021/050 – JANN Jayasinghe  
- PS/2021/169 – GLL Hansamali  
- PS/2021/025 – AJMVS Jayasinghe  
- PS/2021/176 – MDRD Rupasighe  
- PS/2021/009 – DSY Dissanayaka  
- PS/2021/111 – LMIK Thilakasiri  
- PS/2021/069 – SASC Ariyarathna  
- PS/2021/112 – GJE Amarasinghe  
- PS/2021/121 – SD Hendavitharana  

---

## 🧠 Project Overview
This project analyzes **global COVID-19 data** to build a **multiple linear regression model** capable of predicting total deaths in case of a future pandemic similar to COVID-19. The analysis aims to identify significant predictors and regional disparities in pandemic mortality.

**Primary Objective:**
- Develop a linear regression model to predict total deaths during a pandemic.

**Secondary Objectives:**
- Identify significant predictors influencing death rates.
- Build continent/region-specific models.
- Compare regional variations in healthcare and mortality.

**Dataset Source:**  
[Kaggle - Coronavirus Report Dataset](https://www.kaggle.com/datasets/imdevskp/corona-virus-report)

---

## 🧾 Methodology

1. **Data Cleaning**
   - Removed missing or redundant variables (`NewCases`, `NewDeaths`, etc.).
   - Imputed missing values using mean and median where necessary.

2. **Data Splitting**
   - 80% training data, 20% testing data.

3. **Modeling Approach**
   - Developed multiple linear regression models.
   - Performed stepwise regression (using `stepAIC()` from the MASS package).
   - Conducted diagnostic tests (normality, homoscedasticity, multicollinearity).

4. **Transformation**
   - Used Box-Cox and log transformations to improve model assumptions.

5. **Validation**
   - Evaluated model using R-squared, Adjusted R-squared, and residual diagnostics.

---

## 📈 Results Summary

- **Final Model Predictors:**
  - `Population`
  - `TotalCases`
  - `Serious.Critical`
  - `Tot.Cases.1M.pop`
  - `Deaths.1M.pop`

- **Model Performance:**
  - Adjusted R² = 0.89 (Strong explanatory power)
  - All predictors significant at 5% level
  - Residuals independent (Durbin-Watson test)
  - Log transformation improved normality

---

## 💡 Key Insights
- Total cases and healthcare capacity are strong predictors of death rate.
- Regions with weaker healthcare infrastructure show higher mortality risk.
- Predictive models can guide **policy planning and healthcare preparedness** for future pandemics.

---

## 🛠️ Technologies Used
- **R Language**
- **Libraries:** `caTools`, `MASS`, `car`, `corrplot`, `dplyr`, `lmtest`, `randtests`
- **Tools:** RStudio, Kaggle dataset

---

## 📚 References
- Kaggle COVID-19 Dataset – *imdevskp*
- Worldometer Data Repository
- R Documentation (Base & MASS Packages)

---

## 📄 License
This project is developed for academic purposes under the **University of Kelaniya** curriculum.  
Feel free to fork, reuse, or adapt the analysis with proper attribution.

---

