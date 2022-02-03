# Linear-Programming-Optimisation

### Problem Statement
For the given problem statement, we require to minimize the cost of electricity production while also ensuring that the supply meets the demand, that varies hourly over the period of 24 hours for a single day. The resources provided are ten generators with different configurations which can be tuned as per the demand.

### Notations
Since demand and supply from generators depends on time, we define T as the set of integer values in [1, 24], denoting the hour of the day. Demand at any time t can be represented as Dt , where t ϵ T. Let H, SD, G, SLR be the sets of hydro, solid, gas, and solar generators respectively. Also, let Px,t denote the production of any generator x at time t, where t ϵ T.

### Constraints and Decision Variables
Apart from the lower and upper bound constraints of generators which are already given, we also have a constraint that at any time t ϵ T, supply from all generators should be equal to demand. Using the above notations, it can be defined as:
$\sum P_{h,t}\ \forall\ h \in H + \sum P_{s,t}\ \forall\ s\in SD + \sum P_{g,t}\ \forall\ g\in G + \sum P_{r,t}\ \forall\ r \in SLR=D_{t}\ \ \ \ \ ...\ eq(i)$
