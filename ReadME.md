# Outsmart Your Partner's Spending Spree: A Statistical Analysis of Consumer Behavior

This project explores the behavioral economics of spending—specifically, whether **seasonality** or **gender** influences consumer spending patterns in luxury vs. necessity categories. Using hypothesis testing, ANOVA, and regression modeling, we analyzed a real-world dataset of 26,051 credit card transactions to extract meaningful, data-backed insights.

---

## Objective

To determine whether external variables like **time of year** and **gender** significantly impact how individuals spend on discretionary (luxury) versus essential (necessity) goods, and what this implies for financial behavior and consumer targeting.

---

## Dataset Overview

- **Source**: Kaggle – "Credit Card Spend Analysis"
- **Records**: 26,051 individual-level transaction entries
- **Key Variables**:
  - `amount_spent` (converted to USD)
  - `spend_type` (e.g., groceries, entertainment, travel)
  - `gender`, `month`, `year`
  - Categorized spending into **luxury** vs. **necessity**

---

## Tools and Technologies

- **Languages**: Python, SPSS
- **Libraries**: pandas, matplotlib, seaborn
- **Statistical Techniques**:
  - One-way ANOVA
  - Linear Regression
  - Independent Samples T-Test
- **Data Engineering**:
  - Dummy variable creation for categorical data
  - Manual currency conversion (INR → USD)
  - Spending category aggregation

---

## Methodology

### 1. **ANOVA on Seasonality**
- Tested for statistical differences in average monthly spend across four seasons (Spring, Summer, Autumn, Winter) for both genders.
- Created seasonal dummy variables for regression analysis.

### 2. **Linear Regression**
- Modeled seasonal dummy variables against spend amount to assess variance explained by seasonality.
- Separate models built for male and female subsets.

### 3. **T-Tests on Luxury vs Necessity**
- Compared male vs. female average spend in:
  - **Luxury categories**: entertainment, travel, eating out
  - **Necessities**: groceries, household, fuel

---

## Key Findings

### 1. Seasonality Does Not Affect Spending
- **ANOVA p-values**: 0.3 (female), 0.34 (male) → fail to reject null hypothesis
- **R² < 0.01**: Seasonality explains less than 1% of spending variance
- Likely Explanation: Year-round access to online shopping diminishes seasonal trends in both discretionary and essential categories.

### 2. Gender Significantly Impacts Luxury Spending
- **T-Test Result**: Men spend significantly more on luxury purchases
  - T = 5.69, p < 0.000000013 → strong statistical significance
  - Possible causes: social roles, gift-giving, or financial responsibility in relationships

### 3. No Gender Difference in Necessity Spending
- T = -1.02, p = 0.31 → fail to reject null hypothesis
- Suggests parity in baseline living costs across genders for essential items

---

## Additional Insights

- **Cultural and behavioral biases** often attribute higher luxury spending to women; our findings contradict this and align with external research (e.g., Luxury Daily 2017).
- **Technology and E-commerce** have reshaped shopping behavior, flattening historical seasonal trends and promoting consistent year-round consumption.
- The **lack of detailed demographic attributes** (e.g., income, relationship status) in the dataset limits the ability to personalize behavior-based models—suggesting strong potential for future research with richer customer profiles.

---

## Limitations

- No data on income, relationship status, or purchase purpose
- Sample only includes Indian credit card holders — not globally representative
- Cannot distinguish between self-purchases vs. partner purchases

---

## Takeaways

- Behavioral spending models need to account for **shifts in consumer access and habits**, especially post-digital adoption.
- Gender-based segmentation strategies should be reassessed, especially in luxury product marketing.
- Seasonality assumptions in marketing and budget planning may be outdated for digitally native audiences.

