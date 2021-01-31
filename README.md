# The Nurse scheduling: A discrete combinatorial optimization problem
Andrea Henshall, Azza Fadhel, Maninder Kaur, Srikar Vanavasma

## Abstract
The aim of this paper is to study the nurse scheduling problem using the Discrete Quadratic Model (DQM) solver. In this project, we seek out the optimal solution of assigning a group of nuurses under scheduling constraint in order to streamline the process of scheduling nursing staff and reducing the overall hospital costs.  

## Introduction 
Quantum Annealing is the most promising quantum technology to solve combinatorial optimzation problems involving large number of solutions by using the concept of quantum tunneling, entanglement, and superpoistion. We are invetigating the Nurse Scehduling Problem (NSP) with hard constraints using the D-Wave quantum annealing system with the Discreta Quadratic Model (DQM) solver accesible through Leap [1]. In this project, we are implementing the DQM solver to assign given number of nurses over a given number of schedule days and shifts with a hard constraint that nurses are not shceduled for more than 1 shift a day [2]. 

A discrete quadratic model is a polynomial over discrete variables with terms all of degree two or less. In this model, the variables can take discrete values from {0,1,2,3..} with the condition of no constarints applied.  Using a binary variable x_{i,u} to indicate whether discrete variable f{d}_i is set to case u, the objective function can be expressed by the equation:


\( E(\bf{x})
= \sum_{i=1}^N \sum_{u=1}^{n_i} a_{i,u} x_{i,u} + \sum_{i=1}^N \sum_{j=i+1}^N \sum_{u=1}^{n_i} \sum_{v=1}^{n_j} b_{i,j,u,v} x_{i,u} x_{j,v} + c \)


## Model implementation 

Here is the general overview of solving the problem:
* Assign the sie of the problem and parameters (number of schedule days, number of shifts, number of nurses)
* Assign the size of the problem (number of nurses and days) and parameters
* Assign the name and values of variables in DQM.
* Add quadratic costs and hard constraints 
- Don't schedule the same person for multiple shifts
- Don't change a nurse's schedule from 1 day to another
* Solve the problem 
* Check no nurses are scheduled for more than 1 shift per day
* Print the nurse schedule

## Results


## To do 

## Demonstrations
The GitHub repository link is https://github.com/iQuHACK/2021_JAMS/blob/main/DQM_nurse_v2_for_push.ipynb

## References

[1] Ikeda, K., Nakamura, Y. & Humble, T.S. Application of Quantum Annealing to Nurse Scheduling Problem. Sci Rep 9, 12837 (2019). https://doi.org/10.1038/s41598-019-49172-3

[2] Nurse scheduling problem, Wikipedia, https://en.wikipedia.org/wiki/Nurse_scheduling_problem

