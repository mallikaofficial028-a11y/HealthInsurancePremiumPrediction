# HealthInsurancePremiumPrediction
Health Insurance Premium Prediction Using Linear Regression

**Problem Statement**
**_Business Context_**
BluePeak Health Plans is a mid-sized health insurance carrier headquartered in Nashville, TN, serving individual policyholders across the Southeast and Midwest.

BluePeak prices individual health policies using broad demographic bands (age group and region), a model that treats a 45-year-old non-smoking, healthy individual the same as a 45-year-old obese smoker in the same region. As healthcare costs have continued to rise post-ACA, this blunt approach is creating an adverse selection problem: price-sensitive low-risk customers are leaving for leaner competitors, while high-risk individuals, who are underpriced relative to their actual claims, are staying and renewing. The result is a worsening loss ratio that the actuarial team can see in claims data (approximately 1 in 5 high-risk applicants is currently underpriced by more than $3,000 in annual expected charges) but cannot systematically address with the current pricing infrastructure.

The underwriting team manually flags high-risk applications for override, but there are no consistent rules, no documented criteria, and no way to apply the process at scale during open enrollment when application volumes spike. The VP of Underwriting needs a model that predicts expected annual medical charges per applicant at the point of policy issuance using variables already collected on every application (age, BMI, smoking status, number of dependents, and region), so that pricing reflects actual individual risk rather than demographic averages.

**_Constraints:_**

_Process_: The manual flagging workflow has no documented criteria. Different underwriters apply different thresholds, making decisions inconsistent and difficult to defend to state regulators.

_Platform_: The current policy issuance system has no individual-level scoring capability. The model output will be delivered through a simple web-based scoring interface where underwriters enter five application fields, receive a predicted annual charge, and see an actuarially defined risk tier at the point of decision.

_People_: The actuarial team has experience with band-based pricing but no prior exposure to dynamic pricing based on predictive mathematical models. Adoption will require interpretable outputs rather than black-box scores.

**_Objective_**
Build a model that predicts individual annual medical charges using age, BMI, smoking status, number of dependents, and region, and identify which factors most strongly drive cost so that BluePeak can move from band-based pricing to individual risk-based pricing. The model must be interpretable enough for underwriters to explain a pricing decision to a policyholder or regulator and accurate enough to meaningfully differentiate low-risk from high-risk applicants.

**_Data Description_**
The dataset consists of the following key attributes:

age: Age of the insured individual.
children: Number of dependents.
smoker: Smoking status (yes / no).
region: Residential region (northeast, northwest, southeast, southwest).
plan: Selected insurance plan (Bronze, Silver, Gold).
charges: Insurance premium charged to the individual (target variable).
