# 💻 The Hidden Cost of Overwork: A Data-Driven Analysis
## Project Background
The company name is Thasos. We are a large pharmaceutical company that operates across all six populated continents. It was recently discovered that, although we aim to hire top talent to remain at the cutting edge of our industry, we experience high rates of employee turnover. The issue is of such concern that the Data Analytics team was given the task of finding out both **_why_** employees were leaving, but also **_what_** emergency measures could be implemented to resolve this issue as soon as possible.

The team chose to research **three key areas** and discover their influencing variables to enact swift change:
- Burnout
- Physical Illness
- Mental Illness

## Data Structure & Initial Checks
The dataset constructed came from surveys that were sent company-wide, as shown in Figure 1.
<div align="center">
  <img src="https://i.imgur.com/vb2yuBh.png" alt="TfL Cycle Hire" width="200" />
  <p><em>Figure 1: Entity-Relationship Diagram of Dataset</em></p>
</div>

Prior to beginning the analysis, PowerQuery was used to clean and preprocess all of the data. It was also used to query the dataset, leaving us with 3157 lines of clean, ordered, usable data. The data was then imported into Python and subsequently analysed.

## Executive Summary
### Overview of Findings

- The optimal working arrangement is **_Hybrid_**. It manages to balance between the high levels of social isolation prevalent amongst Remote workers and the high rates of mental illness amongst Onsite workers.

- In the regions of both Africa & Asia, rates of mental illness are shown to be abnormally high relative to the other regions. This is most likely due to the intense work culture ingrained within those societies, as well as their stigmatisation towards mental health. To counteract this, our company could enact more stringent policies to combat this problem. 

- Physical illness is shown to be a weak indicator of Burnout.
- Mental Illness is a weak indicator of Burnout.

- Demographic variables (age, salary, hours per week) have little change in the outcome of the presence of mental and physical health issues.

### Burnout

- **Burnout is a widely used metric for ranking employee satisfaction** based on many factors such as: workload, organisational culture, management practices and work-life balance, to name a few.

- **Remote workers are experiencing a statistically significant 37.8% higher burnout than their Onsite counterparts.** Thus backing the hypothesis:
  - **_"Work-arrangement is the most significant variable in determining levels of Burnout, with Remote employees experiencing it the most and Onsite employees experiencing it the least."_**

- Onsite working arrangements are therefore shown to be the best and most sustainable.

<p align="center">
  <img src="https://i.imgur.com/y64cyAT.png" alt="Burnout Levels" width="45%" />
  <img src="https://i.imgur.com/ioydxgr.png" alt="Aggregated Burnout Score" width="45%" />
</p>

<p align="center">
  <em>Figure 2: Burnout Levels across Work Arrangements (left) &nbsp;&nbsp;|&nbsp;&nbsp; 
  Figure 3: Aggregated Burnout Score by Work Arrangement (High=2,Medium=1,Low=0) (right)</em>
</p>



### Physical Illness
- **_"Poor physical health is a large contributing factor to burnout."_**
  
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

- **_"Advancements in the age of employees as well as the number of hours worked per week lead to higher rates of physical illness"_**.

- R² is **0.0066 for Age** & **0.0084 for Hours Per Week**. It shows there is practically no correlation between either of these variables and the prevalence of physical illness, which thus disproves the hypothesis for this dataset.

<div align="center">
  <img src="https://i.imgur.com/h8Hxvvj.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 6: Percentage with Physical Illness by Age & Hours</em></p>
</div>

The data shows us that the frequency of physical illness amongst employees provides no link to burnout whatsoever. Also, there is no link between Age, Hours Per Week and Work Arrangement to Physical Illness Prevalence. It can only then be linked to a variable that is beyond the scope of this dataset, since it seems highly unusual that physical ailments are equally present amongst 30-year-olds as they are amongst 60-year-olds.

### Mental Illness
- **_"Poor mental health is a large contributing factor to burnout. In combination, they can negatively affect rates of burnout to a high degree."_**

- **Onsite employees are ~9% more likely to develop a mental health condition than both Remote _and_ Hybrid employees.** Although seemingly small, the difference is shown to be statistically significant in Figure 7.

- Onsite working is therefore not the best arrangement possible. According to both Figure 7 and Figure 3 it is **_Hybrid_** working. In Figure 3 it is shown to have no significant difference between either Remote or Onsite, and in Figure 7, it is shown to minimise mental health illnesses.

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

- **_"A typical reflection of poor mental health is a greater number of hours per week worked by employees."_**

- **R² is 0.018 for Work-Life Balance and 0.0020 for Social Isolation.** It shows practically no significant correlation between either of the two variables and Hours (representing hours worked per week). It refutes the hypothesis that working more hours per week harms either Work-Life Balance or Social Isolation.

- **R² is 0.030 for the correlation between Work-Life Balance and Social Isolation.** Although larger than the relationship between either variable and hours per week, it is still below a 0.05 alpha which allows us to write it off as insignificant.

- The data therefore suggests the hypothesis is indeed false.

<div align="center">
  <img src="https://i.imgur.com/fxWyJOZ.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 8: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>



