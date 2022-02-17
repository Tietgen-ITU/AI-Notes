---
id: Idk4hdRnaBgcVe1a6lQ4q
title: Monte Carlo Tree Search (MCTS) Algorithm
desc: ''
updated: 1645094088818
created: 1645093321720
---
>**Important:** This is not a part of the curriculum

What the monte carlo simulation is to build up a tree by simulating the game to see which portion we win the most.

The reason why this is better is because:

![](/assets/images/2022-02-17-11-22-56.png)

# The algorithm
What we want is to find the "Hot-path".

![](/assets/images/2022-02-17-11-26-53.png)

The numbers in the nodes is the number of simulation. This signals that with this amount of simulations it won this much times. So therefore we take this move.

![](/assets/images/2022-02-17-11-28-43.png)
![](/assets/images/2022-02-17-11-28-56.png)
>**Note:** The fat arrow is the hot path

![](/assets/images/2022-02-17-11-29-09.png)
>**Note:** It is important to notice the difference between the probability and the form of calculation that is actually being applied. That is because we want to be able to be eager to explore more paths. 
>The `C` is the constant for how eager we want to be to explore more paths.


This is called a policy.
We run this policy alot of times and grow the tree. So in other words we are training the policy in order to become more sure that the path that we took is the correct one.