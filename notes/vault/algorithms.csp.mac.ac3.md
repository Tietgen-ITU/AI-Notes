---
id: qo5hnz2gcg7z8w551g7zt18
title: AC3
desc: 'Arc consistency algorithm'
updated: 1653811462154
created: 1653763663479
---
This algorithm goes through every Arc and makes an inference on them. Also it checks that there is a consistency with the domain of values that there are allowed to be signed to a given variable after a variable has been assigned. 

The algorithm look like this:
![](./assets/images/2022-03-18-08-38-18.png)

## Walkthrough
This walkthrough is how you should to it at the exam.

When doing the AC3 all arcs are in the queue to begin with. An arc is the dependency or link between to variables. The essential thing here is that it e.g. takes the variable $x_1$ and compares it with $x_x$. $x_1$ then checks if its Domain is up to date compared to the other variable domain in $x_x$(Revise algorithm).

**Step 1.**

Pick the first item of the queue. Its usually the first variable and it neighbors that goes first, then the second variable and its neighbors. 

**Step 2.**

Call `Revise`. Revise goes through each and every value in the domain of the variable we just picked and updates it domain if that variable is not possible to be assigned anymore. 

NOTE: It does not update the other variables. It only updates its own domain.

**Step 3.**

If something has been Revised in the domain $D_i$ then add all neighbors to variable $x_i$ except the one variable we just looked with which was $x_j$ .

**Step 4.**

Continue to do this until the queue is empty or an inconsistency is there. 

