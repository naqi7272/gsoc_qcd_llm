# Quantum Circuit Design with LLMs- GSoC 2026 Evaluation Task
 
**ML4SCI – QMLHEP | Google Summer of Code 2026**
 
**Applicant:** Syed Naqi Abbas ([naqi8756@gmail.com](mailto:naqi8756@gmail.com))
 
---
 
## Overview
 
This repository contains my evaluation task submission for the **Quantum Circuit Design with LLMs** project under ML4SCI (QMLHEP) for GSoC 2026. The project demonstrates an agentic framework for quantum machine learning using [Orchestral AI](https://github.com/orchestralAI/orchestral-ai), [PennyLane](https://pennylane.ai/), and the Anthropic Claude API.
 
## Tasks Completed
 
**Task 1 — Orchestral AI Setup & Custom Tool:** Created a `hilbert_space_dimension` tool with comprehensive docstrings and demonstrated reliable agent invocation across simple, comparative, and applied reasoning queries.
 
**Task 2 — QNN Training Tool:** Built a 4-qubit variational quantum circuit (angle embedding, RY/RZ rotations, CNOT entanglement) for binary MNIST classification. Wrapped as an Orchestral AI tool (`train_qnn`) with configurable hyperparameters, returning structured JSON metrics.
 
**Task 3 — Agent-Driven Hyperparameter Optimization:** Implemented a closed-loop pipeline where the agent autonomously explores 5 learning rates, observes training metrics, and identifies the optimal configuration through reasoning.
 
## Repository Structure
 
```
├── gsoc_qcd_llm_evaluation.ipynb   # Complete evaluation notebook (single file, all figures inline)
└── README.md
```
 
## Setup
 
```bash
pip install orchestral-ai pennylane scikit-learn matplotlib
```
 
Set your API key:
```python
os.environ["ANTHROPIC_API_KEY"] = "your-key-here"
```
 
Requires **Python 3.13+**.
 
## Technical Stack
 
- **Agent Framework:** Orchestral AI v1.3.0
- **Quantum Simulation:** PennyLane (default.qubit, autograd interface)
- **LLM Provider:** Anthropic Claude (provider-agnostic — switchable to GPT-4, Llama, etc.)
- **ML/Data:** scikit-learn, NumPy, Matplotlib
