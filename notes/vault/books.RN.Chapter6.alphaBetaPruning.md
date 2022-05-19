---
id: ugs2OiaroR6mhWQYyyZli
title: Alpha-Beta Pruning
desc: ''
updated: 1652990332711
created: 1644836534344
---
The biggest problem with [[algorithms.search.games.miniMax]] is that it has to examine exponential in the depth of the tree.

We cannot eliminate the exponential element of the time-complexity, but we can cut the exponent in half. We borrow the idea of **pruning**, in that way we do not need to look at every branch in the tree. 

![](./assets/images/2022-02-14-12-16-32.png)
![](./assets/images/2022-02-14-12-16-53.png)

Alpha-Beta pruning get its name by the following:

![](./assets/images/2022-02-14-12-18-17.png)

#### From the lecture
![](./assets/images/2022-02-17-10-47-23.png)

It is important to notice here that the cut happens for different reasons. So the alpha cut happens for the perspective of us (i.e. MAX) where we want to best choice. 
The beta cut is the value with lowest value. That is the best choice for MIN.

So in order to add some context then the alpha cut happens in the *MIN-Value* function when it can see that the value in the MIN-Value function is less than the Alpha value. Because then we wont take that route because then MIN could potentially take a route where we get less for winning.

And the other way around the beta cut happens in *MAX-Value* function where it cuts when it sees the result is greater than the current beta. Because then we know(i.e. MAX even though it is for MIN) that MIN will not choose this path and for that reason it does not make sense to continue

The alpha cut:

![](./assets/images/2022-02-17-10-47-40.png)

The beta cut: 

![](./assets/images/2022-02-17-10-47-59.png)

## Implementation
![](./assets/images/2022-02-14-12-19-09.png)

#### Implementation from the lecture
![](./assets/images/2022-02-17-10-49-42.png)

## Move ordering
The effectiveness of alpha-beta pruning is highly dependent of the order in which the states are examined. 

If we can examine the first successor then the time complexity of the minimax becomes $O(b^{m/2})$.

![](./assets/images/2022-02-17-11-11-47.png)

