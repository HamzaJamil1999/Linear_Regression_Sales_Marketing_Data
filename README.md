# Simple Linear Regression Analysis: Marketing and Sales Data

## Project Overview
This project uses a simple linear regression model to analyze the relationship between marketing budgets (with a focus on radio promotion) and sales revenue. As part of an analytics team, the goal is to provide insights into how marketing budgets, particularly for radio promotions, correlate with sales outcomes. This information can guide the company's resource allocation in future marketing campaigns.

The dataset provided includes marketing campaign data across TV, radio, and social media channels, alongside the corresponding revenue generated. The insights derived will help stakeholders make more data-informed decisions on where to focus marketing resources.

## Dataset
The fictional dataset used in this project, `marketing_sales_data.csv`, contains 572 rows and 5 columns, including:

- **TV**: Categorical data (Low, Medium, High) indicating the TV budget.
- **Radio**: Continuous data representing the radio promotion budget in millions of dollars.
- **Social Media**: Continuous data representing the social media promotion budget in millions of dollars.
- **Influencer**: Categorical data (Nano, Micro, Macro, Mega) indicating the type of influencer collaboration.
- **Sales**: Continuous data indicating the revenue generated from the marketing campaign in millions of dollars.

## Project Steps

### Data Import & Exploration
1. Imported necessary Python libraries (`pandas`, `matplotlib`, `seaborn`, `statsmodels`).
2. Loaded the dataset and inspected the first few rows.
3. Identified the structure of the dataset with 572 rows and 5 columns.
4. Checked for missing values and removed rows containing any missing entries.

### Model Assumptions Check
1. Examined scatter plots and histograms to visually assess the data's linearity and normality.
2. Confirmed linearity between Radio budget and Sales through scatter plot inspection.
3. Conducted a residuals analysis and created Q-Q plots to validate the normality assumption.
4. Checked for independent observation and homoscedasticity assumptions using a scatter plot of residuals against fitted values.

### Linear Regression Model Building
1. Created a new DataFrame with only the `Radio` and `Sales` columns.
2. Defined a linear regression formula to model the relationship: `Sales ~ Radio`.
3. Built and fit an Ordinary Least Squares (OLS) regression model.
4. Retrieved the summary of the model to interpret coefficients and validate statistical significance.

### Model Evaluation and Interpretation
1. Analyzed model outputs, including slope, intercept, R-squared, and p-values.
2. Found a statistically significant positive relationship between the radio promotion budget and sales.
3. Confirmed model assumptions through residual and Q-Q plot analyses.

## Key Findings
The simple linear regression equation derived from the model is:
- **Interpretation**: On average, for every 1 million dollars increase in the radio promotion budget, sales are expected to increase by approximately 8.1733 million dollars.
- The results are statistically significant with a p-value of 0.000, supporting the rejection of the null hypothesis that there is no relationship between radio promotion budget and sales.
- A 95% confidence interval for the slope indicates that the true slope value likely falls between 7.791 and 8.555.

## Conclusion and Recommendations
The analysis demonstrates a notable positive association between the radio promotion budget and sales. For the companies in this dataset, increasing the radio promotion budget could lead to higher sales. These findings suggest that further investments in radio promotion could be beneficial. Future analyses could examine the effect of radio promotion budgets across different industries and product types to ensure targeted investment strategies.

