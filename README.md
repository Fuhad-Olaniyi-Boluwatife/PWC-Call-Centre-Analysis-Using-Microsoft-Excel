# PWC Call centre Customer Care
## Introduction

In today’s world, good customer service is crucial for any business. It shapes how people see a company, builds loyalty, and keeps customers happy. That’s why improving customer support isn’t just about internal operations—it affects everyone who interacts with the business.

As part of a PwC Switzerland Virtual Internship Program through Forage, I worked on a Call Centre Trends Analysis project. Using real data, I analysed key metrics like:

- Calls answered, unanswered, resolved and unresolved, etc.

- Call duration and resolution rates

- Agent performance

- Customer satisfaction and Customer attended to per agent, etc.


I created an interactive Excel dashboard with filters, charts, and summaries to track monthly performance and agent productivity. This involved cleaning data, using Excel functions, and organising information clearly. The goal was to find ways to improve call centre efficiency and enhance customer experience.

https://github.com/user-attachments/assets/f3b2e987-d6bd-4294-9c29-b39fa7c93132



## Problem Statement

This project provides clear insights into customer service operations to help improve call centre performance. Here's what we track:

- **Overall Performance Snapshot** – A quick summary of call volume, agent activity, and customer behaviour to see how the call centre is doing as a whole.
- **Individual Agent Performance** – Tracks each agent’s stats, including call resolution rates and answered vs. missed calls, with filters to check performance by time of day (morning/afternoon/evening).
- **Call Trends Over Time** – Identifies patterns like busiest days of the week or month to help with staffing and resource planning.
- **Customer Problems & Solutions** – Lists common issues customers face and shows how many were resolved, helping measure how well agents handle problems.
- **Core Call Centre Metrics** – Key numbers like total calls, answered/missed calls, and resolved/unresolved issues to track overall efficiency.
- **Service Quality & Efficiency** – Measures like average call time, speed of answering, customer ratings (if available), and how many customers each agent helps per month.



## Tools used

**Microsoft Excel** (Power Query, Pivot Tables, VBA Macros, Data Visualization)

**Key Components**

- **Power Query**
  *The Data Engineer* – Automated transformation of raw call logs into structured datasets with consistent formatting.
- **Pivot Tables**
  *The Insight Generator* – Dynamic aggregation of call data into actionable agent performance metrics and operational trends.
- **VBA Macros**
  *The Efficiency Tool* – Single-command dashboard reset with full filter clearance and data refresh capabilities.
- **Data Visualization**
  *The Decision-Making Lens*:

- **Pie Charts**: Resolution rate effectiveness
- **Bar Charts**: Individual agent call throughput
- **Line Graphs**: Hourly/daily call volume patterns
- **Stacked Columns**: Customer issue categorization

## Data source

Data was provided by the PwC Switzerland Virtual Internship Program through Forage. The data contains a sheet with 5000 rows and 10 columns. [Dataset.xlsx](https://github.com/user-attachments/files/20140275/Dataset.xlsx)

![raw Data](https://github.com/user-attachments/assets/7fab2d14-d28b-4a12-b983-286b9fb71a2b)


## Data exploration and transformation

The dataset is nearly in its final cleaned form, with only minor amendments made to ensure data efficiency. These transformations were performed using Microsoft Excel's Power Query Editor.


![power query](https://github.com/user-attachments/assets/7191e0c0-1c05-4e9d-94e2-e325a9aa5eaf)


This include;

- **Dataset Comprehension**: Initial analysis to understand data structure and content.

- **Column Format Validation**: Ensuring each column maintains its correct data type and format

- **Time Period Categorization**: Created new column classifying calls into:

  - **Morning** (≤ 11:59 AM)
  - **Afternoon** (≤ 3:59 PM)
  - **Evening** (all other times)

  Implemented via Power Query M code:

  ```Power Query M formula language
  each if[Time] <= #time(11,59,59) then "Morning"
  else if [Time] <= #time(13,59,59) then "Afternoon"
  else "Evening"
  ```

- **Date Feature Extraction**: Derived day of week and month from date columns

- **Duration Standardization**: Added column converting average talk duration to seconds

![cappture 2](https://github.com/user-attachments/assets/7b980031-83fb-4a31-a453-ee8c1d34244e)


## Data Analysis and Visuals

Below is the dashboard I created
![Dashboard](https://github.com/user-attachments/assets/7d24d5a8-9d8d-4ca1-8dd3-6af3bb0c1b90)

[CLICK HERE TO DOWNLOAD](Dashboard.xlsm)

### **From the dashboard, it is observer that**
1. ### **Call Volume Summary (January - March)**

   - **Total Calls Recorded:** 5,000

   - **Answered Calls:** 4,054 (81.08% answer rate)

   - **Unanswered Calls:** 946 (18.92%)

   - **Resolution Performance:**
     - Resolved Calls: 3,646 (90.0% of answered calls)
     - Unresolved Calls: 408 (10.0% of answered calls)
![kpi's](https://github.com/user-attachments/assets/c33e3a4e-e571-4566-a13c-4694ee8d4f77)


       
