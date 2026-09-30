# Fundamentals of Quantum Algorithms with Qiskit

A hands-on exploration of quantum algorithms using IBM's [Qiskit](https://www.ibm.com/quantum/qiskit) framework. The notebooks follow the [Fundamentals of Quantum Algorithms](https://quantum.cloud.ibm.com/learning/en/courses/fundamentals-of-quantum-algorithms/) course on IBM Quantum Learning, with explanations added for learning purposes.

This folder is updated as the course progresses.

## Notebooks

### 1. [Deutsch's Algorithm](deutsch's_algorithm.ipynb)
The simplest quantum algorithm that beats every classical algorithm: deciding whether a one-bit function $f : \{0,1\} \to \{0,1\}$ is **constant** or **balanced**.

- Encoding each of the four one-bit functions as a quantum query gate $U_f$ using CNOT and X gates
- Building the Deutsch's algorithm circuit around any oracle (X + Hadamards → $U_f$ → Hadamard → measure)
- Phase kickback: how an output qubit in state $|-\rangle$ turns $f(x)$ into a phase $(-1)^{f(x)}$
- Running the circuit on `AerSimulator` with a single shot and interpreting the result

| | Queries needed |
|---|---|
| **Classical** (deterministic) | 2 |
| **Deutsch's algorithm** | 1 |

The measured bit equals $f(0) \oplus f(1)$: `0` means constant, `1` means balanced.

## Requirements

- Python 3.8+
- [Qiskit](https://pypi.org/project/qiskit/) `>= 2.0`
- [qiskit-aer](https://pypi.org/project/qiskit-aer/) (for circuit simulation)
- Matplotlib (for circuit visualizations)

```bash
pip install qiskit qiskit-aer matplotlib
```

## Source

All code originates from the IBM Quantum Learning course [Fundamentals of Quantum Algorithms](https://quantum.cloud.ibm.com/learning/en/courses/fundamentals-of-quantum-algorithms/), with explanations added for personal learning and deeper understanding.
