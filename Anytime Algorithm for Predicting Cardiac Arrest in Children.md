# Summary
The paper describesthe use of cardiac arrest in children in CICU using boosted regression trees traind on the EHR medical data. 
Since the algorithm makes use of the Anytime framework, the cardinality of the decision trees increases as new data is received.

The data collected for the model consists of EHR from 48 hours to the hour of cardiac arrest. Moreover, the data collected was 
discretized into bins using kmeans to accomodate data from children of different age groups. Finally, to allow for models to work
on sumbols instead of features, the data is converted into predicate logic. Once the data is collected, Statistical Relational Learning 
is used to create models for cardiac arrest. The model makes use of weakly generated regression trees to get the probability of the 
target getting a cardiac arrest. Since the model makes use of an anytime framework, regression trees trained on the new data are
concatenated to our current trees at each interval. The predicates added to the regression trees are ones that maximize the wighted
variance. 

The model is compared to ones where the regression tress are learned from scratch at each stage. the model learnt using concatenation
performs bettwe than the ones trained from scratch from all the data collected so far. The authors theorize that the better result
may be due to the fact that data coolected only few hours before the cardiac arrest may be more relevant to the data on hand.

# Positive Points
1. The model described in the paper is much more data efficient that
