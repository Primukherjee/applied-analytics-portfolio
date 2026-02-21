# When High Performers Still Leave: A Data-Driven View of Employee Turnover
I was trained in psychology to treat outcomes as clues, not explanations, which is why employee turnover has always bothered me more than most workplace metrics. Yet in organizational settings, I see patterns breaking that rule. In spite of those hitting targets, meeting expectations and being praised by supervisors, some still choose to leave. When employees quit while doing well, it raises questions. These moments point back to hidden pressures in the system. Stability does not always keep them around and the real cause hides earlier in the process. I didn’t start thinking about employee turnover because I love HR metrics. I started because the explanations always felt too neat. What leads someone to walk away?

## What I’m Curious About
What patterns appear when employees exit companies?
More specifically:
- Could it be that higher-rated performers walk away for reasons unlike those of their lower-rated performers?
- Do those just starting out face different stresses compared to employees who’ve been around longer in the organization? 
- Do some teams see a sudden drop in employees in clusters despite solid individual metrics? Could quiet patterns beneath the surface explain it?
Instead of focusing on a single predictor, I plan to focus on how the context shifts the predictors' weight.

## Why This Matters to Me
Most of the time, turnover gets perceived as just a result or an outcome. An employee resigns, followed by some sort of reaction.
Looking at it through a systems lens, things seem a little backward. When people leave at similar points in their careers, again and again, that pattern hints at deeper issues. Perhaps due to how tasks are set up, what gets praised, or how goals are shared within a company. Seeing each departure as just a personal choice hides the underlying trends. What seems like individual moves might actually reflect steady pressures built into the system. This project is my attempt to look at turnover as a system-level signal rather than an individual failure. From a business perspective, retention patterns influence cost stability, and long-term performance outcomes.

## The Data
I’m using a publicly available HR analytics dataset sourced from Kaggle.
Dataset size:
- 1,470 employees
- 35 variables
- Attrition rate ≈ 16% (237 employees left)

## How I’m Approaching the Analysis
- I'm looking at how turnover rates change across tenure and departments: People spend time on shifting jobs, leaving at different points. What department someone works at within an organization also shapes how long they stay.
- I am looking at how turnover differs between top performers and low performers in an organization.
- I am exploring how engagement relates to turnover differently depending on performance or career stage.
- Logistic regression modeling
- Structural composite index modeling

## What This Can’t Tell Us/Limitations
- I can’t make causal claims
- Measures may be noisy or incomplete  
- Missing the real organizational context where such things happen

## Analysis and Findings
- Overall attrition rate was found to be: ~16%
- Overtime employees showed significantly higher exit probability.
- Early tenure (first few years) showed the highest turnover concentration.
- Overtime was the strongest positive predictor in logistic regression, while job satisfaction, work-life balance, and environment satisfaction were strong negative predictors.

## Structural Composite Modeling:
I constructed composite structural indexes and extended the model after doing the initial regression analysis. I also created:
- Pressure_Index
- Overconfidence_Index
These don't just help in capturing isolated variables but also help capture accumulated strain.

## Pressure_Index:
It all combines where strain is detected by more higher values:
- Overtime (binary)
- WorkLifeBalance (reversed)
- EnvironmentSatisfaction (reversed)
- JobInvolvement
Now coming to descriptive statistics:
- Mean: 1.92, Min: 0.75, Max: 3.13, Std: 0.41
Also, when we compare attrition groups, employees who stayed: 1.89 and those who left: 2.05 which further shows that higher pressure is a factor that leads to higher attrition rates.

## Attrition by Pressure Quartiles
There were 4 pressure bands in this: low, moderate, high and extreme. The attrition rates observed were: 
- Low: 9.56%
- Moderate: 15.79%
- High: 17.08%
- Extreme: 25.42%
This shows that those employees from the extreme sector are much more likely to leave than the rest in the lower sectors. This further suggests that strain increases attrition risk.

## Overconfidence_Index
In this, there is a combination of PerformanceRating, PercentSalaryHike, JobSatisfaction (reversed), and EnvironmentSatisfaction (reversed) where it is all designed to test if dissatisfaction is something that employees mask when they are high performers. 
Statistics here are: Mean- 2.31, Range- 1.53 – 3.63.
Comparison across attrition rates: 
- Stayed: 2.28
- Left: 2.43
This shows that there was higher overconfidence signal on average in employees who left. This further shows that at a time when satisfaction is less, instability is not fully eliminated by performance strength.

## Logistic Probability Gradient:
So here using logistic regression on Pressure_Index + Overconfidence_Index, I predicted attrition probabilities where I found Low: 11.01%, Moderate: 14.38%, High: 19.24%, and Extreme: 25.68%. This goes to show that the findings from earlier are validated by the model probabilities where overall, it signifies that there is an increase in risk gradually before exits in the organization. 

## Model Evaluation
Accuracy was found to be 86% but it was also found, recall for attrition class = 0 as well as precision for attrition class = 0. The reason was due to the imbalance in class (only ~16% attrition cases) which leads me to say that this model ultimately is defaulting toward predicting stability. Further, I want to reiterate that my purpose here was validation and not classification performance. With instabilty, it is observed that there is alignment between coefficient directions and the probability gradients.

## What Should the Business Focus on Next?
In this analysis, I came to the conclusion that attrition is not random and it is clustering around pressure points. So based on findings, I think the organization should focus on:
- Overtime management policies since in the logistic regression model, overtime was found to be the most positive predictor which further indicates that intensity in the workload leads to higher exit probability. So I think the company should audit workload distribution in high pressure situations. 
- Early-tenure employee support since during the first few years of the organization, attrition was the highest in probability so early churn might be reduced by onboarding  and mentorship programs that are structured. 
- Satisfaction drivers over compensation alone
- Since there were strong negative coefficients across job satisfaction and environment satisfaction, this suggests that instead of focusing solely on income, engagement factors shouldn't be ignored and might prove to be more protective.
- The business should try to invest in team culture and manager training that could potentially lead to better retention outcomes.
- It should also focus on risk monitoring across especially high performers.
- Pressure_Index quarterly should also be monitored
- It should also identify employees in extreme pressure band and build dashboards signifying early warnings instead of only relying on post-exit analysis.
