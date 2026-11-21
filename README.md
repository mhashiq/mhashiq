
# Md Mehedi Hassan

**I teach models to imagine where a patient is heading.**

Most medical AI looks at one snapshot and names it. I build **world models**: they learn a hidden state of the body and how that state changes over time, so they can predict what comes next.

```
ECG today ─► latent state z_t ─► dynamics ─► z_t+1 ─► what happens next
```

🌐 [mehedihassan.site](https://mehedihassan.site/)

---

### Beliefs I build on

- **Inductive bias is a bet.** In medicine, know what you're betting on.
- **12 leads are 12 views of one heart**, not 12 random channels.
- **Predict the dynamics, not the noise.** Learn in latent space.
- **A 0.8 should mean 80%.** Calibration matters as much as accuracy.

### Toolkit

`Python` `PyTorch` `CUDA` `Transformers` `Hugging Face` `scikit-learn` `pandas` `SQL` `LaTeX`
World models · Latent dynamics · Attention · Signal processing · Clinical data

### Next on the roadmap

- [ ] Calibrated multi-step forecasts of patient state
- [ ] One latent space for signals, notes and labs
- [ ] "What if?" counterfactuals for treatment decisions
- [ ] Validation across hospitals and devices
