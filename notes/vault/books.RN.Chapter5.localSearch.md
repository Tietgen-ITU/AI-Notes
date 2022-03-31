---
id: j8x7d9vck3yvyyuhi9v2tpw
title: Local Search
desc: 'This is notes about how to perform '
updated: 1647772824924
created: 1647771203609
---
# Overview and motivation
![](/assets/images/2022-03-31-10-02-28.png)
> Anytime algorithms is an algorithm that improves the result over time. When the "time" is over then it returns the best result that it currently have.

# What is Local Search
Local search is an effective algorithm to solve many CSP's.

The way it works is that the initial state assigns a value to every variable, and changes the value of one variable at a time. Local search tries to eliminate the violated constraints. 

When choosing a new value the most obvious heuristic is to use what is called the *min-conflicts heuristic*[^1].

The run time of this algorithm is roughly independent of the problem size[^2]

#### Example of Min-conflict
![](/assets/images/2022-03-20-11-27-15.png)

# Tabu Search
Here are some notes about [[Tabu Search|books.TS]]
Tabu search is keeping a small list of recently visited states and forbidding the algorithm to return to those states. This can be used to escape from plateaux[^3].

# Constraint weighting
This is a technique that can be used to help concentrate the search on the important constraints. 

---
[^1] A heuristic that selects a value with the minimum number of conflicts with other variables.

[^2] This is based on not taking some initial values in to the account - look at page 221 in the old book.

[^3] A plateau is in this case when millions of variable assignments that are only one conflict away from a solution.