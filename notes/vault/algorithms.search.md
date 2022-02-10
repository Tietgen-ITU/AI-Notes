---
id: Yg1JFFmjjhW4znxORv0mD
title: Search
desc: ''
updated: 1644478331144
created: 1644476235535
---
In the book it says that there is a "template" of an algorithm that they generally follow:

![](/assets/images/2022-02-10-07-58-31.png)
![](/assets/images/2022-02-10-07-59-55.png)

>**Note:** that the highlighted black lines in the graph search is the additions to the "general" tree search algotihm

# Infrastructure for search algorithms
There is a general infrastructure for search algorithms. Search algoritm require data structures to keep track of the search tree that being constructed while searching. 

For each node $n$ we have a strucure that contains four components:
![](/assets/images/2022-02-10-08-07-57.png)
![](/assets/images/2022-02-10-08-08-54.png)

## Measuring 
About measuring performance. Go read the following first: [[algorithms.measurePerformance]].

In terms of the theoretical part when analysing algorithms we typically look at Time and Space complexities.
Space of a Graph or Tree is $|V|+|E|$ where $V$ is the set of vertices and $E$ is the set of edges.

This is the way to go when the data structure is explicit i.e. that is input to the search algorithm(e.g. a Map of Denmark).
However, when it comes to **AI** then the graph is often represented as implicitly by the initial state, actions and transition model. Also it is frequently infinite.

Complexity is expressed in terms of three quantities:
- $b$: the branching factor or the maximum number of successors of any node
- $d$: the depth og the shallowest goal node. The number of steps along the path from the root
- $m$: the maximum length of any path in the state space

Time is measured in terms of the number of nodes generated during the search.

Space is measrued in terms of the maximum number of nodes stored in memory.

For often describe time and complexity for [[Search Trees|datastructure.tree]]. However, for graphs the answer depends on how redundant the paths in the state space are.

In terms of **effectiveness** of a search algorithm we can assess the search cost. This depends on the time complexity. There is also the possibility to use the total cost.
