# Summary

## Introduction
The paper wants to explore mitigating the biggest issues with RepRL :- RepRL (because of its high level planner) doesn't work on continous domains . The issue results in <br>
  1. RepRL not making use of DRL as efficiently as it could
  2. Not making use of multi modal data (data from multiple sources)

## Solution Proposed
To mitigate the issue, the architecture HDRepRL described in the paper <br>
  1. Uses information fusion to allow use of multi modal data
  2. Makes use of a Neuro Symbolic Architecture which 
     1. Deliberative High Level Planner
     2. Fast Learning Low level Deep Network

## Doubts and Questions
Not educated enough about DBNs and PRMs to know why they are not used for the problem
Would like to know more about latent predicates
