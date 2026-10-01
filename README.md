# Dark Matter Capture and Thermalization in the Sun

## Propagation of TeV--PeV Scale Dark Matter Inside the Sun within the Framework of Non-Relativistic Effective Field Theory

This repository contains the computational work associated with my M.Sc. Physics research project on the capture, orbital evolution, thermalization, and annihilation of dark matter particles inside the Sun.

The project studies dark matter interactions with solar matter within the framework of **Non-Relativistic Effective Field Theory (NR-EFT)**, with particular emphasis on the evolution of gravitationally captured dark matter particles inside the Sun.

---

## Author

**Sukdev Mahapatra**

M.Sc. Physics — Astroparticle Physics

Ramakrishna Mission Residential College (Autonomous), Narendrapur  
University of Calcutta, India

Research conducted under the supervision of:

**Dr. Divya Sachdeva**  
Indian Institute of Technology Hyderabad, India

---

## Overview

Dark matter particles from the Galactic halo can enter the Solar System and interact with nuclei inside the Sun. If a dark matter particle loses sufficient kinetic energy through scattering, it can become gravitationally bound to the Sun.

The subsequent evolution can be summarized as

\[
\text{Halo Dark Matter}
\rightarrow
\text{Scattering in the Sun}
\rightarrow
\text{Gravitational Capture}
\rightarrow
\text{Initial Bound Orbit}
\rightarrow
\text{Repeated Scattering}
\rightarrow
\text{Thermalization}
\rightarrow
\text{Accumulation in the Solar Core}
\rightarrow
\text{Annihilation}
\rightarrow
\text{Neutrino Production}.
\]

This repository contains the computational work associated with the M.Sc. research project on dark matter capture, orbital evolution, thermalization, annihilation, and neutrino production inside the Sun.

The project studies dark matter interactions with solar matter within the framework of Non-Relativistic Effective Field Theory (NR-EFT).

---

## Scientific Framework

The dark matter–nucleon interaction is described using the **Non-Relativistic Effective Field Theory (NR-EFT)** framework.

The main operators considered in this project are

\[
\mathcal{O}_4,
\qquad
\mathcal{O}_8,
\qquad
\mathcal{O}_{15}.
\]

These operators describe different dependences on spin, velocity, and momentum transfer and therefore lead to different capture and thermalization behavior inside the Sun.

---

## Dark Matter Capture

The dark matter capture rate is calculated by integrating over the radial position inside the Sun, the incoming dark matter velocity, the recoil energy, the solar target number density, and the differential scattering cross section.

The capture rate is written schematically as

\[
C =
4\pi
\int_0^{R_\odot}
dr\,r^2
\int du\,
\frac{f(u)}{u}
w^2
\frac{\rho_\chi}{m_\chi}
\sum_T n_T(r)
\int dE_R\,
\frac{d\sigma_T}{dE_R}.
\]

where

- \(C\) is the dark matter capture rate,
- \(R_\odot\) is the solar radius,
- \(f(u)\) is the halo velocity distribution,
- \(u\) is the dark matter velocity far from the Sun,
- \(w\) is the local dark matter velocity,
- \(\rho_\chi\) is the local dark matter density,
- \(m_\chi\) is the dark matter mass,
- \(n_T(r)\) is the number density of target nucleus \(T\),
- \(E_R\) is the nuclear recoil energy.

The local dark matter velocity inside the Sun is

\[
w(r)
=
\sqrt{
u^2+v_{\rm esc}^2(r)
}.
\]

Here \(v_{\rm esc}(r)\) is the solar escape velocity at radius \(r\).

The capture condition requires that the scattered dark matter particle becomes gravitationally bound to the Sun.

---

## Differential Scattering Cross Section

The differential scattering cross section is calculated using the dark matter response functions and nuclear response functions of the NR-EFT framework.

In general,

\[
\frac{d\sigma}{dE_R}
=
\frac{2m_T}
{(2j_T+1)w^2}
\sum_{\tau,\tau'}
\sum_k
R_k^{\tau\tau'}
(v_T^\perp,q)
W_k^{\tau\tau'}(q).
\]

where

- \(m_T\) is the target nuclear mass,
- \(j_T\) is the target nuclear spin,
- \(w\) is the incoming dark matter–nucleus relative velocity,
- \(q\) is the momentum transfer,
- \(R_k^{\tau\tau'}\) are the dark matter response functions,
- \(W_k^{\tau\tau'}\) are the nuclear response functions.

The momentum transfer is related to the recoil energy by

\[
q=\sqrt{2m_T E_R}.
\]

The indices \(\tau\) and \(\tau'\) denote isoscalar and isovector couplings.

---

## Operator \(\mathcal{O}_4\)

The operator

\[
\mathcal{O}_4
=
\mathbf{S}_\chi
\cdot
\mathbf{S}_N
\]

describes a spin-dependent interaction.

The corresponding differential cross section contains the nuclear spin responses

\[
W_{\Sigma'}
\qquad\text{and}\qquad
W_{\Sigma''}.
\]

The differential cross section can be written as

\[
\frac{d\sigma}{dE_R}
=
\frac{2m_T}
{(2j_T+1)w^2}
\sum_{\tau,\tau'}
\left[
R_{\Sigma'}^{\tau\tau'}
W_{\Sigma'}^{\tau\tau'}
+
R_{\Sigma''}^{\tau\tau'}
W_{\Sigma''}^{\tau\tau'}
\right].
\]

For the targets considered in the thesis calculation, the dominant contribution is associated with hydrogen.

---

## Operator \(\mathcal{O}_8\)

The operator

\[
\mathcal{O}_8
=
\mathbf{S}_\chi
\cdot
\mathbf{v}^{\perp}
\]

introduces a velocity-dependent interaction.

The relevant nuclear response functions include

\[
W_M
\qquad\text{and}\qquad
W_\Delta.
\]

The corresponding differential cross section is

\[
\frac{d\sigma}{dE_R}
=
\frac{2m_T}
{(2j_T+1)w^2}
\sum_{\tau,\tau'}
\left[
R_M^{\tau\tau'}
W_M^{\tau\tau'}
+
R_\Delta^{\tau\tau'}
W_\Delta^{\tau\tau'}
\right].
\]

The velocity dependence of \(\mathcal{O}_8\) modifies the dark matter capture behavior relative to a purely spin-dependent interaction.

---

## Operator \(\mathcal{O}_{15}\)

The operator

\[
\mathcal{O}_{15}
=
-
\left(
\mathbf{S}_\chi
\cdot
\frac{\mathbf{q}}{m_N}
\right)
\left[
\left(
\mathbf{S}_N
\times
\mathbf{v}^{\perp}
\right)
\cdot
\frac{\mathbf{q}}{m_N}
\right]
\]

contains explicit momentum-transfer dependence.

The relevant nuclear response functions include

\[
W_{\Phi''}
\qquad\text{and}\qquad
W_{\Sigma'}.
\]

The differential cross section is

\[
\frac{d\sigma}{dE_R}
=
\frac{2m_T}
{(2j_T+1)w^2}
\sum_{\tau,\tau'}
\left[
R_{\Phi''}^{\tau\tau'}
W_{\Phi''}^{\tau\tau'}
+
R_{\Sigma'}^{\tau\tau'}
W_{\Sigma'}^{\tau\tau'}
\right].
\]

Because of its momentum-transfer dependence, \(\mathcal{O}_{15}\) can produce a different capture behavior compared with \(\mathcal{O}_4\) and \(\mathcal{O}_8\).

---

## Solar Model

The primary solar model used in this project is the **BP2000 Standard Solar Model**.

A comparison with the **AGSS09 solar model** is also included.

The solar model provides the radial dependence of quantities such as

- temperature,
- density,
- enclosed mass,
- hydrogen abundance,
- helium abundance,
- elemental composition.

The tabulated solar profiles are interpolated numerically so that the required quantities can be evaluated at arbitrary radial positions during the capture and orbital calculations.

---

## Solar Targets

For the M.Sc. thesis calculation, the implementation focuses on

\[
\mathrm{H},
\qquad
\mathrm{Fe},
\qquad
\mathrm{P}.
\]

The contribution of each element is calculated separately.

The total capture rate can therefore be written schematically as

\[
C_{\rm total}
=
C_{\rm H}
+
C_{\rm Fe}
+
C_{\rm P}.
\]

For the extended calculation, the implementation can be expanded to include the larger set of solar elements considered in the nuclear-response calculations of Catena and Schwabe.

The 16 solar elements considered in the Catena--Schwabe calculation are

\[
\mathrm{H},
\,{}^3\mathrm{He},
\,{}^4\mathrm{He},
\,{}^{12}\mathrm{C},
\,{}^{14}\mathrm{N},
\,{}^{16}\mathrm{O},
\,{}^{20}\mathrm{Ne},
\,{}^{23}\mathrm{Na},
\,{}^{24}\mathrm{Mg},
\,{}^{27}\mathrm{Al},
\,{}^{28}\mathrm{Si},
\,{}^{32}\mathrm{S},
\,{}^{40}\mathrm{Ar},
\,{}^{40}\mathrm{Ca},
\,{}^{56}\mathrm{Fe},
\,{}^{58}\mathrm{Ni}.
\]

---

## Solar Escape Velocity

The solar escape velocity is calculated from the enclosed solar mass:

\[
v_{\rm esc}(r)
=
\sqrt{
\frac{2GM(r)}{r}
}.
\]

The local velocity of an incoming dark matter particle inside the Sun is

\[
w(r)
=
\sqrt{
u^2+v_{\rm esc}^2(r)
}.
\]

Here \(u\) is the asymptotic dark matter velocity and \(w(r)\) is the local dark matter velocity before scattering.

---

## Initial Semi-Major Axis

After a dark matter particle scatters and becomes gravitationally bound, its orbit can be described by its orbital energy.

The initial semi-major axis is determined from the post-scattering orbital energy.

The capture-weighted mean initial semi-major axis is calculated as

\[
\langle a_0\rangle
=
\frac{1}{C}
\int_0^{R_\odot}
dr
\int dE_R\,
\frac{d^2C}
{dr\,dE_R}
a_0(r,E_R).
\]

The initial semi-major axis provides a measure of the typical orbital scale of a newly captured dark matter particle.

---

## Orbital Evolution

A captured dark matter particle does not necessarily thermalize immediately.

After capture, the particle can continue to cross the solar interior and undergo additional scattering events.

Each scattering event removes part of the orbital energy.

The orbital energy loss can be written schematically as

\[
\Delta E_{\rm orb}(a)
=
\int_{\rm path}
dl
\sum_T n_T(r)
\int dE_R\,
E_R
\frac{d\sigma_T}{dE_R}.
\]

Repeated scattering events gradually reduce the orbital semi-major axis.

The orbital evolution can therefore be represented as

\[
a_0
\rightarrow
a_1
\rightarrow
a_2
\rightarrow
\cdots
\rightarrow
a_{\rm thermal}.
\]

The orbital evolution calculation keeps track of quantities such as

\[
E_{\rm orb},
\qquad
L,
\qquad
r_{\rm peri},
\qquad
r_{\rm apo},
\qquad
a.
\]

where \(E_{\rm orb}\) is the orbital energy, \(L\) is the angular momentum, \(r_{\rm peri}\) is the perihelion distance, \(r_{\rm apo}\) is the apohelion distance, and \(a\) is the semi-major axis.

---

## Monte Carlo Thermalization

The Monte Carlo thermalization calculation is based on the approach developed by Axel Widmark.

Widmark studied WIMP thermalization inside the Sun by following individual WIMP trajectories and scattering events using Monte Carlo integration.

The calculation considers the evolution of captured WIMPs through repeated interactions with solar nuclei.

The quantities followed during the Monte Carlo evolution include

\[
E_{\rm orb},
\qquad
L,
\qquad
r_{\rm peri},
\qquad
r_{\rm apo},
\qquad
a,
\qquad
T_{\rm orbit}.
\]

The recoil energy and scattering probability are also evaluated during the Monte Carlo evolution.

---

## Thermalization

A captured WIMP initially occupies a gravitationally bound orbit that may extend far from the solar core.

Through repeated scattering events, the WIMP loses orbital energy and gradually becomes concentrated toward the solar center.

The thermalized WIMP distribution can be represented schematically by

\[
n_\chi(r)
\propto
\exp
\left[
-\frac{m_\chi\Phi(r)}
{k_B T_c}
\right].
\]

where

- \(m_\chi\) is the dark matter mass,
- \(\Phi(r)\) is the solar gravitational potential,
- \(T_c\) is the solar core temperature,
- \(k_B\) is the Boltzmann constant.

The thermal distribution is determined by the gravitational potential of the Sun and the temperature of the solar core.

---

## Thermalization Time

The thermalization time is the time required for the captured dark matter population to approach thermal equilibrium with the solar interior.

The Monte Carlo calculation follows the orbital evolution until the WIMP reaches the thermalized regime.

The thermalization time depends on quantities such as

\[
m_\chi,
\qquad
\mathcal{O}_i,
\qquad
\sigma,
\qquad
n_T(r),
\qquad
\Phi(r).
\]

The calculation also depends on the adopted solar model.

---

## Annihilation

Once captured dark matter becomes sufficiently concentrated inside the solar core, dark matter particles can annihilate with one another.

The number of captured dark matter particles evolves according to

\[
\frac{dN}{dt}
=
C
-
C_A N^2.
\]

where

- \(C\) is the capture rate,
- \(C_A\) is the annihilation coefficient,
- \(N\) is the number of captured dark matter particles.

The annihilation rate is

\[
\Gamma_A
=
\frac{1}{2}C_A N^2.
\]

The factor of \(1/2\) accounts for the fact that two dark matter particles participate in each annihilation event.

---

## Capture--Annihilation Equilibrium

The solution for the number of captured particles is

\[
N(t)
=
\sqrt{\frac{C}{C_A}}
\tanh
\left(
\sqrt{CC_A}\,t
\right).
\]

The equilibrium condition is approximately

\[
\sqrt{CC_A}\,t_\odot
\gg
1.
\]

where \(t_\odot\) is the age of the Sun.

When equilibrium is reached,

\[
N_{\rm eq}
=
\sqrt{\frac{C}{C_A}},
\]

and therefore

\[
\Gamma_A
\simeq
\frac{C}{2}.
\]

---

## Annihilation Coefficient

The annihilation coefficient can be written as

\[
C_A
=
\frac{\langle\sigma v\rangle}
{V_{\rm eff}},
\]

where \(\langle\sigma v\rangle\) is the thermally averaged annihilation cross section and \(V_{\rm eff}\) is the effective volume of the thermalized dark matter distribution.

The effective volume depends on the dark matter mass and the thermal and gravitational properties of the solar interior.

---

## Neutrino Flux

Dark matter annihilation inside the Sun can produce high-energy neutrinos either directly or through the decay of annihilation products.

A simplified total neutrino flux at Earth can be written as

\[
\Phi_\nu
=
\frac{N_\nu\Gamma_A}
{4\pi D_\odot^2}.
\]

where

- \(N_\nu\) is the number of neutrinos produced per annihilation,
- \(\Gamma_A\) is the dark matter annihilation rate,
- \(D_\odot\) is the Earth--Sun distance.

For the simplified assumption of two neutrinos per annihilation,

\[
\Phi_\nu
=
\frac{2\Gamma_A}
{4\pi D_\odot^2}.
\]

This expression represents a simplified total number flux.

A realistic neutrino prediction requires the neutrino energy spectrum, propagation through the Sun, absorption, interactions, and neutrino oscillations to be included.

---

## Numerical Units

The numerical implementation uses natural units.

The main conversion factors used in the code include

```python
cm_to_GeVinv = 5.07e13
g_to_GeV = 5.62e23
c_light = 3e10
