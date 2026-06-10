---
layout: default
title: Homework 1
permalink: /homework/01/index.html
---

# PyTorch Basics and Classifiers Lab
**Course:** Deep Learning (Master's Degree Program)  
**Institution:** The University of Texas at Austin (UT Austin)

## Overview
This repository contains a lab assignment for the Deep Learning course. The objective of this lab is to explore, implement, and optimize tensor manipulation, classification, and forecasting models using PyTorch.

The project compares inefficient Python operations against vectorized PyTorch implementations, demonstrating the performance benefits and design considerations of tensor-based computing. The system constructs basic classifiers and forecasts temperatures using real-world data from Austin, Texas.

## Features and Execution Methods
The homework is structured into three parts, each focusing on different aspects of PyTorch development:

*   **PyTorch Basics (`pytorch_basics.py`):** Re-implementation of standard functions using efficient, vectorized PyTorch operations without loops, numpy, or in-place assignments.
*   **Nearest Neighbor Classifier (`nearest_neighbor_classifier.py`):** Implementation of a basic machine learning classifier based on proximity search.
*   **Weather Forecasting (`weather_forecast.py`):** Implementation of a simple predictive model for daily temperature forecasting.

## Project Structure
*   [pytorch_basics.py](file:///home/diegof/Documents/master_degree_repos/homework1-deeplearning/homework/pytorch_basics.py): Tensor manipulation exercises and basics.
*   [nearest_neighbor_classifier.py](file:///home/diegof/Documents/master_degree_repos/homework1-deeplearning/homework/nearest_neighbor_classifier.py): Nearest neighbor classifier implementation.
*   [weather_forecast.py](file:///home/diegof/Documents/master_degree_repos/homework1-deeplearning/homework/weather_forecast.py): Temperature prediction and forecasting model.
*   [notebook.ipynb](file:///home/diegof/Documents/master_degree_repos/homework1-deeplearning/notebook.ipynb): Jupyter notebook for playing with tensors.
*   [requirements.txt](file:///home/diegof/Documents/master_degree_repos/homework1-deeplearning/requirements.txt): Python package dependencies.
*   [bundle.py](file:///home/diegof/Documents/master_degree_repos/homework1-deeplearning/bundle.py): Submission bundle generator.
*   `grader/`: Contains local test cases and grading logic.

## Prerequisites
*   **Python 3.11**
*   **PyTorch 2.3.1+**
*   **Miniconda** (recommended for environment management)

## Building the Project
Set up the Conda environment and install the required packages:
```bash
conda create --name deeplearning python=3.11 -y
conda activate deeplearning
pip install torch==2.3.1+cu118 torchvision==0.18.1+cu118 --index-url https://download.pytorch.org/whl/cu118
pip install -r requirements.txt
```

## Running the Code

### 1. Running the Local Grader
You can grade your assignment locally to verify correctness and view test results.
```bash
# Show all output (useful to see print statements)
python3 -m grader homework -vv

# Show individual test cases
python3 -m grader homework -v

# Grade with minimal output
python3 -m grader homework

# Disable colored output
python3 -m grader homework --disable_color
```

### 2. Generating a Submission Bundle
Create a zip archive of your solutions to submit on Canvas:
```bash
python3 bundle.py homework [YOUR UT ID]
```

**Verification:**
Verify that the generated bundle is correct and grades successfully before submitting:
```bash
python3 -m grader [YOUR UT ID].zip
```

## Validation and Profiling
*   **Validation:** The local grader executes tests against your code to ensure correctness and adherence to PyTorch-only operations (no loops, numpy, or assignments). The online grader will convert your code to TorchScript to strictly enforce these rules.
*   **Online Grader Constraints:** Submissions uploaded to Canvas will be processed by an automated grading system. Note that `exit()` commands, file system writes, and network/forking activities are disabled in the grading environment. There is a soft limit of 5 submissions per assignment.

## License and Academic Integrity
This project is developed for educational purposes as part of the Deep Learning course at UT Austin. Please refer to the course syllabus regarding collaboration and academic integrity policies.
