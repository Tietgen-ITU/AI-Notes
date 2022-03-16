---
id: yy2hj6htdi595qe6p73xr21
title: Binary Decision Diagrams
desc: ''
updated: 1647451182061
created: 1646907226932
---
This is about [[books.a97.binaryDecisionDiagrams]].

# If-then-else operator
We are looking at the if then else operator.
![](/assets/images/2022-03-10-11-17-37.png)

The last thing is just a representation of $x$.

![](/assets/images/2022-03-10-11-19-35.png)

This can be used for:
[[books.a97.normalForms#if-then-else-normal-form-inf]]

Any expression can be written in INF

#### Exmples of INF
$$
x \land y = x \to (y\to 1, 0), 0
$$

$$
x \lor y = x \to 1, (y \to 1,0)
$$

$$
\neg x = x = 0,1
$$

$$
x <-> y = x \to (y \to 1,0), (y \to 0,1)
$$

#### Construction of INF
![](/assets/images/2022-03-10-11-27-02.png)

![](/assets/images/2022-03-10-11-27-13.png)

**Another example**
![](/assets/images/2022-03-10-11-29-32.png)

![](/assets/images/2022-03-10-11-29-43.png)

![](/assets/images/2022-03-10-11-29-52.png)

![](/assets/images/2022-03-10-11-30-01.png)

![](/assets/images/2022-03-10-11-32-13.png)

![](/assets/images/2022-03-10-11-36-17.png)

This is the INF representation of the expression.

But some of the nodes do the same trick.
For that reason we do the following:

![](/assets/images/2022-03-10-11-38-01.png)

![](/assets/images/2022-03-10-11-39-04.png)

![](/assets/images/2022-03-10-11-39-13.png)

These are the reductions that we have just used.

## Reductions
![](/assets/images/2022-03-10-11-39-52.png)

#### Example of reduction... again
![](/assets/images/2022-03-10-11-41-07.png)

![](/assets/images/2022-03-10-11-41-52.png)

![](/assets/images/2022-03-10-11-41-59.png)

![](/assets/images/2022-03-10-11-42-10.png)

![](/assets/images/2022-03-10-11-42-25.png)

![](/assets/images/2022-03-10-11-42-34.png)

This is still canonical(unique).

![](/assets/images/2022-03-10-11-45-05.png)

# Practice of ROBDDs
![](/assets/images/2022-03-10-11-45-51.png)

![](/assets/images/2022-03-10-11-46-05.png)

# Size of ROBDDS

![](/assets/images/2022-03-10-11-51-25.png)

![](/assets/images/2022-03-10-11-51-37.png)

![](/assets/images/2022-03-10-11-51-49.png)

![](/assets/images/2022-03-10-11-52-01.png)