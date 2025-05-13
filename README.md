# SayCan-Extended

SayCan-Extended is an enhanced implementation of the original [SayCan](https://say-can.github.io/) robotic task planning framework. It introduces practical improvements for more reliable, cost-efficient, and scalable robotic execution based on natural language instructions.

Developed as a final project for CSCE 585: Machine Learning Systems at the University of South Carolina.

---

## Description

This project enhances SayCan with:

- **Direct control mechanisms** using PyBullet for robotic execution.
- **Improved scoring systems** for language and affordance evaluation.
- **Pipeline optimizations**, including batch processing and response caching.
- **Robust environment compatibility**, updated dependencies, and GPU acceleration.

It supports deterministic robotic actions (e.g., pick-and-place), zero-shot object detection via ViLD, and GPT-3.5-based task planning with scoring logic that improves execution accuracy and latency.

---

## My Contributions

- Replaced CLIPort with direct control in PyBullet for deterministic robotic manipulation.
- Improved affordance and language scoring logic for task selection.
- Implemented batch processing and caching to reduce inference latency and API costs.
- Debugged and modernized environment setup with GPU support.
- Designed and ran performance experiments and analysis.

---

## Setup and Installation

```bash
git clone https://github.com/csce585-mlsystems/SayCan-Extended.git
cd SayCan-Extended
```

### Conda Environment

```bash
conda create -n saycan python=3.8
conda activate saycan
pip install --upgrade pip
pip install -r requirements.txt
```

---

## Running the Project

Launch `SayCanWithDirectControl.ipynb` to:

1. Load the PyBullet simulation environment.
2. Detect objects using ViLD.
3. Score tasks using language and affordance models.
4. Execute pick-and-place actions with optimized performance.

---

## Environment Requirements

- **Python 3.8**
- **CUDA-capable GPU** (optional, for ViLD and GPT-3.5 integration)
- **PyBullet**, **JAX**, **OpenAI GPT API**

Assets are downloaded automatically on first run:
- UR5e robot and gripper models
- Bowls and block assets
- ViLD weights

---

## Key Technologies

- **PyBullet** for simulation and control
- **GPT-3.5-turbo-instruct** for task decomposition
- **ViLD** for object detection
- **JAX**, **PyTorch**, **OpenAI API**

---

## Project Outcomes

- 100% success rate on some sorting tasks (e.g., blocks into bowls)
- Up to 75% success on stacking and alignment tasks
- 38.6s batch latency (down from ~48s originally)
- Reduced API cost via caching and fewer redundant calls

---

## Citation

If referencing this work:

```bibtex
@misc{saycan2022,
    title={Do As I Can, Not As I Say: Grounding Language in Robotic Affordances},
    author={Michael Ahn and Anthony Brohan and Noah Brown and ... Andy Zeng},
    year={2022}
}
```

---

## Additional Resources

- [Video Presentation](https://www.youtube.com/watch?v=EAyNhHgrMJE)
- [Final Report PDF](https://github.com/csce585-mlsystems/SayCan-Extended/blob/main/CSCE585_ProjectSlideshow.pdf)

---

## License

This project is licensed under the Apache License 2.0.
