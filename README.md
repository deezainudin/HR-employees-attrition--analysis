# HR-employees-attrition--analysis
👥 HR Employee Attrition Analytics Dashboard (Power BI). I created an interactive 3-page Power BI dashboard that analyses 5,000 employee records to show why people leave, which departments and roles lose the most staff, and which current employees are most at risk.
<img width="1231" height="698" alt="image" src="https://github.com/user-attachments/assets/6e05db09-df0d-4934-9cbc-f1096fb2a703" />



## Problem Statement

The company loses **17.9% of its workforce** (895 of 5,000 employees). Roughly **44% of those leavers were high performers** (rated 4 or 5), so the loss is costly. Leadership has no single view of **where attrition concentrates, which controllable factors drive it, and which current employees are most likely to leave next**.

## Objectives

1. **Baseline:** measure attrition overall and by department, job role, work mode and demographics.
2. **Drivers:** identify which factors (burnout, engagement, manager support, overtime, pay growth, promotion) separate leavers from stayers.
3. **Talent risk:** quantify the loss of high performers (regretted attrition).
4. **Early warning:** build a transparent, rule-based risk score to flag active employees who are at risk.
5. **Business impact:** estimate the financial cost of attrition with an adjustable assumption.
6. **Action:** turn the findings into specific, prioritised recommendations for HR.

## Dataset

- **Source:** Kaggle employee attrition HR dataset (`employee_attrition_hr_2026.csv`) https://www.kaggle.com/datasets/uditjain13/employee-attrition-and-hr-analytics-2026
- **Size:** 5,000 rows, 29 columns, no null values, no duplicate employee IDs
- **Target:** `attrition` (Yes / No): 895 leavers, 4,105 active

| Group | Columns |
|---|---|
| Demographics | age, gender, marital status, education level |
| Job | department, job role, job level, work mode |
| Compensation | monthly income, salary hike %, stock option level |
| Career | years at company, years since promotion, total working years, prior companies, training hours |
| Workload | overtime hours per week, business travel days, commute minutes |
| Sentiment | burnout, engagement, manager support, work-life balance (1-10 scores) |
| Performance | performance rating, last review score |
| AI context | uses AI tools at work, perceived AI job risk |

## Data Preparation

The dataset was already quite clean, so instead of spending too much time fixing missing values or duplicates, I focused more on checking data quality and making sure the data was reliable for analysis.

Some of the things I did:
- Checked all columns for missing values, duplicates and inconsistent entries.
- Reviewed data logic and identified records with inconsistencies and flagged the records.
- Kept extreme values, such as high overtime hours and salaries, as they could represent genuine employee situations.
- Reconciled the final dataset against the original source to make sure the employee count and attrition figures matched.
- Created categories and bands for easier analysis of factors such as burnout, overtime, engagement, manager support and salary hike.

## Dashboard Pages

| Page | Question | Contents |
|---|---|---|
| **1. Demographic** | Where is attrition highest? | KPI cards, attrition by department, work mode, marital status, job role and age band split by gender |
| **2. Drivers** | Why do people leave? | Gap cards (burnout, overtime, engagement, manager support, work-life balance) and attrition by band for each driver, coloured against the company average |
| **3. Risk & Action** | Who do we act on? | At-risk employees, estimated cost, risk by department, action list of high-risk active employees, recommendations |

### What are the drivers?
<img width="1221" height="691" alt="image" src="https://github.com/user-attachments/assets/7c8dee3e-3dea-4fd7-8e07-fcbe5fa05935" />

### Risk and Actions
<img width="1231" height="690" alt="image" src="https://github.com/user-attachments/assets/78f97eb8-252d-4897-b0f3-1d9417d85cca" />


## Key Insights & Findings

**Headline:** attrition is driven mainly by **workplace experience**, which the company can change. It is not driven by demographics or base pay.

| # | Finding | Evidence |
|---|---|---|
| 1 | **Burnout is the strongest driver** | Attrition rises from 4.7% (low burnout) to **52.2%** (severe). Leavers average 5.06 burnout vs 3.81 for stayers |
| 2 | **Disengagement** | 51.1% attrition among disengaged employees vs 3.9% among highly engaged |
| 3 | **Manager support** | 36.3% attrition with poor support vs 7.2% with excellent support |
| 4 | **Overtime has a threshold effect** | 11.7% at 0-5 hrs/week, 26.9% at 10-15 hrs, **38.3% at 15+ hrs** |
| 5 | **Work-life balance** | 40.7% with poor balance vs 5.7% with excellent balance |
| 6 | **Pay growth matters more than base pay** | 28.5% attrition when the last hike was under 8%, vs 11.4% at 15%+ |
| 7 | **Promotion stagnation** | Attrition climbs from about 14% (promoted within a year) to about 27% (4+ years without promotion) |
| 8 | **Hotspots** | Customer Support (24.1%) and Sales (20.0%) lead; Engineering (14.5%) and R&D (14.9%) are lowest. Support Team Lead (26%) and Support Specialist (25%) are the highest-attrition roles |
| 9 | **Work mode** | Onsite 21.2%, Hybrid 16.8%, Remote 14.7% |
| 10 | **High performers are leaving** | 394 of 895 leavers (**44%**) were rated 4 or 5 |
| 11 | **Risks compound** | Employees with high burnout, low engagement and low manager support together leave at **43%** (550 people, 27% of all leavers) vs 7% for those with none of the three |
| 12 |**What does not matter much** | Gender, marital status, education, business travel and training hours showed little effect on attrition |

Link to power BI : https://app.powerbi.com/groups/me/reports/6e704202-17e7-40df-a25b-a02ab52dafba?ctid=f86bb447-f88c-4336-9a65-f2477e72ee5f&pbi_source=linkShare


