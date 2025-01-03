# Lunar Lander Environment - OpenAI Gymnasium

The Lunar Lander environment is a classic reinforcement learning task provided by OpenAI's Gymnasium library. The goal is to land a lunar module on a designated landing pad using a simulated environment that models physics and dynamics.

## Overview

The environment involves a lander module and a landing pad located at the center of the screen. The agent must control the lander by firing its thrusters to achieve a safe landing. Rewards are provided based on the agent's ability to land successfully and penalized for crashes or excessive fuel consumption.

### Key Features

- **Physics-based Simulation**: Realistic gravity, thrust, and collision dynamics.
- **Discrete and Continuous Actions**: Supports both discrete and continuous action spaces.
- **Customizable Difficulty**: Includes options for wind and terrain variability.
- **OpenAI Gymnasium Compatibility**: Seamlessly integrates with popular reinforcement learning libraries.

## Installation

Make sure you have Python installed. Then, install the `gymnasium` library using pip:

```bash
pip install gymnasium
```

Clone this repository and navigate to the project directory:

```
git clone https://github.com/openai/gymnasium.git
cd gymnasium
```

## Usage

To use the Lunar Lander environment in your reinforcement learning projects, follow the example below:

## Discrete Action Space
```
import gymnasium as gym

env = gym.make("LunarLander-v2")
observation, info = env.reset()

done = False
while not done:
    action = env.action_space.sample()  # Random action
    observation, reward, done, truncated, info = env.step(action)
    env.render()

env.close()
```

## Continuous Action Space

```
env = gym.make("LunarLanderContinuous-v2")
observation, info = env.reset()

done = False
while not done:
    action = env.action_space.sample()  # Random action
    observation, reward, done, truncated, info = env.step(action)
    env.render()

env.close()
```
## Environment Details
### Observations

The environment returns an 8-dimensional observation vector:
1. X-coordinate of the lander (horizontal position).
2. Y-coordinate of the lander (vertical position).
3. Horizontal velocity.
4. Vertical velocity.
5. Angle of the lander.
6. Angular velocity.
7. Left leg contact with the ground (1 if touching, 0 otherwise).
8. Right leg contact with the ground (1 if touching, 0 otherwise).

### Actions
1. Discrete: 0 (Do nothing), 1 (Fire left engine), 2 (Fire main engine), 3 (Fire right engine).
2. Continuous: 2-dimensional vector [main engine power, side engine power] where values range from -1 to 1.

### Rewards
1. Positive reward for landing successfully.
2. Negative reward for crashing or going out of bounds.
3. Penalties for excessive fuel usage.

### Customization
You can customize various aspects of the environment, such as:
1. Wind effects: Add randomness to simulate wind forces.
2. Terrain variability: Modify the surface roughness or obstacles.
For advanced customization, refer to the source code in the gymnasium/envs/box2d/lunar_lander.py file.

## Contributing
Contributions are welcome! If you want to contribute to the development or improve documentation, please submit a pull request.

## License
This environment is released under the MIT License. See the LICENSE file for details.
