# Credit-Card-Financial-Report-Dashboard
# What did I do in this project?
Ans:<br />
1. Developed interactive dashboards using transaction and customer data from an SQL database, to provide real-time insights.<br />
    2. Streamlined data processing & analysis to monitor key performance metrics and trends<br />
    3. Shared actionable insights with stakeholders based on dashboard findings to support the decision-making process.<br />
	
# Project report
# Objective
To develop a comprehensive credit card weekly dashboard that provides real-time insights  into key performance metrics and trends enabling stakeholders to monitor and analyze credit card operations effectively

# Data collection
Data was collected from an online open-source platform. 
Then it was imported in the SQL server using PostgreSQL.
After that the SQL server was connected to the Power BI. From there it was imported to the Power BI dashboards.
    If the SQL server data updates then the dashboard updates after refreshing the data in Power BI.

# Dax queries
current_week_revenue = CALCULATE(<br />
        &emsp SUM('public cc_detail'[revenue]),<br />
        FILTER(<br />
            ALL('public cc_detail'),<br />
            'public cc_detail'[week_num2]=MAX('public cc_detail'[week_num2])<br />
        )<br />
    )<br />
    <br />
prev_week_revenue = CALCULATE(<br />
        sum('public cc_detail'[revenue]),<br />
        FILTER(<br />
            ALL('public cc_detail'),<br />
            'public cc_detail'[week_num2]=MAX('public cc_detail'[week_num2])-1<br />
        )<br />
    )<br />
    <br />
     wow_revenue = DIVIDE(([current_week_revenue]-[prev_week_revenue]),[prev_week_revenue])<br />
# Dashboards
![image](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard/assets/108027559/da23340a-aa76-48d2-857c-e3b036581ce8)
![image](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard/assets/108027559/cb2c9d0d-41f8-4cb6-806d-dae290be41ae)
![Report_insights](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard/assets/108027559/deb688d9-b4db-47f0-97ed-fd2938e2647b)

# Insights in week 53:
## Week on Week change<br />
Revenue increase by 28.8%<br />
Total Transaction Amount & Volume increased by 35% and 3.4%<br />
Customer count increased by 12.8%<br />
## Overview of year to year change<br />
Overall revenue 56.5 Million<br />
Total interest is 8 Million<br />
Total Transaction amount is 45.5 Million<br />
Male customers are contributing more in revenue.<br />
Blue and Silver Credit Card holders are contributing 93% of overall transaction<br />
TX, NY and CA is contributing to 68%<br />
Overall Activation rate is 57.5%<br />
Overall Delinquent rate is 6.06%<br />

# Connect
linkedin (https://www.linkedin.com/in/mdlutfulkabir/)


