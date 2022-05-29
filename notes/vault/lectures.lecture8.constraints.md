---
id: iie3g78j5kwb362jjglje4p
title: Constraints
desc: ''
updated: 1653815020449
created: 1653812696368
---
Constraints are some of the rules in a CSP. 
There are different types of them:

- Unary Constraints: Which is a rule that only involves a single variables e.g. $x_1 \neq red$
- Binary Constraints: Which is a rule that involves pairs of variables e.g. $x_1 \neq x_2$
- Global Constraints: Which involves an arbitrary number of variables e.g. *AllDifferent*

## Example: Binary constraint
**Question:**

Write binary constraints corresponding to the rules in (i) and (ii) above
applied to the puzzle shown in figure (a) below. Note that AllDiff constraints
should be rephrased as a number of binary constraints.
Draw the constraint graph. In the graph, draw the nodes in a 3 ×3 grid as
they appear in figure (b) below.

![](/Users/andreastietgen/Documents/Programmering/UNI/ArtificialIntelligence/AI-Notes/notes/vault/assets/images/2022-05-29-11-02-56.png)

**Answer:**
$$
    x_1 \neq x_2, x_1 \neq x_3, x_1 \neq x_4, x_1 \neq x_7, x_2 \neq x_3, x_2 \neq x_5, x_2 \neq x_8,
$$
$$
    x_3 \neq x_6, x_3 \neq x_9, x_4 \neq x_6, x_4 \neq x_5, x_4 \neq x_7, 
$$
$$
    x_5 \neq x_6, x_5 \neq x_8, 
    x_6 \neq x_9, x_7 \neq x_9, x_7 \neq x_8, x_8 \neq x_9
$$

$$
    x_1 = B \lor (x_1 = blank \land x_2 = B)
$$
$$
    x_6 = A \lor (x_6 = blank \land x_5 = A)
$$
$$
    x_8 = B \lor (x_8 = blank \land x_5 = B)
$$
