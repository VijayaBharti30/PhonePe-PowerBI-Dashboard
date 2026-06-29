# PhonePe Analytics Dashboard — Power BI Business Intelligence Report

An end-to-end business intelligence project analysing PhonePe transaction data and user behavior through an interactive Power BI dashboard. The project covers the complete analytics workflow: cleaning and transforming data, building relationships and calculations using DAX, and presenting business insights through an interactive dashboard.

* * *

## Project Objective

Digital payment platforms generate massive amounts of transaction data every day. Raw transactional data alone provides little value unless transformed into meaningful insights.

The objective of this project is to:

• Analyze transaction trends over time  
• Understand customer behavior patterns  
• Evaluate payment success and failure rates  
• Identify high-performing services and user segments  
• Present findings through an interactive dashboard

* * *

## Table of Contents

- Business Context
- Business Questions
- Headline Results
- Data Sources
- Data Cleaning and Transformation
- Data Modeling
- Calculated Measures
- Dashboard Outputs
- Insights
- Recommendations
- Repository Structure
- Tools and Technologies

* * *

## Business Context

PhonePe operates as a digital payment platform where users perform multiple transaction activities such as UPI transfers, bill payments, recharge services, and merchant transactions.

Business teams need insights into:

- Transaction growth
- User activity
- Service performance
- Payment success rates
- User segmentation patterns

* * *

## Business Questions

| Theme | Question |
|--------|-----------|
| Transaction Trends | How are transactions changing month by month? |
| User Analysis | Which user group contributes most transactions? |
| Payment Performance | What percentage of payments succeed or fail? |
| Service Analysis | Which services generate the highest transaction volume? |
| User Behavior | When does peak user activity occur? |

* * *

## Headline Results

| Metric | Value |
|----------|--------|
| Total Transaction Value | ₹3.47bn |
| Total Transactions | 108K |
| Total Users | 45K |
| Success Rate | 93% |
| Analysis Period | 12 Months |

* * *

## Data Sources

The dashboard uses transaction data containing:

| Table | Description |
|---------|-------------|
| Transactions | Payment details |
| Users | Customer information |
| Services | Service categories |
| Payment Status | Success/Failure details |
| Date Table | Time intelligence calculations |

* * *

## Data Cleaning and Transformation

The following transformations were performed:

• Removed duplicate records

• Handled missing values

• Standardized data types

• Created date hierarchy

• Built calculated columns

• Established table relationships

* * *

## Data Modeling

A star schema model was created with:

- FactTransactions as the main fact table
- User dimension
- Service dimension
- Date dimension
- Payment status dimension

Relationship type:

One-to-many relationships between dimensions and fact table.

* * *

## Calculated Measures

Key DAX measures used:

**Total Transaction Value**

```DAX
SUM(Transactions[Amount])
```

**Total Transactions**

```DAX
COUNT(Transactions[TransactionID])
```

**Average Transaction Value**

```DAX
DIVIDE(
SUM(Transactions[Amount]),
COUNT(Transactions[TransactionID])
)
```

**Success Rate**

```DAX
DIVIDE(
CALCULATE(
COUNT(Transactions[TransactionID]),
Transactions[Status]="Successful"
),
COUNT(Transactions[TransactionID])
)
```

* * *

## Dashboard Outputs

Dashboard includes:

1. KPI Cards
2. Transaction Trend Analysis
3. User Segmentation
4. Service Analysis
5. Payment Status Analysis
6. Interactive Filters
7. Business Insights Page

Dashboard Preview:

![PhonePe Dashboard](Dashboard.png)

* * *

## Insights

The analysis highlighted the following findings:

• Millennials contributed the largest share of transactions

• Successful transactions dominated total activity

• Certain services generated significantly higher transaction volumes

• User activity increased during weekends

• Monthly transaction values showed growth patterns

* * *

## Recommendations

• Improve failed payment handling mechanisms

• Focus marketing on high-engagement user segments

• Promote high-performing services

• Analyze peak activity periods for business opportunities

* * *

## Repository Structure

PhonePe-Analytics-Dashboard/

├── README.md

├── report/

│ └── PhonePeDashboard.pbix

├── outputs/

│ └── Dashboard.png

├── documents/

│ └── Dashboard.pdf

* * *

## Tools and Technologies

• Microsoft Power BI

• Power Query

• DAX

• Data Modeling

• Data Visualization

* * *

If you found this project useful, consider starring the repository ⭐
