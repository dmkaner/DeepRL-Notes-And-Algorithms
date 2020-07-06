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

**Policies:** Policy is the rule an agent uses to decide what to do. There are deterministic (nothing is random) and stochastic (some randomness). Deterministic policy symbol is **"![equation](http://www.sciweavers.org/tex2img.php?eq=%20%5Cmu%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)"** and stochastic is **"![equation](https://bit.ly/2YMk5Q0)"** in equations. For Deep RL there are paramatrized policies that take in paramters for things such as weights in a NN, and paramters are represented by **"![equation](https://bit.ly/2YMk7HC)"** or **"![equation](https://bit.ly/1qZlGxq)"**. 

In stochastic policies for Deep RL, categorical policies (discrete) and diagnol gaussian policies (continuous) are the most used. 

**Trajectories:** Trajectory a sequence of states and actions in the world: **![equation](https://bit.ly/3geD1Nb)**. State transitions can be deterministic: **![equation](https://bit.ly/2Amenem)** or stochastic: **![equation](https://bit.ly/3ihLiBN)**.

Trajectories may also be reffered to as episodes. 

**Different formulations of return:** The reward function is very important, denoted by **"R"** and is dependent on the current state, the current action taken, and the next state coming from that action: **![equation](https://bit.ly/31x7S3i)**. The goal of the agent is to maximize the reward over the trajectory, unlinke a greedy algorithm which would just try to maximize it at the current state. 

There is finite-horizon undiscounted return (sum of rewards in fixed window): **![equation](https://bit.ly/2ZpmDCH)** and infinite-horizon discounted return (sum of all rewards): **![equation](https://bit.ly/2Vwzhij)**.

**The RL optimization problem:** The goal in RL is to select the policy which maximizes **expected return**. Optimal policy for a stochastic policy is: **"![equation](https://bit.ly/3iopRiL)"**. 

**Value function:** Value functions give you the value of a state or state-action pair, like showing how good having a flush is in poker. There are four main value functions:
- On-Policy Value Function: **![equation](https://bit.ly/2NHUoKf)** always act according to policy
- On-Policy Action-Value Function: **![equation](https://bit.ly/2AiwbqB)** take an arbitrary action then always act according to policy
- Optimal Value Function: **![equation](https://bit.ly/3gi6YMt)** always act according to the optimal policy 
- Optimal Action-Value Function: **![equation](https://bit.ly/2YP5FPf)** take an arbitrary action then always act according to optimal policy

### Other important tidbits of info

Model-free vs. model-based: a model of an environment is a function which predicts state transitions and rewards. The algorithms covered here will be mostly model-free.



<!-- ## Vanilla Policy Gradient

VPG is an on policy algorithm which pushes up probabilities of high reward actions and pushes down probabilites of low reward actions, until you arive at the optimal policy. 

## Trust Region Policy Optimization

## Proximal Policy Optimization

## Deep Deterministic Policy Gradient

## Twin Delayed DDPG

## Soft Actor-Critic -->

# Udacity DeepRL Notes

**Episodic vs. Continuing tasks:** Episodic tasks have a well defined ending point like in a game of chess, and  continuing tasks do not, like the life space of a puppy robot perhaps. 

**The reward hypothesis:** All goals can be framed as the maximization of expected cumulative rewards. 

Reward equations can be very important and interesting, prioritizng certain actions over time in a mathematical way. Take a robot that you want to teach how to walk from A to B as fast as possible. The reward equation might look like a multi-term equation where there is a term for the robots velocity, deviation from the forward direction, and a constant for not falling over time. Each term will add or subtract to the total given reward for the robot in that time frame. 

**Cumulative reward:** It is important to give the robot the objective of increasing cumulative rewards and not just maximizing the nearest reward, for that would be a greedy algorithm and is often not too performant. We call this cumulative reward **return**. 

**Discounted return:** Discounted return refers to making future expected rewards less significant. 

**Markov Decision Process:** MDP is muy importante! And useful. We define reinforcment learning problems as MDPs so they are in a format that we can apply our algorithms to. It's defined as a set of states, actions, and rewards with one step dynamics and a discount rate. 

**Policy:** A policy is what interprets the current state and produces an output, being an action. Hopefully a good one. Choosing a definite action is deterministic, and choosing an action with some randomality is stochastic. 

**State-value fucntion:** The state-value function yields the expected return if the agent started in the specific state and followed the policy for all time steps. 

**Bellman equations:** Bellman equations can simplified down to this: The state-value of a certain state can be recursively obtained by the expected return of the current state plus the discounted state-value of the next state. 

