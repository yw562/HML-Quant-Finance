
# Hamiltonian Memory Layer for Quant Finance (HML-Quant)

🚀 Proof-of-Concept implementation of the **Hamiltonian Memory Layer (HML)**,  
applied to **financial time-series forecasting** (FX and Futures).  

This repo demonstrates how physics-inspired architectures can improve  
**stability** and **interpretability** in noisy, chaotic financial markets.

---

## 🔑 Key Idea
Financial markets behave like **high-dimensional chaotic dynamical systems**:  
- Prices follow noisy, regime-switching trajectories  
- Momentum and shocks resemble "forces" acting on latent states  
- Long-horizon stability and interpretability are crucial but missing in black-box models  

👉 The **Hamiltonian Memory Layer (HML)** models hidden states as a phase space \((q, p)\),  
with energy conservation + dissipation bias. This inductive bias provides:  
- Stable training over long horizons  
- Physically interpretable latent dynamics (phase-space trajectories, energy drift)  
- Competitive predictive performance with standard baselines  

---

## 📊 Current Experiments
### Datasets
- **EUR/USD FX** (HistData 1-min bars)  
- **E-mini S&P 500 Futures** (CME continuous contract)  

### Tasks
- Return direction classification (up/down)  
- Volatility regime prediction  
- Long-horizon sequence stability (1000+ timesteps)

### Models Compared
- **AR(p)** (classical baseline)  
- **LSTM**  
- **Transformer (small)**  
- **HML (ours)**  

### Metrics
- **Prediction**: Sharpe ratio, AUC/F1  
- **Stability**: Gradient variance, long-horizon loss  
- **Interpretability**: Phase-space trajectories, energy diagnostics  

---

## 📈 Example Result (Prototype)
*(placeholder figure)*  

- **LSTM**: unstable gradients after ~500 steps  
- **Transformer-small**: good short horizon, high compute cost  
- **HML**: stable dynamics, interpretable energy trajectory  

<p align="center">
  <img src="docs/phase_space.png" width="400" alt="Phase space trajectory example"/>
</p>

---

## 📂 Repo Structure
