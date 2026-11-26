# Student Performance Analysis: EDA, Hypothesis Testing and PCA

Exploratory and statistical analysis of factors that might affect student CGPA, using a 100-student dataset.

**Dataset:** `Student_Performance.csv` (100 rows, 10 columns). Source: <add where you got it>.
Columns: age, study hours per week, sleep hours, CGPA, stress level (1-5), attendance %, social media hours, part-time job, gender.

## What I did
1. **Cleaning:** checked for duplicates (none found) and filled 5 missing values each in CGPA, sleep hours and study hours with the median.
2. **EDA:** CGPA distribution, attendance vs CGPA, CGPA by stress level, study hours vs CGPA.
3. **Hypothesis tests:**
   - Independent t-test, CGPA by part-time job status: p = 0.91
   - One-way ANOVA, CGPA across stress levels: p = <new value>
4. **PCA** on 7 standardised numeric features: 5 components retain about 81% of variance, and variance is spread fairly evenly across components.
5. **Linear regression** of CGPA on study hours: slope is essentially zero.

## Findings
- No statistically significant difference in CGPA by part-time job status or stress level.
- Study hours have no meaningful linear relationship with CGPA.
- PCA shows no dominant component, so the features are largely independent of each other.
- Attendance vs CGPA looks loosely positive on the scatter plot, but I did not test it.

## Limitations
- Only 100 rows, so tests have low power.
- Small effects could exist and not show up at this sample size.
- CGPA was included among the PCA features, so PCA describes the feature set, not what drives CGPA.

## Tech stack
Python, pandas, NumPy, SciPy, scikit-learn, Matplotlib, Seaborn

## Files
- `student_performance_analysis.ipynb`: code and analysis
