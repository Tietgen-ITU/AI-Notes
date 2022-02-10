---
id: QWT1OVbjMHWd9WVbpGG8N
title: Breadth First Search
desc: ''
updated: 1644479553111
created: 1644478555632
---
This algorithm is good when the step cost are equal.

![](/assets/images/2022-02-10-08-36-11.png)


## Example of the behavior of BFS
![](/assets/images/2022-02-10-08-37-04.png)

## Measures
In terms of the number of nodes generated for Space complexity then:

$$b + b^2 + b^3 + ... + b^d = O(b^d)$$
Where $b$ is the number of nodes at a level and $d$ is the depth of the tree. (This is bad)

![](/assets/images/2022-02-10-08-37-25.png)

>"Two lessons can be learned from Figure 3.13. First, the memory requirements are a bigger problem for breadth-first search than is the execution time. One might wait 13 days for the solution to an important problem with search depth 12, but no personal computer has the petabyte of memory it would take. Fortunately, other strategies require less memory.
>The second lesson is that time is still a major factor. If your problem has a solution at depth 16, then (given our assumptions) it will take about 350 years for breadth-first search (or indeed any uninformed search) to find it. In general, exponential-complexity search problems cannot be solved by uninformed methods for any but the smallest instances."
