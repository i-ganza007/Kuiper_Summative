# Kuiper Summative - AI Drone Control System 🚁

A comprehensive reinforcement learning project implementing multiple RL algorithms to train autonomous drones for wildfire fighting and mission coordination.

## 🎯 Project Overview

This project develops AI-controlled drones capable of:
- **Autonomous Navigation** in grid-based environments
- **Wildfire Detection & Suppression** using water/retardant systems
- **Mission Completion** with optimal path planning
- **Resource Management** (fuel/water capacity constraints)

## 🏗️ Project Structure

```
Kuiper_Summative/
├── main.py                    # Main demo script with trained models
├── requirements.txt           # Python dependencies
├── environment/              
│   ├── custom_env.py         # Core environment logic
│   └── rendering.py          # Visualization & GUI components
├── training/                 # Training notebooks for different algorithms
│   ├── A2C/                  # Advantage Actor-Critic experiments
│   ├── DQN/                  # Deep Q-Network implementations
│   ├── PPO/                  # Proximal Policy Optimization
│   └── Reinforce/            # REINFORCE policy gradient
└── models/                   # Saved trained models
    ├── DQN/
    ├── PPO/
    └── REINFORCE/
```

## 🚀 Quick Start

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Run Demo with Trained Model
```bash
python main.py
```
This launches the wildfire drone simulation using your best trained model.

### 3. Train New Models
Open any training notebook in Jupyter/Colab:
- [`training/PPO/PPO_first.ipynb`](training/PPO/PPO_first.ipynb) - Best performing PPO implementation
- [`training/DQN/`](training/DQN/) - Deep Q-Network variants
- [`training/A2C/A2C_improved_v2.ipynb`](training/A2C/A2C_improved_v2.ipynb) - Actor-Critic methods

## 🎮 Environment Details

### Action Space
- **0**: Move North (↑)
- **1**: Move South (↓) 
- **2**: Move West (←)
- **3**: Move East (→)
- **4**: Extinguish fire / Complete mission

### Observation Space
- Drone position (x, y)
- Water/fuel capacity remaining
- Mission/fire locations and distances
- Completion status

### Rewards
- **+100**: Successfully extinguish fire
- **+50**: Approach fire location
- **-10**: Run out of fuel/water
- **-0.1**: Time step penalty


## 📊 Key Features

### 🔥 Wildfire Simulation
- Realistic forest environment with fire spread mechanics
- Multiple fire hotspots requiring strategic coordination
- Water capacity management and refill stations

### 🎯 Mission Environment  
- Grid-based navigation with obstacle avoidance
- Fuel-constrained exploration
- Multi-objective optimization

### 📈 Training Monitoring
- Real-time performance metrics
- Tensorboard logging
- Comprehensive evaluation plots

### 🎨 Advanced Visualization
- Pygame-based real-time rendering
- Animated drone sprites with propellers
- Fire effects and smoke animations
- Progress tracking UI



## 📋 Requirements

- Python 3.8+
- PyTorch
- Stable-Baselines3
- Gymnasium
- Pygame (for visualization)
- NumPy, Matplotlib

See [`requirements.txt`](requirements.txt) for complete list.

## 🎯 Applications

- **Emergency Response**: Autonomous wildfire suppression
- **Search & Rescue**: Multi-agent coordination
- **Resource Management**: Optimal path planning
- **Disaster Management**: Real-time decision making

## 📝 Technical Notes

- Environment follows OpenAI Gym standard
- CNN wrapper available for image-based observations
- Curriculum learning implemented for complex scenarios
- Multi-environment parallel training supported

## 🏅 Performance Metrics

Monitor training progress using:
- Episode rewards and success rates
- Convergence timesteps
- Average episode length
- Resource utilization efficiency

---

**Developed for advanced reinforcement learning research in autonomous systems and emergency response applications.**