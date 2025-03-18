# OpenAI Setup Guide  

✅ **Step-by-step setup guide (API installation + script usage)**  
✅ **Troubleshooting section (common errors & fixes)**  
✅ **A setup script (`setup.sh` for Bash + `setup.py` for Python) to automate installation**  

---

## 📌 Overview  
This guide explains how to install, configure, and run a Python script that interacts with the OpenAI API to fetch video suggestions based on user input. It also includes setup scripts for easy installation.

## 🛠 Prerequisites  
- macOS, Linux, or Windows  
- Python 3.8+  
- OpenAI API key  
- Git (for cloning repositories)

## 📥 Installation  

### 1️⃣ Clone the Repository  
```bash
git clone https://github.com/yourusername/OpenAI-Setup-Guide.git
cd OpenAI-Setup-Guide
```

### 2️⃣ Install Dependencies  
Using Bash:  
```bash
./setup.sh
```
Or manually using Python:  
```bash
python setup.py install
```

---

## 🔧 Setup Script Files  

### ⚡ `setup.sh` (For Bash Users)  
```bash
#!/bin/bash
# Setup script for OpenAI API video search project

# Upgrade pip and install dependencies
echo "Upgrading pip and installing required packages..."
pip install --upgrade pip
pip install --upgrade openai

echo "Setup complete!"
```

### ⚡ `setup.py` (For Python Users)  
```python
from setuptools import setup

setup(
    name="OpenAI Video Search",
    version="1.0",
    install_requires=[
        "openai"
    ],
    scripts=["video_search.py"]
)
```

---

## 🔑 OpenAI API Key Configuration  
Update your `config.py` file with your API key:  
```python
import os
os.environ["OPENAI_API_KEY"] = "your-api-key"
```
Or set it as an environment variable:  
```bash
export OPENAI_API_KEY="your-api-key"
```

---

## 🚀 Running the Script  
Execute the script using:  
```bash
python video_search.py
```

---

## ⚠️ Troubleshooting  
### 🔹 API Key Not Found  
Ensure the key is set correctly in `config.py` or as an environment variable.

### 🔹 OpenAI Import Error  
Ensure OpenAI is installed:  
```bash
pip install --upgrade openai
```

### 🔹 Permission Denied (Linux/macOS)  
Run the script with:  
```bash
chmod +x setup.sh
./setup.sh
```

### 🔹 Git Clone Issues  
If cloning fails, ensure Git is installed:  
```bash
sudo apt install git  # Debian/Ubuntu
brew install git  # macOS
```

---

## 📜 License  
MIT License
