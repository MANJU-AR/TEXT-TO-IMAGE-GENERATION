# AR Studio - Stable Diffusion Web UI

A beautiful, feature-rich **Stable Diffusion** web interface built with **Gradio** and **Diffusers**. Generate stunning AI images with professional controls, multiple models, and a modern cinematic UI.



## ✨ Features

- **Modern & Elegant UI** with custom CSS and dark cinematic theme
- **Multiple Models**:
  - Stable Diffusion 1.5 (Recommended)
  - Stable Diffusion 2.1
  - RealVisXL V4.0 (Realistic Vision)
- **5 High-Quality Schedulers**:
  - Euler Ancestral (Fast & Creative)
  - Euler
  - DDIM
  - DPM Solver
  - LMS
- Advanced generation controls (resolution, steps, CFG, seed, negative prompt)
- Live image gallery
- Automatic image saving with metadata
- GPU memory optimizations (`xformers`, attention slicing, VAE slicing)
- Responsive design with mobile support

## 🚀 Quick Start (Google Colab)

1. Open the notebook in Google Colab
2. Run all cells (Runtime → Run all)
3. Click the **"Initialize Model"** button
4. Start generating images!

> **Note**: Uses Tesla T4 GPU in Colab. Some older package versions are pinned for compatibility.

## 🛠️ Tech Stack

- **PyTorch** + **CUDA**
- **Hugging Face Diffusers**
- **Gradio** (Web UI)
- **Python 3.12**

## 🎛️ Usage

### Basic Generation
- Enter a detailed prompt (the more descriptive, the better)
- Optionally add a negative prompt
- Adjust resolution, steps, and guidance scale
- Choose your preferred scheduler
- Click **"Generate Image"**

### Tips for Best Results
- Use **Euler Ancestral** for creative results
- Use **DPM Solver** for higher quality
- Higher `Guidance Scale` = closer to prompt (7.5 is a good default)
- 512x512 or 768x768 recommended for speed/quality balance

## 📁 Project Structure
AR-Studio/
├── AR1.ipynb                 # Main Colab Notebook
├── outputs/                  # Generated images (auto-created)
├── requirements.txt          # (optional)
└── README.md
text## 🔧 Installation (Local)

##  🛠️ Installation (Local)
If you want to run this project locally on your computer:

# Clone the repository
git clone https://github.com/yourusername/ar-studio.git

# Go into the project folder
cd ar-studio

# Create a virtual environment (recommended)
python -m venv venv

# Activate the virtual environment
# On Linux / macOS:
source venv/bin/activate

# On Windows:
# venv\Scripts\activate

# Install PyTorch with CUDA support
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

# Install required packages
pip install diffusers==0.21.0 transformers==4.30.2 accelerate==0.20.3

# Install UI and supporting libraries
pip install gradio safetensors xformers
