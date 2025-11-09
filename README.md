# Breathing Black Hole Membrane  
**A 3D Dynamical Model of Horizon Entropy Dispersal Using the Membrane Paradigm**

[![PyPI](https://img.shields.io/pypi/v/bh-breathing-membrane?color=blue)](https://pypi.org/project/bh-breathing-membrane/)
[![Python 3.9+](https://img.shields.io/badge/python-3.9%2B-blue)](https://www.python.org/downloads/)
[![Tests](https://github.com/yourusername/bh-breathing-membrane/actions/workflows/tests.yml/badge.svg)](https://github.com/yourusername/bh-breathing-membrane/actions)
[![Docs](https://readthedocs.org/projects/bh-breathing-membrane/badge/?version=latest)](https://bh-breathing-membrane.readthedocs.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)

---

## Overview

This repository implements a **three-dimensional, time-dependent simulation** of a black hole event horizon using the **membrane paradigm** [Thorne, Price & Macdonald, 1986]. The horizon is modeled as a **viscous 2D fluid sphere** undergoing **radial "breathing" perturbations** that propagate as damped waves and disperse entropy across the surface.

Key features:
- **Exact entropy tracking**: \( \delta S(t) = \frac{1}{4} [A(t) - A_0] \)
- **Quasinormal mode (QNM) reproduction** from fluid dynamics
- **Infalling particle triggers**
- **Gravitational wave proxy extraction**
- **Interactive 3D animations & Jupyter notebooks**
- **Fully tested, documented, and pip-installable**

---

## Physics Motivation

The **Bekenstein-Hawking entropy** of a black hole is proportional to its horizon area:
\[
S = \frac{A}{4} \quad (\hbar = c = G = 1)
\]

In the **membrane paradigm**, the event horizon is replaced by a **fictitious timelike surface** (the *stretched horizon*) just outside \( r = 2M \), endowed with:
- Entropy density: \( s = \frac{1}{4} \)
- Shear viscosity: \( \eta = \frac{1}{16\pi} \)
- Electrical conductivity: \( \sigma = 1 \)

Small perturbations to the horizon shape induce **transient area changes** → **entropy fluctuations** that relax via **viscous damping** and **wave propagation** — analogous to fluid ripples on a droplet.

This model **reproduces the ringdown phase** of binary black hole mergers as seen by LIGO/Virgo, without solving full Einstein equations.

---

## Mathematical Models

We