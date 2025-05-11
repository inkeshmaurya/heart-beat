# 🧠 Foetal Heartbeat Extraction Using Adaptive Filtering (MATLAB)

## 📌 Overview

This MATLAB project focuses on extracting the **foetal ECG signal** (heartbeat) from abdominal ECG recordings that contain both maternal and foetal components. The extraction is achieved using three adaptive filtering algorithms:

- **LMS (Least Mean Squares)**
- **NLMS (Normalized LMS)**
- **LLMS (Leaky LMS)**

Both **SISO (Single Input Single Output)** and **MISO (Multiple Input Single Output)** systems are implemented and analyzed for performance and accuracy.

## 📂 Dataset

The input dataset file is:

```
foetal_ecg.dat
```

It contains 9-channel ECG signals:
- Column 1: Time samples
- Columns 2-6: Abdominal ECG signals (mixed maternal + foetal)
- Columns 7-9: Thoracic ECG signals (mostly maternal)

## ⚙️ Main Features

- **Plotting Raw ECG Signals:** Visualize the abdominal and thoracic ECGs.
- **Signal Preprocessing:** Averaging signals to isolate maternal ECG references.
- **Foetal ECG Extraction:** Using LMS, NLMS, and LLMS adaptive algorithms.
- **Comparison of Algorithms:** Plots of error signals and filtered outputs.
- **SNR Calculation:** Evaluate the signal quality improvement for SISO and MISO systems.

## 📁 Project Structure

- `foetal_ecg.dat` — Input ECG dataset
- `main.m` — Main script for signal processing and visualization
- `lms.m`, `nlms.m`, `llms.m` — Adaptive filtering algorithm functions for SISO
- `lms1.m`, `nlms1.m`, `llms1.m` — Adaptive filtering for MISO systems
- `convm.m` — Helper function to form convolution matrices

## 🧪 Adaptive Filtering Techniques

| Method | Description |
|--------|-------------|
| **LMS** | Basic adaptive filter using least mean square error |
| **NLMS** | Normalized LMS provides stable performance under variable signal powers |
| **LLMS** | Leaky LMS includes a leakage factor to prevent coefficient drift |

## 📊 Output

- **Raw Signal Plots:** Abdominal and Thoracic ECG channels
- **Filtered Output:** Estimated foetal ECG from each method
- **Error Signal Plots:** Performance analysis over time
- **SNR Comparison:** Signal-to-noise ratio for each method

## 🚀 How to Run

1. Open the MATLAB project folder.
2. Ensure `foetal_ecg.dat` and all `.m` files are in the same directory.
3. Run `main.m`.
4. View plots and SNR outputs for LMS, NLMS, and LLMS algorithms.

## 📈 Sample Output (Plotted)

- `Plot of Abdominal and Thoracic ECGs`
- `Filtered Output (Foetal Signal)`
- `Error Signal Comparison`
- `SNR of SISO and MISO Adaptive Filters`

## 📌 Notes

- This code is intended for academic/research use.
- Ensure sampling frequency is set to 500 Hz.
- MATLAB R2016b or higher recommended for full compatibility.

## 👨‍🔬 Applications

- Biomedical signal processing
- Foetal health monitoring
- Real-time ECG filtering and enhancement
