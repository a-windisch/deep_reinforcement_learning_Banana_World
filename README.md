# Project 1 (Deep Reinforcement Learning - Banana World)
---
[Andreas Windisch, Jan. 2019](https://www.linkedin.com/in/andreas-windisch-physics/)

This notebook contains the documentation for Project 1 of the [Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893). Feel free to play with this code as you please. Also, in case you have any questions or comments, or simply want to contact me, use the link to my LinkedIn profile above, or write me directly using [andreas.windisch@yahoo.com](andreas.windisch@yahoo.com). Have fun exploring this nice project! :-)

### 0. Synopsis

In this project, we will train an Agent to pick up bananas in a world with yellow and blue bananas. The agent will be trained to pick up yellow bananas, while avoiding blue ones. The environment is provided by Unity ML and consists of a world with square boundaries. Within those boundaries (walls), the Agent is allowed to move around freely. In this particular example, the Agent percieves the world through ray-based information. The Agent could also be trained using pixel information, which would require a Convolutional Neural Network instead of the fully connected one used in this example.  

#### Action Space
The Agent can choose from four different actions:
- move forward
- move backward
- turn left
- turn right

#### Observation Space
The size of the observation space in this example is 37.

#### Rewards
For every yellow banana collected, the Agent receives a reward of +1.
For every blue banana collected, the Agent receives a reward of -1.

#### Goal
The training of the Agent is over, once it manages to collect an average reward of +13 over 100 consecutive episodes (the task is formulated in an episodic fashion).

#### The untrained Agent
Here is an animation of the untrained Agent who doesn"t have a clue as of what to do in this world. The actions are chosen uniformly random, hence the random-walk like behavior.
![The untrained Agent](random.gif)

#### The trained Agent
After siccessful training, the Agent's actions are not erratic and random anymore. The Agent tries to collect as many yellow bananas as possible, as shown in the animation.
![The trained Agent](trained.gif)

### 1. Files in this repository

* README.md - This file
* Report.md - A report containg the details of the implementation 
* Banana_World.ipynb - A Jupyter Notebook containing the main code for training the Agent 
* model.py - The fully connected Neural Network used for training (PyTorch)
* dqn_agent.py - Definitions for the Agent and its actions
* checkpoint.pth - The saved status of the network
* score.png - A plot of the score over the training episodes
* random.gif - Animation of the untrained Agent
* trained.gif - Animation of the trained Agent

### 2. Running the code
The code is this repository requires numpy, PyTorch, Unity ML Agents and Jupyter. Make sure that those are installed. Then, just clone the repository and open the Notebook 'Banana_World.ipynb'. Follow the instructions within the notebook to train the Agent.
