
# SayCan-Extended

**Extending SayCan Framework**: Enhancing language-driven robotic task planning and execution with improved scoring, direct control, and pipeline optimization.

---

## Overview

This project extends the original [SayCan](https://say-can.github.io/) robotic task planning framework. Key updates include:
- **Direct Control Mechanisms** using PyBullet.  
- **Enhanced Scoring Systems** for affordance and language evaluations.  
- **Batch Processing Optimization** to improve throughput and reduce latency.

---

## Setup and Installation

Follow these steps to set up the environment and run the experiments:

### 1. Clone the Repository

```bash
git clone https://github.com/csce585-mlsystems/SayCan-Extended.git
cd SayCan-Extended
```

### 2. Create and Activate Conda Environment

```bash
conda create -n saycan python=3.8
conda activate saycan
```

### 3. Install Dependencies

Ensure all required packages are installed:

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Required Assets

The project will download necessary assets automatically on the first run, including:
- UR5e robot URDF files  
- Robotiq 2F-85 gripper files  
- Bowl assets  
- ViLD pretrained model weights  

---

## Environment

The simulation environment is built using **PyBullet** and includes:
- **UR5e robotic arm**
- **Robotiq 2F-85 gripper**
- **Manipulatable objects** (blocks, bowls)
- **Cameras** for top-down and perspective views

---

## Key Components

- **Vision Module**: ViLD (Vision-Language Detection) for zero-shot object detection.  
- **Language Module**: GPT-3.5-turbo-instruct for task planning and decomposition.  
- **Manipulation Module**: PyBullet direct control for pick-and-place actions.  

---

## Usage

Run the main notebook **`SayCanWithDirectControl.ipynb`** to:
1. Set up the PyBullet simulation environment.  
2. Perform object detection using ViLD.  
3. Execute tasks with optimized scoring and batch processing.  

### To Start:
Launch Jupyter Notebook:
```bash
jupyter notebook
```

---

## Hardware Requirements

- **CUDA-capable GPU** recommended for running vision and language models.  
- Tested on **Python 3.8** with **PyTorch and JAX**.  

---

## Updating Dependencies

To install or update dependencies based on your conda environment:
```bash
pip freeze > requirements.txt
```

---

## Citation

If you use this work, please cite:
```bibtex
@misc{saycan2022,
    title={Do As I Can, Not As I Say: Grounding Language in Robotic Affordances},
    author={Michael Ahn and Anthony Brohan and Noah Brown and ... Andy Zeng},
    year={2022}
}
```

---

## License

This project is licensed under the Apache License 2.0. See the LICENSE file for details.

---

## Links
- **Code**: [GitHub Repository](https://github.com/csce585-mlsystems/SayCan-Extended)  
- **Video Presentation**: [YouTube Video](https://www.youtube.com/your-video-link)
