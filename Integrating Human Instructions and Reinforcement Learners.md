# Summary

## Introduction
The paper mainly talks about the use of Statistical Relational Learning to allow for more natural language instructions for teaching an agent. Instead of providing tne agent with concise instructions, the agent makes out the meaning of instructions iteself.

## Model 
### Domain
The approach is used on the Sorter domain which involves putting collected objects in the correctly colored boxes. The state space for the sorter domain encapsulates the color of the boxes and baskets, the fact whether an agent is carrying a particular object, and if the object is already in the basket.

### Learning
The model learning is done using Q-learning with options (modelled as SMDP) to allow the model to accomodate the stochasity in learning the actions and to learn the acions in a continous state space by discrtetizing the actions

## Instructions
Instuctions are defined as <br>
_inviolate external inputs to the RL agent which affect its decision making or direct its exploration or alter its belief on a policy._
<br>
There are two types of instructions that we are mostly concerned about
1. $\pi$



# Positive Points


# Negative Points
Some of the biggest isses and limitations regarding the current model are
1. The use of maximization of the confidence interval doesn't feel like the best method to select among the actions. It may be better to use a weighted sum to learn a better policy
  1. Without evidence, this may be the reason why the current instruction denoted actions are chosen less as compared to other actions as the number of episodes increase
2. The current instructions are limited to pointing instructions and do not allow for more complex advice like _Pickup the ball and drop it in the basket_
3. There seems to be inconsitencies with the predicates in the paper which limits comprehension.

# Extensions
1. Extending the framework to allow for more complex instructions and better measures of confidence (instead of maximization) should allow us to increase the overall performance of the model
