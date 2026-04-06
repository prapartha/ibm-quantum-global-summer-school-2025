# IBM Quantum Global Summer School 2025 — Solutions

Personal solutions for the [IBM Quantum Global Summer School 2025](https://github.com/qiskit-community/qgss-2025), completed on IBM Quantum Platform.

> **Official course repository:** [qiskit-community/qgss-2025](https://github.com/qiskit-community/qgss-2025)

---

## Completion

| Lab | Status |
|-----|--------|
| Lab 0 — Hello Quantum World | ✅ [Proof](completions/lab0-complete.png) |
| Lab 1 — Recreating Famous Experiments | ✅ [Proof](completions/lab1-complete.png) |
| Lab 2 — Cutting Through the Noise | ✅ [Proof](completions/lab2-complete.png) |
| Lab 3 — Good Sampling for Chemistry Hamiltonians | ✅ [Proof](completions/lab3-complete.png) |
| Lab 4 — Quantum Error Correction | ✅ [Proof](completions/lab4-all-complete.png) |

[PennyLane Certificate](completions/pennylane-certificate.png)

---

## Structure

```
ibm-quantum-global-summer-school-2025/
├── labs/
│   ├── lab-0/                 # Hello Quantum World
│   ├── lab-1/                 # Recreating Famous Experiments at Home
│   │   ├── lab1.ipynb
│   │   ├── Supplemental_long_range_entanglement_...ipynb
│   │   ├── grumpy.png         # image assets used in exercises
│   │   └── happy.png
│   ├── lab-2/                 # Cutting Through the Noise
│   ├── lab-3/                 # Good Sampling for Chemistry Hamiltonians
│   └── lab-4/                 # Quantum Error Correction
│       ├── lab4.ipynb
│       ├── N2_device_bitarray.npy
│       ├── backend_target_v20.pkl
│       └── backend_target_v21.pkl
├── scripts/                   # Reusable utility modules
├── completions/               # Lab completion screenshots & certificate
└── README.md
```

---

## Labs

### Lab 0 — Hello Quantum World!
[`labs/lab-0/lab0.ipynb`](labs/lab-0/lab0.ipynb)

Introduction to quantum circuits using Qiskit — building, visualizing, and running circuits on IBM backends.

---

### Lab 1 — Recreating Famous Experiments at Home!
[`labs/lab-1/lab1.ipynb`](labs/lab-1/lab1.ipynb)

Implements landmark quantum experiments (Bell inequality, entanglement) using real IBM quantum hardware. Includes a supplemental notebook on long-range entanglement with limited qubit connectivity.

**Also in this folder:**
- [`Supplemental_long_range_entanglement_with_limited_qubit_connectivity.ipynb`](labs/lab-1/Supplemental_long_range_entanglement_with_limited_qubit_connectivity.ipynb) — deep dive into entanglement across constrained topologies

---

### Lab 2 — Cutting Through the Noise
[`labs/lab-2/Lab2.ipynb`](labs/lab-2/Lab2.ipynb)

Explores quantum noise characterization and error mitigation techniques — Pauli noise, twirling, zero-noise extrapolation (ZNE), and probabilistic error cancellation (PEC).

---

### Lab 3 — The Power of Good Sampling for Simulating a Chemistry Hamiltonian
[`labs/lab-3/lab3.ipynb`](labs/lab-3/lab3.ipynb)

Applies advanced sampling strategies (classical shadows, randomized measurements) to estimate properties of the N₂ molecule Hamiltonian efficiently on quantum hardware.

---

### Lab 4 — Quantum Error Correction: From Core Concepts to Fault Tolerance
[`labs/lab-4/lab4.ipynb`](labs/lab-4/lab4.ipynb)

Implements quantum error correcting codes and explores the road to fault-tolerant quantum computing using real IBM backend data.

**Data files:**
- `N2_device_bitarray.npy` — measurement bitarray from real hardware runs
- `backend_target_v20.pkl` / `backend_target_v21.pkl` — serialized IBM backend target objects

---

## Scripts

| File | Description |
|------|-------------|
| [`utils.py`](scripts/utils.py) | Shared utilities for visualization and circuit helpers |
| [`lab4_util.py`](scripts/lab4_util.py) | Helper functions specific to Lab 4 (error correction) |

---

## Setup

```bash
pip install qiskit qiskit-ibm-runtime qiskit-aer \
            matplotlib numpy scipy
```

IBM Quantum account required for real hardware runs:

```python
from qiskit_ibm_runtime import QiskitRuntimeService
QiskitRuntimeService.save_account(channel="ibm_quantum", token="<YOUR_TOKEN>")
```

---

## Reference Papers

Papers used as course reading material (links to arXiv):

- [arXiv:1904.06560](https://arxiv.org/abs/1904.06560) — Quantum computing in the NISQ era and beyond (Preskill)
- [arXiv:2302.11320](https://arxiv.org/abs/2302.11320) — Reference paper (QGSS 2025 course material)
- [arXiv:2308.07915](https://arxiv.org/abs/2308.07915) — Reference paper (QGSS 2025 course material)
- [arXiv:2504.15725](https://arxiv.org/abs/2504.15725) — Reference paper (QGSS 2025 course material)
- [arXiv:2507.11536](https://arxiv.org/abs/2507.11536) — Reference paper (QGSS 2025 course material)
- Girvin — *Circuit QED: Superconducting Qubits Coupled to Microwave Photons* (Les Houches Lectures) — superconducting qubit background

---

## Reference

- [QGSS 2025 — Official Repo](https://github.com/qiskit-community/qgss-2025)
- [IBM Quantum Platform](https://quantum.ibm.com/)
- [Qiskit Documentation](https://docs.quantum.ibm.com/)
