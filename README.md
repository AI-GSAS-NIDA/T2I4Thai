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

## 🔑 Key Contributions

- Lightweight **Thai encoder** for Stable Diffusion.  
- Demonstrated that **synthetic bilingual data** can replace huge multilingual datasets.  
- Achieved **100% win rate** on Thai Cultural benchmark (CLIPScore, ImageReward, PickScore).  

---

## ⚙️ Installation

