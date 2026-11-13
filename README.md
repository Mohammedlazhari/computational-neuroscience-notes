# Computational Neuroscience Notes — PhD Preparation

**Research preparation for Computational Neuroscience PhD applications**  
**Target:** Sainsbury Wellcome Centre, Gatsby Computational Neuroscience Unit, Systems Neuroscience programs

**Author:** Mohammed Lazhari Krobba  
**Background:** M.Sc. Data Science & AI, ML Researcher (AAIET 2025 publication)

---

## 🎯 Purpose

This repository documents my **self-directed preparation** for Computational Neuroscience PhD applications. It bridges my **machine learning research background** (sequence modeling, predictive learning, temporal dynamics) with **computational neuroscience theory** (predictive coding, normative modeling, neural dynamics).

> **Core thesis:** The computational principles I discovered in deep learning (TCN's dilated temporal integration, predictive coding dual-model, generalization vs memorization) are not just engineering tricks — they are **normative hypotheses** for how biological neural circuits implement temporal processing, prediction, and adaptive behavior.

---

## 📚 Repository Structure

```
computational-neuroscience-notes/
├── README.md                           # This file
├── predictive_coding/
│   ├── theory.md                       # Mathematical foundations
│   ├── implementations/
│   │   ├── predictive_coding_pytorch.py
│   │   ├── hierarchical_pcn.py
│   │   └── active_inference_agent.py
│   └── papers/
│       ├── rao_predictive_coding_1999.pdf
│       ├── friston_free_energy_2010.pdf
│       └── keller_predictive_coding_2018.pdf
├── temporal_credit_assignment/
│   ├── theory.md                       # TCN ↔ cortical hierarchy
│   ├── implementations/
│   │   ├── tcn_dilated_convolutions.py
│   │   ├── neural_cdes.py
│   │   └── lstm_gating_analysis.py
│   └── papers/
│       ├── bai_tcn_2018.pdf
│       ├── saxon_ccp_2023.pdf
│       └── goldstein_cortical_timescales_2017.pdf
├── neural_manifolds/
│   ├── theory.md                       # Population dynamics, GPFA
│   ├── implementations/
│   │   ├── gpfa_implementation.py
│   │   ├── jpca_analysis.py
│   │   └── latent_dynamics.py
│   └── papers/
│       ├── gallego_neural_manifolds_2020.pdf
│       ├── cunningham_dimensionality_2014.pdf
│       └── pandarinath_latent_dynamics_2018.pdf
├── active_inference/
│   ├── theory.md                       # Free energy, expected free energy
│   ├── implementations/
│   │   ├── active_inference_gridworld.py
│   │   ├── epistemic_value_calculation.py
│   │   └── planning_as_inference.py
│   └── papers/
│       ├── friston_active_inference_2017.pdf
│       ├── parr_active_inference_2022.pdf
│       └── millidge_active_inference_2021.pdf
├── sequence_modeling/
│   ├── tcn_dilated_convolutions.md     # My thesis connection
│   ├── lstm_gru_gating.md              # Gating ↔ synaptic mechanisms
│   ├── transformer_attention.md        # Attention ↔ predictive coding
│   ├── neural_cdes.md                  # Irregular time series
│   └── papers/
│       ├── bai_tcn_2018.pdf
│       ├── vaswani_transformer_2017.pdf
│       ├── kidger_neural_cdes_2020.pdf
│       └── schmidhuber_lstm_1997.pdf
├── experimental_design/
│   ├── theory.md                       # Testable predictions, task design
│   ├── implementations/
│   │   ├── sequence_prediction_task.py
│   │   ├── prediction_error_task.py
│   │   └── reversal_learning_task.py
│   └── papers/
│       ├── sariyanidi_predictive_coding_behavior_2020.pdf
│       └── heilbron_prediction_error_2022.pdf
└── papers_to_read.md                   # Curated reading list with status
```

---

## 🧠 Core Research Connections

### 1. TCN Dilated Convolutions ↔ Cortical Hierarchy

| TCN Component | Cortical Analogue | Evidence |
|---------------|-------------------|----------|
| **Dilated conv (d=1)** | L2/3 fast integration | 10-50ms windows |
| **Dilated conv (d=2,4,8...)** | L5/6 slow integration | 100-500ms windows |
| **Causal constraint** | Feedforward > feedback | Lamina-specific connectivity |
| **Residual connections** | Recurrent loops | Cortical microcircuits |
| **Weight sharing across time** | Stationary statistics | Translation invariance in time |

**My finding:** TCN generalizes because dilated causal convolutions **learn temporal integration kernels** that match cortical timescale hierarchy. LSTM/GRU/Transformer overfit because they lack this inductive bias.

### 2. Dual-Model Architecture ↔ Predictive Coding

| My Architecture | Predictive Coding | Biological Basis |
|-----------------|-------------------|------------------|
| **Forecaster (TCN)** | Generative model (top-down) | L5/6 pyramidal → L2/3 |
| **Validator (MLP)** | Prediction error units (bottom-up) | L2/3 → L5/6 |
| **Anomaly = high error** | Surprise = precision-weighted PE | Neuromodulatory gating |
| **Retraining loop** | Free energy minimization | Synaptic plasticity |

### 3. Generalization Gap ↔ Overfitting vs Dynamics Learning

| Model | Test Performance | Forecast Performance | Mechanism |
|-------|-----------------|---------------------|-----------|
| LSTM/GRU | Good | Poor | Memorizes sequences |
| Transformer | Good | Poor | Memorizes attention patterns |
| CNN-1D | Good | Poor | Local features only |
| **TCN** | Medium | **Good** | **Learns dynamics** |

This pattern suggests biological systems face the same computational tradeoff and have evolved **dilated temporal integration** as the solution.

---

## 📖 Papers to Read — Status Tracker

### Foundational (Read ✓ / In Progress 📖 / Planned 📅)

| Paper | Topic | Status | Notes |
|-------|-------|--------|-------|
| Rao & Ballard 1999 | Predictive coding in visual cortex | 📅 | Foundation |
| Friston 2010 | Free energy principle | 📅 | Theory |
| Bastos et al. 2012 | Canonical microcircuits | 📅 | Circuit |
| Keller & Mrsic-Flogel 2018 | Predictive coding in cortex | 📅 | Experimental |
| Heilbron & Chait 2022 | Prediction error signals | 📅 | Review |
| **Saxe et al. 2019** | **Mathematical principles of learning** | 📅 | **Saxe Lab** |
| **Saxe et al. 2021** | **Hierarchical structure** | 📅 | **Saxe Lab** |
| Bai et al. 2018 | TCN paper | ✓ | My thesis |
| Kidger et al. 2020 | Neural CDEs | 📅 | Irregular time |
| Gallego et al. 2020 | Neural manifolds | 📅 | Analysis |
| Pandarinath et al. 2018 | Latent dynamics | 📅 | GPFA |
| Friston et al. 2017 | Active inference | 📅 | Decision-making |
| Parr et al. 2022 | Active inference review | 📅 | Theory |
| Millidge et al. 2021 | Active inference in DL | 📅 | Bridge |

---

## 🔬 Implementation Status

| Module | Theory | Code | Tests | Docs |
|--------|--------|------|-------|------|
| Predictive Coding | ✓ | 📅 | 📅 | 📅 |
| TCN ↔ Cortex | ✓ | ✓ | 📅 | ✓ |
| Neural Manifolds | 📅 | 📅 | 📅 | 📅 |
| Active Inference | 📅 | 📅 | 📅 | 📅 |
| Neural CDEs | 📅 | 📅 | 📅 | 📅 |
| Experimental Design | 📅 | 📅 | 📅 | 📅 |

---

## 🚀 Quick Start

```bash
git clone https://github.com/your-username/computational-neuroscience-notes.git
cd computational-neuroscience-notes

# Create environment
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Run TCN ↔ Cortex analysis
python sequence_modeling/implementations/tcn_dilated_convolutions.py

# Run predictive coding demo
python predictive_coding/implementations/predictive_coding_pytorch.py
```

### Requirements
```txt
torch==2.1.0
numpy==1.24.3
matplotlib==3.7.2
scipy==1.11.0
sklearn==1.3.0
jupyter==1.0.0
```

---

## 🎯 PhD Application Alignment

### Sainsbury Wellcome Centre (SWC) / Gatsby Unit

| SWC/Gatsby Focus | My Preparation |
|------------------|----------------|
| **Predictive coding** | Dual-model architecture, hierarchical implementation |
| **Normative modeling** | Free energy, active inference, Bayesian brain |
| **Theory-experiment loop** | Testable predictions, task designs, neural manifolds |
| **Saxe Lab: Learning theory** | TCN inductive bias, generalization, overparameterization |
| **Gatsby: Normative modeling** | Free energy, Bayesian inference, neural coding |

### Key Talking Points for Interviews

1. **"My TCN finding isn't just an ML result — it's a hypothesis about cortical temporal integration.""**
2. **"Predictive coding isn't a metaphor — I implemented the dual-model loop and it works for sensor validation.""**
3. **"The generalization gap in DL mirrors the overfitting problem brains solve — TCN's inductive bias is the answer.""**
4. **"I want to move from engineering analogues to normative models tested against neural data.""**

---

## 📄 License

MIT License — see LICENSE file.