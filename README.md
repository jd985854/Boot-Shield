# ViT‑Malware — Vision Transformer for Malware Detection

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-161b22?style=for-the-badge&logo=githubpages&logoColor=white)](https://jd98554.github.io/ip-rotator/)

Convert binary executables to grayscale images and classify them using a **Vision Transformer (ViT)**. Achieves **98.5%** accuracy on MalImg and **94.8%** on Microsoft BIG datasets.

---

## 📊 Results

| Dataset | Accuracy | Precision (macro) | Recall (macro) | F1 (macro) |
|---------|----------|-------------------|----------------|------------|
| MalImg  | 98.50%   | 96%               | 97%            | 96%        |
| MS BIG  | 94.85%   | 90%               | 88%            | 89%        |

---

## 🚀 Quick Start

```bash
# Clone
git clone https://github.com/jd98554/vit-malware
cd vit-malware

# Install
pip install -r requirements.txt

# Prepare dataset (place MalImg images in data/malimg/)
# Train
python src/train.py --dataset malimg --epochs 30 --batch-size 64

# Predict
python src/predict.py --file sample.exe --weights weights/best.pth
