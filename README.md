Executive Summary

This project analyzes a bank marketing campaign dataset to evaluate marketing funnel performance and identify conversion bottlenecks. Using Power BI, key metrics such as conversion rate, campaign effectiveness, and channel performance were calculated.

The analysis highlights major drop-off stages in the marketing funnel and provides actionable business recommendations to improve subscription rates and optimize campaign strategy.

Business Problem

The bank conducted direct marketing campaigns to promote term deposit subscriptions. However, the conversion rate remained low despite multiple customer contacts.

The objective of this project is to:

Identify funnel drop-offs

Analyze marketing channel performance

Evaluate campaign intensity impact

Provide data-driven recommendations to improve conversions

 Dataset Description

Dataset Used: bank-additional-full.xlsx

The dataset contains customer demographic and campaign information including:

Age

Job

Marital Status

Education

Contact Type (Cellular / Telephone)

Campaign Calls (Number of contacts)

Previous Campaign Outcome (poutcome)

Subscription Status (y – Yes/No)

Target Variable:

y = yes → Customer subscribed (Final Conversion)

 Marketing Funnel Definition

Since this dataset represents campaign performance, the funnel was defined as:

 Total Customers
 Contacted Customers
 Previous Campaign Success
 Subscribed Customers (y = "yes")

This structure allows analysis of conversion drop-offs across stages.

 Key Performance Indicators (KPIs)

The following DAX measures were created in Power BI:

Total Customers
Total Customers = COUNTROWS('Bank Data')
Total Subscribed
Total Subscribed =
CALCULATE(
    COUNTROWS('Bank Data'),
    'Bank Data'[y] = "yes"
)
Conversion Rate
Conversion Rate =
DIVIDE([Total Subscribed], [Total Customers]) * 100
Previous Campaign Success
Previous Success =
CALCULATE(
    COUNTROWS('Bank Data'),
    'Bank Data'[poutcome] = "success"
)
Average Campaign Calls
Avg Campaign Calls =
AVERAGE('Bank Data'[campaign])
Dashboard Overview

The Power BI dashboard includes:

KPI Cards (Total Customers, Total Subscribed, Conversion Rate, Avg Campaign Calls)

Funnel Chart (Customer → Contact → Previous Success → Subscription)

Channel Performance Analysis (Cellular vs Telephone)

Monthly Conversion Analysis

Campaign Intensity Analysis

Customer Segment Analysis (Job, Education, Age)

 Key Insights

Overall conversion rate is relatively low compared to total contacts.

Cellular marketing performs better than telephone outreach.

Customers with previous successful campaign outcomes show higher subscription probability.

Excessive campaign calls negatively impact customer responsiveness.

Certain months demonstrate stronger subscription trends.

Specific job and education segments have higher conversion performance.

 Business Recommendations

Focus marketing efforts on cellular contact channels.

Reduce excessive repeat calls to prevent customer fatigue.

Retarget customers with previous successful interactions.

Optimize campaigns during high-performing months.

Personalize offers for high-converting customer segments.

Implement A/B testing to improve messaging effectiveness.

Tools Used

Power BI Desktop

DAX (Data Analysis Expressions)

Power Query (Data Cleaning)

Microsoft Excel

 Future Improvements

Apply predictive modeling to estimate subscription probability.

Perform ROI analysis for campaign cost optimization.

Develop drill-through reports for deeper customer segmentation.

Implement machine learning classification models.

 Conclusion

This project demonstrates how marketing campaign data can be transformed into actionable insights using Power BI. By identifying funnel drop-offs and analyzing channel performance, businesses can optimize their marketing strategies and improve customer conversion rates effectively.


Tell me what you need 😊📊
