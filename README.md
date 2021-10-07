# Infections-Spread-Influence-Maximization
A repository to supplement the paper "Modeling the Spread of Infectious Diseases through Influence Maximization".

### Comparison of Different Edge Densities


(a) SIS-LT model             | (b) SIR-LT model 
:-------------------------:|:-------------------------:
![](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIS_compared.png)  |  ![](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIR_compared.png)

**Fig. 1** Comparison of different edge densities in LT optimization model with initial values $|V|=50, T=70$,$ t_0=5, B=5.$ 

We use three connected Watts-Strogatz small-world graphs of different edge densities for comparison. Each node joined with $5,7$ and $10$ nearest neighbors in a initial ring topology, which generates three graphs of size $m =100, 150, 250$. Other parameters: the number of nodes $n = 50$, the random reconnection probability $p=1/2$, the ratio $|V_1|/n = 1/2$, the period $T=70$, the budget $B =5$. 

It can be seen in **Fig. 1 (a)** that, at a given time period ($t>10$), the difference between the number of susceptible and infected individuals becomes larger as the edge density increases. The similar phenomenon also happens between the number of infected and recovered individuals in the end stage of SIR-LT model, as shown in **Fig. 1 (b)**. Moreover, from above figures, we can also find out the time when the number of infections peaked for the first time becomes shorter as the edge density increases.

(a)              | (b) 
:-------------------------:|:-------------------------:
![](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIR-dynamic.png)  |  ![](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIR-masks.png)

**Fig. 2** Diagram of the SIR-LT dynamic network model with initial values $|V|=50,|V_1|/|V|=1/2, T=70$, $t_0=5,B=5,n_0=1$. (a) the susceptible, infected and recovered population fraction curves; (b) fraction of individuals wearing masks versus time in the network $G$.

Moreover, considering the change of behavior on the transmission process, we compute the infection curves for dynamic network model. **Fig. 2** shows how this strategy of wearing masks affects the transmission process in SIR model. The total number of infected individuals within $70$ days in this dynamic SIR-LT model is much less than that of SIR-LT model, and three curves in **Fig. 2 (a)** becomes stable quickly. To some extent, **Fig. 2** illustrates that if people can take precautions quickly to protect themselves, it will be very effective to prevent epidemic spread.
