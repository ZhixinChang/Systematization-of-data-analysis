# Cognitive-insight
Methodology for data-driven value presentation and transmission before the project officially begins execution.

## Business issues
- Priority: Given business metrics and multiple actionable metrics, which actionable metrics are more important?
- Optimizing value: Does the performance indicator have an impact on business indicators?
- Optimization space: How much optimization space is there for work indicators?
- Anomaly detection: What dimension values do indicators perform better or worse, and what are the reasons for indicator fluctuations?

## How to solve problems?
- Data driven value presentation: using causal inference analysis to confront and answer business questions, driving value presentation.
- Data driven value transmission: rigorous data conclusions and sufficient information exchange ensure the full transmission of value.

### Data driven value presentation
Causality rather than correlation：the essence of business data requirements is to understand the causal relationships between various indicators, and causal inference is naturally developed to solve this problem. And the correlation may be biased by confounding factors.

| Demand scenario | Input | Output | Analytical ability |
|:---------------:|-------|--------|--------------------|
| Which indicators are more important among multiple performance indicators? | 1. Target indicators (business indicators).<br>2. Several intervention indicators (work indicators that require prioritization).<br>3. Logical relationship (business logic of the impact of work indicators on business indicators) | 1. Priority sorting.<br>2. Roughly estimated revenue. | SCM scheme based on observation data. |
| Does the performance indicator have an impact on business indicators? | 1. Target indicators (business indicators for target improvement).<br>2. Intervention indicators (work indicators that require judgment of business value).<br>3. Confusion indicators (potential factors affecting value judgments).<br>4. User characteristics (optional, attributes that may affect value). | 1. The degree and relationship of the impact of work indicators on business indicators.<br>2. Revenue estimation. | RCM scheme based on observational data/reversal experiments. |
| What is the optimization space for work performance indicators? | 1. Target indicators (business indicators for target improvement).<br>2. Intervention indicators (work indicators that require judgment of business value).<br>3. Confusion indicators (potential factors affecting value judgments).<br>4. User characteristics (optional, attributes that may affect value). | 1. The impact of work indicators on business indicators leaves room for optimization.<br>2. Revenue estimation. | RCM scheme based on observational data/reversal experiments. |
| Which scenarios of business indicators perform significantly better/worse than the overall market? | 1. Related dimensions and indicators.<br>2. Business indicators. | The dimension of significant improvement/deterioration in overall business indicators. | ML scheme based on observation data (supporting decoupling of cross dimensional impact contributions). |
| If there is a change in business indicators, which indicators/dimensions are the root causes of the abnormality? | 1. Related dimensions and indicators.<br>2. Business indicators.<br>3. Base period current judgment. | Indicators/dimensions that cause changes in business indicators. | 1. ML scheme based on observation data (supporting decoupling of cross dimensional impact contributions).<br>2. SCM scheme based on observation data.|


### Data driven value transmission
1. **Clarify business issues and analysis objectives**. Understanding business requirements and identifying the problems that need to be analyzed and solved are crucial, which determines how to develop analysis plans and answer questions in the future.
2. **Clarify the representativeness of the data**. Before using data, understand the entire process of data processing from reporting to reporting, and clarify whether the data indicators have sufficient representativeness for the analysis objectives. Otherwise, unexpected analysis results may occur.
3. **Analyze the objectivity and rationality of the process**. Analysis should focus on the big picture and follow the principle of "potential cognitive set ->data validation ->cognition ->action optimization" rather than "subjective cognition already in mind ->attempting to find data validation ->the subjective cognition is valid ->action optimization". Due to the varying levels of expertise and perspectives on things among individuals, it is easy to overlook other more important factors, and the user base that is worth optimizing is usually limited, making it difficult to determine whether it is worth optimizing. On the contrary, when the user experience problem is significant enough to warrant optimization, the impact pattern can usually be captured in the data.
4. **Objective and rigorous conclusions**.
- 1. **Avoid using "AB experiment shows that xx index has an impact on business" or "reverse experiment shows that xx index is worth doing work"**. The experiment can only demonstrate that the optimized new strategy has an impact on business indicators, and further analysis and exploration are needed to determine how this strategy affects business indicators.
- 2. **Avoid cognitive rigidity**. Cognition comes from data conclusions, and as users' demands for experience change over time, historical cognition may not be applicable to the future. For example, optimizing xx performance indicators has brought business benefits, but further optimization may result in no benefits, which is in line with the basic understanding of diminishing marginal returns. Therefore, analysis needs to be continuously conducted, and cognition needs to be continuously updated.
- 3. **All data conclusions only represent possibilities**. All causal inferences will provide P-values and confidence intervals, which means that if the P-value is less than 0.05, it can only indicate a 95% probability that the indicator/strategy will have an impact, and even if no impact is later found, it is still interpretable. Similarly, if the P-value is greater than 0.05, it only indicates that there is no evidence to suggest that the indicator/strategy has an impact, but it does not mean that the indicator actually has no impact, and there is a 5% probability that the conclusion will be incorrect.
