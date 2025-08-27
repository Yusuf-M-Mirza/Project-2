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
- Poor physical health is a large contributing factor to burnout alongside poor mental health. In combination, they can negatively affect rates of burnout to a high degree.
  
- **Figure 4** reflects **Figure 3** in support of this hypothesis that in order of Remote, Hybrid and Onsite by how prevalent physical illness is amongst employees.

<div align="center">
  <img src="https://i.imgur.com/QDcJOiV.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 4: Percentage with Physical Illness by Work Arrangement</em></p>
</div>
  
- **Figure 5 shows the statistical insignificance of job role on physical illness prevalence** as a result of how a majority of all the error bars overlap.
  
- **UX Designer experiences 14.3% _higher_  percent than Digital Marketing Specialist** showing significantly higher rates of physical illness.

- **Aggregate burnout is as follows for each position (standard deviation = 4.66).** It shows the difference in burnout is insignificant, which refutes our first hypothesis that physical illness is a contributing factor to levels of burnout
  - Digital Marketing Specialists = **106.97**
  - UX Designers = **100.38**
  
-  **Onsite employment is most prevalent amongst UX Designers** (Figure 6). Thus supporting the previous findings that remote work contributes the most to burnout.
  
-  **Aggregate burnout points are higher amongst Digital Marketing Specialists**. This contrasts our first statement that physical illness is linked to burnout, when in the case between these two roles, it is shown to be the opposite and instead be linked to _working arrangement_.
<div align="center">
  <img src="https://i.imgur.com/KQlUxpw.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 4: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>
<div align="center">
  <img src="https://i.imgur.com/KMuMfSE.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 5: Percentage Breakdown of Work Arrangements for Digital Marketing Specialists and UX Designers</em></p>
</div>

- **Advancements in the age of employees as well as the number of hours worked per week lead to higher rates of physical illness**.

- Correlation coefficient is **0.0066 for Age** & **0.0084 for Hours Per Week**. It shows there is practically no correlation between either of these variables and the prevalence of physical illness, which thus dispproves the hypothesis for this dataset.

<div align="center">
  <img src="https://i.imgur.com/h8Hxvvj.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 6: Percentage with Physical Illness by Age & Hours</em></p>
</div>

In conclusion, there is no way of knowing for certain, using our current dataset, what causes the large prevalence of physical illness. However, the data _does_ reveal something quite telling. From the age of 20 to 70 years old, there is no change in physical illness amongst employees. What we would instead expect is that we would see an exponential _increase_ as workers are older. I believe this is due to our dataset being comprised exclusively of desk jobs as opposed to more physical jobs. This supports the theory of poor ergonomics, meaning a potential change an employer could make is to ensure proper equipment for employees.

### Mental Illness
Mental Health is a bad, bad thing.

<div align="center">
  <img src="https://i.imgur.com/IThdz7o.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 8: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

- Irrespective of cultural divides, there seems to be little difference in mental health on the region of employee.

<div align="center">
  <img src="https://i.imgur.com/fxWyJOZ.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 8: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

- There is also no statistically significant difference between work-arrangment and prevalence of mental illness. Standard deviation bars overlap.

<div align="center">
  <img src="https://i.imgur.com/KAQoFtG.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 8: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>


