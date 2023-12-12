# Matcha Chat

<img src="https://github.com/puff-dayo/matcha-chat/assets/84665734/5401d53a-2265-4038-a812-e9c2bd28afa4" width="64" />

## Introduction

**Matcha Chat** is a **GUI** chat app for **Windows OS** designed to chat with a **local language model AI**, built with a [Python](https://www.python.org/) backend and a [Pyside](https://pypi.org/project/PySide6/) front end.

The app interface allows for **easy** clicks installation of [llama.cpp](https://github.com/ggerganov/llama.cpp) , [Wizard Vicuna](https://huggingface.co/TheBloke/Wizard-Vicuna-7B-Uncensored-GGUF) and vision ability from [llava-v1.5-7b-q4](https://huggingface.co/jartine/llava-v1.5-7B-GGUF/), message sending, system configuration, and management of character cards.

**How to update: simply replace the .exe file.**

## Features

- **Easy-to-use chat interface**: A simple and intuitive chat interface.
- **Clicks installation**: Download essential files and start a chat with just some pushes of button. Configure settings easily.
- **Character management**: Load and save character cards(json) for personalized chat experiences. 
- **Hardware acceration support**: Choose between openBLAS and cuBLAS.
- **Highly efficient**: The GUI component of the software is consuming only ~64MB of RAM, representing a significant resource saving compared to running a web UI in Chrome, allowing even devices with 8GB of RAM to run text models quantized to 5-bit.
- **Vision ability**: Send images into your llama chat.

![1700484685905](https://github.com/puff-dayo/Matcha-Chat/assets/84665734/e998b24f-46f3-4d67-9ab7-ee70c1ba6659)

## Installation Guide

### Step 1: Get the executable

Download the built binary executable file for x64 Windows OS from [Release](https://github.com/puff-dayo/matcha-chat/releases/).

### Step 2: The first click

> [!CAUTION]
> Using GPU or setting more GPU layers ≠ Faster speed!
> Choose **CPU Acceleration** unless you have a STRONG enough GPU.

#### CPU Acceleration

Click on the upper button "*1. Download llama.cpp*" to install Llama.cpp with openBLAS support.

At least 4GB of free memory for the recommended configuration.

#### GPU Acceleration

Directly click on the button "*1. Enable GPU acceleration*" located below the buttons, instead of the upper one,to install Llama with cuBLAS support.

It is recommended to have at least 4GB of free BRAM and 4GB of VRAM available.

Before lauching the llama.cp service, make sure to set the number of layers to be loaded into the GPU (default is 10).

Note: Generally, a modern graphics card is required to achieve better performance than CPU acceleration.

### Step 3: The second click

After completing the installation with step 2, proceed with the following steps:



1. Use button "*2. Download a model*" to download the model.
2. Afterward, use "*3. Launch Llama server*" to launch.



NOTE: Once you have configured all three stpes, you only need to press "*3. Launch Llama server*" to start the llama for future chats.



## Other Useful Infomation

### Run from source

Before running Matcha Chat, ensure you have Python installed. Clone the repository to your local machine:

```bash
git clone https://github.com/puff-dayo/Matcha-Chat.git
```

Navigate to the cloned directory and install the required packages, then lauch the GUI:

```bash
pip install -r requirements.txt
python gui.py
# or py gui.py if you are using powershell
```

### Compile your own binary file....

If you like to~

```bash
nuitka --onefile --disable-console --plugin-enable=pyside6 --windows-icon-from-ico=PATH-TO-ICON gui.py
```
