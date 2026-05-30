# Basics of Quantum Information with Qiskit

A hands-on exploration of quantum computing fundamentals using IBM's [Qiskit](https://www.ibm.com/quantum/qiskit) framework. The notebooks follow the [Basics of Quantum Information](https://quantum.cloud.ibm.com/learning/en/courses/basics-of-quantum-information) course on IBM Quantum Learning, with personal modifications and additional explanations added for learning purposes.

## Notebooks

### 1. [Single Systems](Basics_of_Quantum_Information/single_systems.ipynb)
Foundations of quantum computing applied to a single qubit.

- Representing qubit states as vectors using NumPy and Qiskit's `Statevector` class
- Checking state validity (normalization condition)
- Simulating single-shot measurements and sampling outcome statistics
- Applying quantum gates (Y, H, S, T) as unitary operators via the `Operator` class
- Building and visualizing quantum circuits with `QuantumCircuit`
- Extracting the combined unitary matrix from a circuit

### 2. [Multiple Systems](Basics_of_Quantum_Information/multiple_systems.ipynb)
Extending single-qubit concepts to multi-qubit systems using the tensor product.

- Constructing multi-qubit states with `.tensor()` and the `^` shorthand
- Extended single-qubit basis states: `|+⟩`, `|−⟩`, `|+i⟩`, `|−i⟩`
- Building multi-qubit operators by tensoring single-qubit gates (H, I, X, T)
- Evolving multi-qubit states with composite operators
- Creating entanglement with the CNOT (CX) gate to produce Bell states
- Simulating partial measurements on multi-qubit states (e.g., the W state)

### 3. [Entanglement Protocols](Basics_of_Quantum_Information/entanglement.ipynb)
Three foundational quantum communication protocols, each powered by shared entangled Bell pairs (ebits).

| Protocol | What it achieves | Resources used |
|---|---|---|
| **Quantum Teleportation** | Transfer a qubit state using only classical communication | 1 ebit + 2 classical bits |
| **Superdense Coding** | Transmit 2 classical bits by sending 1 qubit | 1 ebit + 1 qubit |
| **CHSH Game** | Demonstrate quantum advantage over all classical strategies | 1 ebit |

The CHSH game result: the quantum strategy wins ~85.4% of games vs. the classical ceiling of 75%, directly demonstrating quantum non-locality.

## Requirements

- Python 3.8+
- [Qiskit](https://pypi.org/project/qiskit/) `>= 2.0`
- [qiskit-aer](https://pypi.org/project/qiskit-aer/) (for circuit simulation)
- NumPy
- Matplotlib (for circuit and histogram visualizations)

```bash
pip install qiskit qiskit-aer numpy matplotlib
```

## Source

All code originates from the IBM Quantum Learning course [Basics of Quantum Information](https://quantum.cloud.ibm.com/learning/en/courses/basics-of-quantum-information), with modifications made for personal learning and deeper understanding.
