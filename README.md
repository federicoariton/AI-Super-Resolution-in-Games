# AI Super-Resolution in Games: A Comparative Study of Real-ESRGAN and SRCNN 
Using Big Data

## 🎮 Project Overview

This project investigates the application of AI-based super-resolution models to enhance low-resolution visuals in retro video games. It evaluates and compares different models—**SRCNN**, **ESRGAN**, and **Real-ESRGAN**—for their effectiveness in improving image quality from emulated retro games like  *SuperTux*.

The research is conducted as part of a Master’s level assessment under the Springboard+ MSc in Data Analytics program.

- [Click here to read my Research Paper](https://github.com/federicoariton/AI-Super-Resolution-in-Games/blob/main/Federico_Ariton_sba22090_Lvl9_CA1_Research_paper.pdf)

---

## 🧪 Objectives

- Evaluate AI super-resolution models on retro game screenshots.
- Compare SRCNN (trained on DIV2K) vs. Real-ESRGAN (pretrained) on PSNR and SSIM metrics.
- Demonstrate a big data pipeline for image preprocessing using **Hadoop HDFS** and **Apache Spark**.
- Explore feasibility of real-time enhancement in emulated gameplay scenarios.

---

## 🧠 Models Used

| Model        | Type         | Trained On | Notes |
|--------------|--------------|------------|-------|
| SRCNN        | CNN (Shallow) | DIV2K Dataset | Trained from scratch |
| Real-ESRGAN  | GAN (Generalized) | Pretrained | Handles real-world degradation, great for blurry inputs |

---

## 🛠️ Technologies

- **Python (Jupyter Notebook)**
- **Pytorch** – For SRCNN training
- **Hadoop HDFS** – Image storage
- **Apache Spark** – Distributed image preprocessing
- **OpenCV / skimage** – Image manipulation and metric evaluation
- *CPU** – Model training & inference

---

## 🗃️ Dataset

- **DIV2K Dataset**: 800 high-resolution images and downsampled versions (used to train SRCNN).
- **Game Screenshots**: 
  - *SuperTux* (Open-source)

Images were preprocessed into LR-HR pairs, stored in HDFS, and processed via Spark for model input.

---

## 📊 Evaluation Metrics

- **PSNR (Peak Signal-to-Noise Ratio)**
- **SSIM (Structural Similarity Index)**

Both metrics were computed for SRCNN and Real-ESRGAN output to assess model performance.

---

## 📈 Key Findings

- **Real-ESRGAN** consistently outperformed **SRCNN** in both PSNR and SSIM.
- SRCNN provided smoother, less detailed upscaling.
- Real-ESRGAN is more suitable for low-quality or blurry frames typical of older games.
- Integrating Spark and HDFS allowed efficient image handling at scale.


