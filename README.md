# AI-OFI: AI-Assisted Oil Film Interferometry for Wall Shear Stress Estimation

![Python](https://img.shields.io/badge/python-3.10-blue)
![License](https://img.shields.io/badge/license-MIT-green)

AI-assisted Oil Film Interferometry (AI-OFI) for automated wall shear stress (WSS) estimation using deep learning.

This repository implements the method presented in:

**"Automated Local Measurement of Wall Shear Stress with AI-Assisted Oil Film Interferometry"**

---

## 🔬 Overview

Accurate measurement of wall shear stress (WSS) is essential in fluid dynamics, but traditional Oil Film Interferometry (OFI) requires manual processing and expert intervention.

This project introduces **AI-OFI**, a fully automated pipeline that combines:

* YOLO for droplet detection
* FFT-based interrogation window selection
* VGG16 for fringe spacing (Δx) regression
* Temporal analysis to compute wall shear stress (τw)

The method transforms OFI into a real-time, operator-independent measurement system.

---

## ⚙️ Pipeline

```text
Input Image Sequence
        ↓
YOLO Detection (droplets)
        ↓
Smart Interrogation Window (FFT)
        ↓
VGG16 Regression → Δx
        ↓
Temporal Evolution of Δx
        ↓
Wall Shear Stress (τw)
```

Each component is modular and can be used independently.

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/MMYoushanlouei/AI-OFI.git
cd AI-OFI
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 📁 Data

Example test case and calibration image are provided:

- `data/test_case_200_R2/` → sample image sequence  
- `data/calibration/` → calibration image  

Pretrained weights are available in:

- `models/weights/`

----

📥 Data & Pretrained Models

Due to GitHub file size limitations, large files are hosted externally.

🔹 Model, Pretrained weights, test data, and calibration image 

Download:  https://kth-my.sharepoint.com/:u:/g/personal/momy_ug_kth_se/IQAEUCpM9uwBSa3lMVU87lRsAZRU8JWqNp_5SBw5b66fZbM?e=nzQa8u
Password:  MMYoushanlouei

-------

Outputs include:

* Detected droplets
* Selected interrogation window
* Predicted fringe spacing (Δx)
* Estimated wall shear stress (τw)

---

## 📊 Results

The AI-OFI method achieves:

* High accuracy compared to conventional OFI
* Reduced operator dependency
* Robust performance under varying lighting and droplet conditions

Validation against reference measurements shows deviations below 5%.

---

## 📁 Project Structure

```
AI-OFI/
│
├── data/                # Sample data
├── models/              # Pretrained models
├── src/
│   ├── detection/       # YOLO detection
│   ├── iw_selection/    # FFT-based window selection
│   ├── regression/      # VGG16 model
│   └── pipeline/        # Full pipeline
│
├── notebooks/           # Demo notebooks
├── results/             # Output examples
└── tests/               # Test scripts
```

---

## 📌 Citation

If you use this repository, please cite:

```bibtex
@article{AI_OFI_2026,
  title={Automated Local Measurement of Wall Shear Stress with AI-Assisted Oil Film Interferometry},
  journal={Sensors},
  year={2026}
}
```

---

## 📬 Contact

Mohammad Mehdizadeh Youshanlouei
University of Bologna
