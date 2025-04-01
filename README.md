# Treasure Maze - Reinforcement Learning Agent

## Purpose

This project implements a reinforcement learning (RL) environment designed as a grid-based maze, where an autonomous agent (represented by a pirate) learns to navigate from a starting point to a target cell containing a treasure. The primary aim is to demonstrate core concepts of reinforcement learning, such as environment interaction, state-based decision making, reward acquisition, and experience replay.

## Implementation

### Environment

The environment is defined by the `TreasureMaze` class (`TreasureMaze.py`). It models the maze as a 2D NumPy array:

- `1.0` represents a free cell.
- `0.0` represents a blocked cell.
- The agent (pirate) starts at a designated cell and seeks to reach the bottom-right corner, which holds the treasure.

The environment tracks:
- Agent position and visited cells.
- State transitions based on agent actions.
- Reward assignment for each movement.
- Game termination conditions (win/loss based on reward threshold or goal achievement).

### Agent Experience

The agent's learning process is supported by the `GameExperience` class (`GameExperience.py`), which provides:

- Memory storage for past episodes.
- Sampling of state-action-reward tuples for training.
- Calculation of Q-values using a neural network model to guide policy improvement.

### Notebooks

The Jupyter Notebook (`Ward_Dennis_ProjectTwoMilestone.ipynb`) integrates the environment and experience logic. It orchestrates:

- Training loops using episodes.
- Interaction between agent and environment.
- Learning via mini-batch updates from stored experience.
- Visualization of learning progress and performance.

## Files

- `TreasureMaze.py`: Defines the environment logic.
- `GameExperience.py`: Implements the experience replay memory.
- `Ward_Dennis_ProjectTwoMilestone.ipynb`: Demonstrates the agent training process and environment interaction.
- `.pyc` files: Compiled bytecode versions for runtime efficiency (optional for source-based projects).
