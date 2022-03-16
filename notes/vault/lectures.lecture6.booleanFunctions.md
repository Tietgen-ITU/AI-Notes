---
id: u2b2gpx34a18l7sa8zpkyfj
title: Boolean Functions
desc: ''
updated: 1647451162181
created: 1646904819327
---
![](/assets/images/2022-03-10-10-06-14.png)

![](/assets/images/2022-03-10-10-30-52.png)

![](/assets/images/2022-03-10-10-32-24.png)
We can have $2^{2^n}$ boolean functions.


## Representation of Boolean functions
![](/assets/images/2022-03-10-10-39-15.png)

**Canonicity** means that the boolean function only have one representation.

#### Why does the property solve prop 2, 5 and 6?
With 2 we just do an ID check.

SAT Check is to see if there is any representation that makes it true

With 5 we...

It is the oposite of the SAT Check
With 6 we just check if the id is true.

## Compact representation
![](/assets/images/2022-03-10-10-46-21.png)

### Ways to represent a boolean function

#### Truth table
![](/assets/images/2022-03-10-10-48-26.png)

We do not like that the truth table is huge. But it satisfies all the other properties. This is good for nothing because the table becomes so hugh. Soooo all the other operations takes time. 

#### CNF - Representation
![](/assets/images/2022-03-10-10-49-34.png)

![](/assets/images/2022-03-10-10-55-26.png)

![](/assets/images/2022-03-10-10-59-10.png)

![](/assets/images/2022-03-10-10-58-12.png)

This is what we call a canonical CNF

![](/assets/images/2022-03-10-10-59-48.png)


But this is also horrible in terms of size.