<!-- SUMMONIQ-OSS-HEADER:START -->
<div align="center">

  <h1>USB Uncensored LLM</h1>
  <p>Air-gapped, zero-dependency local AI environment for macOS.</p>

  <p>
    <a href="https://github.com/SummonIQ/USB-Uncensored-LLM"><img alt="Repository" src="https://img.shields.io/badge/github-SummonIQ%2FUSB-Uncensored-LLM-24292f?logo=github"></a>
    <a href="https://unlicense.org/"><img alt="License: Unlicense" src="https://img.shields.io/badge/license-Unlicense-blue.svg"></a>
  </p>

</div>

---
<!-- SUMMONIQ-OSS-HEADER:END -->
# USB-Uncensored-LLM (macOS Edition) ⚡

**USB-Uncensored-LLM** is a fully air-gapped, zero-dependency, plug-and-play Local AI environment designed specifically for **macOS**. It bypasses complex installations, executing large language models directly on your hardware with no internet required.

🎥 **Watch the Setup & Demo Video:** [https://youtu.be/60PSXsoXc8A](https://youtu.be/60PSXsoXc8A)

[![USB-Uncensored-LLM Setup & Demo](https://img.youtube.com/vi/60PSXsoXc8A/maxresdefault.jpg)](https://youtu.be/60PSXsoXc8A)

## 🚀 Core Features
* **Zero Dependency Setup:** Ships with isolated engine binaries. No system permissions, registry edits, or package managers required.
* **Mac Optimized:** Uses a custom-compiled Ollama engine, natively capitalizing on Apple Metal GPU accelerators.
* **Censorship Free:** Integrates cutting-edge ablative and heretic fine-tuned models for completely unfiltered interactions.
* **Network Proxied UI:** The custom Python HTTP server instantly serves a blazing-fast dark mode UI. You can access the AI from your phone or tablet on the same WiFi network.

---

## 💻 System Requirements
Before preparing your drive, ensure you have:
- **Storage:** A USB 3.0+ flash drive or SSD with an absolute minimum of **8 GB** free space (16 GB is **highly** recommended).
- **RAM:** At least **8 GB of system memory** to run the 2B/4B models, and **16 GB of memory** to fluidly run the 9B/12B models.
- **OS:** macOS 11.0 or later.

---

## 📂 Folder Architecture

```text
[Portable USB Drive]
 ├── 📁 Mac        # Native macOS offline installers & launchers
 └── 📁 Shared     # Unified Data System
      ├── 📁 bin         (Holds isolated executables: ollama-darwin)
      ├── 📁 chat_data   (Houses persistent conversation history)
      ├── 📁 models      (HuggingFace GGUF Weights & local database mapping)
```

---

## ⚙️ Quick Start Guide

### Step 1: Initialize the Engine
1. Open Terminal.
2. Drag `Mac/install.command` into the terminal window.
3. Press **Enter**.

> **Note:** Initializing downloads the ~50MB execution engine and sets up the required folder structure.

### Step 2: Download AI Models 
The installer provides an interactive, terminal-based catalog to easily select and download highly curated, uncensored GGUF Models. 
1. Run the installer as described in Step 1.
2. When prompted, select one or more models from the menu.
3. The system will automatically download them into the `Shared/models` folder.

*(Alternatively, you can manually download `.gguf` weights from HuggingFace and place them into the `Shared/models` folder yourself).*

### Step 3: Launch
Open the **Mac** folder and double-click **`start.command`**.

The engine will spin up in the background, and your default web browser will automatically open the locally-served Chat UI.

---

## 📱 LAN Mobile Access
If you want to use the AI from your phone:
1. Ensure your Mac and your phone are on the exact same WiFi network.
2. The terminal window will display a **Network Access** IP Address (e.g., `http://192.168.1.15:3333`).
3. Type that URL into your mobile browser (Safari/Chrome).

---

## 🛠️ Troubleshooting

- **"Ollama Engine Not Found":** You attempted to run the `start` script before the `install` script. Run `install.command` first!
- **Slow Generation Speeds:** Your model is too large for your Mac's RAM. Re-run the installer and select the **Gemma 2 2B Abliterated** model.
- **Python Not Found:** Ensure you have Python installed. You can check by typing `python3 --version` in Terminal.

---
> *Disclaimer: USB-Uncensored-LLM is built for uncompromising computational freedom. By utilizing ablative models, the system will not moralize, lecture, or refuse your prompts. Please use responsibly.*
