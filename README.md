# Experiment-With-Learning-Policies-On-Simple-Reinforcement-Policies
Our goal will be to experiment with learning policies on simple reinforcement policies using different methods. This experment will be devided into two parts. 

# Part 1

We will consider a simple 5 × 5 gridworld problem, described below. This is the simplest abstraction of a reinforcement learning problem that allows us to benchmark and compare various learning algorithms to one another and is known as the ‘gridworld’ environment.

![image](https://github.com/user-attachments/assets/19d72840-7bc8-479a-bd35-d846579a7d1e)

Each of the 25 cells of the gridworld represent a possible state of the world. An agent in the gridworld environment can take a step up, down, left or right. If the agent attempts to step off the grid, the location of the agent remains unchanged.

The blue, green, red and yellow squares represent special states at which the behaviour of the system is as follows. At the blue square, any action yields a reward of 5 and causes the agent to jump to the red square. At the green square, any action yields a reward of 2.5 and causes the agent to jump to either the yellow square or the red square with probability 0.5.

An attempt to step off the grid yields a reward of −0.5 and any move from a white square to another white square yields a reward of 0. Intuitively, an agent with a good policy should try to find the states with a high value, and exploit the rewards available at those states.

Our Experiment Tasks For Part 1 As follows-

1. We will consider a reward discount of γ = 0.95 and a policy which simply moves to one of the four directions with equal probability of 0.25. Estimate the value function for each of the states using-
   
   1.1 Solving The System of Bellman Equations Explicitly
   
   1.2 Iterative Policy Evaluation
   
   1.3 Value Iteration

3. Determine the optimal policy for the gridworld problem by -

   2.1 Explicitly Solving The Bellman Optimality Equation
   
   2.2 Using Policy Iteration With Iterative Policy Evaluation
   
   2.3 Policy Improvement With Value Iteration.

# Part 2

For Part 2, we will change the environment a bit by adding some terminal states represented as the black squares. This gives rise to episodes where termination occurs once the agent hits one of the black squares. We will also assume, unlike in Part 1, that any move from a white square to a white square yields a reward of -0.2.

![image](https://github.com/user-attachments/assets/9ffd4384-a787-4c7d-8c9d-c04cd5eeb0ef)

Our Experiment Tasks For Part 2 As follows-

1. We will use the Monte Carlo method with
   
   1.1 Exploring Starts

   1.2 Without Exploring Starts

   But the ϵ-soft approach to learn an optimal policy for this modified gridworld problem. We will use the same discount factor of γ = 0.95 as we have in the Part 1 above. We will start with a policy with equiprobable moves.

2. After that we will use a behaviour policy with equiprobable moves to learn an optimal policy. The dynamics of the world are known exactly, so we can actually compute the importance weights needed for this.

3. Finally, let’s suppose that at every step, we permute the locations of the green and blue squares with probability 0.1, while preserving the rewards and transition structure as before. So we will use policy iteration to determine a suitable policy for this environment.

# How To Run The Code


To run the code for this assignment, follow the steps below:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AzmolFK/Experiment-With-Learning-Policies-On-Simple-Reinforcement-Policies.git
   ```

2. **Navigate to the repository directory:**
   ```bash
   cd Experiment-With-Learning-Policies-On-Simple-Reinforcement-Policies
   ```

3. **Open the notebook in Google Colab:**
   - Go to [Google Colab](https://colab.research.google.com/).
   - Click on the "GitHub" tab.
   - Enter the repository URL: `https://github.com/AzmolFK/Experiment-With-Learning-Policies-On-Simple-Reinforcement-Policies`.
   - Select the notebook `Assignment_2_(Part1+Part2).ipynb`.

4. **Run the notebook:**
   - Once the notebook is open in Google Colab, follow the instructions provided within the notebook to run the code cells.
   - Ensure you have all the necessary libraries installed. You can install any missing libraries by running:
     ```python
     !pip install numpy matplotlib
     ```

5. **Reproduce the results:**
   - Follow the step-by-step instructions within the notebook to reproduce the results for both Part 1 and Part 2 of the assignment.

## Repository Structure
- `Assignment 2 RL Report.pdf`: PDF report of the assignment, including the problem statement, methodology, results, analysis, and conclusions for both Part 1 and Part 2.
- `Assignment_2_(Part1+Part2).ipynb`: Main notebook containing the implementation and analysis of reinforcement learning methods for both Part 1 and Part 2.
- `README.md`: Instructions for running the notebook and an overview of the assignment.
