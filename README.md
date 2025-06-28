# Multi-Feature Flow-Level Adversarial Attacks Against ML-Based Network Intrusion Detection Systems

**Authors:** Durmuş Ali Sucu, İbrahim Barış Uysal  
**Advisor:** Dr. Salih Sarp  
**Date:** March 2025

---

## 📌 Overview

This project proposes a novel adversarial attack pipeline designed to fool ML-based Network Intrusion Detection Systems (NIDS) by mutating multiple flow-level traffic features using a Genetic Algorithm (GA). The goal is to create minimally modified yet effective adversarial samples that evade detection by machine learning classifiers while remaining valid within the TCP/IP protocol constraints.

---

## 🚀 Highlights

- Optimization-based black-box adversarial attack generation.
- Modification of flow-level features such as packet sizes, IATs, TCP flags, and durations.
- Evaluation against various classifiers: 1D-CNN, Logistic Regression, Random Forest, and XGBoost.
- Realistic traffic ensured via protocol-aware constraints.

---

## 🧪 Methodology Summary

- **Feature Selection:** 17 primitive flow-level features post-handshake.
- **GA Operations:** Tournament selection, crossover, Gaussian mutation.
- **Fitness Criteria:** Lower detection probability + minimal feature distortion.
- **Constraints:** MTU size enforcement, timing consistency, TCP flag validity.

---

## 📊 Results Overview

| Model              | Evasion Rate (%) | Mean ℓ₂ | Median ℓ₂ | Mean ℓ₀ |
|--------------------|------------------|---------|------------|----------|
| 1D–CNN             | 68               | 0.404   | 0.401      | 6.13     |
| Logistic Regression| 73               | 0.514   | 0.511      | 6.49     |
| Random Forest      | 38               | 0.199   | 0.200      | 6.29     |
| XGBoost            | 49               | 0.228   | 0.231      | 6.44     |

---

## 📂 Folder Structure

- [`/dataset`](./dataset) – Dataset directory.
- [`/model`](./model) – Trained ML models.
- [`/results`](./results) – Performance metrics, graphs, mutation logs.
- [`/src`](./src) – Source code for Genetic Algorithm and evaluation logic.
- [`/README.md`](./README.md) – This file.

---

## 📥 Dataset Access

The dataset used in this project is **CICIDS2018**. Due to size constraints, it is **not included in this repository**.

➡️ You can download it from the following Google Drive link:  
🔗 [Download Dataset](https://drive.google.com/drive/u/2/folders/1A9xV6f1Z5XhCMOjQ0XSihRSWJuKi9gbW)

Once downloaded, place the relevant `.csv` files in a local folder of your choice and update the file paths in the code accordingly.

---

## ⚙️ Tools & Dependencies

- `Python`, `NumPy`, `Pandas`
- `Scikit-learn`, `XGBoost`, `TensorFlow/Keras`
- `DEAP` (Genetic Algorithms)
- `Scapy`, `tcpreplay` (optional, for real packet manipulation)

---

## 🙌 Acknowledgements

- **Dr. Salih Sarp** – Project Advisor
- **CIC** – For publicly releasing high-quality NIDS datasets
- **Open Source Projects** – DEAP, Scapy, TensorFlow, and more
