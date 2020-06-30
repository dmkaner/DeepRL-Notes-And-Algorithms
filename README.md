# DeepRL Notes & Algorithms



## Table of Contents

### Notes
Will be added soon.

### Implementations
Will be added soon.



# Spinning Up Algorithms



## RL Notes from Spinning Up Docs

Introduced terminology:
- states and observations
- action spaces
- policies
- trajectories
- different formulations of return
- the RL optimization problem
- value function

**States and observations:** State is a complete description of the world that the agent lives in, and observation is an incomplete picture of the state. State is most often represented in vector form. **"s"** represents state and **"o"** represents observation in equations.

**Action spaces:** Action spaces refer to the set of actions an agent can take in a given state. Action spaces make be different in different states in a state space. Actions spaces can be discrete and continuous. 

**Policies:** Policy is the rule an agent uses to decide what to do. There are deterministic (nothing is random) and stochastic (some randomness). Deterministic policy symbol is **"[img]http://www.sciweavers.org/tex2img.php?eq=%20%5Cmu%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0[/img]"** and stochastic is **"\pi"** in equations. For Deep RL there are paramatrized policies that take in paramters for things such as weights in a NN, and paramters are represented by **"\theta"** or **"\phi"**. 

In stochastic policies for Deep RL, categorical policies (discrete) and diagnol gaussian policies (continuous) are the most used. 

**Trajectories:** Trajectory a sequence of states and actions in the world: **\tau = (s_0, a_0, s_1, a_1, ...)**. State transitions can be deterministic: **s_{t+1} = f(s_t, a_t)** or stochastic: **s_{t+1} \sim P(\cdot|s_t, a_t)**.

Trajectories may also be reffered to as episodes. 

**Different formulations of return:** The reward function is very important, denoted by **"R"** and is dependent on the current state, the current action taken, and the next state coming from that action: **r_t = R(s_t, a_t, s_{t+1})**. The goal of the agent is to maximize the reward over the trajectory, unlinke a greedy algorithm which would just try to maximize it at the current state. 

There is finite-horizon undiscounted return (sum of rewards in fixed window): **R(\tau) = \sum_{t=0}^T r_t** and infinite-horizon discounted return (sum of all rewards): **R(\tau) = \sum_{t=0}^{\infty} \gamma^t r_t**.

**The RL optimization problem:** The goal in RL is to select the policy which maximizes **expected return**. Optimal policy for a stochastic policy is: **"\pi^*"**. 

**Value function:** Value functions give you the value of a state or state-action pair, like showing how good having a flush is in poker. There are four main value functions:
- On-Policy Value Function: **V^{\pi}(s)** always act according to policy
- On-Policy Action-Value Function: **Q^{\pi}(s,a)** take an arbitrary action then always act according to policy
- Optimal Value Function: **V^*(s)** always act according to the optimal policy 
- Optimal Action-Value Function: **Q^*(s,a)** take an arbitrary action then always act according to optimal policy



## Vanilla Policy Gradient

VPG is an on policy algorithm which pushes up probabilities of high reward actions and pushes down probabilites of low reward actions, until you arive at the optimal policy. 

## Trust Region Policy Optimization

## Proximal Policy Optimization

## Deep Deterministic Policy Gradient

## Twin Delayed DDPG

## Soft Actor-Critic


<!-- # An Introduction to Deep Reinforcement Learning Notes
[Book Here](https://arxiv.org/abs/1811.12560)

## Chapter 1: Introduction

Chapter 1 just goes over the motivation of the book and lays out the contents of each chapter.

## Chapter 2: Machine Learning & Deep Learning

Machine learning is ultimately a form of pattern recognition and can be summarized in three topics, being: 
- Supervised Learning: training from labeled data
- Unsupervised Learning: training from unlabeled data
- Reinforcement Learning: training to maximize cumulative rewards from certain actions

All three of these are greatly helped through function approximators, which are essentially the heart of ML. Some examples being:
- Linear models
- SVMs
- Descision trees
- Gaussian processes
- Deep Learning

### Supervised learning and the concepts of bias and overfitting

### Unsupervised learning

### The deep learning approach



## Chapter 3: Intro to RL

## Chapter 4: Value-based Methods for Deep RL

## Chapter 5: Policy Gradient Methods for Deep RL

## Chapter 6: Model-base Methods for Deep RL

## Chapter 7: The Concept of Generalization

## Chapter 8: Particular Challenges in the Online Setting

## Chapter 9: Benchmarking Deep RL

## Chapter 10: Deep RL Beyond MDPs

## Chapter 11: Perspectives on Deep RL 

## Chapter 12: Conclusion -->