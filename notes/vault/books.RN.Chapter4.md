---
id: tsylehr1hznctzq4plbyzdh
title: 4. Chapter - Search in complex environments
desc: ''
updated: 1648614951840
created: 1648614951840
---
# Local Search and Optimization problems

# Local Search Definition
What is local search? Local Search operates only by going through the neighboring states. It does not save the path that it took to get to the result.
Why is this a good algorithm?
- It uses very little memory because it does not save the path it took to get there.
- It can find a reasonable solution in a large infinite state space for which systematic algorithms are unsuitable.

And then it can solve optimization problems[^1].

In order to understand Local search the we can imagine the problem state laid out on a landscape. Each point(state) in the landscape has an elevation value defined which has been given by the objective function.
If elevation corresponds to an objective function then the goal is to find the highest peak or *global maximum*[^2] this process is called *hill climbing*.

If elevation corresponds to cost, then the aim is to find the lowest valley i.e. a *global minimum*[^3] also called *gradient descent*

## Hill Climbing
The *Hill Climbing* is one the most basic Local Search technique. 
This algorithm goes to the next node where theres is the steepest ascent. It terminates when it reaches a "peak".

```
function Hill-Climbing(problem) returns a state that is a local maximum
    current ← problem.INITIAL

    while true do
        neighbor ← a highest-valued successor state of current
        if VALUE(neighbor) ≤ VALUE(current) then return current
        current ← neighbor
```
The stupid thing is that the algorithm can get stuck in these different situations 
- by reaching a peak at the *Local Maxima*[^4]
- by reaching *ridges*[^5]. This is very difficult for greedy algorithms to navigate.
- by being at a *plateau* i.e. a flat area, the algorithm does not know where to go.


## Simulated Annealing
This is an algorithm that is both efficient and complete. What it does is roll the ball over the surface. Here it can get stuck in a local gradient descents. The trick here is that it tries to simulate that it shakes the surface so that the ball gets out of the "local gradient descents". 
This algorithm is a lot like the *Hill-Climbing* algorithm except that instead of picking the best move, it picks a random move. If that move improves the situation then it is accepted. 
$\leftarrow$
```
function SIMULATED-ANNEALING(problem, schedule) returns a solution state
    current ← problem.INITIAL
    for t = 1 to infinite do 
        T ← schedule(t)
        if T = 0 then return current
        next ← randomly selected successor of current
        AE ← VALUE(current) - VALUE(next)
        if AE > 0 then current ← next
        else current ← next only with probability
```

## Local Search Beam
The local search beam keeps track of $k$ states rather than just one. It begins by randomly generating $k$ states. At each step all the successors of all $k$ state are generated. If any one is a goal, the algorithm stops. Otherwise it selects the best $k$ successors and repeats the process.




---
[^1] The optimization problem is one where you have to find the best state according to an objective function. 

[^2] The global maximum is the highest point according to the objective function. Depending on the objective this is what you could search for.

[^3] The global minimum is the lowest point according to the objective function. Depending on the objective this is what you could search for.

[^4] The local maxima is a peak that is higher than each of the neighboring states but is lower than the Global maximum.

[^5] Ridges are a sequence of local maximas.