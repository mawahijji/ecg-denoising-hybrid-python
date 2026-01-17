# ecg-denoising-hybrid-python
# Signal-Quality-Driven Hybrid ECG Denoising (Python Implementation)

## 📄 Publication Status
**Accepted for Publication:** *13th International Conference on Electrical and Electronics Engineering (ICEEE), 2026.*

## 📌 Project Overview
This repository contains the complete Python source code for an optimized hybrid framework designed to denoise ECG signals. The framework combines **Discrete Wavelet Transform (DWT)** and **Variational Mode Decomposition (VMD)** to remove baseline wander and high-frequency noise while preserving critical cardiac features.

## 💡 Key Innovation
Standard VMD is computationally expensive. This project implements meta-heuristic algorithms to automatically tune VMD parameters ($K$ and $\alpha$) and Wavelet thresholds, achieving optimal signal quality with minimal computational cost.

## 🏆 Performance Metrics
Tested on the **MIT-BIH Arrhythmia Database**, this optimized framework achieved:
* **Computational Efficiency:** Demonstrated that adaptive switching between DWT and VMD saves **90% of computational energy** compared to pure VMD.
* **Signal Quality:** Average output **SNR of 12.36 dB**.
* **Safety:** Validated using **SSIM (Structural Similarity Index)** to ensure QRS complex morphology is preserved for accurate diagnosis.

## 🛠️ Tech Stack
* **Language:** Python 3.10+
* **Environment:** Jupyter Notebook / Google Colab
* **Key Libraries:**
    * `vmdpy` (Variational Mode Decomposition)
    * `PyWavelets` (Discrete Wavelet Transform)
    * `scipy.signal` (Signal Processing)
    * `wfdb` (PhysioNet Data Loading)
    * `pandas` & `numpy` (Data Analysis)

## 📂 File Structure
* `main.ipynb`: The complete research notebook containing:
    1.  **Data Loading:** Automated fetching from MIT-BIH.
    2.  **Optimization:** Custom classes for Particle Swarm Optimization (PSO) and Sparrow Search Algorithm (SSA).
    3.  **Logic:** Adaptive cascade denoising (DWT $\to$ VMD).
    4.  **Benchmarking:** Comparative analysis of execution time and SNR.

