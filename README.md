# Infections-Spread-Influence-Maximization
A repository to supplement the paper "Modeling the Spread of Infectious Diseases through Influence Maximization".

### Comparison of Different Edge Densities

![](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIS_compared.png)  |  ![](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIR_compared.png)
:-------------------------:|:-------------------------:
(a) SIS-LT model             | (b) SIR-LT model 

**Fig. 1** Comparison of different edge densities in LT optimization model with initial values $|V|=50, T=70$,$ t_0=5, B=5.$ 

We use three connected Watts-Strogatz small-world graphs of different edge densities for comparison. Each node joined with $5,7$ and $10$ nearest neighbors in a initial ring topology, which generates three graphs of size $m =100, 150, 250$. Other parameters: the number of nodes $n = 50$, the random reconnection probability $p=1/2$, the ratio $|V_1|/n = 1/2$, the period $T=70$, the budget $B =5$. 

It can be seen in **Fig. 1 (a)** that, at a given time period ($t>10$), the difference between the number of susceptible and infected individuals becomes larger as the edge density increases. The similar phenomenon also happens between the number of infected and recovered individuals in the end stage of SIR-LT model, as shown in **Fig. 1 (b)**. Moreover, from above figures, we can also find out the time when the number of infections peaked for the first time becomes shorter as the edge density increases.

![](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIR-dynamic.png)  |  ![](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIR-masks.png)
:-------------------------:|:-------------------------:
(a)              | (b) 

**Fig. 2** Diagram of the SIR-LT dynamic network model with initial values $|V|=50,|V_1|/|V|=1/2, T=70$, $t_0=5,B=5,n_0=1$. (a) the susceptible, infected and recovered population fraction curves; (b) fraction of individuals wearing masks versus time in the network $G$.

Moreover, considering the change of behavior on the transmission process, we compute the infection curves for dynamic network model. **Fig. 2** shows how this strategy of wearing masks affects the transmission process in SIR model. The total number of infected individuals within $70$ days in this dynamic SIR-LT model is much less than that of SIR-LT model, and three curves in **Fig. 2 (a)** becomes stable quickly. To some extent, **Fig. 2** illustrates that if people can take precautions quickly to protect themselves, it will be very effective to prevent epidemic spread.

### Numerical Results

We compare the running times and solution properties of above-mentioned optimization models and they are displayed in **Table 1**. The proposed models were implemented in Python 3.6 using the optimization solver CPLEX 12.10 with default settings. 
All the experiments were performed on a Linux server running CentOS 7 with one AMD EPYC 7642 48-Core processor (2.3GHz) and 512GB memory. Computational time is reported by CPU seconds.

From **Table 1**, we can observe that the computation time of these models is 
closely related to the number of edges in a graph and the budget we provided. And the optimization solver was not efficient in solving these models in large networks. Computational experiments also illustrate that solving SIR-LT-dynamic model is more challenging than solving the other models, as some instances are practically unsolvable within 24 hours in this dynamic model. 

![](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/Table-1.png)

### Included files

Inputs -  the connected Watts-Strogatz small-world graphs we used in the paper 

SI.ipynb, SIS.ipynb, SIR.ipynb - three LT optimization models provided in the paper

### Requirements

This project relies on the `docplex` package to solve integer linear optimization models,  more instructions can be found here:

- https://pypi.org/project/docplex/
- https://ibmdecisionoptimization.github.io/docplex-doc/
