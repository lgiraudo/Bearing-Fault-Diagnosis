# Bearing Envelope Analysis Lab

**Educational Project for MSc Engineering Students**

---

## Overview

This repository contains educational materials for a hands-on lab on **vibration signal analysis** and **rolling-element bearing fault diagnosis**. Students will learn fault diagnosis and envelope analysis techniques for rolling element bearings.

**Total lab time**: ~1.3 hours

---

## Learning Objectives

By completing this lab, you will be able to:

1. **Understand bearing fault mechanisms** and their vibration signatures
2. **Compute time-domain features** (RMS, peak, kurtosis) for fault diagnosis
3. **Apply envelope analysis** using the Hilbert transform to detect bearing faults

---

## Repository Structure

**Inside the content directory you will find**

```
.
├── README.md                                  # This file
├── QUICKSTART.md                               # Quick start guide for students
├── requirements.txt                            # Python dependencies
├── data/                                       # Public dataset (2-second samples)
│   ├── H_353rpm_sample.mat
│   ├── H_877rpm_sample.mat
│   ├── IR_353rpm_sample.mat
│   ├── IR_877rpm_sample.mat
│   ├── OR_353rpm_sample.mat
│   ├── OR_877rpm_sample.mat
│   ├── Roller_353rpm_sample.mat
│   └── Roller_877rpm_sample.mat
├── Notebook1_BearingEnvelopeAnalysis.ipynb     # Lab 1: Envelope analysis
└── Notebook2_BearingFaultMetrics.ipynb         # Lab 2: Classification metrics
```

---

## Bearing Diagnostics Overview

![Bearing Diagnostics](images/Bearing_diagnostics.png)

---

## Dataset Description

### Test Rig Conditions

The data come from a bearing test rig operating under:

- **Radial load**: 124.8 kN
- **Axial load**: 0 kN
- **Rotational speeds**: 353 rpm and 877 rpm

### Bearing Conditions

Four bearing health states were tested:

| Label  | Condition              | Description                    |
|--------|------------------------|--------------------------------|
| **H**  | Healthy                | No damage                      |
| **IR** | Inner Race Fault       | Localized damage on inner race |
| **OR** | Outer Race Fault       | Localized damage on outer race |
| **Roller** | Rolling Element Fault | Damage on rolling element      |

### Dataset Files

Each `.mat` file in the `data/` folder contains a **2-second snippet** of vibration data:

- `time_acc`: Time vector for acceleration (s)
- `acc_m_s2`: Acceleration from sensor 4 (m/s²)
- `acc_g`: Acceleration from sensor 4 (g)
- `fs_acc`: Sampling frequency of acceleration (Hz)
- `time_rpm`: Time vector for tacho rpm (s)
- `rpm`: Rotational speed time series (rpm)
- `fs_rpm`: Sampling frequency of rpm (Hz)
- `mean_rpm`: Mean rotational speed (rpm)
- `condition`: Bearing condition label (H, IR, OR, Roller)
- `rpm_nominal`: Nominal rotational speed (353 or 877 rpm)

**Data format**: MATLAB `.mat` files, loadable with `scipy.io.loadmat()` in Python or directly in MATLAB.

**Note**: The full dataset (longer recordings) is private and not included in this repository.

---

## Installation and Setup

### Requirements

- Python 3.8+
- Jupyter Notebook or JupyterLab
- Git (for cloning the repository)

### Quick Start

I recommend using this (link)[https://lgiraudo.github.io/Bearing-Fault-Diagnosis/] to the jupyterlite editor to work on files directly in your browser.

If you prefer to work on a personal editor you should download the files in the content directory

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

This project is provided for educational purposes. Please check with your institution regarding data sharing and usage policies.

---

## Contributing

This is an educational project designed for MSc engineering students. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

---

## Acknowledgments

This educational material was developed for hands-on laboratory sessions in vibration analysis and machine fault diagnosis.

---

## Contact

For questions or issues, please contact your course instructor or open an issue on GitHub.

---

**Happy learning!** 🎓⚙️
