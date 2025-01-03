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
