[image]: https://raw.githubusercontent.com/francnascimento/DeepQLearningBananaGrabber/master/plot_reward.png "Plot Reward"

# Project Report

## Objective
The objective of this experiment was to train an agent, using Deep Q-Learning, that by performing 100 sessions would be able to reach the average scores greater than 13 in the pre-defined environment.

## Results
My trained brain(Agent) was able to successfully meet specifications at episode 397 of simulation.

#### Average per 100 episodes:
Episode 100	Average Score: 0.92</br>
Episode 200	Average Score: 4.05</br>
Episode 300	Average Score: 7.33</br>
Episode 400	Average Score: 10.64</br>
Episode 497	Average Score: 13.00</br>
Environment solved in 397 episodes!	Average Score: 13.00

#### Rewards per episode.
![Plot Reward][image]

## Model Architecture
The neural-network used have the following structure defined in model.py:

#### At Input Layer:
A fully connected layer with 37 inputs and 64 outputs with ReLU activations

#### Followed by a Hidden Layer:
A fully connected layer with 64 inputs and 64 outputs with ReLU activations

#### Then finally a Output Layer:
A fully connected layer with 64 inputs and 4 outputs

# Parameters used in DQN algorithm

* BUFFER_SIZE  = int(1e5) # replay buffer size. 
* BATCH_SIZE   = 64       # minibatch size
* GAMMA        = 0.99     # discount factor
* TAU          = 1e-3     # for soft update of target parameters
* LR           = 5e-4     # learning rate(step size) to adjust neural network weights
* UPDATE_EVERY = 4        # how often to update the network
</br>

* EPSILON       = 1 # factor that controls exploration
* EPSILON_DECAY = 0.995 # decay factor
* with the decay function as: EPSILON = EPSILON_DECAY*EPSILON
* and min value for EPISON as 0.01

# Ideas for Future Work
Below are some ideas and techniques that I belevie would bring some new perspective to this simple DQN approach:

* Implement a diferent neural network architecture for more accurate learning
* Implement techniques that would bring improvements to the original Deep Q-Learning algorithm, like
  * Double DQN
  * Dueling DQN
  * Prioritized Experience Replay
* Use images from the environment together with a Convolutional neural network to train the Agent.
* Also try out some Dicretization Technique for the continuos values from the environment.
