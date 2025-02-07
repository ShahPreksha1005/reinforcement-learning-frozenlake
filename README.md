# Reinforcement Learning with FrozenLake

## Introduction
This project introduces core Reinforcement Learning (RL) concepts using the OpenAI Gym (now Gymnasium) library. The **FrozenLake-v1** environment is used to demonstrate how an agent interacts with the environment, chooses actions, and maximizes rewards.

## Key Concepts in Reinforcement Learning
- **Agent:** The decision-maker (our RL policy).
- **Environment:** The world the agent interacts with (FrozenLake).
- **State:** A specific situation in the environment.
- **Action:** A move the agent can take (Left, Down, Right, Up).
- **Reward:** A signal received after an action indicating success or failure.

## Environment Setup: FrozenLake
**FrozenLake-v1** is a grid-based environment where an agent must navigate a slippery 4x4 grid world to reach a goal while avoiding holes.

- **Map:** 4x4 grid (Agent starts at top-left, Goal is at bottom-right).
- **Objective:** Reach the goal ("G") while avoiding holes ("H").
- **Action Space:**  
  - `0`: Left  
  - `1`: Down  
  - `2`: Right  
  - `3`: Up  

## Installation
To run the code, install the required packages:

```bash
pip install gymnasium numpy
```

## Implementation
The implementation demonstrates agent-environment interaction using a deterministic policy (is_slippery=False):

```python
import gymnasium as gym

# Create the FrozenLake environment (deterministic setup)
env = gym.make('FrozenLake-v1', map_name="4x4", render_mode='human', is_slippery=False)
```

## Running the Code
Execute the script to observe how the agent navigates the environment based on the deterministic policy.

## Results and Observations
- The agent follows a predefined strategy to navigate the grid.
- Deterministic behavior ensures predictable movements without slipping.

## Future Enhancements
- Implementing Q-learning for improved decision-making.
- Testing stochastic environments (`is_slippery=True`) for real-world unpredictability.
- Experimenting with different reward structures.

## References
- OpenAI Gymnasium Documentation: [https://gymnasium.farama.org/](https://gymnasium.farama.org/)

---
