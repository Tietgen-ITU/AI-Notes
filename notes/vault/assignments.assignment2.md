---
id: vtk3sfdqwge6j2nusapalq9
title: Assignment2
desc: ''
updated: 1645978712676
created: 1645978710679
---
```
function MINIMAX-DECISION(state) returns an action
return arg maxa ∈ ACTIONS(s) MIN-VALUE(RESULT(state, a))
```
---
```
function MAX-VALUE(state) returns a utility value
    if TERMINAL-TEST(state) 
        then return UTILITY(state) 
    
v ← CHANCE-MAX(state) 
    
return v
```
---
```
function MIN-VALUE(state) returns a utility value
if TERMINAL-TEST(state) 
    then return UTILITY(state) 

v ← CHANCE-MIN(state)

return v
```
---
```
function CHANCE-MAX(state) returns a utility value

chanceValues ← new List

for each (c, weight) in CHANCEPATHS() do
    v ← −∞
    
    for each a in ACTIONS(state) do
        v ← MAX(v, MIN-VALUE(RESULT(s, a))) 
        
    ADD(chanceValues, v * weigth)
    
return SUM(chanceValues)
```
---
```
function CHANCE-MIN returns a utility value

chanceValues ← new List

for each (c, weight) in CHANCEPATHS() do

    v←∞

    for each a in ACTIONS(state) do
        v ← MIN(v, MAX-VALUE(RESULT(s, a)))

    ADD(chanceValues, v)

return SUM(chanceValues)
```
