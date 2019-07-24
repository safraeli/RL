# Report of Navigation Project Submission

The submission implementnts a Deep Q Network Algorithm where the agent hold a deep NN of the format:
* fc1 = nn.Linear(state_size, fc1_units)
* fc2 = nn.Linear(fc1_units, fc2_units)
* fc3 = nn.Linear(fc2_units, action_size)

* The activation function for layers 1-2 is Relu.
* fc1_units=64, fc2_units=64

There are two identical networks of that size. Namely, Local and Target. 
The networks are initilized identically.  A Soft Update mechanizm transfers the information from the Local network to the Target network 
The network optimizer is ADAM

The netwroks are being updated using two (external) functions:
1. agent.step(state, action, reward, next_state, done). The step function also triggers the learn function (every UPDATE_EVERY stpes) which perfroms the soft update of the target network.

2. agent.act(state, eps) The act function also triggers the train function for the local network

A Replay Buffer is used to reduce the amount of sampling.  

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

![Trainig Progress](/images/trainigProgress.png)
Format: ![Trainig Progress](url)


