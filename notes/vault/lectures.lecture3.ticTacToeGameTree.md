---
id: sgImqL6IZVMevG7O8qpgx
title: Tic-Tac-Toe Game Tree
desc: ''
updated: 1645093403803
created: 1645089191679
---
Here we are going to construct a tic-tac-toe game tree.

![](/assets/images/2022-02-17-10-13-23.png)

The player we are playing for is the Max utility. The opponent is the Min utility.
A **ply** is a move down the tree or a move in the game.

#### What are we trying to achieve?
We are trying to find a path to a goal state where we win. 

![](/assets/images/2022-02-17-10-22-33.png)

# Problem definition
We have the following problem definiton:

![](/assets/images/2022-02-17-10-15-22.png)

The `Utility` function is only working on the terminal states.

We can solve this with the [[algorithms.search.games.miniMax]]

