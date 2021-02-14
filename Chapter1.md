## Chapter 1
Reinforcement Learning: the main idea is that the agent learn from the environment by interacting with it and receving rewards. Process:
- S0: Our Agent receives state S0 from the Environment — we receive the first frame of our game (environment).
- A0: Based on that state S0, the agent takes an action A0 — our agent will move to the right.
- S1: Environment transitions to a new state S1 — new frame.
- R1: Environment gives some reward R1 to the agent — we’re not dead (Positive Reward +1).

Markov Decision Process (MDP): the process to maximize the cumulative reward.

#### Observations/States
- Observations: partial world with only observed environment.
- States: complete world with no hidden information

#### Action Space
- Discrete space: finite number of possible actions
- Continuous space: infinite number of possible actions.

#### Reward & Discounting
Cumulative reward: R(τ) is simply adding reward at each step t. 其中τ指一系列的States和Actions
单纯的使用cumulative reward不够，因为游戏刚开始一般reward较容易获得，而后更难。
因此需要引入discount rate: gamma

New Q = Current Q + lr * [Reward + discount_rate * (highest Q value between possible actions from new state) — Current Q value ]
