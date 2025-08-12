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
### Work Arrangement
Like it has been mentioned previously, since the pandemic, there has been an increased push towards remote working and its many supposed benefits. However, the data may show that to be untrue. 
<div align="center">
  <img src="https://i.imgur.com/DEPG10Z.png" alt="TfL Cycle Hire" width="650" />
  <p><em>Figure 2: Burnout Levels across Work Arrangements</em></p>
  <img src="https://i.imgur.com/G1WzQxm.png" alt="TfL Cycle Hire" width="650" />
  <p><em>Figure 3: Aggregated Burnout Score by Work Arrangement (High=2, Medium=1, Low=0)</em></p>
</div>

- **'Burnout'** is a common metric of gauging job satisfaction amongst employees.
- Remote workers experience **37.8% _higher_** levels of burnout than onsite workers and **13.8% _higher_** than hybrid workers (Figure 3).
- Although the data is **suggestive**, it is inconclusive. There are _many_ other potential factors leading to higher rates of burnout that are unrelated to working arrangements.
- 'Burnout' is also a qualitative metric that is personal to each individual.

### Age




