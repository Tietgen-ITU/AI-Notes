---
id: riv9xhdfq8qg6keo67dgp2z
title: Apply
desc: ''
updated: 1651149163480
created: 1651148172859
---
Since build is not very efficient we want another method to try and build our BDDs with. 
What we want is to construct a BDD based of an expression tree:

![](/assets/images/2022-04-28-14-21-50.png)

So what we are going to construct is a multi-rooted BDD:

![](/assets/images/2022-04-28-14-24-52.png)

So in here every node corresponds to an expression. The unique table now contains many BDDs.

So Apply is trying to create that:

![](/assets/images/2022-04-28-14-27-00.png)

What *Apply* tries to do is to create a BDD by applying the negative cofactor and the postive cofactor to other expressions that the following operation should try and create. 

![](/assets/images/2022-04-28-14-32-11.png)

# The algorithm
![](/assets/images/2022-04-28-14-32-41.png)