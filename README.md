# Optimizing Low-Resource Language Encoders for Text-to-Image Generation (Thai Case Study)

[![Paper DOI](https://img.shields.io/badge/Paper-10.1007/s00530--025--01834--1-blue)](https://doi.org/10.1007/s00530-025-01834-1)

Official repository for the paper:  
**“Optimizing low-resource language encoders for text-to-image generation: a case study on Thai”**  
*Thitirat Siriborvornratanakul, Songpol Bunyang* (Multimedia Systems, 2025)

---

## 🌏 Overview

Diffusion models like **Stable Diffusion** are powerful for text-to-image generation, but most are English-only.  
This project introduces a **Thai-specific text encoder** (`PYBsyn`) trained with a **teacher–student cross-lingual learning framework**.  

- Preserves **Thai cultural nuance** in image generation.  
- Uses **121k enriched synthetic captions** for efficient training.  
- Outperforms **GlueGen** and translation-based baselines.  

---

## 🔑 Method

<p align="center">
  <img src="Figure 1.jpg" width="600"/>
</p>

**Fig. 2: Two-stage framework**  
1. **Teacher Learning:** Align Thai text encoder (student) with frozen CLIP text encoder (teacher) using English–Thai parallel captions.  
2. **Inference:** Thai embeddings are injected into Stable Diffusion’s UNet, guiding image generation directly from Thai prompts.  

This ensures **compatibility with Stable Diffusion** while capturing **Thai linguistic and cultural nuances**.

---

## 🖼️ Results 

<p align="center">
  <img src="Figure 4.jpg" width="800"/>
</p>

**Fig. 4: Qualitative comparison**  
- **Rows:** Translation → GlueGen → Ours (FT + PEFT).  
- **Columns:** Different benchmarks (PartiP-70, General-50, Cultural-21).  
- Our models (`PYB` and `PYBsyn`) generate **more culturally faithful and aesthetically pleasing images** compared to translation and GlueGen.  

Highlights:  
- Translation often misses nuance.  
- GlueGen produces low-aesthetic results.  
- **Our method captures Thai-specific details** (e.g., Muay Thai, Pad Thai, landmarks).

---


## 🚀 Quick Start with Google Colab

For a hands-on demonstration without any local setup, you can run this project directly in **Google Colab**.  
The notebook provides a complete environment to load our pretrained Thai text encoder, run Stable Diffusion, and generate images from Thai prompts.  

👉 [Open in Colab](https://colab.research.google.com/github/YOUR-USERNAME/thai-t2i-encoder/blob/main/notebooks/Thai_T2I_Demo.ipynb)

The Colab notebook covers:
- Installing dependencies automatically  
- Downloading pretrained checkpoints (PYBsyn / PYB)  
- Running inference with Thai prompts  
- Visualizing and saving generated images  



### 📬 Contact
Thitirat Siriborvornratanakul (NIDA) — thitirat@as.nida.ac.th
Songpol Bunyang — songpol.buny@gmail.com

## 📖 Citation
If you use this work, please cite:

```bibtex
@article{siriborvornratanakul2025thaiT2I,
  title={Optimizing low-resource language encoders for text-to-image generation: a case study on Thai},
  author={Siriborvornratanakul, Thitirat and Bunyang, Songpol},
  journal={Multimedia Systems},
  year={2025},
  publisher={Springer},
  doi={10.1007/s00530-025-01834-1}
}



