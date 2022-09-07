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



# Positive Points

# Negative Points

# Extensions
