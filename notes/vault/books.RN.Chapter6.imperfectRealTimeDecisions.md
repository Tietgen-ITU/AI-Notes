---
id: XPamZALf7Y9XMg9IpZFlI
title: Imperfect Real-time Decisions
desc: ''
updated: 1644839000090
created: 1644838462027
---
The minimax algorithm generates the entire game search space. And the beta-alpha version of the algorithm still has to search all the way to the terminal states for a smaller portion of the search space. 

The compution in the length of the depth every times is not optimal. We should instead apply a heuristic to the search so that we cut of the search.

We do so by replacing the `utility` function with a heuristic evaluation function called `Eval`.
![](/assets/images/2022-02-14-12-41-13.png)

# Evaluation functions
The evaluation function returns an estimate of the expected utility function of the game from a given position. 
