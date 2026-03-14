
# Domain Generalization for Cardiac Activation Localization

Localizing the origin of ventricular activations from 12-lead ECG signals using domain-invariant deep learning. Year-long capstone research conducted with Professor Linwei Wang at Rochester Institute of Technology.

## Problem

Patient-specific variation in ECG morphology causes standard classifiers to fail when applied to unseen patients. A model trained on one patient's data cannot reliably localize activation origins in another — the domain shift between patients degrades performance significantly.

## Approach

Implemented two domain generalization strategies to learn patient-invariant representations:

**Domain Adversarial Neural Network (DANN)**
- Adversarial training framework that learns features predictive of activation origin while being invariant to patient identity
- Feature extractor + label predictor + domain discriminator with gradient reversal
- Achieved +30% accuracy improvement over baseline VAE

**Maximum Mean Discrepancy (MMD)**
- Kernel-based distribution matching to minimize the distance between feature distributions across patient domains
- Further improved generalization to unseen patients by +18% over DANN alone

## Key Results

| Model | Accuracy on Unseen Domains |
|-------|---------------------------|
| Vanilla VAE (baseline) | — |
| DANN | +30% over baseline |
| MMD | +18% over DANN |

## Technical Details

- **Data:** Simulated and clinical ECG signals from multiple patients, labeled across 54 ventricular regions
- **Architecture:** Adversarial neural network with gradient reversal layer for domain-invariant feature learning
- **Evaluation:** Leave-one-domain-out protocol — train on N-1 patients, test on held-out patient
- **Iteration:** Explored dozens of algorithmic approaches before arriving at the DANN → MMD progression

## What This Research Taught Me

The path was not linear. We systematically explored numerous approaches before finding what worked. The discipline of iterating through failure with methodical rigor — not finding the answer on the first try, but persisting until breakthrough — is something I carry into every technical challenge.

## Context

- **Advisor:** Professor Linwei Wang, Rochester Institute of Technology
- **Duration:** Full academic year (2023-2024)
- **Course:** DSCI 601 Capstone Research
- **Dataset:** Cannot be made public (clinical data restrictions); code is provided.

## Tech Stack

Python · PyTorch · NumPy · Pandas · Matplotlib · Jupyter
