---
id: ii8rrtvvhi908l3npmffbdg
title: Assignment6
desc: ''
updated: 1652990320741
created: 1648041722806
---
![](../assets/images/2022-03-23-14-22-21.png)

![](../assets/images/2022-03-23-14-22-32.png)

# Question 1
![](../assets/images/2022-03-23-14-22-51.png)

#### Answer

So in order to make the negation of the expression $u$ with apply then we can use the $\oplus$, called EXOR(Exclusive OR). So a call to the `Apply` method would look like the following:

```
APPLY(EXOR, 1, U)
```

# Question 2
![](../assets/images/2022-03-23-14-47-45.png)

#### Answer

So in order to use the function `Mk` to construct a ROBDD of a variable $x_i$, we can call it like the following:
```
Mk(i, 0, 1)
```

# Question 3
![](../assets/images/2022-03-23-14-53-48.png)

#### Answer

```
function Expr2ROBDD(expr) returns ROBDD

    if expr.type() equals TRUE 
        u ← 1
    else if expr.type() equals FALSE
        u ← 0
    else if expr.type() equals VAR
        u ← Mk(expr.idx(), 0 ,1)
    else if expr.type() equals AND
        left = Expr2ROBDD(expr.left())
        right = Expr2ROBDD(expr.right())
        u ← Apply(and,left,right)
    else if expr.type() equals OR
        left = Expr2ROBDD(expr.left())
        right = Expr2ROBDD(expr.right())
        u ← Apply(or,left,right)
    else if expr.type() equals NOT
        right = Expr2ROBDD(expr.right())
        u ← Apply(EXOR,1,right)
    endif
    
    return u
```