# walmart_analysis-9900
# Walmart Case Study Analysis 

## 1. Dataset Overview
- **Structure**: Loaded `customers` dataset and inspected structure.
- **Data Types**: All columns’ data types confirmed (int, float, object).
- **Shape**: Rows × Columns printed clearly.
- **Missing Values**: Missing values per column computed.

---

## 2. Nulls and Outliers
- **Null Values**: No missing values were detected in the dataset.
- **Outliers**: Outliers were identified in the `Purchase` variable using the IQR method. Most outliers occurred on the higher side of the distribution.
- **Treatment**: The data was clipped between the 5th and 95th percentiles to reduce the impact of extreme values. Post-clipping, the distribution was re-checked and appeared more balanced.

---

## 3. Data Exploration
- **Age vs Products**: Histplots used to show product preferences by age groups.
- **Age + Marital Status + Amount Spent**: Multivariate plots showed relationships.
- **Gender Preferences**: Male/female compared for product categories.

---

## 4. Gender vs Amount Spent (Central Limit Theorem & Bootstrapping)
- Bootstrapped confidence intervals for average purchase amount per gender.
- Calculations done for **full dataset** and smaller samples (n=300, 3000, 30000).
- **Findings**:
  - Interval widths shrink as sample size grows.
  - Some overlap between male/female distributions.
  - Larger samples produce narrower, more normal distributions.

---

## 5. Marital Status vs Amount Spent
- Confidence intervals computed for Married vs Unmarried.
- Same CLT procedure as gender analysis.
- **Findings**:
  - Sample size strongly affects interval width.
  - Overlaps in some cases, suggesting partial similarity in spending.

---

## 6. Age vs Amount Spent
- Age group confidence intervals bootstrapped.
- **Findings**:
  - Younger vs older groups showed differences in means.
  - Interval width narrowed with larger samples.
  - Overlaps were partial, suggesting distinct patterns but not absolute separation.

---

## 7. Reporting (Confidence Interval Comparisons)
- **Gender**: Male vs Female spending intervals overlap → spending habits broadly comparable.
- **Marital Status**: Married vs Unmarried overlap partly → marketing should consider family-oriented offers.
- **Age Groups**: Clearer differentiation, especially for certain brackets → targeted marketing possible.

---

## 8. Recommendations
1. **Targeted Promotions**: Focus on age groups with higher spending potential.
2. **Family-Oriented Campaigns**: Marital status overlaps suggest bundling offers could attract both segments.
3. **Gender-Neutral Strategy**: Since gender spending overlaps, no need for heavily gendered promotions.
4. **Data Quality**: Regularly check for nulls, outliers, and validate dataset structure.
5. **Scalability**: Larger samples give more reliable estimates; Walmart should invest in richer, continuous data collection.

---

## Appendix (Methods)
- **Boxplots** for outlier detection.
- **`np.clip()`** for clipping data to 5th–95th percentile.
- **Histplots** for demographic vs product relationships.
- **Bootstrapping & CLT** for CI estimation at multiple sample sizes.

---

