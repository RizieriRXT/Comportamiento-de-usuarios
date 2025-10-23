# 🍽️ User Behavior & A/A/B Testing: Optimizing App Engagement for a Food Startup

This project analyzes user behavior within a food product app and evaluates the impact of a font redesign through an A/A/B experiment. The goal is to understand the sales funnel, identify drop-off points, and determine whether the new font design improves user engagement.

---

## 🎯 Objective

To test two hypotheses:

1. Users drop off at specific stages of the sales funnel, and identifying these stages can improve conversion.
2. Font redesign impacts user behavior, and A/A/B testing can determine its effectiveness.

---

## 🛠️ Technologies Used

- **Python**: Pandas, NumPy, Matplotlib, Seaborn, SciPy
- **Jupyter Notebook**: Interactive environment for analysis
- **CSV Dataset**: `/datasets/logs_exp_us.csv`

---

## 🔍 Key Steps

### 1. Data Preparation
- Renamed columns for clarity.
- Checked data types and handled missing values.
- Extracted date and time features from timestamps.

### 2. General Data Exploration
- Counted total events and unique users.
- Calculated average events per user.
- Identified complete data period by plotting histograms and excluding early incomplete logs.
- Verified presence of users in all three experiment groups (ExpId: 246, 247, 248).

### 3. Sales Funnel Analysis
- Ranked events by frequency and user participation.
- Calculated conversion ratios between funnel stages.
- Identified the stage with highest user drop-off.
- Measured the percentage of users completing the full journey to purchase.

### 4. A/A/B Experiment Evaluation
- Compared user counts across groups.
- Validated similarity between control groups (246 vs 247) using statistical tests.
- Selected most frequent events and compared user engagement across groups.
- Assessed statistical significance of differences using proportion tests.
- Compared test group (248) against each control group and combined controls.
- Evaluated experiment reliability and sample size adequacy.

---

## ✅ Results

- **Sales Funnel Insights**:
  - Major drop-off occurs after product view but before adding to cart.
  - Only a small percentage of users complete the full purchase journey.

- **A/A/B Test Findings**:
  - Control groups 246 and 247 showed no significant differences → experiment setup is valid.
  - Test group 248 showed slightly lower engagement on key events.
  - No statistically significant improvement from font redesign at standard significance level (α = 0.05).

- **Significance Level**:
  - Set at **0.05** to reduce false positives.
  - Adjusted for multiple hypothesis testing using Bonferroni correction.

---

## 📚 Sources Consulted

1. **Pandas Documentation** – Data manipulation and timestamp handling.
2. **Matplotlib & Seaborn Docs** – Visualizing event distributions and funnel stages.
3. **SciPy Stats Module** – Proportion testing and statistical significance.
4. **A/B Testing Best Practices (Optimizely)** – Experimental design and validation.
5. **User Funnel Analysis (Mixpanel Blog)** – Understanding drop-off and conversion.
6. **Bonferroni Correction Guide (StatQuest)** – Adjusting significance for multiple tests.
7. **Jupyter Notebook Tips (Real Python)** – Workflow optimization.
8. **Data Cleaning Techniques (Towards Data Science)** – Handling incomplete logs.
9. **GitHub Markdown Guide** – Project documentation formatting.
10. **Product Analytics for Startups (Amplitude)** – Interpreting behavioral data.

---

