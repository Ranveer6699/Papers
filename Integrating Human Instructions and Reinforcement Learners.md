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
There are two types of instruction interpretations considered by the model at the same time. If we point at _Object 3_
1. $\pi$ Instructions: Instructions like _Goto Object 3_. These instructions affect the action taken by the agent directly
2. $\phi$ Instructions: These instructions reduce the state space considered by the model by ignoring all states not concerning object 3

## Algorithm Built 
Quoting directly from the paper:- 
1. _The algorithm is split into two phases. During the training phase, the learner accumulates instructions, if available, to be used later to train an instruction model. This model is used to select actions in the post-training phase._
2. _Models ˆΠπ and ˆ ΠΦ are learned using the training sets. Learning these models requires us to represent the probabilistic dependencies among attributes of the related objects. We use Markov Logic Networks (MLN) to perform the generalization as they can succinctly represent these dependencies resulting in sample-efficient learning and inferring._

## Results and Conclusions
1. The instruction framework generalizes well unlike Simple SMDP Q-learning
2. As the number of episodes increase, the increase in confidence level results in better performance of the instructions framework.
3. As the training proceeds, the control shifts from the instructions framework to the Q-learner due to increasing estimates.
4. The relative performance of $\pi$ and $\phi$ instructions is domain dependent
5. The current confidence performance measure is naive and doesn't well capture the relative performance of the models


# Positive Points
The model allows for the use of more natural language type instructions when instructing the agent. Since the agent uses multiple interpretations of the instruction allows for more efficient learning.

# Negative Points
Some of the biggest isses and limitations regarding the current model are
1. The use of maximization of the confidence interval doesn't feel like the best method to select among the actions. It may be better to use a weighted sum to learn a better policy
  Without evidence, this may be the reason why the current instruction denoted actions are chosen less as compared to other actions as the number of episodes increase
2. The current instructions are limited to pointing instructions and do not allow for more complex advice like _Pickup the ball and drop it in the basket_
3. There seems to be inconsitencies with the predicates in the paper which limits comprehension.

# Extensions
1. Extending the framework to allow for more complex instructions and better measures of confidence (instead of maximization) should allow us to increase the overall performance of the model
