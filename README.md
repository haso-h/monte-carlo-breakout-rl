# Monte Carlo Reinforcement Learning Agent for Breakout

## Overview
This project demonstrates a **reinforcement learning approach** to training an agent to play a simplified version of the classic game Breakout.  
The agent interacts with a custom-built grid-based environment, using **Monte Carlo control** to learn an optimal policy for moving a paddle and breaking all bricks while avoiding losing the ball.

---

## Objectives
- Implement a **custom Breakout environment** from scratch using Python.
- Develop a reinforcement learning agent based on **Monte Carlo control**.
- Explore key RL concepts:
  - Episodic learning
  - State-action value functions (Q-values)
  - ε-greedy exploration
  - Policy improvement based on episode returns
- Compare performance across different game layouts and hyperparameter settings.

---

## Environment
The environment is a simplified grid-world representation of Breakout:
- **Grid size:** 15 (width) × 10 (height) cells.
- **Elements:**
  - Bricks arranged in different patterns (rectangle, triangle, zigzag).
  - A paddle that can move left, stay still, or move right.
  - A ball with discrete horizontal (`vx`) and vertical (`vy`) velocities.
- **Actions:** {-1 = move left, 0 = stay, 1 = move right}.
- **Rewards:**
  - `+1` for hitting a brick.
  - `-1` for losing the ball.
- **Episode termination:** All bricks cleared or ball lost.

---

## Algorithm – Monte Carlo Control
- **Policy:** ε-greedy policy that balances exploration and exploitation.
- **Returns:** Total reward collected during an episode.
- **Q-value update:**
  - After each episode, state-action pairs are updated with the average return observed.
- **Goal:** Learn an optimal policy that maximizes the total reward (i.e., clearing all bricks).
