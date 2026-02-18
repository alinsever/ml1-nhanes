# README — NHANES Modeling Project

## Project Overview

This project applies statistical and machine-learning methods to data from the **NHANES (National Health and Nutrition Examination Survey)** in order to study three major public-health topics: obesity, mental health, and alcohol consumption. The goal is not only to build predictive models, but also to compare different modelling approaches and understand their strengths and limitations in real-world data analysis.

The results are presented as a **Quarto book**, which contains separate sections for each modelling approach as well as a joint introduction and conclusion.

---

## Data Source

The dataset is based on the **NHANES survey**, conducted by the U.S. Centers for Disease Control and Prevention (CDC).

Source website:  
https://www.cdc.gov/nchs/nhanes/

NHANES includes demographic, socioeconomic, health, and lifestyle variables collected through interviews and medical examinations. A prepared subset of NHANES data is used in this project and stored in the `data` directory.

---

## Project Structure (Quarto Book)

All results are compiled into a Quarto book. The structure is defined in `_quarto.yml` and follows this layout:

```
index.qmd                  → Joint Introduction
linear_model.qmd           → Obesity: Linear Regression
support_vector_machine.qmd → Obesity: SVM
glm-binomial.qmd           → Mental Health: GLM (Binomial)
gam-binomial.qmd           → Mental Health: GAM
glm_poisson.qmd            → Alcohol consumption: GLM (Poisson)
neural_network.qmd         → Alcohol consumption: Neural Network
conclusion.qmd             → Joint Conclusion
index.html                 → Rendered introduction page
data/                      → Data files (NHANES subset, results, processed data)
_quarto.yml                → Quarto book configuration
README.md                 → Project documentation (this file)
```

The compiled book is generated using:

```
quarto render
```

---

## Individual Contributions

### Part 1 — Obesity  
**Author:** Alin Sever  
**Models:**  
- Linear Regression (lm)  
- Support Vector Machine (SVM)

Focus: Predicting BMI and comparing linear vs. non-linear modelling approaches. 
Full methodology, validation details, and performance metrics are documented in the rendered Quarto report.

---

### Part 2 — Mental Health  
**Author:** Daniel Huber  
**Models:**  
- GLM Binomial (Logistic Regression)  
- Generalized Additive Model (GAM)

Focus: Modelling depression status using both binomial regression and non-linear smooth terms.

---

### Part 3 — Alcohol Consumption  
**Author:** Robin Girardin  
**Models:**  
- GLM Poisson  
- Neural Network

Focus: Explaining and predicting daily alcohol consumption using count regression and deep learning.

---

## Joint Work

The **Introduction** and **Conclusion** chapters were written collaboratively by all group members.

All modelling decisions, evaluation discussions, and threshold choices were coordinated as a team.

---

## Notes

This repository contains both:
- the rendered HTML outputs, and  
- the source `.qmd` files used to generate them.

Data files are included so the project can be rendered without requiring external downloads.
