---
title: "Optimization Algorithm"
date: 2024-12-07
---


# iterative algorithm
## elements
* initial point(fine for convex problem)
* search direction
* step size/ learning rate
* stopping criterion

## A useful Algorithm Design Framework
suppose the task is min L, then we design a framework as:

$$  
\theta_{k+1} = min\{q_{k}+\frac{1}{2u_k}\|\theta-\theta_k\|_2^2\}
$$

**comment** cannot directly minimize the first approximation term, which is accurate only around $\theta_k$, thus we need the proximal term, which can pinish a large step

* when $q_k$ is linear approximation of L $Rightarrow$ gradient descent
* when $q_k$ is second-order approximation of L $Rightarrow$ Newton's method
* when $q_k$ is L $Rightarrow$ proximal point method(solving nonsmooth problem)
* when $q_k$ is single component linear approximation of L $Rightarrow$ stochastic gradient method

**almost universal algorithmic design strategy**
solving the original problem by solving a sequence of simpler subproblems

# Choice of search direction
## Gradient-based Optimization Algorithm

> most learning problems do not have closed form solution, but they are convex problems, which provide great property when using gradient-based methods
>
> ex. Logistic regression, SVM, ...,
> 
> namely, the point where $\{nbala}=0$ is the global optimal point

### GD
more info will be shown in optimization part! 
- [] to be down
                                                                                                                                               
### convergence

# Choice of Learing rate


