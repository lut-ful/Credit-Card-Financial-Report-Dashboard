# Credit-Card-Financial-Report-Dashboard
# What did I do in this project?
Ans:
	1. Developed interactive dashboards using transaction and customer data from an SQL database, to provide real-time insights.
        2. Streamlined data processing & analysis to monitor key performance metrics and trends
        3. Shared actionable insights with stakeholders based on dashboard findings to support the decision-making process.
	
# Project report
## Objective
        To develop a comprehensive credit card weekly dashboard that provides real-time insights '<br>'  into key performance metrics and trends enabling stakeholders to monitor and analyze credit card operations effectively

## Data collection\
        Data was collected from an online open-source platform. 
        Then it was imported in the SQL server using PostgreSQL.
        After that the SQL server was connected to the Power BI. From there it was imported to the Power BI dashboards.
        If the SQL server data updates then the dashboard updates after refreshing the data in Power BI.

## Dax queries\
        current_week_revenue = CALCULATE(
            SUM('public cc_detail'[revenue]),
            FILTER(
                ALL('public cc_detail'),
                'public cc_detail'[week_num2]=MAX('public cc_detail'[week_num2])
            )
        )
        prev_week_revenue = CALCULATE(
            sum('public cc_detail'[revenue]),
            FILTER(
                ALL('public cc_detail'),
                'public cc_detail'[week_num2]=MAX('public cc_detail'[week_num2])-1\
            )
        )
        wow_revenue = DIVIDE(([current_week_revenue]-[prev_week_revenue]),[prev_week_revenue])\
## Dashboards
![image](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard/assets/108027559/da23340a-aa76-48d2-857c-e3b036581ce8)
![image](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard/assets/108027559/cb2c9d0d-41f8-4cb6-806d-dae290be41ae)
![Report_insights](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard/assets/108027559/deb688d9-b4db-47f0-97ed-fd2938e2647b)

## Insights in week 53:
        ### Week on Week change
                Revenue increase by 28.8%
                Total Transaction Amount & Volume increased by 35% and 3.4%
                Customer count increased by 12.8%
        ### Overview of year to year change
                Overall revenue 56.5 Million
                Total interest is 8 Million
                Total Transaction amount is 45.5 Million
                Male customers are contributing more in revenue.
                Blue and Silver Credit Card holders are contributing 93% of overall transaction\
                TX, NY and CA is contributing to 68%
                Overall Activation rate is 57.5%
                Overall Delinquent rate is 6.06%


                --------------------------------End--------------------------------



