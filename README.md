# Localizing the origin of ventricular activation from 12-Lead ECG using Domain Generalization 🫀
The aim was to develop a domain generalized model to localize the origin of ventricular activations, using domain invariant patient data using DANN (Domain Adversarial Neural Network). 

This project localizes the origin of ventricular activations from ECG signals using DANN to address domain shift across patients.
Built on simulated multi-patient data, it leverages adversarial learning to achieve a +30% accuracy boost in heartbeat source classification.
The pipeline combines robust time-series modeling with domain adaptation, supporting future clinical generalization. 
A step toward patient-agnostic, AI-driven cardiac diagnostics.

## Dataset:
Dataset cannot be made public, so only code is provided. The dataset includes both simulated and clinical ECG signals from multiple patients, with each heartbeat labeled by its origin across 54 ventricular regions—enabling evaluation across synthetic and real-world domains.

DANN perfoms better than our Vanilla classifier. I've further implemented Maximum Mean Discrepancy to improve genralization. 
