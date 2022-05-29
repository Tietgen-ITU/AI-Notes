---
id: yxsbv7tvg5yb4542sto94ml
title: Backtracking Algorithm
desc: 'This is the backtracking algorithm for CSPs'
updated: 1653752987910
created: 1648116307981
---
This algorithm uses a depth first search approach.
The algorithm is the following:

![](./assets/images/2022-03-24-11-06-23.png)

All version that we cover regarding CSPs is some type of version of the backtracking algorithm.

## Example
![](./assets/images/2022-03-24-11-05-45.png)

![](./assets/images/2022-03-24-11-06-02.png)

## Select-Unassigned-variable function
![](./assets/images/2022-03-24-11-10-16.png)

![](./assets/images/2022-03-24-11-10-28.png)

## Order-Domain-Values
![](./assets/images/2022-03-24-11-14-34.png)

# Forward Checking
![](./assets/images/2022-03-24-11-20-02.png)

![](./assets/images/2022-03-24-11-19-51.png)

![](./assets/images/2022-03-24-11-20-15.png)

![](./assets/images/2022-03-24-11-20-24.png)

If we had done arc consistency between NT and SA then we would have realized that there is a constraint between those two.

#### Algorithm of forward checking
![](./assets/images/2022-03-24-11-20-46.png)

![](./assets/images/2022-03-24-11-20-57.png)

# Maintaining Arc consistency (MAC)
![](./assets/images/2022-03-24-11-23-14.png)

![](./assets/images/2022-03-24-11-23-22.png)

![](./assets/images/2022-03-24-11-23-31.png)

#### MAC Algorithm
![](./assets/images/2022-03-24-11-23-49.png)