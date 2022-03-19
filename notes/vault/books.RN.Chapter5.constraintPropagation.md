---
id: wf7029vaichwfemwfql6com
title: Constraint Propagation - Inference in CSPs
desc: ''
updated: 1647589218334
created: 1647588557665
---
State space search in a regular search algorithm can do only one thing, and that is to search. However, in a CSP there is a choice: You can either search or do a specific type of inference which is called **constraint propagation**.

Constraint propagation is when you use the constraints to reduce the number of legal values for a variable. 

The key thing is **Local Consistency**. That is, if we treat each variable as a node in a graph and each binary constraint as an arc, then the process of enforcing local consistency in each part of the graph causes inconsistent values to be eliminated. 

# Node Consistency
Node consistency is if a variable (which is a node in the CSP network), if all the values in the variables domain satisfy its(i.e. variable) unary constraint.

So for example:

![](/assets/images/2022-03-18-08-36-49.png)

# Arc Consistency
The variable is arc-consistent if every value in its domain satisfies the variables binary constraints. 

![](/assets/images/2022-03-18-08-37-48.png)

#### Arc consistency algorithm
![](/assets/images/2022-03-18-08-38-18.png)

# Global Constraints
A Global constraint is one involving an arbitrary number of variabels. 