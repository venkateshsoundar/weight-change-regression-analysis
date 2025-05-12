# Weight Change Regression Analysis

A data-driven investigation of factors influencing weight change through multiple linear regression, comparing quantitative, qualitative, and combined models to identify key predictors of weight gain or loss. citeturn2file4

---

## 🔍 Project Overview

Obesity and weight management are critical public-health challenges. In this project, we analyze how demographics, dietary habits, physical activity, sleep quality, and stress levels relate to weight change over time. We build and compare three regression models—quantitative only, qualitative only, and combined—to determine which variables best predict weight change and yield the most reliable fit. citeturn2file0

---

## 📊 Dataset

- **Source**: Publicly available on Kaggle; no licensing required citeturn2file4  
- **Size**: 100 participants  
- **Key Features**:  
  - **Quantitative**: Age, Current Weight (lbs), BMR (Calories), Daily Calories Consumed, Daily Caloric Surplus/Deficit, Duration (weeks), Final Weight (lbs), Weight Change (lbs)  
  - **Categorical**: Gender (M/F), Physical Activity Level (5 tiers), Sleep Quality (Excellent–Poor), Stress Level (1–9) citeturn2file4  

---

## 📐 Methodology

We structure our analysis around three guiding questions: citeturn2file6  
1. **Combined effects** of all predictors on weight change, including interaction terms.  
2. **Quantitative focus**: How do age, BMR, caloric intake, and surplus/deficit drive weight change?  
3. **Qualitative focus**: How do gender, activity level, sleep quality, and stress level affect outcomes individually and jointly?

---

## 🛠️ Workflow

1. **Data Loading & Cleaning**  
2. **Variable Selection**: Remove IDs and collinear predictors (e.g., Current & Final Weight).  
3. **First-Order Model**: Fit initial linear regression and perform t-tests.  
4. **Multicollinearity Check**: Compute VIF and remove highly collinear variables.  
5. **Adjusted Model**: Refit with remaining predictors and reassess significance.  
6. **Model Selection**: Apply AIC, Mallows’ Cp, and adjusted R² criteria.  
7. **Interaction Model**: Test two-way interaction terms.  
8. **Assumption Testing**: Evaluate linearity, homoscedasticity (Breusch-Pagan), normality (Shapiro-Wilk), and influential points (Cook’s Distance).  
9. **Final Model & Interpretation**: Choose the model with optimal balance of fit and parsimony, interpret coefficients, and make predictions. citeturn2file9

---

## 📈 Key Findings

- **Quantitative Model** alone showed low explanatory power (adjusted R² ≈ –0.01).  
- **Qualitative Model** (Sleep Quality + Stress Level) achieved adjusted R² ≈ 0.69, with “Poor” sleep and high stress (levels 8–9) significantly associated with greater weight loss. citeturn2file2  
- **Combined Final Model** (including interaction/log transforms) reached adjusted R² = 0.8509, explaining 85.09% of variance. citeturn2file11  
- **Practical Example**: A participant with *poor* sleep quality and stress level 5 over 6 weeks is predicted to lose ~4.71 lbs. citeturn2file11

---

## 📁 Repository Structure

```
.
├── data/
│   └── weight_data.csv         # Raw dataset
├── notebooks/
│   └── weight_change_analysis.ipynb
├── outputs/
│   ├── figures/                # Residual plots, Cook’s Distance, etc.
│   └── model_summary.csv
├── requirements.txt            # Python dependencies
└── README.md
```

---

## 🚀 Setup & Installation

1. **Clone** this repository:  
   ```bash
   git clone https://github.com/venkateshsoundar/CalgaryChildCareCompliance_Analysis.git
   cd CalgaryChildCareCompliance_Analysis
   ```
2. **Create** and activate a virtual environment:  
   ```bash
   python3 -m venv venv
   source venv/bin/activate     # Linux/Mac
   venv\Scripts\activate        # Windows
   ```
3. **Install** dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
4. **Launch** the analysis notebook:  
   ```bash
   jupyter notebook notebooks/weight_change_analysis.ipynb
   ```

---

## 🤝 Contributions

- **Jackson**: Project introduction, objectives, interpretation, conclusion  
- **Venkateshwaran**: Methodology framework, variable categorization, workflow design, testing citeturn2file9  
- **Steen**: Quantitative models and interaction analyses  
- **Harpreet**: Qualitative variable modeling  
- **Aaron**: Combined model with all variables  

---

## 📚 References

1. Kaggle weight change dataset  
2. Twells et al. (2014). Obesity trends and health impacts  
3. National Institute of Diabetes and Digestive and Kidney Diseases  
