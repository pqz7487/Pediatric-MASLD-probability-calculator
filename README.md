# Pediatric-MASLD-probability-calculator
A simple web-based calculator for estimating the probability of Metabolic dysfunction associated steatotic liver disease (MASLD) using a logistic regression equation derived from anthropometric measurements and lifestyle factors.

📌 Overview

This calculator implements a logistic regression model to estimate MASLD risk using easily obtainable clinical variables.

Key features:

✅ Instant MASLD probability estimation

✅ No backend required (pure HTML + JavaScript)

✅ Automatic imputation using training medians

✅ Feature contribution visualization (interpretability)

✅ Adjustable risk threshold

⚙️ Model Specification

Model: Logistic Regression (closed-form)

Output:

Probability (MASLD)
Formula : [y=​−10.7088−1.2385×Sex+0.3618×Age+0.1605×Household income+2.3815×BMI SDS+1.3968×WC SDS+0.0009×Systolic BP−0.0734×Regular physical activity+0.0209×Frequency of home-prepared meals]

📊 Input Variables
1. Anthropometric & Clinical Variables

Height, weight, waist circumference (WC)

Derived indices:

Height SDS

Weight SDS

BMI SDS

WC SDS

👉 SDS calculated using:

2017 Korean National Growth Charts (KNHANES)

CDC Growth Reference (NHANES)

2. Socioeconomic Status

Household income (quartiles)

3. Lifestyle Variables

Regular physical activity

Defined as number of days/week with ≥60 min exercise

Frequency of home-prepared meals

7-level ordinal scale:

1: <1/month
2: 1–3/month
3: 1–2/week
4: 3–4/week
5: 5–6/week
6: 1/day
7: ≥2/day

🧪 MASLD Definition (Reference Standard)

Based on multisociety Delphi consensus:

MASLD is defined as:

Hepatic steatosis + ≥1 cardiometabolic risk factor

Cardiometabolic risk factors:

(A) Overweight/central obesity

BMI ≥ 85th percentile OR WC ≥ 95th percentile

(B) Glucose abnormality

FPG ≥ 100 mg/dL OR HbA1c ≥ 5.7%

(C) Elevated blood pressure

≥95th percentile (age/sex/height)

OR ≥130/80 (<13 yrs)

OR ≥130/85 (≥13 yrs)

(D) Triglycerides ≥150 mg/dL

(E) HDL ≤40 mg/dL

🧬 Hepatic Steatosis Assessment

Two non-invasive surrogates were used:

1. Hepatic Steatosis Index (HSI)

Cutoff: ≥30.0

2. Controlled Attenuation Parameter (CAP)

Cutoff: >248 dB/m

🖥️ How to Use

Open the HTML file in a browser

Enter input values

Click PREDICT

Outputs:

🟢 Predicted probability (%)

🧮 Linear predictor (η)

📊 Feature contribution chart

📈 Feature Contribution Visualization

Displays each variable’s contribution to η

Two modes:

Baseline-adjusted (default):

𝑤
(
𝑥
−
𝑚
𝑒
𝑑
𝑖
𝑎
𝑛
)
w(x−median)

Raw contribution:

𝑤
𝑥
wx

Interpretation:

Right (green): increases risk

Left (red): protective effect

📄 License

Specify your license here (e.g., MIT, Apache 2.0)
