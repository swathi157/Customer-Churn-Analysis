# Customer Churn Analysis Dashboard

An interactive **Power BI Customer Churn Analysis Dashboard** designed to analyze customer behavior, identify churn patterns, evaluate customer value, and generate actionable retention insights using an e-commerce customer behavior dataset.

---

## Project Overview

Customer churn is a major challenge for e-commerce businesses because losing existing customers can directly impact revenue and long-term customer value.

This project uses **Python, SQL, and Power BI** to analyze customer behavior and build an interactive business intelligence dashboard that helps identify:

* Customer churn and retention patterns
* Customer engagement behavior
* High-value customers
* Factors associated with customer churn
* Customer groups and markets requiring retention attention

---

## Business Objectives

The dashboard aims to answer key business questions:

1. How many customers are currently active or churned?
2. What is the overall customer churn rate?
3. What is the customer retention rate?
4. Which customer behaviors are associated with higher churn?
5. Which customer groups have higher customer lifetime value?
6. Which markets require greater retention attention?
7. How does customer engagement relate to churn?
8. Which customers represent potential retention opportunities?

---

## Dataset

Dataset: E-Commerce Customer Behavior Dataset

Source: Kaggle

The dataset contains customer-level behavioral, demographic, engagement, purchasing, and value-related attributes, including:

* Gender
* Country
* Signup Quarter
* Membership Years
* Login Frequency
* Session Duration
* Pages Per Session
* Cart Abandonment Rate
* Wishlist Items
* Email Open Rate
* Mobile App Usage
* Social Media Engagement
* Total Purchases
* Average Order Value
* Days Since Last Purchase
* Discount Usage Rate
* Return Rate
* Payment Method Diversity
* Customer Service Calls
* Product Reviews Written
* Lifetime Value
* Churned

---

## Technologies Used

| Technology      | Purpose                                             |
| --------------- | --------------------------------------------------- |
| **Power BI**    | Dashboard development and interactive visualization |
| **DAX**         | KPI calculations and analytical measures            |
| **Power Query** | Data cleaning and transformation                    |
| **Python**      | Exploratory data analysis and preprocessing         |
| **SQL**         | Customer and churn analysis                         |
| **Excel/CSV**   | Data source and preparation                         |

---

#  Dashboard Structure

##  Page 1 — Churn Overview

The first page provides a high-level summary of customer churn and customer value.

### KPI Cards

* **Total Customers**
* **Churned Customers**
* **Churn Rate**
* **Retention Rate**
* **Average Lifetime Value**
* **Average Order Value**

The page provides an immediate overview of the overall health of the customer base.

---

##  Page 2 — Customer Behavior

This page analyzes customer behavior and engagement patterns associated with churn.

Example analyses include:

* Churn Rate by Membership Years
* Churn Rate by Login Frequency
* Churn Rate by Cart Abandonment
* Churn Rate by Customer Service Calls
* Churn Rate by Average Order Value

Interactive slicers allow users to analyze customer behavior across different segments and demographic dimensions.

---

##  Page 3 — Customer Value & Retention Insights

This page focuses on understanding customer value and retention-related patterns.

Analyses include:

* Customer Lifetime Value comparisons
* Customer engagement patterns
* Customer value across markets
* Customer feedback behavior
* Relationships between engagement and customer value

Interactive visualizations allow users to explore relationships between customer characteristics and business outcomes.

---

##  Page 4 — Retention Strategy & Business Insights

The final page focuses on identifying potential retention opportunities and supporting business decision-making.

The dashboard can be used to identify:

* High-value customers requiring attention
* Customer groups with elevated churn
* Markets with retention opportunities
* Engagement patterns associated with customer loss
* Potential areas for targeted retention campaigns

---

# Key DAX Measures

### Total Customers

```DAX
Total Customers =
COUNTROWS('YourTable')
```

### Churned Customers

```DAX
Churned Customers =
CALCULATE(
    COUNTROWS('YourTable'),
    'YourTable'[Churned] = 1
)
```

### Churn Rate

```DAX
Churn Rate =
DIVIDE(
    [Churned Customers],
    [Total Customers],
    0
)
```

### Retention Rate

```DAX
Retention Rate =
1 - [Churn Rate]
```

### Average Lifetime Value

```DAX
Average Lifetime Value =
AVERAGE('YourTable'[Lifetime_Value])
```

### Average Order Value

```DAX
Average Order Value =
AVERAGE('YourTable'[Average_Order_Value])
```

> Replace `YourTable` with the actual table name used in the Power BI model.

---

# 🎛️ Interactive Features

The dashboard includes interactive Power BI functionality such as:

* Dynamic slicers
* Cross-filtering between visuals
* Interactive KPI cards
* Tooltips
* Visual highlighting
* Drill-through analysis
* Reset-filter functionality

Users can dynamically explore the dashboard instead of viewing static charts.

---

#  Business Insights

The dashboard is designed to help businesses:

* Monitor customer churn
* Identify high-risk customer groups
* Understand customer engagement
* Prioritize high-value customers
* Analyze retention patterns
* Develop targeted customer-retention strategies
* Support data-driven decision-making

---

#  Project Structure

```text
E-Commerce-Customer-Churn/
│
├── PowerBI/
│   └── Customer_Churn_Analysis.pbix
|
|── ecommerce_customer_behavior.csv
│
├── Python/
│   └── customer_churn_analysis.ipynb
│
├── SQL/
│   └── churn_analysis.sql
│
├── Screenshots/
   ├── churn overview.png
   ├── customer behavior.png
   ├── customer value & retention insights.png
   └── retention strategy & business insights.png

```

---

#  How to Use

1. Download or clone the project repository.
2. Open the Power BI `.pbix` file.
3. Refresh the dataset if required.
4. Use the slicers to filter the dashboard.
5. Interact with charts to explore customer behavior.
6. Use drill-through and tooltips for deeper analysis.
7. Review the retention insights to identify potential business opportunities.

---

#  Future Enhancements

Future versions can include:

* Machine Learning-based churn prediction
* Customer risk scoring
* Automated Power BI refresh
* Customer Lifetime Value prediction
* AI-powered churn explanations
* Personalized retention recommendations
* Real-time customer monitoring

---

##  Project

**Customer Churn Analysis Dashboard**

**Technologies:** Power BI • DAX • Power Query • Python • SQL

Built to transform customer behavior data into **interactive insights for customer retention and business decision-making**.
