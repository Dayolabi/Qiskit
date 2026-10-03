# Qiskit

My notebooks from learning quantum computing with IBM's [Qiskit](https://www.ibm.com/quantum/qiskit) framework. Each folder follows a course on [IBM Quantum Learning](https://quantum.cloud.ibm.com/learning), with my own modifications and added explanations.

This repository is updated as I work through more material.

## Courses

| Folder | Course | Topics |
|---|---|---|
| [Basics of Quantum Information](Basics_of_Quantum_Information/) | [Basics of Quantum Information](https://quantum.cloud.ibm.com/learning/en/courses/basics-of-quantum-information) | Single and multiple systems, entanglement, teleportation, superdense coding, CHSH game |
| [Fundamentals of Quantum Algorithms](Fundamentals_of_Quantum_Algorithms/) | [Fundamentals of Quantum Algorithms](https://quantum.cloud.ibm.com/learning/en/courses/fundamentals-of-quantum-algorithms/) | Deutsch's algorithm, Deutsch–Jozsa algorithm, Bernstein–Vazirani problem |

Each folder has its own README describing the notebooks inside it.

## Getting started

```bash
git clone https://github.com/Dayolabi/Qiskit.git
cd Qiskit
pip install qiskit qiskit-aer numpy matplotlib jupyter
jupyter notebook
```

### Requirements

- Python 3.8+
- [Qiskit](https://pypi.org/project/qiskit/) `>= 2.0`
- [qiskit-aer](https://pypi.org/project/qiskit-aer/) (for circuit simulation)
- NumPy
- Matplotlib (for circuit and histogram visualizations)

## Structure

```
Qiskit/
├── Basics_of_Quantum_Information/
│   ├── README.md
│   ├── single_systems.ipynb
│   ├── multiple_systems.ipynb
│   └── entanglement.ipynb
└── Fundamentals_of_Quantum_Algorithms/
    ├── README.md
    ├── deutsch's_algorithm.ipynb
    └── deutsch-jozsa_algorithm.ipynb
```