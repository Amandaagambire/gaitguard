# Gait Biometrics Reseach : Gait-Guard
<a href="#"><img alt="Python" src="https://img.shields.io/badge/Python-00543D.svg?logo=python&logoColor=white"></a>
<a href="#"><img alt="Pandas" src="https://img.shields.io/badge/Pandas-006750.svg?logo=pandas&logoColor=white"></a>
<a href="#"><img alt="NumPy" src="https://img.shields.io/badge/Numpy-008B76.svg?logo=numpy&logoColor=white"></a>
<a href="#"><img alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-55A38B.svg?logo=matplotlib&logoColor=white"></a>
<a href="#"><img alt="TensorFlow" src="https://img.shields.io/badge/TensorFlow-A4C9BB.svg?logo=TensorFlow&logoColor=white"></a>
<a href="#"><img alt="Keras" src="https://img.shields.io/badge/Keras-C5DDD6.svg?logo=Keras&logoColor=white"></a>

by **[Amanda Agambire](https://www.linkedin.com/in/amanda-agambire/)**

*August 2024*


---

## Project Description

**Can you trust gait as a biometric?**

This research explores that question by testing whether walking patterns (gait) captured from accelerometer data can serve as **unique, spoof-resistant, and privacy-preserving biometric identifiers**.

Unlike facial recognition or fingerprints, gait is harder to replicate and can be captured passively via wearable devices or smartphones. However, gait-based authentication remains underexplored in terms of **trustworthiness**, especially under adversarial conditions or in privacy-sensitive scenarios.

> **Goal**: To rigorously evaluate the **uniqueness**, **spoof resistance**, and **privacy viability** of gait biometrics using ML pipelines, time-series analysis, and adversarial robustness tests.

---

## 📌 Research Objectives

### Gait Uniqueness Across Individuals
- Demonstrate high accuracy in distinguishing users solely using time-series gait data.
- Use both classical (TSFRESH + ML) and deep learning (CNN+LSTM) pipelines.

### Spoofing Resistance
- Simulate adversarial attacks (e.g., FGSM, PGD) to mimic another user's gait.
- Assess how the model withstands these attacks without degrading performance.

### Fusion Theme: *Privacy + Inclusivity*
- Propose gait biometrics as a secure, **non-invasive**, **inclusive** form of authentication.
- Align with ethical AI goals for *transparent*, *passive*, and *user-friendly* security systems.

---

## Methodology

### Data Collection

- Aggregated datasets from multiple users wearing accelerometer-based sensors.
- Focused on a curated subset of 29 users with consistent format and sampling rate.
- Performed data segmentation using **sliding windows**.

### Time-Series Feature Extraction

- Used `TSFRESH` to extract over 2,000 statistical, temporal, and frequency features.
- Applied supervised feature selection based on user identity labels.

### Modeling Pipelines

- **TSFRESH + Decision Tree**: Baseline model using selected features.
- **CNN + LSTM**: Deep learning model on raw segmented sequences.
- Accuracy and f1-scores evaluated per user.

### Adversarial Robustness Testing

- Implemented **FGSM** (Fast Gradient Sign Method) and **PGD** attacks.
- Compared clean model accuracy vs. adversarial accuracy.
- Demonstrated **100% robustness** in proof-of-concept setup.

---

## Results (so far)

| Metric                  | Value     |
|-------------------------|-----------|
| Clean Accuracy (DT)     | 83–100%   |
| Deep Learning Accuracy  | 100%      |
| FGSM Adversarial Accuracy | 100%    |
| Selected TSFRESH Features | 127     |
| Users Tested (PoC)      | 6         |

---

## Tech Stack

- Python, Pandas, NumPy
- Matplotlib, Seaborn
- TSFRESH (for feature engineering)
- TensorFlow & Keras (for deep learning)
- Sklearn (for classical modeling)
- FGSM & PGD (adversarial robustness)

---

## Key Insights

- Gait is **distinct enough** to authenticate individuals in short time windows.
- Even simple decision trees on TSFRESH features can classify users with high precision.
- Spoofing via adversarial attacks can be **mitigated** with robust architectures.
- Gait-based authentication promotes **privacy**, **passivity**, and **accessibility** over visual biometrics.

---

## Societal Impact

> In a world grappling with surveillance overreach, identity theft, and exclusionary biometric systems, **gait** offers a future-forward path for **privacy-first, inclusive security**.

This research supports the ethical deployment of gait biometrics in:
- Smart homes and IoT environments
- Public access control and surveillance
- Wearables and healthcare authentication systems

---

## Next Steps

- Expand to full dataset (29+ users)
- Integrate **differential privacy** in training
- Simulate real-world spoof scenarios
- Compare against other biometrics (e.g., keystroke, voice)
- Publish results in an academic conference

---

## Contact

Reach out or collaborate:  
📧 amanda.agambire@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/amanda-agambire/)  
🔗 [GitHub](https://github.com/Amandaagambire)



