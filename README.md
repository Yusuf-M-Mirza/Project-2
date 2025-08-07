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
The dataset used consisted of a single table that contained all the data needed.
<div align="center">
  <img src="https://i.imgur.com/vb2yuBh.png" alt="TfL Cycle Hire" width="200" />
</div>

Prior to beginning my analysis, PowerQuery was used to clean and preprocess all of the data. It was also used to query the dataset. The data was then imported into Python as a .csv file and subsequently analysed. That left us with 3157 lines of clean, ordered, usable data.

## Executive Summary
### Overview of Findings
### Work Arrangement
Like it has been mentioned previously, since the pandemic, there has been an increased push towards remote working and its many supposed benefits. However, the data may show that to be untrue. 
<div align="center">
  <img src="https://i.imgur.com/DEPG10Z.png" alt="TfL Cycle Hire" width="650" />
</div>

In the professional world, an overall metric for job satisfaction can be measured by levels of 'burnout'. Coined by psychologist Herbert Freudenberger in the 1970s, it describes the consequences of prolonged stress and exhaustion, particularly within careers. Levels of burnout can be rated as either 'High', 'Medium' or 'Low', and the chart above indicates in what proportions these levels are present based upon each working arrangement.
As can be seen, Remote workers have an extremely high proportion of people ranked with 'High' burnout as opposed to Onsite and Hybrid employees. A far better method to quantify this would be giving each 'High', 'Medium' and 'Low' value a denomination of 2,1 and 0 respectively; tallying them up and comparing them.
<div align="center">
  <img src="https://i.imgur.com/DEPG10Z.png" alt="TfL Cycle Hire" width="650" />
</div>
