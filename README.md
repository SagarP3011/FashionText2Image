# 👗 FashionAI – Domain-Specific Text-to-Image Generation using Stable Diffusion

## 🔥 Project Overview

**FashionAI** is a modular, domain-specific text-to-image generation system built using **Stable Diffusion**, **LoRA fine-tuning**, and **transformer-based prompt enhancement**.  
It generates **fashion-relevant, safe, and high-resolution** images from simple natural language prompts like `"bridal lehenga"` or `"formal blue suit"`.
---
## 🎯 Key Features

- 🧠 **Prompt Enhancement** using lightweight LLM (Zephyr)
- 🧵 **Fashion-Specific LoRA Fine-tuning** on Stable Diffusion v2.1 (UNet)
- 🖼️ **Image Enhancement** with SwinIR super-resolution transformer
- 🔒 **Content Safety** using NudeNet to block NSFW outputs
- 🌐 **Interactive UI** via Gradio, running on Kaggle's free T4 GPU

---

🖼️ **Example Prompts:**
text
- A traditional Indian bridal lehenga with intricate embroidery
- Men’s formal navy blue suit with white shirt
- Cute toddler in pink frock holding a toy
- A model wearing a translucent gown under stage lights

User Prompt -> Prompt Enhancer (LLM) -> Prompt Filter (Fashion Only) -> LoRA-tuned Stable Diffusion -> SwinIR (Super-Resolution) -> NudeNet (NSFW Filtering) ->Gradio UI Output
                                                        
Tech Stack
Language: Python 3.11
Core Models: Stable Diffusion v2.1, LoRA, SwinIR, NudeNet, Zephyr-7B
Libraries: PyTorch, HuggingFace Diffusers & Transformers, PEFT, OpenCV, Pillow
Deployment: Gradio UI, Kaggle T4 GPU

Dataset Used
FashionGen Subset (2,000+ curated fashion image-caption pairs)

Preprocessed to 512×512 / 768×768 resolution

Focused on Indian and global fashion diversity

Safety & Ethical AI
NSFW content detection is enforced using NudeNet

Non-fashion prompts are rejected with:
"I can only generate fashion-related images."
