---
id: XPamZALf7Y9XMg9IpZFlI
title: Imperfect Real-time Decisions
desc: ''
updated: 1652990334692
created: 1644838462027
---
The minimax algorithm generates the entire game search space. And the beta-alpha version of the algorithm still has to search all the way to the terminal states for a smaller portion of the search space. 

The issue with [[books.RN.Chapter6.alphaBetaPruning]] is that we still need to look up a lot of the nodes/states in the tree.

The compution in the length of the depth every times is not optimal. We should instead apply a heuristic to the search so that we cut of the search.

![](./assets/images/2022-02-17-11-13-07.png)
![](./assets/images/2022-02-17-11-15-26.png)

We do so by replacing the `utility` function with a heuristic evaluation function called `Eval`.
![](./assets/images/2022-02-17-11-18-34.png)

# Evaluation functions
The evaluation function returns an estimate of the expected utility function of the game from a given position. 

This function guesses, so to speak, what the outcome could be.

In order to calculate the "score" we first define weights to the different elements. In chess this could be the different pieces(e.g. pawn = 1, bishop = 3, rook = 5, queen = 9). Features could be the postion of the pawn.

#### From the lecture
![](./assets/images/2022-02-17-11-19-24.png)
![](./assets/images/2022-02-17-11-19-39.png)
![](./assets/images/2022-02-17-11-20-10.png)

This kind of evaluation function is called a Weighted linear function becuase it can be expressed as:

![](./assets/images/2022-02-15-20-48-58.png)
![](./assets/images/2022-02-15-20-49-38.png)

# Cutting off search
Now we implement the heuristic in the [[books.RN.Chapter6.alphaBetaPruning]]. We replace the two lines in the pseudo code that mention `Terminal-Test` with the following line:
```
if CUTOFF-TEST(state, depth) then return Eval(state)
```
![](./assets/images/2022-02-17-11-20-35.png)

Also we must bookkeep the current depth so that on each recursive call it gets incremented. 
![](./assets/images/2022-02-15-20-55-04.png)

# Forward pruning
In forward pruning we look ahead of certain moves in order to be more certain that the moves are correct. But we do not want to do this for all the moves possible. For that reason we only look at the n best possible moves instead of all possible moves. This is called **beam search**.

However this is a dangerous algorithm because there is no guarantee that the best move will not be pruned away.

# Search vs. lookup
In the past experience both at the start of a game and at the end of a game it is a good idea to have a table lookup. We can here rely on the statistics of good openings. After that we rely on search until we reach near the end of the game. 
