# PWC-Call-Centre-Customer-Care-Analysis-Using-Microsoft-Excel

### Table of content
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Tools used](#tools-used)
- [Data source](#data-source)
- [Data exploration and transformation](#data-exploration-and-transformation)
- [Data Analysis and Visuals](#data-analysis-and-visuals)
- [Conclusion](conclusion)


## Introduction
In today’s world, good customer service is crucial for any business. It shapes how people see a company, builds loyalty, and keeps customers happy. That’s why improving customer support isn’t just about internal operations—it affects everyone who interacts with the business.

As part of a PwC Switzerland Virtual Internship Program through Forage, I worked on a Call Centre Trends Analysis project. Using real data, I analysed key metrics like:
- Calls answered, unanswered, resolved and unresolved, etc.
- Call duration and resolution rates
- Agent performance
- Customer satisfaction and Customer attended to per agent, etc.

I created an interactive Excel dashboard with filters, charts, and summaries to track monthly performance and agent productivity. This involved cleaning data, using Excel functions, and organising information clearly. The goal was to find ways to improve call centre efficiency and enhance customer experience.


https://github.com/user-attachments/assets/0249d9fc-1b55-410c-ad3d-0538cfed64d3






## Problem Statement
This project provides clear insights into customer service operations to help improve call centre performance. Here's what we track:
- **Overall Performance Snapshot** – A quick summary of call volume, agent activity, and customer behaviour to see how the call centre is doing as a whole.
- **Individual Agent Performance** – Tracks each agent’s stats, including call resolution rates, call answered, call missed calls, with filters to check their monthly performance.
- **Call Trends Over Time** – Identifies patterns like busiest days of the week to help with staffing and resource planning.
- **Customer Problems & Solutions** – Lists common issues customers face and shows how many were resolved, helping measure how well agents handle problems.
- **Core Call Centre Metrics** – Key numbers like total calls, answered/missed calls, and resolved/unresolved issues to track overall efficiency.
- **Service Quality & Efficiency** – Measures like average call time, speed of answering, customer ratings, and how many customers each agent helps per month.





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
- **Column Format Validation**: Ensuring each column maintains its correct data type and format.
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
  
- **Date Feature Extraction**: Derived day of week and month from date columns.
- **Duration Standardization**: Added column converting average talk duration to seconds and many more.

![cappture 2](https://github.com/user-attachments/assets/7b980031-83fb-4a31-a453-ee8c1d34244e)

## Data Analysis and Visuals
Below is the dashboard I created

![Dashboard](https://github.com/user-attachments/assets/1a09f245-4114-4a06-9c83-42516758abcb)

[CLICK HERE TO DOWNLOAD](Dashboard.xlsm)

### **From the dashboard, it is observer that**
1. **Call Volume Summary (January - March)**
   - **Total Calls Recorded:** 5,000
   - **Answered Calls:** 4,054 (81.08% answer rate)
   - **Unanswered Calls:** 946 (18.92%)
   - **Resolution Performance:**
     - Resolved Calls: 3,646 (90.0% of answered calls)
     - Unresolved Calls: 408 (10.0% of answered calls)
       ![kpi's](https://github.com/user-attachments/assets/c33e3a4e-e571-4566-a13c-4694ee8d4f77)
     

2. **Number of Calls Per Agent (3-Month Period)**
   1. **Total Calls per Agent**
      - View each agent's total call volume over the 3-month period
      - Jim is the top-performing agent by overall call volume 

           ![call per agent](https://github.com/user-attachments/assets/733785f1-76da-4e54-9c79-3d1423acc1de)


   2. **Monthly Breakdown**
      - Compare monthly performance (e.g., see which agent handled the most calls in January)
      - Track consistency or fluctuations in agent productivity month-to-month. For example Jim which is the over top performance is the second in the month of january.

        ![Janu](https://github.com/user-attachments/assets/9a429358-7e7e-43b4-8956-e64504eac759)


3. **Agent Call Performance Analysis**: a selected agent can be pick from list of agent and see the agent performance over the cause of 3 months or a specfic month. for instance let take Martha's Performance Details.

   1. **Martha call outcome**
      - Total Answer Calls by Martha: 514
      - Call Resolution Rate: **89.69%**
   
        ![resolution rate](https://github.com/user-attachments/assets/06a47ecd-5a06-4ec2-ba72-c043ca324948)

      - **Detailed Breakdown of Martha's Answered Calls:**
        - Morning : 166 Resolved, 15 Unresolved (Total: 181)
        - Afternoon : 101 Resolved, 14 Unresolved (Total: 115)
        - Evening : 194 Resolved, 24 Unresolved (Total: 218)
        - **Total Answered = 461 + 53 = 514**;  461 Resolved (166+101+194), 53 Unresolved (15+14+24)
      
            ![image 2](https://github.com/user-attachments/assets/65b36a99-fe65-4782-8796-7640853e1a94)

      - **Detailed Breakdown of Martha's Unanswered Calls:**
        - Morning : 45
        - Afternoon : 28
        - Evening : 51
        - **Total Unanswered Calls :** 124 (45+28+51)

          ![image 3](https://github.com/user-attachments/assets/7acf2fef-c386-4eb6-bfc4-d76857677ec6)


   2. **Martha Call Discussion with Customer (Breakdown of her answered calls by topic)**
      This section shows the topics of Martha's calls and how many were resolved vs. unresolved for each:
      - **Technical:** 94 Resolved, 8 Unresolved
      - **Streaming:** 87 Resolved, 18 Unresolved
      - **Payment related:** 99 Resolved, 9 Unresolved
      - **Contract related:** 98 Resolved, 9 Unresolved
      - **Admin Support:** 83 Resolved, 9 Unresolved
        - **Totals from this section:** 461 Resolved (94+87+99+98+83), 53 Unresolved (8+18+9+9+9)
      
        ![image4](https://github.com/user-attachments/assets/b7061ea1-e863-452b-ac2a-7bf9bd58815a)

   3. **Martha Daily Call Trend**
      This line graph shows Martha's call volume for the duration of 3 month on a daily basis:

      - **months Minimum calls (Fri):** 72
      - **Maximum calls (Thu):** 112
       
          ![image5](https://github.com/user-attachments/assets/de19f995-5e07-4029-952c-bf19f68af429)

      *(Note: The data can still be filtered on a monthly basis - for example, when viewing January's results, we observe the agent received a minimum of 23 calls on Friday and reached a maximum of 39 calls on Monday. This monthly filtering capability enables detailed performance analysis while maintaining the option to assess the full three-month period.)*
      
      ![image5b](https://github.com/user-attachments/assets/a4628b6d-e3d2-44f0-bb28-a71c330a28eb)

    4. **Overall Average Performance Metrics**
    These metrics appear to be for the entire call centre or an average across agents:
    - **Average customer performance rating:** 3.47 (out of 5.0)
    - **Average customer Served per Month:** 171.3
    - **Average answering speed:** 69.49 sec
    - **Average call duration:** 223.7 sec
    
     ![image 6](https://github.com/user-attachments/assets/23e70a83-82ff-4af6-9b51-edc64096786d)


4. **Agent Performance Filtering**
The agent performance metrics can be:
- Filtered monthly to analyze individual month performance
- Reset to the full 3-month view to assess overall trend (Data represents January-March period)

  ![image7](https://github.com/user-attachments/assets/e24c90c8-de70-4d9d-93bb-240be67a5b25)

## Conclution 
This call center analysis project has provided valuable insights into customer service operations over a three-month period. The data reveals that, while the call center maintains a strong 81% answer rate and a 90% resolution rate, opportunities exist to enhance performance further. Key findings show variations in agent productivity, with top performers like Jim handling significantly higher call volumes. Additionally, time-based patterns indicate higher unresolved rates during the evenings, as more calls come in during that time for agents.

## Recommedation 
To further improve call center performance, two key initiatives should be implemented. First, a detailed survey should be conducted to analyze the root causes of unanswered calls, examining factors responsible. This investigation will enable targeted solutions to significantly reduce missed calls. Second, a comprehensive study of unresolved calls is needed to identify patterns in customer issues, agent knowledge gaps, and process breakdowns. The insights gained from this analysis will allow for focused training programs and workflow improvements to enhance problem resolution capabilities. Together, these measures will systematically address both call response rates and solution effectiveness, leading to measurable improvements in overall customer service quality.




​    

