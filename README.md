# 🖼️ AI vs Human Image Classification – Vision Transformer Project

Can machine learning detect what’s *real* and what’s AI-generated? In this project, I fine-tuned **Google’s Vision Transformer (ViT)** using the Hugging Face ecosystem to classify images as either **AI-generated** or **real**.

The goal: build a model that can distinguish human-taken photos from AI-generated visuals with high accuracy—even when the differences are subtle.

---

## 📊 Overview

- **Type:** Binary Image Classification  
- **Model:** Vision Transformer (ViT – `google/vit-base-patch16-224-in21k`)  
- **Frameworks:** Hugging Face Transformers, PyTorch, TensorFlow, scikit-learn  
- **Dataset Size:** 11GB+ (custom blend of AI and real images)  
- **Tools:** 🤗 Datasets, Transformers, Matplotlib, scikit-learn  

---

## 🔧 Project Breakdown

### 📁 1. Dataset & Preprocessing
- Compiled and labeled a dataset of **real** vs **AI-generated** images
- Applied normalization, resizing, and augmentation (horizontal flip, rotation, brightness adjustment) using `torchvision.transforms`
- Split dataset: 70% train, 15% validation, 15% test

### 🧠 2. Model & Training
- Fine-tuned Google’s pre-trained **ViT model** using Hugging Face Trainer API  
- Used **AdamW optimizer**, **cross-entropy loss**, and early stopping  
- Trained for 3 epochs on GPU, monitoring training loss and validation loss

### 📈 3. Results:
- Minimal overfitting thanks to data augmentation and early stopping

---

## 📝 Want More Detail?

I wrote a blog walking through the full process:
🔗 [Read it here →](https://pranjalikdeshmukh1.wixsite.com/my-site-1/post/classifying-ai-generated-images-using-google-s-vision-transformer-vit)

---

## 🧪 Try It Yourself

```bash
git clone https://github.com/PranjaliD11/AI_Vs_Human_Classifier.git
cd AI_Vs_Human_Classifier
open classifier_notebook.ipynb
