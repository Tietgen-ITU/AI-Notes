---
id: bjoiodoyhiilww8x0ipvwk3
title: Defining Constraint Satisfaction Problems
desc: ''
updated: 1647588534963
created: 1647587116095
---
When we define a satisfaction problem then it consists of three components, $X, D$, and $C$.

- $X$ is a set of variables, $\{ X_1, \dots, X_n \}$

- $D$ is a set of domains, $\{ D_1, \dots, D_n \}$. Each $D_i$ consists of a set of allowable values, $\{v_1, \dots v_n \}$ for variable $X_i$
  
- $C$ is a set of constraints that specify allowable combinations of values. Each $C_i$ consists of a pair $(scope, rel)$ where the $scope$ is a tuple of variables that participate in the constraint and $rel$ is a relation that defines the values that those variables can take on.

This is also explained in the lecture:

![](/assets/images/2022-03-24-10-13-17.png)

So! For example if $X_1$ and $X_2$ both have the domain $\{A,B\}$ then the constraint saying the two variables must have different values can be written as the following:

![](/assets/images/2022-03-18-08-14-46.png)

In order to solve a *CSP*, we need to define a state space and the somekind of solution. Each state in a *CSP* is defined by an assignment of values to some of the variables.

That is denoted by:
$$
\{X_i = v_i, X_j = v_j\}
$$

A complete assignment is one where every variable is assigned and a solution to a *CSP* is a consistent(what ever that means) and complete assignment. 

A Partial Assignment is on that assigns values to only some of the variables.

# CSP Solutions - Assignments
![](/assets/images/2022-03-24-10-16-58.png)
# Example
![](/assets/images/2022-03-18-08-19-30.png)

# Why use CSP
The cool thing about CSP is that you can define constraints such that when a variable has been defined then by the constraints you can eliminate a lot of the neighboring variables. 

![](/assets/images/2022-03-18-08-28-45.png)
