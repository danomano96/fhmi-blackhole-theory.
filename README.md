# Breathing Black Hole Membrane

[![PyPI version](https://badge.fury.io/py/bh-breathing-membrane.svg)](https://badge.fury.io/py/bh-breathing-membrane)
[![Tests](https://github.com/yourusername/bh-breathing-membrane/actions/workflows/test.yml/badge.svg)](https://github.com/yourusername/bh-breathing-membrane/actions)
[![Docs](https://readthedocs.org/projects/bh-breathing-membrane/badge/?version=latest)](https://bh-breathing-membrane.readthedocs.io)

A 3D numerical model of black hole horizon dynamics using the **membrane paradigm**. Simulates "breathing" perturbations that disperse entropy via damped waves on the sphere. Matches quasinormal modes (QNMs) and extracts GW proxies.

## Physics
- **Dynamics**: Damped wave eq. \( \partial_t^2 u = \nabla^2 u - \gamma \partial_t u \)
- **Entropy**: \( \delta S(t) = \frac{1}{4} [A(t) - A_0] \), with exact area integral.
- **Features**: QNM validation, infalling triggers, GW extraction.

## Quick Start
```bash
git clone https://github.com/yourusername/bh-breathing-membrane.git
cd bh-breathing-membrane
pip install -e .[dev]
jupyter
