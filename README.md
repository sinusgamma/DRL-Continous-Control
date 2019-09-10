# DRL Continous Control
 Deep Reinforcement Learning AI - multiple robot arms

 This project is part of Udacity's Nanodegree on Deep Reinforcement Learning (https://eu.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893).

## Multiple Robot Arms

![Robot Arms](https://github.com/sinusgamma/DRL-Continous-Control/blob/master/reacher.gif)

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1

The environment contains 20 identical agents, each with its own copy of the environment.

Solving the environment: The agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores.
This yields an average score for each episode (where the average is over all 20 agents).

## Install the Environment

### Step 1: Clone the DRLND Repository
To set up the environment, please follow the instructions in the [DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies). These instructions can be found in [README.md]((https://github.com/udacity/deep-reinforcement-learning#dependencies)) at the root of the repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.

(For Windows users) The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a Windows VM such as Bootcamp or Parallels.

### Step 2: Download the Unity Environment
For this project, you will not need to install Unity - this is because we have already built the environment for you, and you can download it from one of the links below. You need only select the environment that matches your operating system:

Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)<br>
Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)<br>
Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)<br>
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)<br>

Then, place the file in the p1_navigation/ folder in the DRLND GitHub repository, and unzip (or decompress) the file.

## Training the AI

The Continous_Control.ipynb file containes the training code and the test run. Running all the cells will train and save a new model, then calculate a test score with the trained agent.