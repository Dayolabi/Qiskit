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

### 2. [Deutsch–Jozsa Algorithm](deutsch-jozsa_algorithm.ipynb)
The generalization of Deutsch's algorithm to functions $f : \{0,1\}^n \to \{0,1\}$ that are promised to be either **constant** or **balanced** (0 on exactly half of the inputs). The notebook also covers the **Bernstein–Vazirani** problem, which uses the same circuit.

- Generating a random query gate that satisfies the promise, using X gates and multi-controlled X (`mcx`) gates
- Extending the Deutsch's algorithm circuit to $n$ input qubits
- Why the all-zeros outcome has amplitude $\frac{1}{2^n}\sum_x (-1)^{f(x)}$, which is $\pm 1$ for constant functions and $0$ for balanced ones
- Recovering a hidden string $s$ from $f(x) = s \cdot x$ (Bernstein–Vazirani) with a query gate built from CNOTs

| | Deutsch–Jozsa queries | Bernstein–Vazirani queries |
|---|---|---|
| **Classical** (deterministic) | $2^{n-1} + 1$ | $n$ |
| **Quantum** | 1 | 1 |

Deutsch–Jozsa: measuring all zeros means constant, anything else means balanced. Bernstein–Vazirani: the measured string is $s$.

## Requirements

- Python 3.8+
- [Qiskit](https://pypi.org/project/qiskit/) `>= 2.0`
- [qiskit-aer](https://pypi.org/project/qiskit-aer/) (for circuit simulation)
- NumPy (for generating random query gates)
- Matplotlib (for circuit visualizations)

```bash
pip install qiskit qiskit-aer numpy matplotlib
```

## Source

All code originates from the IBM Quantum Learning course [Fundamentals of Quantum Algorithms](https://quantum.cloud.ibm.com/learning/en/courses/fundamentals-of-quantum-algorithms/), with explanations added for personal learning and deeper understanding.
