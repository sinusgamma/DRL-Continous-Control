# Report Continous Control

### The Algorithm

I have implemented the DDPG (Deep Deterministic Policy Gradient) algorithm for solving the environment. [DDPG algorithm description.](https://arxiv.org/abs/1509.02971)

### The Parameters

The actor and critic networks have two hidden layers. Sizes: [256, 128]
I used one batch normalization layer for the networks.
For updating the critic network I used gradient clipping to avoid exploding gradients.

replay buffer size:                     BUFFER_SIZE = int(1e5)  
minibatch size:                         BATCH_SIZE = 1024      
discount factor:                        GAMMA = 0.99           
for soft update of target parameters:   TAU = 1e-3            
earning rate of the actor:              LR_ACTOR = 1e-4         
learning rate of the critic:            LR_CRITIC = 1e-3        
L2 weight decay:                        WEIGHT_DECAY = 0

### Experiences

It was very hard to solve the environment. I trained the single agent version of the environment as well. The scores of the single agent version showed very large variance.
In the case of the multi-agent version using batch normalization and larger batch size helped to stabilize the training and resulted in fast score increase.

![scores](https://github.com/sinusgamma/DRL-Continous-Control/blob/master/result.jpg)

After the alterations the environment was solved after 138 episodes.

### Optional Future Improvements

The environment was solved fast with the above parametes, but there is place for improvements. It is possiple to tune the hyperparameters, try out different neural network architectures.

In the help it was suggested, that instead of updating the actor and critic networks 20 times at every timestep, we could update the networks 10 times after every 20 timesteps. 

It is possible to try out different algorithms than DDPG. As discussed in [this paper](https://arxiv.org/abs/1604.06778), Trust Region Policy Optimization (TRPO) and Truncated Natural Policy Gradient (TNPG) should achieve better performance. It is also possibleto implement Proximal Policy Optimization (PPO), which has also demonstrated good performance with continuous control tasks.

