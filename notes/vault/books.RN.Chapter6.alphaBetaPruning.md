---
id: ugs2OiaroR6mhWQYyyZli
title: Alpha-Beta Pruning
desc: ''
updated: 1645092975272
created: 1644836534344
---
The biggest problem with [[algorithms.search.games.miniMax]] is that it has to examine exponential in the depth of the tree.

We cannot eliminate the exponential element of the time-complexity, but we can cut the exponent in half. We borrow the idea of **pruning**, in that way we do not need to look at every branch in the tree. 

![](/assets/images/2022-02-14-12-16-32.png)
![](/assets/images/2022-02-14-12-16-53.png)

Alpha-Beta pruning get its name by the following:

![](/assets/images/2022-02-14-12-18-17.png)

#### From the lecture
![](/assets/images/2022-02-17-10-47-23.png)

The alpha cut:

![](/assets/images/2022-02-17-10-47-40.png)

The beta cut: 

![](/assets/images/2022-02-17-10-47-59.png)

## Implementation
![](/assets/images/2022-02-14-12-19-09.png)

#### Implementation from the lecture
![](/assets/images/2022-02-17-10-49-42.png)

## Move ordering
The effectiveness of alpha-beta pruning is highly dependent of the order in which the states are examined. 

If we can examine the first successor then the time complexity of the minimax becomes $O(b^{m/2})$.

![](/assets/images/2022-02-17-11-11-47.png)
