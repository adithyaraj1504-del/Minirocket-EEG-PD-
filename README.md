# EEG MiniRocket Evaluation & Benchmarking Project

This repository contains a collection of Jupyter notebooks investigating the performance of **MiniRocket** (and its proposed variants) on EEG data, alongside several state-of-the-art deep learning models used for benchmarking.

---

## 📂 Project Structure & Notebook Overview

The codebase is divided into **Proposed MiniRocket Variants**, **Robustness & Ablation Studies**, and **Benchmarking Models**.

### 1. Proposed MiniRocket Variants (Channel-Specific & All-Channel Evaluations)
These notebooks evaluate the proposed MiniRocket architecture using specific subsets of EEG brain regions and the complete channel set to analyze performance.

| Notebook | Description | Channels Used |
| :--- | :--- | :--- |
| `advanced-minirocket-correct-version.ipynb` | **Proposed MiniRocket Model (All Channels)** | **All Channels (Complete EEG Set)** |
| `advanced-minirocket-frontal-channels.ipynb` | Frontal channel evaluation | `Fp1`, `Fp2`, `AFz`, `AF3`, `AF4`, `Fz`, `F1`, `F2`, `F3`, `F4`, `F5`, `F6`, `F7`, `F8`, `F9`, `F10` |
| `advanced-minirocket-occiptial-channels.ipynb` | Occipital channel evaluation | `O1`, `O2`, `Oz`, `POz`, `PO3`, `PO4` |
| `advanced-rocket-pariental-channel.ipynb` | Parietal channel evaluation | `Pz`, `P1`, `P2`, `P3`, `P4`, `P5`, `P6`, `P7`, `P8`, `P9`, `P10`, `POz`, `PO3`, `PO4` |
| `advanced-rocket-temporal-channel.ipynb` | Temporal channel evaluation | `T7`, `T8`, `T9`, `T10`, `FT7`, `FT8`, `TP7`, `TP8`, `TP9`, `TP10` |
| `central-channels.ipynb` | Central channel evaluation | `C1`, `C2`, `C3`, `C4`, `C5`, `C6`, `FCz`, `FC1`, `FC2`, `FC3`, `FC4`, `FC5`, `FC6`, `CP1`, `CP2`, `CP5`, `CP6` |

---

### 2. Robustness & Ablation Studies
These notebooks test the sensitivity, resilience, and generalizability of the proposed MiniRocket framework under varying signal conditions, sampling rates, and perturbations.

| Notebook | Description | Perturbation / Setting |
| :--- | :--- | :--- |
| `advanced-minirocket-noise-analysis.ipynb` | Noise robustness analysis | Added Gaussian noise (`noise_db = 10`) |
| `amplitude_scaling_for_mini_rocket_work_.ipynb` | Amplitude scaling evaluation | All channels evaluated with amplitude scaled by factor of 2 |
| `different-sampling-rate.ipynb` | Sampling rate frequency test | Evaluated at 200 Hz (standard: 256 Hz) |
| `record_trunkation_for_mini_rocket_work_.ipynb` | Signal truncation test | Evaluated by truncating signals to 50% length |
| `time-shifting.ipynb` | Temporal shift robustness | Evaluated by shifting signals by 2 seconds |

---

### 3. Benchmarking Models & Baselines
These notebooks implement various baseline architectures to compare against the proposed MiniRocket variants.

| Notebook | Model / Framework | Description |
| :--- | :--- | :--- |
| `minirocket_original_model_for_minirocket_work.ipynb` | **Original MiniRocket** | Standard MiniRocket baseline for comparison |
| `motion_codes_pd.ipynb` | **MiniRocket (Motion/PD)** | Motion/Parkinson's Disease specific MiniRocket application |
| `atc_model_for_minirocket_work.ipynb` | **ATC Model** | Attention-based Temporal Convolution benchmarking |
| `conformer-resting.ipynb` | **Conformer (Resting)** | Conformer model evaluated using resting-state EEG data |
| `conformer-walking.ipynb` | **Conformer (Walking)** | Conformer model evaluated using walking-state EEG data |
| `eeg_model_for_minirocket_work.ipynb` | **EEGNet** | Compact convolutional neural network for EEG-based BCI |
| `fedformer-pd.ipynb` | **FEDformer** | Frequency Enhanced Decomposed Transformer for time-series forecasting/classification |
| `inception-time-eeg-pg.ipynb` | **InceptionTime** | Ensemble of Inception networks for time-series classification |
| `mamba-for-pd.ipynb` | **Mamba** | State Space Model (SSM) architecture benchmarking |
