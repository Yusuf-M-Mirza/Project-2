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

<p align="center">
  <img src="https://i.imgur.com/y64cyAT.png" alt="Burnout Levels" width="45%" />
  <img src="https://i.imgur.com/ioydxgr.png" alt="Aggregated Burnout Score" width="45%" />
</p>

<p align="center">
  <em>Figure 2: Burnout Levels across Work Arrangements (left) &nbsp;&nbsp;|&nbsp;&nbsp; 
  Figure 3: Aggregated Burnout Score by Work Arrangement (High=2,Medium=1,Low=0) (right)</em>
</p>



### Physical Illness
- **_"Working at Thasos contributes greatly towards the development of physical illness."_**
  
- **No significant link between work arrangement and increased presence of physical illnesses.** (Figure 4)

<div align="center">
  <img src="https://i.imgur.com/Sfd6lq9.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 4: Percentage with Physical Illness by Work Arrangement</em></p>
</div>
  
- **Figure 5 shows the _general_ statistical insignificance of job role on physical illness prevalence** across most jobs.

- Several careers show significantly higher rates of physical illnesses than when compared to others **suggesting that job role plays a _significant_ contribution**. 
  - UX Designers are **14.3% _higher_** than Digital Marketing Specialists.
  - IT Support / Financial Analyst
  - HR Manager / Project Manager

<div align="center">
  <img src="https://i.imgur.com/KQlUxpw.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 5: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

- **_"Advancements in the age of employees as well as the number of hours worked per week lead to higher rates of physical illness"_**.

- R² is **0.0066 for Age** & **0.0084 for Hours Per Week**. It shows there is practically no correlation between either of these variables and the prevalence of physical illness, which thus disproves the hypothesis for this dataset.

<div align="center">
  <img src="https://i.imgur.com/h8Hxvvj.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 6: Percentage with Physical Illness by Age & Hours</em></p>
</div>

The data shows us a clear link between specific job roles and a greater or lesser prevalence of physical illness. However, neither Age, Hours per Week, nor work arrangement has any significant impact. This suggests that the reason is beyond the scope of the dataset, which would therefore require more data collection. A theory is that all of these positions are desk jobs. Spending more time at a desk with poor posture and ergonomics can lead to increased physical strain. However, to say this is a problem specifically at Thasos is preemptive; without figures on industry standards, we cannot conclude.

### Mental Illness
- **_"Current working conditions at Thasos contribute greatly towards the development of mental illness."_**

- **Onsite employees are ~9% more likely to develop a mental health condition than both Remote _and_ Hybrid employees.** Although seemingly small, the difference is shown to be statistically significant in Figure 7.

- Figure 8 shows how social isolation can affect mental health, with either extreme being detrimental, suggesting a Hybrid working arrangement is the most beneficial.

<div align="center">
  <img src="https://i.imgur.com/KAQoFtG.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 7: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

<div align="center">
  <img src="https://i.imgur.com/FsbM7oG.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 7: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

- **Employees from both Africa and Asia are shown to have a statistically significantly higher risk of suffering from a mental illness.** With there being no significant difference across the remaining four regions.

<div align="center">
  <img src="https://i.imgur.com/SXYnhnU.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 8: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

- **_"A typical reflection of poor mental health is a greater number of hours per week worked by employees."_**

- **R² is 0.018 for Work-Life Balance and 0.0020 for Social Isolation.** There is no significant correlation between either of the two variables and Hours (representing hours worked per week). It refutes the hypothesis that working more hours per week harms either Work-Life Balance or Social Isolation.

- **R² is 0.030 for the correlation between Work-Life Balance and Social Isolation.** Although larger than the relationship between either variable and hours per week, it is still below a 0.05 alpha which allows us to write it off as insignificant.

- The data therefore suggests the hypothesis is indeed false.

<div align="center">
  <img src="https://i.imgur.com/fxWyJOZ.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 8: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>



