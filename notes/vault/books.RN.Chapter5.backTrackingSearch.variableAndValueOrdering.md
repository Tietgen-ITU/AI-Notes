---
id: ytcvwkcfm8z5jt7a7mzz1x0
title: Variable and Value Ordering
desc: ''
updated: 1647590283996
created: 1647589848819
---
The backtracking algorithm contains the following line:

$var \leftarrow SELECT-UNASSIGNED-VARIABLE(csp)$

The simple solution is to just take the next unassigned variable in order. 
This is actually quite efficient. 
Now you can perform heuritics so you can define that order:

There is **minimum-remaining-values (MRV)** heuristic where it takes the variable with the fewest legal values. 

Then there is **degree heuristic** where it attempts to reduce the branching factor on future choices by selecting the variable that is involved in the largest number of constraints.

Then there is the opposite, which is called **Least constraining value**.
