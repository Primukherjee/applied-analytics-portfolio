# When High Performers Still Leave: A Data-Driven View of Employee Turnover
I was trained in psychology to treat outcomes as clues, not explanations, which is why employee turnover has always bothered me more than most workplace metrics. Yet in organizational settings, I see patterns breaking that rule. In spite of those hitting targets, meeting expectations and being praised by supervisors, some still choose to leave. 

When employees quit while doing well, it raises questions. These moments point back to hidden pressures in the system. Stability does not always keep them around and the real cause hides earlier in the process. I didn’t start thinking about employee turnover because I love HR metrics. I started because the explanations always felt too neat. What leads someone to walk away?
## What I’m Curious About
What patterns appear when employees exit companies?

More specifically:
- Could it be that higher-rated performers walk away for reasons unlike those of their lower-rated performers?
  
- Do those just starting out face different stresses compared to employees who’ve been around longer in the organization?
  
- Do some teams see a sudden drop in employees in clusters despite solid individual metrics? Could quiet patterns beneath the surface explain it?

Instead of focusing on a single predictor, I plan to focus on how the context shifts the predictors' weight.
## Why This Matters to Me
Most of the time, turnover gets perceived as just a result or an outcome. An employee resigns, followed by some sort of reaction.
Looking at it through a systems lens, things seem a little backward. When people leave at similar points in their careers, again and again, that pattern hints at deeper issues. Perhaps due to how tasks are set up, what gets praised, or how goals are shared within a company. Seeing each departure as just a personal choice hides the underlying trends. What seems like individual moves might actually reflect steady pressures built into the system. 

This project is my attempt to look at turnover as a system-level signal rather than an individual failure. From a business perspective, retention patterns influence cost stability, and long-term performance outcomes.
## The Data
I’m using a publicly available HR analytics dataset sourced from Kaggle that includes information on employee tenure, performance ratings, engagement indicators, department, and attrition status.
I’m treating this data as illustrative rather than representative. What matters here is spotting trends that make sense alongside real workplace patterns about why employees leave organizations. If needed, I may also simulate small extensions of the data to test specific scenarios that aren’t fully captured in the original dataset.
## How I’m Approaching the Analysis
I’m keeping the analysis intentionally simple and interpretable. I plan to include:

- Looking at how turnover rates change across tenure and departments: People spend time on shifting jobs, leaving at different points. What department someone works at within an organization also shapes how long they stay.
  
- Looking at how turnover differs between top performers and low performers in an organization.
  
- Exploring how engagement relates to turnover differently depending on performance or career stage.
## What This Can’t Tell Us/Limitations
This is an exploratory analysis using cross-sectional and partially simulated data. Looking into patterns here means working with a snapshot of real information mixed, in some cases with made-up details. Though the numbers come from different sources, they help sketch out early observations without claiming full accuracy.
That means:
- I can’t make causal claims
  
- Measures may be noisy or incomplete
  
- Missing the real organizational context where such things happen
## Analysis and Findings
This project began as an attempt to understand how workforce data can be used to identify patterns behind employee turnover and translate those patterns into actionable insights. For this project, I worked with an employee attrition dataset to explore how different workplace factors might influence the likelihood of employees leaving an organization. I started by examining overall attrition rates and then explored how turnover varied across departments, overtime status, performance ratings, and tenure length. As the analysis progressed, I built visualizations to better understand how attrition probability shifted across groups. I found that employees working overtime had a significantly higher likelihood of leaving, and that the first few years at a company showed the highest turnover risk. I also compared whether high performers were still at risk under high workload conditions. To move beyond descriptive analysis, I built a logistic regression model to predict attrition using features such as age, income, job satisfaction, tenure, overtime status, work–life balance, and environment satisfaction. The model helped identify which variables had the strongest relationship with the likelihood of an employee leaving. Overtime emerged as the strongest positive predictor, while job satisfaction, environment satisfaction, and work–life balance were strong negative predictors, suggesting protective effects against turnover.

## What Should the Business Focus on Next?
The analysis suggests that attrition is not random. It clusters around structural pressure points.
Based on the findings, the organization should focus on:
• Overtime management policies
 Overtime emerged as the strongest positive predictor of attrition in the logistic regression model. This indicates that workload intensity directly increases exit probability. The company should audit workload distribution and introduce capacity buffers in high-pressure roles.
• Early-tenure employee support
 Attrition probability was highest in the first few years at the company. Structured onboarding programs and early mentorship initiatives may reduce early churn.
• Satisfaction drivers over compensation alone
 Job satisfaction and environment satisfaction showed strong negative coefficients. This suggests engagement factors may be more protective than income alone. Investment in team culture and manager training could yield better retention outcomes than purely financial incentives.
• High performer risk monitoring
 Even strong performers may exit under sustained pressure. Performance alone is not a retention guarantee. The organization should monitor burnout indicators among top contributors.
Retention should not be reactive. It should be structural.
