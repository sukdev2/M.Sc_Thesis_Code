# Dark Matter Capture and Thermalization in the Sun

### M.Sc. Research Project

This repository contains the computational work associated with my M.Sc. Physics thesis on the **capture, propagation, and thermalization of TeV-scale dark matter inside the Sun** using **Non-Relativistic Effective Field Theory (NR-EFT)**.

The main operators studied are

$$\mathcal{\hat{O}}_4, \qquad \mathcal{\hat{O}}_8, \qquad \mathcal{\hat{O}}_{15}$$

The analysis considers **Hydrogen (H), Iron (Fe), and Phosphorus (P)** as representative solar target nuclei. And also we neglect the thermal motion of the target nuclei.

---

## Dark Matter Capture

The dark matter speed inside the Sun is

$$w(r)=\sqrt{u^2+v_{\rm esc}^2(r)}$$

The recoil energy is related to the momentum transfer by

$$E_R=\frac{q^2}{2m_T}$$

The capture rate is obtained by integrating over the solar radius, halo velocity distribution, and recoil energy:

$$C=
4\pi
\int_0^{R_\odot}dr\,r^2
\int du\,
\frac{f(u)}{u}\,
w\,\Omega_v^-(w)$$

where

$$\Omega_v^-(w) =
\sum_T n_T(r)\,w
\int_{E_R^{\min}}^{E_R^{\max}}
dE_R\,
\frac{d\sigma_T}{dE_R}$$

Thus, the capture calculation contains the factor $w^2$ after substituting $\Omega_v^-(w)$.

The differential cross section is written in terms of dark-matter and nuclear response functions:

$$\frac{d\sigma}{dE_R}=
\frac{1}{2J_T+1}
\frac{2m_T}{w^2}
\sum_{\tau,\tau'}
\sum_k
R_k^{\tau\tau'}W_k^{\tau\tau'}$$

---

## EFT Operators

### $\mathcal{\hat{O}}_4$

$$\mathcal{\hat{O}}_4 = \mathbf{S}_\chi\cdot\mathbf{S}_N$$

spin-dependent interaction.

### $\mathcal{\hat{O}}_8$

$$\mathcal{O}_8 = \mathbf{S}_\chi\cdot\mathbf{v}^{\perp}$$

velocity-dependent interaction.

### $\mathcal{\hat{O}}_{15}$

$$\mathcal{O}_{15} = -\left(
\mathbf{S}_\chi\cdot\frac{\mathbf q}{m_N}
\right) \left[\left(\mathbf S_N\times\mathbf v^\perp\right) \cdot \frac{\mathbf q}{m_N} \right]$$

This operator contains both momentum- and velocity-dependent contributions.

---

## Heavy Dark Matter

For a collision between dark matter and a target nucleus,

$$\frac{\Delta E}{E} \sim \frac{4m_\chi m_T}{(m_\chi + m_T)^2}$$

In the heavy-DM limit,

$$
m_\chi \gg m_T, \qquad \frac{\Delta E}{E} \sim \frac{4m_T}{m_\chi}$$

Therefore, heavy dark matter loses only a small fraction of its energy in each scattering, making capture and subsequent thermalization increasingly inefficient.

---

## Orbital Evolution

After capture, the dark matter particle follows a gravitationally bound orbit inside the Sun. Repeated scattering events remove orbital energy and reduce its semi-major axis.

The capture-weighted initial semi-major axis is

$$\langle a_0\rangle = \frac{1}{C} \int dr\int dE_R\, \frac{d^2C}{dr\,dE_R} a_0(r,E_R)$$

The orbital evolution is studied through the energy lost in subsequent scatterings.

---

## Capture--Annihilation

The number of captured dark matter particles satisfies

$$\frac{dN}{dt} = C-C_A N^2$$

Its solution is

$$N(t) = \sqrt{\frac{C}{C_A}}\, \tanh\left(\sqrt{CC_A}\,t\right)$$

The annihilation rate is

$$\Gamma_A = \frac{1}{2}C_A N^2$$

The spatial dark matter distribution is written as

$$n(r)=N(t_\odot)g(r)$$

with

$$\int g(r)\,dV=1$$

and

$$C_A = \langle\sigma v\rangle \int g^2(r)\,dV$$

---

## Neutrino Flux

For the simplified annihilation channel

$$
\chi\chi\rightarrow\nu\nu
$$

two neutrinos are produced per annihilation. The differential flux at Earth is

$$\frac{d\Phi_\nu}{dE_\nu} = \frac{2\Gamma_A}{4\pi D_\odot^2} \delta(E_\nu-m_\chi)$$

---

## Main Results

We investigates the mass range

$$10^2~{\rm GeV} \leq m_\chi \leq 10^5~{\rm GeV}$$

with particular emphasis on the heavy-dark-matter regime.

The results show that:

- Capture depends strongly on the NR-EFT operator and nuclear response.
- $\mathcal{\hat{O}}_4$ is associated with spin-dependent interactions.
- $\mathcal{\hat{O}}_8$ contains transverse-velocity dependence.
- $\mathcal{\hat{O}}_{15}$ has strong momentum dependence.
- Heavy dark matter suffers very small fractional energy loss per scattering.
- Thermalization becomes inefficient and extended non-thermal orbits can persist.
- The capture--annihilation system remains far from equilibrium, with

$$\sqrt{CC_A}\,t_\odot\ll1$$

These features determine the resulting annihilation rate and neutrino flux.

---

## Repository Contents

```text
M.Sc_Thesis_Code/
│
├── README.md
├── LICENSE
├── Code/
├── Data/
├── Figures/
└── Notebook/
```

The notebooks contain the numerical implementation of the capture, orbital evolution, annihilation, and neutrino-flux calculations.

---

## References

1. R. Catena and B. Schwabe,  
   *Form factors for dark matter capture by the Sun in effective theories*,  
   JCAP 04 (2015) 042.  
   [arXiv:1501.03729](https://arxiv.org/abs/1501.03729)

2. A. Widmark,  
   *Thermalization time scales for WIMP capture by the Sun in effective theories*,  
   JCAP 05 (2017) 046.  
   [arXiv:1703.06878](https://arxiv.org/abs/1703.06878)

3. A. L. Fitzpatrick et al.,  
   *The Effective Field Theory of Dark Matter Direct Detection*,  
   JCAP 02 (2013) 004.  
   [arXiv:1203.3542](https://arxiv.org/abs/1203.3542)
---
