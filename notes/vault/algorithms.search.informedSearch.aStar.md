---
id: DmTpWuxO4Y2mco94nBFtD
title: A*
desc: ''
updated: 1644480555257
created: 1644480129935
---
This is the most known heuristic search form of the best-first search. 
It evaluates nodes by combining $g(n)$, which is the cost to reach the node, and $h(n)$ the cost to get from the node to the goal.

$f(n)=g(n)+h(n)$

In other words $h(n)$ is the estimated cost of the cheapest path from node $n$ to the goal. And $g(n)$ is the path cost from the start node to node $n$.

This algorithm is nearly identical to [[algorithms.search.uninformedSearch.uniformCostSearch]], but A* uses the $g+h$ instead of only $g$.

![](/assets/images/2022-02-10-09-07-19.png)

THIS IS NOT APART OF THIS???
![](/assets/images/2022-02-10-09-09-13.png)
