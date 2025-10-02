# Deep-Q-Network

## Technologies Used
- PyTorch
- OpenAI Gym

## Problem Statement
The goal of this project is to train a DQN agent to balance a pole on a cart for as long as possible. This classic control problem serves as a benchmark to evaluate the performance of reinforcement learning algorithms.

## Solution Approach
The solution uses a DQN agent with experience replay and target network. The key components of the project are:
- Q-Network: A neural network that approximates the action-value function.
- Replay Buffer: A data structure to store and sample past experiences for training.
- DQNAgent: A class that defines the agent's behavior, including action selection and learning.

The agent is trained using a variant of the Q-learning algorithm that incorporates deep learning for function approximation.

## Results
The trained agent achieved an average reward of 185.08 over 100 test episodes, demonstrating its ability to effectively solve the CartPole-v1 environment.
