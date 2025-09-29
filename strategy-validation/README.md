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
| Experimental period | - | - | Statistical testing and business understanding. The experimental period is usually at least one week, including weekdays and weekends.<br>1. When the impact amplitude is less than Uplift to detect and not significant after one week of observation, it indicates that the strategy has a weak impact and the experiment can be considered closed.<br>2. When the impact amplitude is greater than Uplift to detect and not significant after one week of observation, it indicates that the variance of the indicator is large, and it can be considered to continue observing for a period of time to wait for the data to stabilize. |
| Evaluation impact | Experimental data, including variables such as time, grouping, and indicators. | Conclusion on the degree and significance of strategic influence, including P-value and confidence interval. | CUPED, DID, inter group comparison, etc. |

### Data driven value transmission
1. **Clarify business issues and analysis objectives**. Understanding business requirements and identifying the problems that need to be analyzed and solved are crucial, which determines how to develop analysis plans and answer questions in the future.
2. **Clarify the representativeness of the data**. Before using data, understand the entire process of data processing from reporting to reporting, and clarify whether the data indicators have sufficient representativeness for the analysis objectives. Otherwise, unexpected analysis results may occur.
3. **Analyze the objectivity and rationality of the process**. Analysis should focus on the big picture and follow the principle of "potential cognitive set ->data validation ->cognition ->action optimization" rather than "subjective cognition already in mind ->attempting to find data validation ->the subjective cognition is valid ->action optimization". Due to the varying levels of expertise and perspectives on things among individuals, it is easy to overlook other more important factors, and the user base that is worth optimizing is usually limited, making it difficult to determine whether it is worth optimizing. On the contrary, when the user experience problem is significant enough to warrant optimization, the impact pattern can usually be captured in the data.
4. **Objective and rigorous conclusions**.
- 1. **Avoid using "AB experiment shows that xx index has an impact on business" or "reverse experiment shows that xx index is worth doing work"**. The experiment can only demonstrate that the optimized new strategy has an impact on business indicators, and further analysis and exploration are needed to determine how this strategy affects business indicators.
- 2. **Avoid cognitive rigidity**. Cognition comes from data conclusions, and as users' demands for experience change over time, historical cognition may not be applicable to the future. For example, optimizing xx performance indicators has brought business benefits, but further optimization may result in no benefits, which is in line with the basic understanding of diminishing marginal returns. Therefore, analysis needs to be continuously conducted, and cognition needs to be continuously updated.
- 3. **All data conclusions only represent possibilities**. All causal inferences will provide P-values and confidence intervals, which means that if the P-value is less than 0.05, it can only indicate a 95% probability that the indicator/strategy will have an impact, and even if no impact is later found, it is still interpretable. Similarly, if the P-value is greater than 0.05, it only indicates that there is no evidence to suggest that the indicator/strategy has an impact, but it does not mean that the indicator actually has no impact, and there is a 5% probability that the conclusion will be incorrect.
