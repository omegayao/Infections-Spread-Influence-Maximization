# Infections-Spread-Influence-Maximization
A repository to supplement the paper "Modeling the Spread of Infectious Diseases through Influence Maximization".

### Comparison of Different Edge Densities

![SIS-LT model](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIS_compared.png "SIS-LT model")![SIR-LT model](https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIR_compared.png "SIR-LT model")

<center class="half">    
<img src="https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIS_compared.png" alt="SIS-LT model"/><img src="https://github.com/omegayao/Infections-Spread-Influence-Maximization/blob/main/Figures/SIR_compared.png" alt="SIR-LT model"/>
</center>



We use three connected Watts-Strogatz small-world graphs of different edge densities for comparison. Each node joined with $5,7$ and $10$ nearest neighbors in a initial ring topology, which generates three graphs of size $m =100, 150, 250$. Other parameters: the number of nodes $n = 50$, the random reconnection probability $p=1/2$, the ratio $|V_1|/n = 1/2$, the period $T=70$, the budget $B =5$. 

It can be seen in Fig. \ref{LT-compared} (a) that, at a given time period ($t>10$), the difference between the number of susceptible and infected individuals becomes larger as the edge density increases. The similar phenomenon also happens between the number of infected and recovered individuals in the end stage of SIR-LT model, as shown in Fig. \ref{LT-compared} (b). Moreover, from Fig. \ref{LT-compared}, we can also find out the time when the number of infections peaked for the first time becomes shorter as the edge density increases.
