# RL-Epidemic-Control-Networks

> A reinforcement learning framework for learning interpretable social policies to mitigate epidemic spread over dynamic contact networks using SEIR models and Proximal Policy Optimization.

---

## 📚 Project Overview

This project explores whether an intelligent agent can learn to mitigate epidemic spread by applying high-level, interpretable social policies—such as quarantine or moderate distancing—on a dynamic population graph, without micromanaging individual behavior. The model integrates:

- **SEIR-based epidemic modeling**
  **Graph-Based Simulation**  
- **Network rewiring dynamics**
- **Reinforcement learning via PPO**

The goal is to discover strategies that effectively balance public health outcomes with the preservation of social connectivity.

---

## 🧠 Research Question

> Can an agent learn to control an epidemic by selecting interpretable, population-level policies that reduce infections while preserving social interaction?

---

## 🛠️ Repository Structure

| File | Description |
|------|-------------|
| `Mathematical_models.ipynb` | Implements deterministic SEIR and SEIR-TTI models using ODEs. Includes parameter analysis and model variants. |
| `graph_rewiring.ipynb` | Simulates epidemic spread on dynamic contact networks using EoN. Studies the impact of different rewiring strategies across graph topologies. |
| `rewiring_with_ppo.ipynb` | Defines a Gymnasium-compatible RL environment and trains a PPO agent to control epidemic progression using population-level social strategies. |

---

## 🧪 Methodology

1. **Epidemic Modeling**  
   The SEIR model is used to simulate infection dynamics. An extended SEIR-TTI (Test, Trace, Isolate) model is also implemented for realism.

2. **Graph-Based Simulation**  
   Network-based spread is simulated using the `EoN` (Epidemics on Networks) library with stochastic Gillespie dynamics. Graph topologies include:
   - Random Regular Graphs
   - Erdős–Rényi
   - Watts–Strogatz (default)

3. **Policy-Based Rewiring**  
   Four discrete social strategies simulate public policy:
   - `normal`
   - `moderate_distancing`
   - `strict_distancing`
   - `quarantine`

4. **Reinforcement Learning**  
   A Proximal Policy Optimization (PPO) agent from `Stable-Baselines3` is trained to select policies based on compact observations of the epidemic and network state. The environment is built using `Gymnasium`.

---

## 📦 Requirements

Being Jupyter notebooks, all the requirements are present in the first cells. If you encounter any error, check that the output cell for TensorBoard is not specific to Kaggle/Colab, since training has been done on them mainly.

