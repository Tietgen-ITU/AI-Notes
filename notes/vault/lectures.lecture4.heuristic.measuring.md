---
id: 0ra9j7rt26bnqagoseftoep
title: Measuring
desc: ''
updated: 1645695732408
created: 1645694938319
---
The effective measure of a heuristic is called *effective branching factor*.

![](/assets/images/2022-02-24-10-29-39.png)

$
b^*
$ is the effective branching factor.

The closer we get to 1 the better the effective branching factor is.

With heuristics we want to reduce the branching factor even when the problem space is getting bigger.

# The dominance of admissible heuristic
![](/assets/images/2022-02-24-10-37-38.png)

So if a heuristic is admissible and you compare the two, then the one who shows a larger output is the dominant heuristic.

So the thing to note here is that if $h_2$ dominates $h_11 then e.g. $A^*(h_1)§ expands at least as many reachable states as $A^*(h_2)$.

# Combining heuristic
If we do not know which one will be the best heuristic then we can combine them.

![](/assets/images/2022-02-24-10-42-03.png)

