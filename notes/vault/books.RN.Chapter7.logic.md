---
id: n2cef63sy4zug9mj4lpr9dt
title: Logic
desc: ''
updated: 1652990339631
created: 1645981594116
---
Logic must define somekind of semantic or meaning of sentences. These semantics defines the thruth of each sentence with respect to each possible world. 

Here is an example of semantic:

![](./assets/images/2022-02-27-18-17-49.png)

![](./assets/images/2022-02-27-18-20-24.png)
This here is also called model checking because it enumerates all possible model sto check that alpha is true in all models in which KB is true that is that

![](./assets/images/2022-02-27-18-27-37.png)

### Definition of entailment
![](./assets/images/2022-02-27-18-23-08.png)
![](./assets/images/2022-02-27-18-23-22.png)
 
When you have to prove entailment then only look at the example where the left side of the entailment symbol is true, and then see if the expression on the right side is true as well. If not then the beta is not entailed by alpha.

## Properties
- **Soundness / Truth preserving**:
    It is basically if it is true. The book describes the unsound inference procedure as an algorithm that comes up with things as it goes a long.
- **Completeness**:
    The inference algorithm is complete if it can derive any sentence that is entailed. 

![](./assets/images/2022-02-28-08-19-59.png)