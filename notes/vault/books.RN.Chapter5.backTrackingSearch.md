---
id: 9o6m8u88cx7jxx16vhnr421
title: Backtracking Search
desc: ''
updated: 1647765733274
created: 1647589327599
---
This is an algorithm that works for partial assignments([[books.RN.Chapter5.definingConstraintSatisfactionProblems]]). 

With this algorithm we notice that we want to remove where values assigned to variables reach the same partial assignment regardless of the order.

#### Algorithm
![](/assets/images/2022-03-18-08-46-55.png)

This is an algorithm that uses the Depth-first search. This algorithm repeatedly chooses an unassigned variable, and then tries all values in the domain of that variable in turn, trying to find a solution.

We have before added heuristics in order to improve the performance of the algorithm. It turns out that we do not need to here:

![](/assets/images/2022-03-18-08-49-44.png)
![](/assets/images/2022-03-18-08-49-56.png)
