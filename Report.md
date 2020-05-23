## This Report is a part of my Udacity project submission 

The aim of this project is to train a RL agent to navigate into a 3D virtual environment and collect yello bananas while avoiding yello bananas . 
it gains a reward of +1 on collecting yellow bananas and a reward of -1 on collecting blue bananas 

# the environment is as follows:
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The RL task here is an episodic task to sove the environment and the RL must get an average of +13 score over 100 constructive episodes. 

# Algorithm Used : 

A Deep Q network was implemented to the following enviroment . A DQN takes agents states as inputs and outputs Q action values . further it uses experience replay and target network to stabilize the unstabilities the neural network does to the agent . 

The Architecture of the model is as follows:
	 The Model has 3 fully convolutional layers. The no of neurons in the first layer is 64 and the last layer are equal to the action size . all the layers except the last 		 layer uses Relu activation function 


# Hyperparameters :

    BUFFER_SIZE = int(1e5) # replay buffer size
    BATCH_SIZE = 64 # minibatch size
    GAMMA = 0.99 # discount factor
    TAU = 1e-3 # for soft update of target parameters
    LR = 5e-4 # learning rate
    n_episodes = 2000 # maximum number of training episodes
    max_t = 1000 # maximum number of time steps per episode
    eps_start = 1.0 # starting value of epsilon, for epsilon-greedy action selection
    eps_end = 0.01 # minimum value of epsilon
    eps_decay = 0.995 # multiplicative factor (per episode) for decreasing epsilon

