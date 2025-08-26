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
- Hybrid employees exhibit lower burnout scores than remote workers, but slightly higher than onsite employees. On-site employees consistently report the lowest burnout levels  

- The shown correlation is inconclusive since it is a **self-reported, qualitative measure** with various confounding variables. This is supported by the **mass-overlap of standard deviations we see in Figure 3**.


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
  
- **Figure 4 shows the statistical insignificance of job role on physical illness prevalence** as a result of how a majority of all the error bars overlap.
  
- **UX Designer 14.3% _higher_ than Digital Marketing Specialist** showing significantly higher rates of physical illness.
  
-  **Onsite employment is most prevalent amongst UX Designers**. Showing that working remotely or in a hybrid position can actually hedge against the development of physical issues.
  
-  **Aggregate burnout points are higher amongst Digital Marketing Specialists**. This contrasts our first statement that physical illness is linked to burnout when in the case between these two roles, it is shown to be the opposite case.
<div align="center">
  <img src="https://i.imgur.com/KQlUxpw.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 4: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>
<div align="center">
  <img src="https://i.imgur.com/KMuMfSE.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 5: Percentage Breakdown of Work Arrangements for Digital Marketing Specialists and UX Designers</em></p>
</div>

- Very little significance between jobs and the prevalence of physical illness.
- We can then conclude that any illness an individual experiences is unrelated to the career.
- A theory could be that all of these positions are desk jobs and the illnesses such as eye strain, back pain and shoulder pain could all be a consequence of poor ergonomics in the work environment. However since the data does not provide any information based on employee work environment, this is left to assumption.

This then begs the question of what kind of _arrangements_ lead to poor physical health which can be demonstrated in Figure 5 below.

<div align="center">
  <img src="https://i.imgur.com/QDcJOiV.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 5: Percentage with Physical Illness by Work Arrangement</em></p>
</div>

- Across all 3 arrangements, there seems to be an equal proportion of people who suffer physically.
- We can then say it is in fact _not_ related to the working arrangement.

Within the dataset, there are only 2 possible variables that could affect the prevalence of physical illness. They are hours worked and age. Relating to what was said previously, it was suggested that physical ailments could be brought on by the strain of working at a desk for hours on end. A greater number of hours per week would naturally relate to a greater prevalence of illness. When coupled with how the body can deteriorate with age, if there is any sort of correlation, it should be clear.

<div align="center">
  <img src="https://i.imgur.com/4cgoMdY.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 6: Percentage with Physical Illness by Age</em></p>
  <img src="https://i.imgur.com/llqMaU3.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 7: Percentage with Physical Illness by Hours Worked Per Week</em></p>
</div>

- No clear correlation between prevalence of physical illness and hours or ages worked.
- Further confirmed by correlation coefficients calculated for each graph
- **0.0066** for Figure 6 and **0.0084** for Figure 7

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


