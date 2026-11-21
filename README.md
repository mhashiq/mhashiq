<div align="center">

# Md. Mehedi Hassan

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&duration=2800&pause=900&color=D94C4C&center=true&vCenter=true&width=640&lines=I+build+world+models+for+the+human+heart.;Snapshot+%E2%86%92+latent+state+%E2%86%92+future.;Predict+the+dynamics%2C+not+the+noise.;Inductive+bias+is+a+bet." alt="typing intro" />

<img src="https://raw.githubusercontent.com/mhashiq/mhashiq/main/ecg.svg" width="100%" alt="heartbeat" />

[![Website](https://img.shields.io/badge/mehedihassan.site-111111?style=for-the-badge&logo=googlechrome&logoColor=white)](https://mehedihassan.site/)

</div>

---

### 🫀 What I do

Most medical AI looks at one snapshot and names it.
I build **world models**: they learn a hidden state of the body and **how it moves through time**, so they can predict what comes next.

```
 ECG(t) ──► encoder ──► z_t ──► dynamics ──► z_t+1 ──► z_t+2 ──► … ──► what happens next
```

### 🧮 The idea in four equations

**1. Encode** an observation $x_t$ (for example, a 12-lead ECG) into a latent state:

$$z_t = f_\theta(x_t)$$

**2. Step forward** in latent space, optionally conditioned on an intervention $a_t$:

$$\hat{z}_{t+1} = g_\phi(z_t,\ a_t)$$

**3. Roll out** $k$ steps into the future and read out a clinical prediction:

$$\hat{z}_{t+k} = g_\phi^{(k)}(z_t), \qquad \hat{y}_{t+k} = h_\psi(\hat{z}_{t+k})$$

**4. Train** by matching predicted states to encoded future states, not raw signals:

$$\mathcal{L} = \sum_{k=1}^{K} \big\lVert \hat{z}_{t+k} - \mathrm{sg}\big[f_\theta(x_{t+k})\big] \big\rVert_2^2 \ + \ \lambda\, \mathcal{L}_{\text{task}}$$

<sub>$\mathrm{sg}[\cdot]$ = stop-gradient. Predicting in latent space spends capacity on dynamics instead of noise and baseline wander.</sub>

### 🧭 Beliefs I build on

| | |
|---|---|
| **Inductive bias is a bet** | In medicine, know what you're betting on. |
| **12 leads = 12 views** | One heart, seen from twelve angles. |
| **Latent over raw** | Learn the dynamics, skip the noise. |
| **0.8 means 80%** | Calibration matters as much as accuracy. |

### 🛠️ Toolkit

<img src="https://skillicons.dev/icons?i=python,pytorch,sklearn,latex,git,vscode" alt="skills" />

`CUDA` · `Hugging Face` · `Transformers` · `pandas` · `SQL` · world models · latent dynamics · attention · signal processing

### 🚀 Roadmap

- [ ] Calibrated multi-step forecasts of patient state
- [ ] One latent space for signals, notes and labs
- [ ] "What if?" counterfactuals: compare $g_\phi(z_t, a)$ vs $g_\phi(z_t, a')$
- [ ] Validation across hospitals and devices

<div align="center">
<sub>Always open to talk about world models and healthcare AI · <a href="https://mehedihassan.site/">mehedihassan.site</a></sub>
</div>
