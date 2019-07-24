# Report of Navigation Project Submission

The submission implementnts a Deep Q Network Algorithm where the agent hold a deep NN of the format:
* fc1 = nn.Linear(state_size, fc1_units)
* fc2 = nn.Linear(fc1_units, fc2_units)
* fc3 = nn.Linear(fc2_units, action_size)

The activation function for layers 1-2 is Relu.

The network optimizer is ADAM

The netwrok is working at two functions:
1. agent.step(state, action, reward, next_state, done)
2. agent.act(state, eps)

Agent Hyperparameters:
* BUFFER_SIZE = int(1e5)  # replay buffer size
* BATCH_SIZE = 64         # minibatch size
* GAMMA = 0.99            # discount factor
* TAU = 1e-3              # for soft update of target parameters
* LR = 5e-4               # learning rate 
* UPDATE_EVERY = 4        # how often to update the network



Episode 100	Average Score: 1.12
Episode 200	Average Score: 4.88
Episode 300	Average Score: 8.34
Episode 400	Average Score: 10.43
Episode 487	Average Score: 13.03
Environment solved in 387 episodes!	Average Score: 13.03
