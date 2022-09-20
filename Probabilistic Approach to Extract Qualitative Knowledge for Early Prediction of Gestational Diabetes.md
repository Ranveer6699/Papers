## Sumamry
The paper talks about extracting qualitative influence (QI) statements from learned probabilistic models on the GDM dataset. The QI statements can be used to employ the relationship in Machine Learning in how changes in a one or more features may effect the target. The approach described in the paper focuses on extrating two types of QI statements; Monotonicity (Direct relationship) and Synergy (Interaction among influences) and sub-synergic influence. 

The paper describes **QuaKE** algorithm to extract the QI statements from the knowledge base. The QuaKE algorithm iterates over each feature, first computing its monotonic influence, and adding the corresponding monotonic statement to the rules subset if the influence is over a certain threshold. The algorithm conditions the current feature with the remaining feature, and calculates the Synergy Influence. If the Synergy Influence is over a certain threshold, the corresponding SI statement is added to the the rule set.

Comparing the influences learnt by the **QuaKE** with the prior provided by a medical expert to the ones learnt directly on the model (baseline), the monotonic influence learnt by the QuaKE algorithm align well with the prior knowledge, and learn influences for which the prior knowledge is uncertain.

## Positive Points
1. The model described by the paper learns useful QI statements 
2. The algorithm described is quite simple and concise

## Negative Points
1. It would have been better to have more than a single domain expert to validate the influences learnt. I think that additional domain knowledge may 
help us to deal with some of the influences for which the prior is not sure
2. Synergy is limited to influence between two variables.  

## Possible Extensions
1. Extend the framework to allow for synergy between 2 or more variables (user defined).
2. Looking into other type of constraints might be helpful
