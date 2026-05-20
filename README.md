# Quantum Coding with Qiskit
A course to teach the basics of IBM's Qiskit SDK

## Course Information
Quantum Coding with Qiskit | A Course for Beginners

- Duration: 3-months, with weekly sessions and study weeks
- Focus: hands-on learning of Qiskit using the IBM Quantum Platform
- Format: virtual, weekly course modules covering core quantum concepts, qubits, superposition, entanglement, applications, and discussion

## Learner
- Carlos Araque — Qiskit Advocate


## Installation

This project uses **uv** for dependency management. The repository includes:

- `pyproject.toml` — project dependencies  
- `uv.lock` — locked dependency versions for reproducible environments  

Using **uv** is recommended because it is fast and ensures everyone installs the same dependency versions.

---

## Option 1 (Recommended): Install with uv

### Install uv

See the official installation instructions:  
https://docs.astral.sh/uv/getting-started/installation/

Or install directly from the terminal.

**macOS / Linux**

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows (PowerShell)**

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Alternatively, install with pip:

```bash
pip install uv
```

---

### Install project dependencies

Clone the repository and run:

```bash
uv sync
```

This will:

- create a virtual environment (`.venv`)
- install all dependencies from `pyproject.toml`
- reproduce the exact environment defined in `uv.lock`

Activate the environment:

**macOS / Linux**

```bash
source .venv/bin/activate
```

**Windows**

```powershell
.venv\Scripts\activate
```

---

## Option 2: Install with pip

If you prefer using pip, you can install the project directly from `pyproject.toml`.

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it:

**macOS / Linux**

```bash
source .venv/bin/activate
```

**Windows**

```powershell
.venv\Scripts\activate
```

Install the project:

```bash
pip install .
```

---

## Option 3: Install with Conda

If you prefer Conda, create an environment and install the project using pip.

Create the environment:

```bash
conda create -n qiskit-fundamentals python=3.12
```

Activate it:

```bash
conda activate qiskit-fundamentals
```

Install the project:

```bash
pip install .
```
## IBM Quantum credentials

This repository does not include IBM Quantum credentials.

Before running hardware examples, save your IBM Quantum credentials locally:

```python
from qiskit_ibm_runtime import QiskitRuntimeService

QiskitRuntimeService.save_account(
    channel="ibm_quantum_platform",
    token="YOUR_IBM_API_KEY",
    instance="YOUR_IBM_INSTANCE_CRN",
    overwrite=True,
    set_as_default=True
)