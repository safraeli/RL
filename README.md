# Reinforcement Learning exercises
## Udacity RL - First Exercise

The submission includes four files:
* model.py - code for defining the NN
* dqn_agent.py - code with the Class Agent
* Navigation.ipynb - code for training the model 
* checkpoint_dqn.pth - the trained model

Note that the two py files were taken as-is with minor changes to meet the different environment from the sample DQN code provided as part of the Deep Q-Networks lesson.

The Notebook file was changed to:
1. Different environment (unity instead of gim)
2. Slightly different code for training the Agent

State and Action Spaces:
States: 37
Actions: 4 (directions in 2D)
Termination condition (environment is considered solved when): the agent is able to receive an average reward (over 100 episodes) of at least +13

Output:
Episode 100	Average Score: 1.12
Episode 200	Average Score: 4.88
Episode 300	Average Score: 8.34
Episode 400	Average Score: 10.43
Episode 487	Average Score: 13.03
Environment solved in 387 episodes!	Average Score: 13.03

To run the code, simply go thru the Notebook cells and execute one-by-one.

