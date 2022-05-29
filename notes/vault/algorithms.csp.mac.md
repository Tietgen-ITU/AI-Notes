---
id: jp9f43ejed1n4awig5lc1y0
title: MAC
desc: 'Maintaining Arc Consistency'
updated: 1653765568801
created: 1653763400645
---
MAC also known as Maintaining Arc Consistency looks like the following:

![](./assets/images/2022-03-24-11-23-49.png)

## Walkthrough
This walkthrough is a step by step guide on how to go through it at the exam. This includes the AC3 algorithm.

**Step 1.**

First run AC3 before doing the Recursive MAC. (There is a link at the bottom)

**Step 2.**

Check that the assignment is complete i.e. that all variables has been assigned and that they do not violate the assignements.

If it is then return the result.

**Step 3.**

Select the next unassigned variable from the CSP.

**Step 4.**

Go through each value in the domain of the variable(that is the allowed variables to be assigned to the variable) and check if it is consistent.

**Step 4.a.**
If it is consistent add the value to the variable and add to the assignment. 
Then go through with AC3 

**Step 4.b.**
Check if the inferences has any failures. If not, then add all the inferences to the domain and call the RECURSIVE-MAC recursively. 

Go through step 2 to 4.b again until a complete assignment is found.

