---
id: i87755r3yzb7eomu2pa9ype
title: 5. Chapter - Constraint Satifaction Problems
desc: ''
updated: 1647587080972
created: 1647586812047
---
This chapter is about the *Constraint Satisfaction problems*. So what is a constraint satisfaction problem you ask?

>"Constraint satisfaction problems (CSPs) represent a state with a set of variable/value pairs and represent the conditions for a solution by a set of constraints on the variables. Many important real-world problems can be described as CSPs." - Book RN, Ch. 6.6

We are going more in depth on what it is in the other sub pages.

# Summary

- Constraint satisfaction problems (CSPs) represent a state with a set of variable/value pairs and represent the conditions for a solution by a set of constraints on the variables. Many important real-world problems can be described as CSPs.

- A number of inference techniques use the constraints to infer which variable/value pairs are consistent and which are not. These include node, arc, path, and k-consistency.

- Backtracking search, a form of depth-first search, is commonly used for solving CSPs. Inference can be interwoven with search.

- The minimum-remaining-values and degree heuristics are domain-independent meth- ods for deciding which variable to choose next in a backtracking search. The least- constraining-value heuristic helps in deciding which value to try first for a given variable. Backtracking occurs when no legal assignment can be found for a variable. Conflict-directed backjumping backtracks directly to the source of the problem.

- Local search using the min-conflicts heuristic has also been applied to constraint satis- faction problems with great success.

- The complexity of solving a CSP is strongly related to the structure of its constraint graph. Tree-structured problems can be solved in linear time. Cutset conditioning can reduce a general CSP to a tree-structured one and is quite efficient if a small cutset can be found. Tree decomposition techniques transform the CSP into a tree of subproblems and are efficient if the tree width of the constraint graph is small.
