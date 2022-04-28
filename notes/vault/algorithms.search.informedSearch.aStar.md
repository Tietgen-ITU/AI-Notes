---
id: DmTpWuxO4Y2mco94nBFtD
title: A*
desc: ''
updated: 1650529502942
created: 1644480129935
---
![](/assets/images/2022-02-10-11-37-47.png)

This is the most known heuristic search form of the best-first search. 
It evaluates nodes by combining $g(n)$, which is the cost to reach the node, and $h(n)$ the cost to get from the node to the goal.

$f(n)=g(n)+h(n)$

![](/assets/images/2022-02-10-11-38-12.png)

In other words $h(n)$ is the estimated cost of the cheapest path from node $n$ to the goal. And $g(n)$ is the path cost from the start node to node $n$.

This algorithm is nearly identical to [[algorithms.search.uninformedSearch.uniformCostSearch]], but A* uses the $g+h$ instead of only $g$.

![](/assets/images/2022-02-10-09-07-19.png)


# Admissible heuristic
![](/assets/images/2022-02-10-11-38-48.png)
It should never overestimate the cost. So that means if the distance to the goal is 13 then an admissible heuristic would give a result equal or less than that.

## A valid Heuristic
A valid heuristic is a heuristic where the goal node has a heuristic of 0 and that the heuristic is non-negative for all the other states.

# Consistent Heuristic
![](/assets/images/2022-02-10-11-41-45.png)
>**NOTE:** Just to add. If a node $a$ has a heuristic that is 13 then the distance between node $a$ and node $b$ (which is this c function) plus the heuristic from node $b$ to the goal has to be greater than or equal to 13 in order for that to be consistent. Remember this has to be true for all nodes. 


![](/assets/images/2022-02-10-11-42-20.png)

With consistent heuristic, every time it expands a node it has found an optimal path to that node.

This is nice because there is a lot of book keeping that we do not need to do, when we know that we have found an optimal path.
# Properties
![](/assets/images/2022-02-10-11-42-42.png)
$h^*(n)$ is the real distance.

The true issue with A* is the memory consumption.
# Example
![](/assets/images/2022-02-10-11-39-49.png)
![](/assets/images/2022-02-10-11-39-58.png)
![](/assets/images/2022-02-10-11-40-07.png)
![](/assets/images/2022-02-10-11-40-19.png)
![](/assets/images/2022-02-10-11-40-34.png)
![](/assets/images/2022-02-10-11-40-51.png)

THIS IS NOT APART OF THIS???
![](/assets/images/2022-02-10-09-09-13.png)
