
# Hi, I'm Mehedi Hassan

I'm a researcher working on deep learning for healthcare. My focus is **world models for physiological signals**: models that learn how a patient's state changes over time, not just what label a single snapshot gets.

🌐 **Website:** [mehedihassan.site](https://mehedihassan.site/)

---

## What I work on

**World models for clinical time series**
A classifier answers *"what is this ECG?"* A world model answers *"where is this patient heading?"* I build models that:

- **Encode** each observation into a compact latent state `z_t`
- **Learn a transition** `z_t → z_{t+1}` that captures how physiology evolves
- **Predict in latent space** rather than raw signal space, so the model spends capacity on dynamics instead of reconstructing noise and baseline wander
- **Decode** latent states into clinically meaningful outputs a clinician can inspect

```
  observation x_t ──► encoder ──► z_t ──► transition ──► ẑ_{t+1} ──► decoder ──► prediction
                                    ▲                        │
                                    └────── next step ───────┘
```

**Structure-aware signal models**
A 12-lead ECG is 12 views of one heart, not 12 interchangeable channels. I design per-lead encoders with shared weights and lead embeddings, combined by cross-lead attention, so predictions can be traced back to the leads that drove them.

**Trustworthy evaluation**
Patient-level splits, calibration alongside AUROC, robustness to device and site shift, and results that reproduce across hardware and seeds.

---

## Skills

**Languages:** Python · SQL · LaTeX · Bash / PowerShell

**Deep learning:** PyTorch · CUDA / mixed-precision training · Hugging Face Transformers · scikit-learn · NumPy · pandas

**Modelling:** World models & latent dynamics · Transformers & attention · CNNs for 1-D signals · Self-supervised / representation learning · Vision–language models (medical)

**Healthcare data:** ECG signal processing · Electronic health records · Credentialed clinical datasets (privacy-preserving, local-only workflows)

**Research practice:** Experiment tracking · Reproducible pipelines · Calibration & uncertainty · Publication-quality figures (matplotlib)

---

## Roadmap

- [x] Structure-aware ECG encoders with interpretable lead-level attention
- [x] Latent world model for patient-state trajectories
- [x] GPU training pipeline with reproducible retraining
- [ ] Uncertainty-aware rollouts: calibrated multi-step forecasts
- [ ] Multimodal world models: signals + notes + labs in one latent space
- [ ] Counterfactual queries: "what if this intervention were applied?"
- [ ] External validation across hospitals and devices
- [ ] Open-source tooling for clinical world-model research

---

## How I think about the work

> Inductive bias is a bet. In medical AI, know what you're betting on.

When data is scarce and noisy, the assumptions built into the architecture do much of the work. I try to make those assumptions explicit, testable and grounded in physiology.

---

📫 Open to research collaborations and conversations about world models, healthcare AI and representation learning. Reach me through my [website](https://mehedihassan.site/).
