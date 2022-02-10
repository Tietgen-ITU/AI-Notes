---
id: WtzrwEZBEnJs8QcbrQ1D4
title: Problem Solving Agents
desc: ''
updated: 1644317728725
created: 1644314907043
---
Goals help organize behavior by limiting the objectives that the agent is trying to achieve and the actions that it needs to consider. Therefore, a **goal formulation**, based on the current situation and the agents performance measure is the first step in problem solving. 

**Problem formulation** is the process of choosing which actions and states to consider when given a goal. 

**The execution phase**
Is when a solution is found and the action(s) a search algorithm recommends can be carried out. 

# Well-defined problems and solutions
A problem can be defined formally by five different components:
- The **initial state** in which the starts in.
- A description of the possible *actions* available to the agent e.g. given a particular  state $s$, $Action(s)$ returns the set of actions that can be executed in $s$.
- Description of what each action does. This is formally called **transition model**. This is specified by a function $Result(s, a)$ that returns the state that results from doing an action $a$ in state $s$.

These things three things forms what is called a [[books.RN.Chapter3.problemSolvingAgents.stateSpace]].

The **goal test** determines whether a given state is a goal state. Sometimes there is an explicit set of possible goal states.

A **Path cost** function that assigns a numeric cost to each. The problem-solving agent chooses a cost function that reflects its own performance measure. This could for example be the length of the road plus how fast you are allowed to drive on that road. 

A **Solution** to a problem is an action sequence that leads from the initial state to a goal state. An **Optimal solution** is a solution that has the lowest path cost of all of the solutions available. 

An example of how such problems are being described:
![](/assets/images/2022-02-08-11-55-27.png)

## Summary
This was a model to describe a problem in terms of:
- Initial state
- Actions
- Transition Model
- Goal test
- Path cost

# Formulating Problems
The previous section formulated a model that is reasonable however it is an abstract mathematical description and the real thing.

There are a lot of other factors that has not been taken into account which could be the weather, travel companions, and etc. 
All these considerations are left out because the maybe are irrelevant to the problem of maybe finding a route to a specific place. Removing those details form a representation is called a **abstraction**.

An abstraction is valid if we can expand any abstract solution into a solution in the more detailed world. 
>*"For example, we could drive with the radio on between Sibiu and Rimnicu Vilcea, and then switch it off for the rest of the trip"*[^1]

The abstraction is useful if carrying out each of the actions in the solution is easier than the original problem.

A good abstraction is removing as much of the irrelevant detail as possible while still retaining the validity and ensuring that the abstract actions are easy to carry out.

---
[^1] - RN Book, Page 64, line 19