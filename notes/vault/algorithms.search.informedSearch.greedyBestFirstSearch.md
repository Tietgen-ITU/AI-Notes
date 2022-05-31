---
id: lYiSWvXN7BkyK8KHSCayZ
title: Greedy Best First Search
desc: ''
updated: 1653989337410
created: 1644479898371
---
**Note:** this could look alike [[algorithms.search.informedSearch.aStar]]. However the difference is that A* includes the cost of reaching the node.

This algorithm tries to expand the node that is the closest to the goal. It does so, because it thinks that it is likely to lead to a solution quickly. 

This algorithm ignores the previous cost of the path. It only cares which next node is the closest.

It uses a heuristic function to determine the node which is closest:

$f(n)=h(n)$

![](./assets/images/2022-02-10-11-30-42.png)

This is complet because it does not ignore other nodes.

# Algorithm
![](/Users/andreastietgen/Documents/Programmering/UNI/ArtificialIntelligence/AI-Notes/notes/vault/assets/images/2022-05-31-11-28-55.png)
# Example from the book
![](./assets/images/2022-02-10-11-31-08.png)
![](./assets/images/2022-02-10-11-31-17.png)
![](./assets/images/2022-02-10-11-31-32.png)
![](./assets/images/2022-02-10-11-31-48.png)
![](./assets/images/2022-02-10-11-32-03.png)