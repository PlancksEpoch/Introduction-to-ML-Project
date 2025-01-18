# Introduction to ML Project - Mazerunner T-maze (Reinforcement Learning in Unity)

## Overview

This repository documents my journey to create an intelligent virtual agent, named **Boats**, capable of completing a waypoint-finding task within a custom-built video game environment. The project combines reinforcement learning (RL) techniques with Unity's ML-Agents toolkit to explore the metaphysical concept of "the present moment" through data-driven behavior analysis.

## Key Highlights

1. **Philosophical Motivation**: This project explores "thick time" — the idea that each moment contains a spectrum of potential futures, represented here as the many possible pathways Boats can take to reach its goal.
2. **Technical Achievement**: Integration of Unity ML-Agents with custom code to train an autonomous avatar in a Bomberman-inspired environment.
3. **Visualization of Outcomes**: While initial plans for line visualizations were deferred, the project's results showcase the agent's progress and the viability of RL for virtual task environments.

## Repository Structure

- **Proposal**: Contains the project proposal detailing the philosophical foundation and technical approach. ([View PDF](https://github.com/PlancksEpoch/Introduction-to-ML-Project/blob/main/Proposal/DSC412_001_FA24_PR_sbrantl.pdf))
- **Final Report**: Documents the project's development, results, and future directions. ([View PDF](https://github.com/PlancksEpoch/Introduction-to-ML-Project/blob/main/Final_Report/DSC412_001_FA24_FR_sbrantl.pdf))
- **Mazerunner_ML_Final_Code_Base**: The Unity project files, including scripts and configurations for training Boats.
- **config/mazerunner_config.yml**: YAML file for training configurations.
- **requirements.txt**: Python dependencies for setting up the conda environment.

## Metaphysics Meets Virtual Reality

### What is "Thick Time"?
"Thick time" refers to the spread of actualizable spatial arrangements available at any moment. This project seeks to operationalize this concept by generating and analyzing Boats' pathways within the game environment. Each trajectory represents one of many possible futures emerging from a common starting point.

### Project Significance:
- Reinforces the potential of virtual task environments as tools for studying decision-making.
- Suggests parallels between human neurophysiology and agent learning trajectories.
- Bridges philosophical inquiry and computational experimentation.

## Technical Details

### Environment Setup:
The Mazerunner game is a simplified Bomberman-style environment featuring a T-maze with a single waypoint. Key modifications included:
- Stripping down the game to remove extraneous mechanics (e.g., bombs, enemies) for initial training.
- Adding Ray Perception Sensors and reward structures to guide agent behavior.

### Learning Algorithm:
The project employed Proximal Policy Optimization (PPO), balancing exploration and exploitation to refine the agent's navigation.

### Reward Function:
The final reward function encouraged exploration and efficiency:
- Positive rewards for movement, discovering new locations, and reaching waypoints.
- Penalties for collisions, time delays, and inefficient paths.

## Results

Boats demonstrated significant learning:
- Achieved 10 successful waypoint completions across trials.
- Highlighted the potential for RL to generate meaningful spatiotemporal data.

While the project fell short of creating line visualizations, it underscored the feasibility of using RL for behavior analysis in controlled environments.

## Future Directions
1. **Restoring Complexity**: Reintroducing elements like bombs and enemies for more challenging tasks.
2. **Model Comparisons**: Exploring other RL algorithms (e.g., Deep Q-Learning).
3. **Human Comparisons**: Comparing agent trajectories with human player data to investigate shared decision-making heuristics.

## Setup Instructions

### Prerequisites:
- Unity 2021.1 or higher
- Unity ML-Agents package 3.0.0
- Python 3.8

### Steps:
1. Clone the repository:
    - `git clone https://github.com/YourRepoLink/Introduction-to-ML-Project.git`
2. Create a conda environment:
    - `conda create --name mazerunner python=3.8`
    - `conda activate mazerunner`
    - `pip install -r requirements.txt`
3. Open the Unity project in Unity Hub.
4. Start training:
    - `mlagents-learn config/mazerunner_config.yml --run-id=MazerunnerRun1`
5. Press "Play" in Unity to begin training episodes.
