To solve the environment, we used a Deep Deterministic Policy Gradients (DDPG) algorithm that uses 20 agents in parallel. The networks were trained for 200 episodes with a maximum timesteps per episode of 2000. Gradient clipping was used. Each agent adds to the replay buffer, and the actor and critic networks are updated once every timestep.

Both the actor neural network and the critic neural neutwork used 3 linear layers, with hidden dimensions of 128. We used Relu and tanh activation functions.

The hyperparameters used are as follow:

Buffer size: 1e5
Batch size: 128
Gamma: 0.99
Tau:1e-3 
Weight decay: 0
actor learning rate : 1e-3
critic learning rate : 5e-4

The hyperparameters for the Ornstein-Uhlenbeck process are:
mu:0
theta:0.15
sigma:0.1

The progression can be seen on the graph bellow. A score of 30 is reached by episode 25, and the average remains over 30 for more than 100 episodes.The highest reward (over 40) was reached around episode 50.

![download](https://user-images.githubusercontent.com/38821613/126284113-b8974db8-7d76-4a09-8f06-13a4792cf9ad.png)

A better score could be reach by spending more time finetuning the hyperparameters, notably the learning rate. We could also try to use newer models such as TD3.
