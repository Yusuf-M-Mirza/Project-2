# 💻 The Hidden Cost of Overwork: A Data-Driven Analysis
## Contents
- Project Background
- Data Structure & Initial Checks
- Executive Summary
  - Overview of Findings
  - Burnout
  - Physical Illness
  - Mental Illness
- Recommendations
## Project Background
The company name is Thasos. We are a large pharmaceutical company that operates across all six populated continents. It was recently discovered that, although we aim to hire top talent to remain at the cutting edge of our industry, we experience high rates of employee turnover. The issue is of such concern that the Data Analytics team was given the task of finding out both **_why_** employees were leaving, but also **_what_** emergency measures could be implemented to resolve this issue as soon as possible.

The team chose to research **three key areas** and discover their influencing variables to enact swift change:
- **_Burnout_**
- **_Physical Illness_**
- **_Mental Illness_**

_Disclaimer: All findings are based upon self-reported survey data, thus showing associations and not direct causations._

## Data Structure & Initial Checks
The dataset constructed came from surveys that were sent company-wide, as shown in Figure 1.
<div align="center">
  <img src="https://i.imgur.com/vb2yuBh.png" alt="TfL Cycle Hire" width="200" />
  <p><em>Figure 1: Entity-Relationship Diagram of Dataset</em></p>
</div>

Prior to beginning the analysis, PowerQuery was used to clean and preprocess all of the data. It was also used to query the dataset, leaving us with 3157 lines of clean, ordered, usable data. The data was then imported into Python and subsequently analysed.

## Executive Summary
### Overview of Findings

- We found that a Remote working arrangement contributes the most to employee Burnout at Thasos. This can be linked to the high degree of social isolation experienced by those who work remotely. It is also linked to a lack of divide between the professional and personal elements of one's life that leads to an inability to compartmentalise appropriately once work has ended.

- Onsite employment also proved to be detrimental, but instead it was to mental health. The lack of autonomy, strenuous commute as well as the social pressures of an office environment are all contributing factors.

- **_Hybrid_** working arrangement is optimal (**balancing social isolation and mental health; [evidenced to reduce turnover by 33%](https://www.bps.org.uk/research-digest/hybrid-workers-are-more-satisfied-quit-less-onsite-workers) than working onsite**).

- Job role was shown to be the _only_ factor that influences physical illness, with factors such as Age, as well as Hours Per Week, being shown to be insignificant.

- Reducing rates of physical illness **_will_** reduce turnover as evidenced in [both](https://www.wilmarschaufeli.nl/publications/Schaufeli/204.pdf) of [these](https://pmc.ncbi.nlm.nih.gov/articles/PMC6163261) studies showing a direct correlation between higher MSD prevalence and how they're associated with a greater 'intention to leave' amongst employees.

- Mental health was also shown to be statistically significantly poorer in Asia and Africa than when compared to the other regions.

### Burnout
- **H₀: _"Working at Thasos does not lead to Burnout."_**

- **Burnout is a widely used metric for ranking employee satisfaction** based on many factors such as: workload, organisational culture, management practices and work-life balance, to name a few.

- **Remote workers are experiencing a statistically significant 37.8% higher burnout than their Onsite counterparts.** It is reflected in the correlating Social Isolation Scores, suggesting increased Social Isolation can be linked to greater levels of Burnout.

<p align="center">
  <img src="https://i.imgur.com/y64cyAT.png" alt="Burnout Levels" width="45%" />
  <img src="https://i.imgur.com/lk0YOwi.png" alt="Aggregated Burnout Score" width="45%" />
</p>

<p align="center">
  <em>Figure 2: Burnout Levels across Work Arrangements (left) &nbsp;&nbsp;|&nbsp;&nbsp; 
  Figure 3: Aggregated Burnout Score by Work Arrangement (High=2,Medium=1,Low=0) (right)</em>
</p>

- According to [DHR Global](https://www.staffingindustry.com/news/global-daily-news/82-of-workers-globally-experiencing-burnout-survey-says) and [Randstad](https://www.randstad.co.uk/market-insights/employee-engagement/state-workplace-wellbeing-across-globe), figures on Burnout rates globally are 82% and 63% respectively.

- If we count only Medium and High reported rates, as well as factor across all 3 working arrangements, Thasos has a company average of 76.5%. This proves **Burnout at Thasos is the typical industry-standard** and is not an exclusive issue. **_Fail to reject the null hypothesis_**.

- Burnout can also be caused by the working arrangement itself. GoRemotely.net [states](https://goremotely.net/blog/remote-working-statistics) that **84% of remote workers work from home**, and a [study](https://assets.eurofound.europa.eu/f/279033/f163d67b7f/ef1658en.pdf) conducted by Eurofound explained how working from home erodes work-home boundaries, leaving employees unable to properly compartmentalise.

### Physical Illness
- **H₀: _"Working at Thasos does not contribute towards the development of physical illness."_**
  
- **No significant link between work arrangement and increased presence of physical illnesses.** (Figure 4)

<div align="center">
  <img src="https://i.imgur.com/Sfd6lq9.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 4: Percentage with Physical Illness by Work Arrangement</em></p>
</div>
  
- **Figure 5 shows the _general_ statistical insignificance of job role on physical illness prevalence** across most jobs.

- Several careers show significantly higher rates of physical illnesses than when compared to others **suggesting that job role plays a _significant_ contribution**. 
  - UX Designers are **14.3% _higher_** than Digital Marketing Specialists
  - IT Support is **9.4% _higher_** than Financial Analysts
  - Project Managers are **6.1% _higher_** HR Managers

- Additionally, all illnesses named in the dataset are musculoskeletal diseases (MSDs) and are all related to poor ergonomics while working desk jobs:
  - **Eye Strain**
  - **Neck Pain**
  - **Shoulder Pain**
  - **Wrist Pain**
  - **Back Pain**

<div align="center">
  <img src="https://i.imgur.com/KQlUxpw.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 5: Prevalence of Physical Illness by Occupation (±2% Margin of Error)</em></p>
</div>

- A common explanation is that older employees are more likely to suffer from MSDs than their younger counterparts. Additionally, working longer hours leaves less time for self-care, leaving employees more prone.

- R² is **0.0066 for Age** & **0.0084 for Hours Per Week** (α=0.05). It shows there is practically no correlation between either of these variables and the prevalence of physical illness, which thus disproves the hypothesis for this dataset (Figure 6).

<div align="center">
  <img src="https://i.imgur.com/h8Hxvvj.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 6: Percentage bearing a Physical Illness by Age & Hours</em></p>
</div>

- **No clear link between any social variables and an increased risk of developing physical illness**. The only **_real_** indicator is the job role.

- It is still a company-wide epidemic. According to this [study](https://pmc.ncbi.nlm.nih.gov/articles/PMC10840111), **MSDs are present in 33.8% - 95.3% of the adult population globally**. That is a massive range. For _all_ jobs, the average is **91.1%**, suggesting a major problem at Thasos especially. **_We reject the null hypothesis_**.

- Although not available in this dataset, I would want to conduct a further investigation into what percentage of each shift is spent seated at a desk. The hypothesis we could propose is:
  - **_"A greater proportion of work spent seated at a desk correlates to a greater proportion of MSDs"_**

### Mental Illness
- **H₀: _"Current working conditions at Thasos do not contribute towards the development of mental illness."_**

- **Onsite employees are 9% more likely to develop a mental health condition than both Remote _and_ Hybrid employees.** The difference is shown to be statistically significant in Figure 7.

- Figure 8 shows how social isolation can affect mental health, with either extreme being detrimental, suggesting a Hybrid working arrangement is the most beneficial, with a majority focus on working in the office.

<div align="center">
  <img src="https://i.imgur.com/KAQoFtG.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 7: Percentage bearing a Mental Illness by Working Arrangement</em></p>
</div>

<div align="center">
  <img src="https://i.imgur.com/FsbM7oG.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 8: Percentage bearing a Mental Illness by Social Isolation Score</em></p>
</div>

- **Employees from both Africa and Asia are shown to have a statistically significantly higher risk of suffering from a mental illness.** With there being no significant difference across the remaining four regions.

<div align="center">
  <img src="https://i.imgur.com/SXYnhnU.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 9: Prevalence of Physical Illness by Occupation</em></p>
</div>

- A factor typically cited for worsening mental health is longer working hours.

- **R² is 0.018 for Work-Life Balance and 0.0020 for Social Isolation** (α=0.05). There is no significant correlation between either of the two variables and Hours (representing hours worked per week). It refutes the hypothesis that working more hours per week harms either Work-Life Balance or Social Isolation (Figure 10).

- **R² is 0.030 for the correlation between Work-Life Balance and Social Isolation** (α=0.05). Although larger than the relationship between either variable and hours per week is still insignificant.

<div align="center">
  <img src="https://i.imgur.com/fxWyJOZ.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 10:Prevalence of Mental Illness by Region</em></p>
</div>

- Another factor that can be cited is the sociological factors of Age and Gender on mental health within the Thasos work environment.

- In accordance with Figure 11 below, Male, Female and Non-Binary employees were plotted against their Age by the percentage of them who suffer from a mental illness. The results are below:
  - **Male:**
    - R = -0.052
    - P = 0.894
  - **Female:**
    - R = 0.330
    - P = 0.385
  - **Non-Binary:**
    - R = 0.176
    - P = 0.651

- **No statistically significant results.**
 
<div align="center">
  <img src="https://i.imgur.com/nLjWNLl.png" alt="TfL Cycle Hire" width="500" />
  <p><em>Figure 11: Prevalence of Mental Illness by both Age & Gender</em></p>
</div>

- **Working environment is far more influential on mental health than any other variables**. Factors such as hours per week, age or gender were all shown to play little to no role whatsoever.

- **Onsite employees were shown to be the worst affected by mental health** with commonly cited reasons being a [lack of autonomy](https://bmcpublichealth.biomedcentral.com/articles/10.1186/s12889-025-23794-x), [a draining commute](https://journals.sagepub.com/doi/10.1177/20413866221131404), as well as [social pressures](https://pubmed.ncbi.nlm.nih.gov/34659039/).

- Mental health is poorest in Africa and Asia, driven by ingrained work cultures and the stigma surrounding mental illness. These effects are not captured in variables such as Hours-Per-Week or Social Isolation, yet the pattern is unmistakable. In [Japan](https://www.ft.com/content/86bdcdd5-4b26-4cf2-b2e1-d0d460d88cca), [Singapore](https://sg.adp.com/about-adp/press-centre/40-percent-of-singapore-workers-feel-they-work-up-to-10-hours-of-unpaid-time-every-week.aspx), [China](https://www.ft.com/content/d5f01f68-9cbc-11e8-88de-49c908b1f264), and [South Korea](https://pmc.ncbi.nlm.nih.gov/articles/PMC5285313), cultures of unpaid overtime and toxic manager–employee dynamics intensify the problem. Combined with limited access to mental health support, these conditions explain the higher prevalence observed in the data.

- The [World Health Organisation](https://www.who.int/teams/mental-health-and-substance-use/promotion-prevention/mental-health-in-the-workplace) shows 15% of adults are suffering from a mental illness; far exceeding our **average of 62.5%** across all regions. Employment at Thasos _does_ worsen mental health. **_We reject the null hypothesis_**.

## Recommedations
- To _prevent_ Burnout from Remote working, Thasos should limit the number of future job postings that offer a Remote working option, as well as offering current Remote work employees the chance to work from the company office space; a [study](https://www.hcamag.com/asia/specialisation/benefits/is-hybrid-work-the-answer-to-widespread-burnout/493331) by HCAMag showed **75% of employees showed a significant reduction in burnout symptoms**. Since (Figure 3) there is no statistical difference in Burnout between Onsite and Hybrid working, switching Remote workers to Hybrid will yield similar results, whilst also being a far more adaptable change.

- To _prevent_ Mental Illness from Onsite working, Thasos should also limit future job postings from being exclusively in-office and attempt to offer greater flexibility. A [study conducted by BPS](https://www.bps.org.uk/research-digest/hybrid-workers-are-more-satisfied-quit-less-onsite-workers) showed a 33% reduction in turnover amongst employees who were Hybrid as opposed to Onsite. The participants in the Hybrid grouped worked a 3:2 day split between onsite and remote work, which as evidenced in **Figure 8**, is more optimal than 2:3 when balancing social isolation and mental health. Current onsite workers should therefore be offered a 3:2 split Hybrid arrangement if possible.

- Tackling MSDs involves heavily investing in more ergonomic working arrangements for _all_ employees. A [study by MDPI](https://www.mdpi.com/2077-0383/14/9/3034) **showed a positive impact across the back, shoulders, neck and wrists**; and this [study](https://www.emerald.com/shr/article/doi/10.1108/shr.2011.37210cab.006/354856/Reducing-the-impact-on-employers-and-employees-of) proved **a 22:1 return on investment shown in increased productivity** when coupled with a physiotherapist telephone triage.

- Free and confidential counselling services to support mental health would be highly beneficial. Its [implementation](https://psychology.iresearchnet.com/articles/employee-assistance-programs-and-mental-health-interventions-in-the-workplace) proved effective in boosting productivity and lowering employee turnover. Training senior leaders with mental health first aid was [shown](https://www.medrxiv.org/content/10.1101/2024.01.17.23300197v1.full) to provide **'a 10:1 return on investment'** through reduction of absenteeism.

- Studies by [WHO](https://www.who.int/news-room/fact-sheets/detail/mental-health-at-work) and [OECD](https://www.oecd.org/content/dam/oecd/en/publications/reports/2021/11/fitter-minds-fitter-jobs_81033d43/a0815d0f-en.pdf) confirm aggressively combating mental illness greatly reduces employee turnover.

- Implementation of all the above measures should lead to **_significant_** reductions in employee turnover.
