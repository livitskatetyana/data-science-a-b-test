# data-science-a-b-test
Conducted an A/B test to compare user conversion rates between the old (Control) and new (Treatment) landing pages. Calculated conversion rates, performed statistical tests (z-test and confidence intervals), and visualized results. Found no statistically significant difference, indicating the new page does not improve conversions.
# A/B Test Analysis: Landing Page Conversion

## 📌 Project Overview
This project analyzes an A/B test conducted to compare conversion rates between the old (Control) and new (Treatment) landing pages. The goal was to determine if the new landing page improves user conversions.

## 📊 Data
- Dataset: `ab_data.csv`  
- Features:
  - `user_id` — unique identifier of the user  
  - `group` — test group (Control / Treatment)  
  - `landing_page` — page version (old_page / new_page)  
  - `converted` — whether the user converted (0 = No, 1 = Yes)  
- Total users: 290,585  

## 🧹 Data Cleaning
- Filtered users to include only those in proper groups with matching landing pages.  
- Dropped duplicate `user_id`s to ensure independence.  
- Cleaned dataset saved as `ab_data_clean.csv`.

## 🔬 Analysis
1. **Conversion Rates**
   - Control: ~12%  
   - Treatment: ~11.9%  

2. **Statistical Testing**
   - **Null hypothesis (H0):** Conversion rates are equal (Control = Treatment)  
   - **Alternative hypothesis (H1):** Conversion rates are different (Control ≠ Treatment)  
   - Test: z-test for proportions  
   - Results: `z-statistic = 1.3116`, `p-value = 0.1897` → H0 not rejected  

3. **Confidence Intervals (95%)**
   - Control: (0.1187, 0.1221)  
   - Treatment: (0.1171, 0.1205)  

4. **Visualizations**
   - Barplot with confidence intervals  
   - Boxplot of conversions per group  
   - Histogram of conversion distribution  

## 📈 Results & Conclusion
- No statistically significant difference between Control and Treatment groups.  
- Launching the new landing page (Treatment) is **not justified** based on this test.  
- Visualizations support the conclusion: distribution of conversions is almost identical between groups.

## 🛠️ Technologies Used
- Python  
- Pandas  
- Matplotlib  
- Seaborn  
- Statsmodels  

## 📂 Repository Contents
- `ab_data.csv` — raw dataset  
- `ab_data_clean.csv` — cleaned dataset  
- `ab_test_analysis.ipynb` — Collab with full analysis, code, and plots  

## 💡 Notes
This project demonstrates skills in data cleaning, statistical testing, A/B test analysis, and data visualization.
