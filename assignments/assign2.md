# Assignment 2

## Reading 

- Read Sections 3.1, 3.2, 3.3, 3.4, and 3.5 from the main book

- Read Chapter 1 (p. 57 - p. 67) from the supplementary book


## Paper-based 

Prove that adding a constant $c$ to all the rewards adds a constant, $v_c$, to the values of all states, and thus does not affect the relative values of any states under any policies. What is $v_c$ in terms of $c$ and $\gamma$?

## Implementation 

As shown in Figure 3.2 in the main book, the figures illustrates a simple MDP represented by a rectangular gridworld. Each cell in the grid corresponds to a state in the environment. From any cell, the agent can take one of four possible actions: move `north`, `south`, `east`, or `west`. These actions **deterministically** move the agent one cell in the chosen direction. If an action would cause the agent to move off the grid, its position remains the same, but it receives a reward of -1. All other moves yield a reward of 0, except for actions taken in two special states, A and B. From state A, any action gives a reward of 10 and moves the agent to state A’. Similarly, from state B, any action yields a reward of 5 and moves the agent to state B’.

Write a python program that 
1. Define a transition probability matrix (uniform distribution)
1. Start from a chosen initial state, simulate the Markov chain for a large number of transitions (1000 steps)
1. Repeat the above step multiple times to generate as many processes as you can 
1. Compute the value function for each state under two different reward functions 
   1. reward = -1 if the agent moves off the grid, reward = 10 for any action from state A, reward = 5 for any action from state B, reward = 0 for all cases
   2. reward = 5 if the agent moves off the grid, reward = 16 for any action from state A, reward = 11 for any action from state B, reward = 6 for all cases
1. Compare and discuss how the value functions change under these two reward settings
