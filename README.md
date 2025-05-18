# Lunar Lander with Deep Q-Network (DQN)

This project demonstrates the implementation of a **Deep Q-Network (DQN)** to train an autonomous agent to land a lunar module safely using reinforcement learning.

## 🚀 Project Overview

The **Lunar Lander** environment is a dynamic control problem simulated using **Gymnasium**, where the agent learns to fire the lander's thrusters optimally to achieve a smooth landing.

## 🧠 Why DQN?

- The problem involves a **discrete action space** and a **moderate state space**.
- DQN is efficient for such environments due to its use of:
  - Experience replay to stabilize learning
  - Target networks to prevent divergence
  - Neural networks for Q-value approximation

## 🧰 Tech Stack

- **Language:** Python
- **Environment:** Jupyter Notebook
- **Libraries:** PyTorch, NumPy, Gymnasium
- **Others:** `collections.deque` for replay memory

## 🧮 DQN Implementation

- **Replay Buffer:** Stores (state, action, reward, next_state, done) for training
- **Q-Network Architecture:**
  - FC(8, 64) → ReLU → FC(64, 64) → ReLU → FC(64, 4)
- **Action Selection:** Epsilon-greedy
- **Loss Function:** Mean Squared Error (MSE)
- **Optimizer:** Adam

## 🎯 Training Process

- **Q-Value Update Rule:**
  ```
  Q(s, a) = r + γ * max Q(s′, a′)
  ```
- **Soft Update:** 
  ```
  θ_target = τ * θ_local + (1 − τ) * θ_target
  ```

## 🏆 Rewards Scheme

- +100 for landing, -100 for crashing
- +10 per leg contact with the ground
- -0.03 per side engine fire, -0.3 per main engine fire
- Penalties for tilting or moving away from the landing zone
- Episode solved if score ≥ 200

## 🛠️ Hyperparameter Tuning

Top performing configuration:
- Learning Rate: 0.0005
- Batch Size: 64
- Gamma (Discount Factor): 0.99
- Replay Buffer Size: 100000
- Tau: 0.005

## 📈 Performance

- **Solved in:** 359 episodes
- **Test Results (100 episodes):**
  - Avg Reward: 231.10
  - Std Dev: 36.46
  - Max Reward: 307.81
  - Min Reward: 143.33
  - Success Rate: 83%

## 🔮 Future Work

- Implement **Rainbow DQN**
- Explore **PPO, A3C, SAC** for other action spaces
- Use **Optuna** for hyperparameter tuning
- Add harder environmental challenges (e.g., wind, gravity)
- Explore **multi-agent** scenarios

## 📌 Conclusion

This project showcases the strength of Deep Q-Networks in dynamic control environments. By combining experience replay, target networks, and neural approximators, the agent successfully learns to master the Lunar Lander environment.