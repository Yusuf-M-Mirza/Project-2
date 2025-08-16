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
Like it has been mentioned previously, since the pandemic, there has been an increased push towards remote working and its many supposed benefits. However, the data may show that to be untrue. 
<div align="center">
  <img src="https://i.imgur.com/DEPG10Z.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 2: Burnout Levels across Work Arrangements</em></p>
  <img src="https://i.imgur.com/G1WzQxm.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 3: Aggregated Burnout Score by Work Arrangement (High=2, Medium=1, Low=0)</em></p>
</div>

- **'Burnout'** is a common metric of gauging job satisfaction amongst employees.
- Remote workers experience **37.8% _higher_** levels of burnout than onsite workers and **13.8% _higher_** than hybrid workers (Figure 3).
- Although the data is **suggestive**, it is inconclusive. There are _many_ other potential factors leading to higher rates of burnout that are unrelated to working arrangements.
- 'Burnout' is also a qualitative metric that is personal to each individual.

### Physical Illness
A large factor that can tie into burnout from a role is the prevalence of physical illnesses amongst employees. Having to live through physical pain whilst fulfilling a demanding position would naturally take a great mental toll upon the individual, which can lead to far more serious issues later down the line. Therefore, exploring where physical illness stems from and _if_ there is anything we can do about it is important.

<div align="center">
  <img src="https://i.imgur.com/KQlUxpw.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 4: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
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

Within the dataset, there are only 2 possible variables that could affect prevalence of physical illness. They are, hours worked and age. Relating to what was said previously, it was suggested that physical ailments could be brought on by the strain of working at a desk for hours on end. A greater number of hours per week would naturally relate to a greater prevalence of illness. When coupled with how the body can deteriorate with age, if there is any sort of correlation, it should be clear.

<div align="center">
  <img src="https://i.imgur.com/4cgoMdY.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 6: Percentage with Physical Illness by Age</em></p>
  <img src="https://i.imgur.com/llqMaU3.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 7: Percentage with Physical Illness by Hours Worked Per Week</em></p>
</div>

- No clear correlation between prevalence of physical illness and hours or ages worked.
- Further confirmed by correlation coefficients calculated for each graph
- **0.0066** for Figure 6 and **0.0084** for Figure 7

In conclusion, there is no way of knowing for certain, using our current datase,t what causes large prevalence of physical illness. However, the data _does_ reveal something quite telling. From the age of 20 to 70 years old, there is no change in physical illness amongst employees. What we would instead expect is that we would see an exponential _increase_ as workers are older. I believe this is due to our dataset being comprised exclusively of desk jobs as opposed to more physical jobs. This supports the theory of poor ergonomics meaning a potential change an employer could make is to ensure proper equipment for employees.



