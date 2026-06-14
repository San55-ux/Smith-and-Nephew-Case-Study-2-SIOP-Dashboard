# Smith-and-Nephew-Case-Study-2-SIOP-Dashboards
Candidate Details

Name: Sanjay D
Role Applied: Analytics Intern
Tool Used: Microsoft Power BI Desktop

Project Overview

This dashboard was developed as part of the Smith & Nephew Analytics Internship Assessment. The objective of the case study was to analyze Sales, Inventory and Operations Planning (SIOP) forecast data and build an interactive Power BI dashboard that enables business users to compare forecast snapshots, evaluate forecast performance, and gain insights into Revenue, Non-Revenue, and CAPEX forecasts.

Data Sources

The dashboard uses the following datasets provided in the assessment:

Forecast Dataset

Contains:

Country
Item
AsOfPeriod
Period
Revenue Forecast
Non Revenue Forecast
CAPEX Forecast
Actual Dataset

Contains:

Country
Item
Period
Actual Revenue Quantity
Actual Non-Revenue Quantity
Actual CAPEX Quantity
Data Preparation

The following steps were performed:

Imported Forecast and Actual datasets into Power BI.
Loaded and transformed data using Power Query.
Validated forecast and actual values.
Created relationships between forecast and actual datasets.
Developed calculated measures and KPI metrics.
Built interactive visualizations and slicers.
DAX Measures Used
1. Forecast Accuracy %
Forecast Accuracy % =
1 -
DIVIDE(
    ABS(
        SUM(Forecast[Revenue Forecast]) -
        SUM(Actual[Actuals___Revenue_Qty])
    ),
    SUM(Actual[Actuals___Revenue_Qty])
)
Purpose

Measures how accurately forecasted revenue matches actual revenue.

2. Forecast Bias %
Forecast Bias % =
DIVIDE(
    SUM(Forecast[Revenue Forecast]) -
    SUM(Actual[Actuals___Revenue_Qty]),
    SUM(Actual[Actuals___Revenue_Qty])
)
Purpose

Measures forecast overestimation or underestimation compared to actual revenue.

3. Lag Type Classification
Lag Type =
SWITCH(
    [AsOfPeriod],
    "2023 P12", "Resultant",
    "2023 P11", "Lag 0",
    "2023 P10", "Lag 1"
)
Purpose

Classifies forecast snapshots into:

Resultant
Lag 0
Lag 1

for comparative forecast analysis.

4. Total Revenue Forecast
Total Revenue Forecast =
SUM(Forecast[Revenue Forecast])
5. Total Non-Revenue Forecast
Total Non Revenue Forecast =
SUM(Forecast[Non Revenue Forecast])
6. Total CAPEX Forecast
Total CAPEX Forecast =
SUM(Forecast[CAPEX Forecast])
Dashboard Features
KPI Cards

The dashboard includes the following KPI indicators:

Total Revenue Forecast
Total Non-Revenue Forecast
Total CAPEX Forecast
Forecast Accuracy %
Forecast Bias %
Interactive Filters (Slicers)

Users can filter dashboard results using:

AsOfPeriod
Country
Lag Type
Visualizations
Revenue Forecast by Country

Displays forecasted revenue distribution across countries.

Non-Revenue Forecast by Country

Displays forecasted non-revenue distribution across countries.

CAPEX Forecast by Country

Displays forecasted CAPEX distribution across countries.

Detailed Forecast Table

Provides detailed forecast values by:

Country
AsOfPeriod
Revenue Forecast
Non-Revenue Forecast
CAPEX Forecast
Business Insights

The dashboard enables users to:

Compare forecast performance across countries.
Analyze Revenue, Non-Revenue, and CAPEX forecasts.
Evaluate forecast accuracy and forecast bias.
Compare forecast snapshots using Lag Type classification.
Perform interactive analysis through slicers and filters.
Deliverables

The following files are included in the submission:

Power BI Dashboard (.pbix)
README Document
Dashboard Screenshots
Software & Technologies Used
Microsoft Power BI Desktop
Power Query
DAX (Data Analysis Expressions)
Microsoft Excel

Conclusion

The SIOP Reporting Dashboard provides an interactive and scalable reporting solution for forecast analysis. The dashboard enables users to evaluate forecast performance, compare forecast snapshots, and gain meaningful business insights through KPI-driven visualizations and interactive filtering capabilities.