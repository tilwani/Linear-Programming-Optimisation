# Linear-Programming-Optimisation

### Problem Statement
For the given problem statement, we require to minimize the cost of electricity production while also ensuring that the supply meets the demand, that varies hourly over the period of 24 hours for a single day. The resources provided are ten generators with different configurations which can be tuned as per the demand.

### Notations
Since demand and supply from generators depends on time, we define T as the set of integer values in [1, 24], denoting the hour of the day. Demand at any time t can be represented as Dt , where t ϵ T. Let H, SD, G, SLR be the sets of hydro, solid, gas, and solar generators respectively. Also, let Px,t denote the production of any generator x at time t, where t ϵ T.

### Constraints and Decision Variables
Apart from the lower and upper bound constraints of generators which are already given, we also have a constraint that at any time t ϵ T, supply from all generators should be equal to demand. Using the above notations, it can be defined as:<br>

![\sum P_{h,t}\ \forall\ h \in H + \sum P_{s,t}\ \forall\ s\in SD + \sum P_{g,t}\ \forall\ g\in G + \sum P_{r,t}\ \forall\ r \in SLR=D_{t}\ \ \ \ \ ...\ eq(i)](https://latex.codecogs.com/png.image?\dpi{110}&space;\bg_white&space;\inline&space;\sum&space;P_{h,t}\&space;\forall\&space;h&space;\in&space;H&space;&plus;&space;\sum&space;P_{s,t}\&space;\forall\&space;s\in&space;SD&space;&plus;&space;\sum&space;P_{g,t}\&space;\forall\&space;g\in&space;G&space;&plus;&space;\sum&space;P_{r,t}\&space;\forall\&space;r&space;\in&space;SLR=D_{t}\&space;\&space;\&space;\&space;\&space;...\&space;eq(i)&space;)

![\sum P_{h,t}\ \forall\ h \in H + \sum P_{s,t}\ \forall\ s\in SD + \sum P_{g,t}\ \forall\ g\in G + \sum P_{r,t}\ \forall\ r \in SLR=D_{t}\ \ \ \ \ ...\ eq(i)](https://latex.codecogs.com/png.image?\dpi{80}&space;\bg_white&space;\inline&space;\sum&space;P_{h,t}\&space;\forall\&space;h&space;\in&space;H&space;&plus;&space;\sum&space;P_{s,t}\&space;\forall\&space;s\in&space;SD&space;&plus;&space;\sum&space;P_{g,t}\&space;\forall\&space;g\in&space;G&space;&plus;&space;\sum&space;P_{r,t}\&space;\forall\&space;r&space;\in&space;SLR=D_{t}\&space;\&space;\&space;\&space;\&space;...\&space;eq(i)&space;)


<img src="https://latex.codecogs.com/png.image?\dpi{110}&space;\bg_white&space;\inline&space;\sum&space;P_{h,t}\&space;\forall\&space;h&space;\in&space;H&space;&plus;&space;\sum&space;P_{s,t}\&space;\forall\&space;s\in&space;SD&space;&plus;&space;\sum&space;P_{g,t}\&space;\forall\&space;g\in&space;G&space;&plus;&space;\sum&space;P_{r,t}\&space;\forall\&space;r&space;\in&space;SLR=D_{t}\&space;\&space;\&space;\&space;\&space;...\&space;eq(i)&space;" title="\bg_white \inline \sum P_{h,t}\ \forall\ h \in H + \sum P_{s,t}\ \forall\ s\in SD + \sum P_{g,t}\ \forall\ g\in G + \sum P_{r,t}\ \forall\ r \in SLR=D_{t}\ \ \ \ \ ...\ eq(i) " />
<br> $\sum P_{h,t}\ \forall\ h \in H + \sum P_{s,t}\ \forall\ s\in SD + \sum P_{g,t}\ \forall\ g\in G + \sum P_{r,t}\ \forall\ r \in SLR=D_{t}\ \ \ \ \ ...\ eq(i)$
The decision variables for the problem are the productions of all of the generators in 24 hours as shown in eq(i). Hence the total number of decision variables is 24 * 10 = 240.
Below is the code for the addition of decision variables and then the constraints.

### Objective Function
 Objective is the minimization of the cost which is provided in EUR/MW. We define the total cost for the day as the production of generators multiplied by their corresponding cost information provided, as shown below.
