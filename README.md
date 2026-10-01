# Dark Matter Capture and Thermalization in the Sun

## M.Sc. Research Project

This repository contains the computational work associated with my M.Sc. Physics research project:

**Propagation of TeV--PeV Scale Dark Matter Inside the Sun within the Framework of Non-Relativistic Effective Field Theory**

---

## Overview

This project studies the capture and subsequent evolution of dark matter particles inside the Sun using **Non-Relativistic Effective Field Theory (NR-EFT)**.

The main physical sequence is

\[
\text{Halo Dark Matter}
\rightarrow
\text{Scattering}
\rightarrow
\text{Gravitational Capture}
\rightarrow
\text{Bound Orbit}
\rightarrow
\text{Orbital Energy Loss}
\rightarrow
\text{Thermalization}
\rightarrow
\text{Annihilation}.
\]

The main NR-EFT operators studied are

\begin{equation}
\mathcal{O}_4,\qquad
\mathcal{O}_8,\qquad
\mathcal{O}_{15}.
\end{equation}

---

## Dark Matter Capture

The capture rate is calculated by integrating over the solar radius, incoming dark matter velocity, recoil energy, and solar target elements:

\[
C =
4\pi
\int_0^{R_\odot} dr\,r^2
\int du\,
\frac{f(u)}{u}
w^2
\frac{\rho_\chi}{m_\chi}
\sum_T n_T(r)
\int dE_R\,
\frac{d\sigma_T}{dE_R}.
\]

The dark matter velocity inside the Sun is

\[
w(r)=
\sqrt{u^2+v_{\rm esc}^2(r)}.
\]

The momentum transfer is

\[
q=\sqrt{2m_T E_R}.
\]

The differential cross section is calculated using the dark matter and nuclear response functions:

\[
\frac{d\sigma}{dE_R}
=
\frac{2m_T}{(2j_T+1)w^2}
\sum_{\tau,\tau'}
\sum_k
R_k^{\tau\tau'}W_k^{\tau\tau'}.
\]

---

## NR-EFT Operators

### Operator \(\mathcal{O}_4\)

\[
\mathcal{O}_4
=
\mathbf{S}_\chi\cdot\mathbf{S}_N.
\]

This is a spin-dependent interaction involving the nuclear responses

\[
W_{\Sigma'}
\quad\text{and}\quad
W_{\Sigma''}.
\]

### Operator \(\mathcal{O}_8\)

\[
\mathcal{O}_8
=
\mathbf{S}_\chi\cdot\mathbf{v}^{\perp}.
\]

This is a velocity-dependent interaction involving responses such as

\[
W_M
\quad\text{and}\quad
W_\Delta.
\]

### Operator \(\mathcal{O}_{15}\)

\[
\mathcal{O}_{15}
=
-\left(
\mathbf{S}_\chi\cdot\frac{\mathbf q}{m_N}
\right)
\left[
(\mathbf S_N\times\mathbf v^\perp)
\cdot
\frac{\mathbf q}{m_N}
\right].
\]

This operator has explicit momentum-transfer dependence and involves responses including

\[
W_{\Phi''}
\quad\text{and}\quad
W_{\Sigma'}.
\]

---

## Solar Models and Targets

The main solar model used in the project is **BP2000**, with an additional comparison using **AGSS09**.

For the thesis calculation, the main target elements are

\[
\mathrm{H},\qquad
\mathrm{Fe},\qquad
\mathrm{P}.
\]

The total capture rate is therefore

\[
C_{\rm total}
=
C_{\rm H}
+
C_{\rm Fe}
+
C_{\rm P}.
\]

The repository keeps the individual elemental contributions separate to study their dependence on dark matter mass and interaction operator.

---

## Initial Orbit and Thermalization

After a scattering event produces a gravitationally bound dark matter particle, its initial semi-major axis is determined from its orbital energy.

The capture-weighted average initial semi-major axis is

\[
\langle a_0\rangle
=
\frac{1}{C}
\int_0^{R_\odot}dr
\int dE_R\,
\frac{d^2C}{dr\,dE_R}
a_0(r,E_R).
\]

Subsequent scatterings remove orbital energy:

\[
\Delta E_{\rm orb}
=
\int_{\rm path}dl
\sum_T n_T(r)
\int dE_R\,
E_R
\frac{d\sigma_T}{dE_R}.
\]

The orbital evolution is followed using a Monte Carlo approach based on the work of Widmark.

---

## Thermalized Distribution

A thermalized dark matter population can be represented schematically as

\[
n_\chi(r)
\propto
\exp\left[
-\frac{m_\chi\Phi(r)}
{k_B T_c}
\right],
\]

where \(\Phi(r)\) is the solar gravitational potential and \(T_c\) is the solar core temperature.

The thermalization time is obtained by following the evolution of the captured dark matter orbit through repeated scattering events.

---

## Annihilation

The number of captured dark matter particles evolves according to

\[
\frac{dN}{dt}
=
C-C_A N^2.
\]

The annihilation rate is

\[
\Gamma_A
=
\frac{1}{2}C_A N^2.
\]

The solution for the captured population is

\[
N(t)
=
\sqrt{\frac{C}{C_A}}
\tanh\left(
\sqrt{CC_A}\,t
\right).
\]

The annihilation coefficient is

\[
C_A
=
\frac{\langle\sigma v\rangle}
{V_{\rm eff}}.
\]

---

## Neutrino Flux

A simplified total neutrino flux at Earth is

\[
\Phi_\nu
=
\frac{N_\nu\Gamma_A}
{4\pi D_\odot^2}.
\]

For the simplified assumption of two neutrinos per annihilation,

\[
\Phi_\nu
=
\frac{2\Gamma_A}
{4\pi D_\odot^2}.
\]

A realistic neutrino prediction requires the neutrino spectrum, propagation through the Sun, absorption, and oscillations to be included.

---

## Repository Structure

```text
.
├── README.md
├── LICENSE
├── DATA_SOURCES.md
├── requirements.txt
│
├── notebooks/
│   |
│   └── annihilation & flux.ipynb
│
├── data/
│   ├── bp2000_standard.txt
│   └── AGSS09/
│
└── figures/
