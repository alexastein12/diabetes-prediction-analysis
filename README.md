# Diabetes Prediction: Logistic Regression Modeling

**Overview**
This project identifies the primary risk factors for developing diabetes using a dataset of Electronic Health Records (EHRs) from a sample of 100,000 patients. The analysis builds a predictive logistic regression model to quantify how clinical variables like HbA1c levels, blood glucose, age, and comorbidities influence the likelihood of a diabetes diagnosis[cite: 2].

**Methodology**
* **Data Wrangling:** Cleaned and recoded overlapping categorical variables for smoking history and converted binary numeric indicators into factor variables.
* **Model Selection:** Implemented backward step-wise logistic regression, utilizing nested likelihood ratio tests to evaluate the significance of continuous predictors and categorical variables like gender and smoking history.
* **Assumption Verification:** Verified linearity using component+residual plots and confirmed the absence of multicollinearity by calculating Variance Inflation Factors (VIF).

**Key Findings**
* **HbA1c Impact:** Hemoglobin A1c is the strongest predictor in the model; adjusting for other variables, a one-unit increase in HbA1c increases the odds of a diabetes diagnosis by a factor of 10.4.
* **Comorbidities:** Individuals with pre-existing hypertension or heart disease have more than double the odds of having diabetes (OR = 2.1 and 2.09, respectively) compared to those without the conditions.
* **Demographics:** Adjusting for all other variables, male patients face 1.32 times higher odds of a diabetes diagnosis compared to female patients.

**Limitations**
The dataset used for this model does not distinguish between Type 1 (an autoimmune condition) and Type 2 (a condition largely tied to lifestyle and age) diabetes, which limits the model's ability to perfectly isolate risk factors. Furthermore, the observational nature of the Kaggle dataset prevents drawing causal conclusions.

**Tools & Libraries**
* **Language:** R
* **Libraries:** `tidyverse`, `ggplot2`, `gtsummary`, `car`, `corrplot`
* **Deliverable:** R Markdown (`github_document`)

**Author Contributions**
I developed the data dictionary mapping the clinical variables and executed the diagnostic checks for the logistic regression assumptions (including linearity and multicollinearity), while collaborating evenly with my teammates across the exploratory data analysis and model selection pipeline.
