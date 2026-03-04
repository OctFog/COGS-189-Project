# COGS-189-Project: EEG Motor Imagery Classification

## Table of Contents

- [Overview](#overview)  
- [Team Information](#team-infomation)  
- [Presentation](#presentation)  
- [Programming Language & Tools](#programming-language--tools)  
- [Dataset](#dataset)  
- [Important Dates](#important-dates)  
- [Repository Structure (Planned)](#repository-structure-planned)  
- [Setup & How to Run our code](#setup--how-to-run-our-code)  

## Overview
This repository contains the final project for *UCSD COGS 189*. The goal of this project is to classify EEG data from a competition dataset to identify motor imagery patterns, including ...

The project covers the full pipeline of EEG data processing, including:
- TBD

Project Proposal: [V1](https://docs.google.com/document/d/1Ued5GemxQ-lzL4ZV4aivkzzAiIMmFG4fhII_fe1RG48/)

## Team Infomation

### Team Name

### Advisor
Prof. Virginia De Sa


### Members (5 People)
| Role | Member | Email |
| - | - | - |
| - | [Claire Gao](https://github.com/Claire6ao) | jig029@ucsd.edu |
| - | [Chengszu Peng](https://github.com/ChengszuPeng) | c7peng@ucsd.edu |
| - | [Kangxin Peng](https://github.com/KpengDS) | k2peng@ucsd.edu |
| - | [Liuxuhong Zhao]() | liz066@ucsd.edu | 
| - | [Xiaogeng Xu](https://github.com/OctFog) | xix063@ucsd.edu |

## Presentation

**Form**: Recorded Video Presentation

The presentation will include:
- TBD

## Programming Language & Tools

**Language:** Python

**Libraries likely used:**
- numpy
- matplotlib.pyplot
- os
- zipfile
- requests
- mne

## Dataset
The dataset we use is ***The BCI Competition IV – Dataset 2a***.
*The BCI Competition IV Dataset 2a* is a benchmark EEG dataset for motor imagery research, provided as part of the international BCI Competition IV hosted by the Berlin BCI group and the Graz BCI lab. It contains multi‑session EEG recordings from **9 subjects** performing **cued motor imagery** tasks of four types: **left hand, right hand, foot, and tongue**.

Each subject performed two sessions on separate days. Each session consists of 6 runs, and each run contains 48 trials — 12 trials per class — yielding **288 trials per session**.

- **EEG channels:** 22 scalp electrodes  
- **EOG channels:** 3 (used for artifact detection, usually removed in preprocessing)  
- **Sampling rate:** 250 Hz  
- **Recordings:** Band‑pass filtered between 0.5–100 Hz with a 50 Hz notch filter  
- **File format:** General Data Format for biomedical signals (GDF)  
- **Classes:**  
  - Left hand imagery  
  - Right hand imagery  
  - Foot imagery  
  - Tongue imagery 

The dataset is widely used for motor imagery classification research and benchmarking classification pipelines (e.g., CSP+LDA, deep learning models).

For more infomation, see https://www.bbci.de/competition/iv/desc_2a.pdf

**Download URL (official):**  
👉 https://www.bbci.de/competition/download/competition_iv/BCICIV_2a_gdf.zip  

## Important Dates

| Milestone                          | Deadline                        |
| -                                  | -                               |
| Project Group Formation Submission | Feb 6                           |
| Project Group Contract             | Feb 13                          |
| Instructor Check-in 1              | Feb 20                          |
| Instructor Check-in 2              | By Mar 19 (earlier recommended) |
| Final Project Submission           | Mar 20 at 3:00 PM               |
| Project Reviews Due                | Mar 22 at 11:59 PM              |

## Repository Structure (Planned)

```
project/
│
├── data/              # EEG datasets
├── environment.yml
├── EEG_Motor_Imagery_Classification.ipynb
└── README.md
```

## Setup & How to Run our code

### 0. Using VS Code (Optional)
VS Code can run ```.ipynb``` notebooks directly:
1. [Download](https://code.visualstudio.com/) and Install.
2. Install the **Python** and **Jupyter** extensions in VSCode.
3. Open the notebook file (```.ipynb```) in VS Code after you have done step 1 - n.
4. Select your Conda environment as the kernel in the top-right corner.
5. Run notebook cells just like in a browser.

### 1. Install Conda
- [Download](https://www.anaconda.com/download/success) and install 
    - Miniconda (lightweight) or 
    - Anaconda (full distribution).  
- Conda manages Python versions, packages, and virtual environments.

### 2. Create & Activate / Deactivate Virtual Environment
- Create a Virtual Environment or Use our environment

    In your terminal (or the terminal in VS Code) 
    -  Create a virtual environment with your own
        create a new environment with the Python version you want:
        ```bash
        conda create -n cogs-189-X-proj-env python=3.12
        ```

        In this project, we use environment named ```cogs-189-X-proj-env``` with **Python 3.12**
    - Use our provided environment::
        ```bash
        conda env create -f environment.yml
        ```

- Activate your environment:
    ```bash
    conda activate cogs-189-X-proj-env
    ```

- Deactivate (after you run our notebook)

    When you’re done working, you can deactivate the environment:
    ```bash
    conda deactivate
    ```
    Your terminal will return to the base environment or system Python.

### 3. Install & Open Our Jupyter Notebook
- Inside the activated environment, install Jupyter: 
    ```bash
    conda install notebook
    ```
- Open Our Jupyter Notebook
1. In terminal:
    1. Open Jupyter Notebook Interface:
        ```bash
        jupyter notebook
        ```
    2. In the Jupyter interface, navigate to the folder containing the ```.ipynb``` file and click it to open.
    3. Stop the server from the terminal

        - Go to the terminal where you ran ```jupyter notebook```.

        - Press ```Ctrl + C``` (hold Ctrl and press C).

        - You will see a message like:
            ```bash
            Shutdown this notebook server (y/[n])?
            ```
        - Type ```y``` and press Enter.

2. In VS Code:

    simply File → Open File → select notebook.

    Make sure the kernel is set to your environment.

### 4. Run Project Code
Once the notebook is open:

- Make sure the correct kernel/environment is selected ```(Python (cogs-189-X-proj-env))```.

Run all cells in order:

- In Jupyter Notebook (browser): Click Cell → Run All or press ```Shift + Enter``` for each cell.

- In VS Code: Click Run Cell on each cell or use the Run All Cells toolbar button.
