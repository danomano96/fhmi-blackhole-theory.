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

We implement **three progressively sophisticated models**:

---

### 1. **Linear Breathing Mode** *(Default)*

Governed by the **damped scalar wave equation on the 2-sphere**:
\[
\boxed{
\partial_t^2 u = c^2 \nabla^2_{\text{sph}} u - \gamma \partial_t u
}
\]
- \( u(\theta,\phi,t) \): radial displacement from \( r_0 = 2M \)
- \( c = 1 \): light speed on horizon
- \( \gamma \): damping from viscosity \( \eta/s = 1/(4\pi) \)

**Entropy perturbation**:
\[
\delta S(t) = \frac{1}{4} \iint (r_0 + u)^2 \sin\theta \, d\theta d\phi - \pi r_0^2
\]

---

### 2. **Nonlinear Extension** *(Optional)*

For large amplitudes, include geometric nonlinearity:
\[
\partial_t^2 u = c^2 \left[ \nabla^2 u + \frac{2u}{r_0^2} (\nabla u)^2 \right] - \gamma \partial_t u
\]
Captures **horizon locking** and **turbulent cascades**.

---

### 3. **Infalling Particle Trigger**

Simulate matter crossing the horizon:
\[
u(\theta,\phi,t) \to u + A_0 \exp\!\left[-\frac{(\theta-\theta_0)^2 + (\phi-\phi_0)^2}{2\sigma^2}\right] \cdot e^{-(t-t_0)^2/\tau^2}
\]
Mimics **Vaidya metric** accretion; triggers QNM ringing.

---

# Breathing Black Hole Membrane – 3D Interactive Models

**Live 3D visualizations of a black hole horizon undergoing "breathing" perturbations using the membrane paradigm.**

[![GitHub](https://img.shields.io/github/stars/yourusername/bh-breathing-membrane?style=social)](https://github.com/yourusername/bh-breathing-membrane)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## Interactive 3D Models (Click to Rotate, Zoom, Pan)

> **All models are `.glb` files — GitHub renders them natively!**

---

### Model 1: Initial Localized Perturbation (t = 0)

```glb
models/initial_bump.glb