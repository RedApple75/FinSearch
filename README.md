# Deep Reinforcement Learning for Algorithmic Trading

## Technologies Used
- Python
- Stable-Baselines3
- OpenAI Gym
- Pandas & NumPy
- Matplotlib
- statsmodels
- TensorFlow

## Problem Statement
The goal of this project was to develop a Deep Reinforcement Learning (RL) agent capable of learning a profitable trading strategy for the Nifty100 index. The primary objective was to determine if this RL approach could outperform traditional time-series forecasting benchmarks like ARIMA and LSTM in a realistic backtesting environment.

## Solution Approach
The solution uses a Proximal Policy Optimization (PPO) agent trained in a custom trading environment. The key components are:

### Custom Trading Environment
An OpenAI Gym environment that simulates the Nifty100 market. It provides a state composed of over 10 technical indicators (RSI, MACD, momentum, etc.) and uses a risk-adjusted reward function that penalizes volatility.

### PPO Agent
A PPO agent from Stable-Baselines3 was chosen for its stability and effectiveness in continuous action spaces. The agent learns a policy to output a continuous action from -1 (full short) to +1 (full long), representing the desired portfolio allocation.

### Benchmark Models
ARIMA and LSTM models were implemented to generate buy/sell/hold signals, serving as a baseline for performance comparison against the RL agent.

### Backtesting Framework
A realistic backtester was built to simulate trades, accounting for practical considerations like transaction costs and drawdown.

## Results
In a rigorous out-of-sample backtest, the trained PPO agent significantly outperformed the traditional benchmarks and a buy-and-hold strategy on a risk-adjusted basis.

- **Return:** 15.3%
- **Sharpe Ratio:** 2.13

The results demonstrate the PPO agent's ability to learn a complete, adaptive trading policy that is more effective than strategies based on simple price prediction.
