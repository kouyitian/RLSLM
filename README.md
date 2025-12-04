# Socially-Aware Navigation with Reinforcement Learning

This repository contains a reinforcement learning framework for socially-aware navigation in a 2D grid-based environment. The agent learns to navigate toward a goal while avoiding human obstacles, whose positions and orientations are considered in a social energy map.

## Top-down View in VR Project
Muiti-person scenario:

https://github.com/user-attachments/assets/4cba6d21-9af8-4023-991a-352dfa9a0251
Single-person scenario:


https://github.com/user-attachments/assets/1b28eae8-ec5b-4de7-9e70-7530f9dd7c79


## 📁 Project Structure

social_nav_rl/  
├── envs/  
│ └── gridworld_env.py # Custom RL environment  
├── scripts/  
│ ├── train.py # Main training script  
│ └── test.py # Model testing script  
├── utils/  
│ ├── callbacks.py # Episode tracking and logging  
│ ├── smooth.py # Gaussian smoothing utils  
│ └── arg_parser.py # CLI argument parser  
├── energy_map/  
│ └── normalized_get_eng_map.py  
├── log/ # Log files  
├── pic/ # Rendered trajectories  
├── main.py # Default entry point  
├── requirements.txt  
└── README.md  


## CLI Arguments

| Argument            | Description                          | Default                |
| ------------------- | ------------------------------------ | ---------------------- |
| `--start`           | Agent start position                 | `[13.5*33, 4.5*33]`    |
| `--end`             | Agent goal position                  | `[4.5*33, 13.5*33]`    |
| `--n_people`        | Number of human obstacles            | `3`                    |
| `--coordinates`     | List of human positions              | `[(4.5*33,3*33), ...]` |
| `--orientation`     | List of human orientations (degrees) | `[-90, 90, -90]`       |
| `--total_timesteps` | Number of training timesteps         | `10000`                |

