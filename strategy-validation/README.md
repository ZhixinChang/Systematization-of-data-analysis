# Strategy-validation
Methodology for verifying the effectiveness of optimization strategies.

## Business issues
- Experimental preparation: How many samples are needed for strategy validation, how many experimental groups and control groups?
- Experimental period: How long can a confidence conclusion be obtained?
- Evaluation impact: Does the optimization strategy have a positive or negative impact on business indicators?

## How to solve problems?
### Data driven value presentation
| Demand scenario | Input | Output | Analytical ability |
|:---------------:|-------|--------|--------------------|
| Experimental preparation | 1. Alpha (Type-I error).<br>2. Beta (Type-II error).<br>3. Treatment Share.<br>4. Effect type.<br>4. Uplift to detect.<br>5. Key outcome metric type.<br>6. (Baseline Conversion) / (baseline mean and standard deviation). | 1. Total Sample Size.<br>2. Treatment Sample Size.<br>3. Control Sample Size. | Hypothesis testing. |
| Experimental period | - | - | The experimental period is usually at least one week, including weekdays and weekends.<br>1. When the impact amplitude is less than Uplift to detect and not significant after one week of observation, it indicates that the strategy has a weak impact and the experiment can be considered closed.<br>2. When the impact amplitude is greater than Uplift to detect and not significant after one week of observation, it indicates that the variance of the indicator is large, and it can be considered to continue observing for a period of time to wait for the data to stabilize. |
| Evaluation impact | Experimental data, including variables such as time, grouping, and indicators. | Conclusion on the degree and significance of strategic influence, including P-value and confidence interval. | CUPED, DID, inter group comparison, etc. |
