---
id: L661Ig5TIhzVhSZKnwfOz
title: Stochastic Games
desc: ''
updated: 1644956451169
created: 1644955790472
---
Stochastic games are when unpredictable external events can put us into unforeseen situations.

Backgammon is such a game:

![](/assets/images/2022-02-15-21-12-05.png)

What is special with these kind of games is that we do not know what the player roll next time. So we cannot take that into account when trying to predict the best move. 

Instead we add what is called **chance nodes** to [[algorithms.search.games.miniMax]] in order to predict the possiblity of what the other player could roll.

![](/assets/images/2022-02-15-21-14-33.png)
![](/assets/images/2022-02-15-21-15-21.png)
![](/assets/images/2022-02-15-21-15-45.png)

# Evaluation functions for games of chance
In terms of the cutoff in order to perform the evaluation function to predict the best move instead of calculation every move is not that easy. 

Instead of using the same method as we did with the chess game in the [[books.RN.Chapter6.imperfectRealTimeDecisions]], we then do it by the chance of winning form a position. This is an important property of situations which uncertainty is involved. 

The running time of the normal mini max function is 

$$$
O(b^m)
$$$

