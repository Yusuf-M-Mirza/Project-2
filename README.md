# 💻 The Hidden Cost of Overwork: A Data-Driven Analysis
## Project Background
If the COVID-19 pandemic has taught us anything, it taught us how remote work was shown to be a viable alternative to the previous status-quo of onsite employment. Employees could find themselves eliminating their daily commute to oftentimes crowded office spaces that would usually take [54 minutes](https://www.gov.uk/government/statistics/transport-statistics-great-britain-2022/transport-statistics-great-britain-2022-domestic-travel) out of the day. Foregoing this aspect of the professional world has shown strong evidence of [improved productivity](https://hrnews.co.uk/how-remote-working-culture-improves-productivity-in-the-uk/), [mental health](https://www.analytics-365.com/blog/mental-health-benefits-of-remote-work/#:~:text=Remote%20and%20flexible%20work%20offer,mental%20health%20and%20business%20success.), as well as [job satisfaction](https://remote.com/blog/global-hr/global-work-life-survey).

Using the dataset provided, I will aim to test the validity of these claims. I will be looking into sociological factors of employees such as age, job role and salary and how they influence both physical and mental health. Those findings will then be provided in this report and will be concluded with an 'ideal arrangement' of how we can optimise physical and mental health based on each job in each industry.

Insights are provided investigating how each factor influences mental and physical health:

- **Work Arragement**
- **Age**
- **Job Role**
- **Hours Per Week**
- **Salary Range**

## Data Structure & Initial Checks
The dataset used consisted of a single table that contained all the data needed shown in Figure 1.
<div align="center">
  <img src="https://i.imgur.com/vb2yuBh.png" alt="TfL Cycle Hire" width="200" />
  <p><em>Figure 1: Entity-Relationship Diagram of Dataset</em></p>
</div>

Prior to beginning my analysis, PowerQuery was used to clean and preprocess all of the data. It was also used to query the dataset. The data was then imported into Python as a .csv file and subsequently analysed. That left us with 3157 lines of clean, ordered, usable data.

## Executive Summary
### Overview of Findings
### Burnout

- **Burnout is a widely used metric for ranking employee satisfaction** based on a number of factors such as: workload, organisational culture, management practices and work-life balance, to name a few.

- Remote employees report significantly higher levels of burnout relative to other groups:  
  - **37.8% higher** compared to onsite employees  
  - **13.8% higher** compared to hybrid employees  

- **Difference between Remote & Onsite employees is _statistically significant_.** Thus backing a the hypothesis:
  - **_"Work-arrangement is the most significant variable in determining levels of Burnout, with Remote employees experiencing it the most."_**

<p align="center">
  <img src="https://i.imgur.com/y64cyAT.png" alt="Burnout Levels" width="45%" />
  <img src="https://i.imgur.com/ioydxgr.png" alt="Aggregated Burnout Score" width="45%" />
</p>

<p align="center">
  <em>Figure 2: Burnout Levels across Work Arrangements (left) &nbsp;&nbsp;|&nbsp;&nbsp; 
  Figure 3: Aggregated Burnout Score by Work Arrangement (High=2,Medium=1,Low=0) (right)</em>
</p>



### Physical Illness
- **_"Poor physical health is a large contributing factor to burnout. In combination, they can negatively affect rates of burnout to a high degree."_**
  
- **Figure 4 shows no significant link between work arrangement and the prevalence of physical illnesses.** Which leads us to looking elsewhere for a potential link.

<div align="center">
  <img src="https://i.imgur.com/Sfd6lq9.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 4: Percentage with Physical Illness by Work Arrangement</em></p>
</div>
  
- **Figure 5 shows the _general_ statistical insignificance of job role on physical illness prevalence**.
  
- **UX Designer experiences 14.3% _higher_  percent than Digital Marketing Specialist** showing significantly higher rates of physical illness.

- **Aggregate burnout is as follows for each position (standard deviation = 4.66).** It shows the difference in burnout is insignificant, which refutes our first hypothesis that physical illness is a contributing factor to levels of burnout
  - Digital Marketing Specialists = **106.97**
  - UX Designers = **100.38**
  
-  **Onsite employment is most prevalent amongst UX Designers and Remote work is the least** (Figure 6). Supporting that remote work contributes _the most_ to burnout.
  
<div align="center">
  <img src="https://i.imgur.com/KQlUxpw.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 5: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>
<div align="center">
  <img src="https://i.imgur.com/KMuMfSE.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 6: Percentage Breakdown of Work Arrangements for Digital Marketing Specialists and UX Designers</em></p>
</div>

- **Advancements in the age of employees as well as the number of hours worked per week lead to higher rates of physical illness**.

- R² is **0.0066 for Age** & **0.0084 for Hours Per Week**. It shows there is practically no correlation between either of these variables and the prevalence of physical illness, which thus disproves the hypothesis for this dataset.

<div align="center">
  <img src="https://i.imgur.com/h8Hxvvj.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 6: Percentage with Physical Illness by Age & Hours</em></p>
</div>

The data shows us that the frequency of physical illness amongst employees provides no link to burnout whatsoever. Also, there is no link between Age, Hours Per Week and Work Arrangement to Physical Illness Prevalence. It can only then be linked to a variable that is beyond the scope of this dataset, since it seems highly unusual that physical ailments are equally present amongst 30-year-olds as they are amongst 60-year-olds.

### Mental Illness
- **_"Poor mental health is a large contributing factor to burnout. In combination, they can negatively affect rates of burnout to a high degree."_**

- **Onsite employees are ~9% more likely to develop a mental health condition than both Remote _and_ Hybrid employees.** Although seemingly small, the difference is shown to be statistically significant in Figure 7.

- It demonstrates an **inverse correlation** between mental health rates and burnout rates, shown in Figure 3.

<div align="center">
  <img src="https://i.imgur.com/KAQoFtG.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 7: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

- **Employees from both Africa and Asia are shown to have a statistically significantly higher risk of suffering from a mental illness.** With there being no significant difference across the remaining four regions.

- **Historically, these regions have a far more intensive work culture**. In factors outside the scope of the dataset impacting work culture, these regions would 

<div align="center">
  <img src="https://i.imgur.com/SXYnhnU.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 8: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

- A typical reflection of poor mental health is a greater number of hours per week worked by employees.

- **R² is **

<div align="center">
  <img src="https://i.imgur.com/fxWyJOZ.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 8: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

- There is also no statistically significant difference between work arrangements and the prevalence of mental illness. Standard deviation bars overlap.


