+++
title = "Corrosion Notes (May 2018)"
date = 2018-05-14T13:25:47+01:00
draft = false

math=true

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["corrosion", "electrochemistry"]
categories = []

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""

+++
As preparation for writing the original grant proposal, Tony Paxton and Andrew
Horsfield put together some notes on their understanding of the definition of
terms used in electrochemistry, and some of the understanding of physics of
corrosion.

Mnemonics and definitions
=========================

-   **OILRIG**: Oxidation Is Loss Reduction Is Gain

-   At an **A**node we have oxid**A**tion

-   At a **C**athode we have redu**C**tion

-   A reduction reaction has the electrons on the left. For example
    $M^{++}+e^{-}\to M^{+}$ is reduction because the oxidation state of
    M(II) is reduced to M(I). Similarly $M\to M^{+}+e^{-}$ is oxidation:
    this happens at the anode during corrosion.

-   A **noble metal** is unreactive and has a large positive standard electrode
    potential. The solid metal is more stable than its aqueous ions.

-   A **base metal** is reactive and has large negative standard electrode
    potential. The solid metal is less stable than its aqueous ions.
    
-   An **ideally polarizable electrode** supports the applied potential without
    allowing any current to flow. It can be thought of as acting like a capacitor.

-   An **ideally non-polarizable electrode** supports a current from the electode
    into the solution with very small applied potentials.

Structure
=========

-   There are several models of the **electrical double layer**

    1.  The **Helmholtz** double layer has a fixed layer of ions

    2.  The **Gouy & Chapman** double layer has point ions that follow Maxwell-Boltzmann
        statistics. The Posson-Boltzmann equation can be linearized in the low concentration
        limit to solve Poisson’s equation.

    3.  The **Stern** double layer combines a fixed layer with a diffuse region.

    4.  The **Grahame** double layer has an Inner Helmholtz Plane (absorbed),
        an Outer Helmholtz Plane, and a diffuse layer.

Equilibrium Thermodynamics
==========================

Corrosion can be described by a series of chemical reactions.

### Standard results from chemistry.

1.  At equilibrium the ratios of the amounts of reactants and products
    can be computed. For a reaction of the form
  
    <div>
    $$n_{1}R_{1}+n_{2}R_{2}+\dots+n_{N}R_{N}\rightleftharpoons m_{1}P_{1}+m_{2}P_{2}+\dots+m_{M}P_{M}\label{eq:N1}$$
    </div>

    we have equilibrium constant $K$ given by

    <div>
    $$K=\frac{\Pi_{j=1}^{M}\left\{ P_{j}\right\} ^{m_{j}}}{\Pi_{i=1}^{N}\left\{ R_{i}\right\} ^{n_{i}}}\label{eq:N2}$$
    </div>

    where $\left\\{ X\right\\}$ is the activity of $X$, and is equal to 1
    under standard conditions ($\left\\{ X\right\\} ^{\ominus}=1$).

1.  Thermodynamic activity is dimensionless and related to concentration by

     <div>$$
     \left\{ X\right\} =\gamma_{X}\frac{\left[X\right]}{\left[X\right]^{\ominus}}
     \label{eq:N3}$$</div>

     where $\gamma\_{X}$ is the activity coefficient. It can also be
     expressed in a similar manner in terms of pressure or mole fraction.

1.  The equilibrium constant can be related to the free energy change for the
    reaction.

    The free energy is stationary at equilibrium, and hence does not change if
    a small amount of the reactants transform into products or vice versa. Thus we
    have $0=\sum\_{j=1}^{M}m_{j}\mu\_{Pu\_{j}}-\sum\_{i=1}^{N}n\_{i}\mu\_{R\_{i}}$ where
    $\mu\_{P\_{j}}$ is the chemical potential for species $P\_{j}$ etc.

1.  Chemical potentials of species vary with their environment according to

    <div>$$
    \mu_{X}=\mu_{X}^{\ominus}+RT\ln\left\{ X\right\} 
    \label{eq:N4}$$</div> 

    where $\mu\_{X}^{\ominus}$ is the chemical potential of $X$ under standard
    conditions.

1.  Substituting the expression for chemical potential into the
    equilibrium condition gives 

    <div>$$\begin{aligned}
    0 & = & \sum_{j=1}^{M}m_{j}\mu_{P_{j}}^{\ominus}-\sum_{i=1}^{N}n_{i}\mu_{R_{i}}^{\ominus}+RT\left(\sum_{j=1}^{M}\ln\left\{ P_{j}\right\} ^{m_{j}}-\sum_{i=1}^{N}\ln\left\{ R_{i}\right\} ^{n_{i}}\right)\\
      & = & \Delta G^{\ominus}+RT\ln\frac{\Pi_{j=1}^{M}\left\{ P_{j}\right\} ^{m_{j}}}{\Pi_{i=1}^{N}\left\{ R_{i}\right\} ^{n_{i}}}
    \end{aligned}$$</div>

    where $\Delta G^{\ominus}=\sum\_{j=1}^{M}m\_{j}\mu\_{P\_{j}}^{\ominus}-\sum\_{i=1}^{N}n\_{i}\mu\_{R\_{i}}^{\ominus}$.

    This can be rearranged to give 

    <div>$$
    K=\frac{\Pi_{j=1}^{M}\left\{ P_{j}\right\}
    ^{m_{j}}}{\Pi_{i=1}^{N}\left\{ R_{i}\right\} ^{n_{i}}}=\exp\left(-\frac{\Delta
    G^{\ominus}}{RT}\right)
    \label{eq:N5}$$</div>

### Nernst Equation

The Nernst equation is a statement about equilibrium for half reactions.
Consider the reaction $$M^{z+}+ze^{-}\rightleftharpoons M\label{eq:N5.1}$$ At
equilibrium the change of Gibbs free energy is zero if you go forwards or
backwards. Thus we have $$\mu\_{M^{z+}}+z\mu\_{e}-\mu\_{M}=0\label{eq:N5.2}$$ 
If we substitute Eq. \[eq:N4\] into Eq. \[eq:N5.2\] we get 

<div>
$$\begin{aligned} 
0 & = & \mu\_{M^{z+}}^{\ominus}+RT\ln\left\{ M^{z+}\right\}
+z\left(\mu\_{e}^{\ominus}+\Delta\mu\_{e}\right)-\mu\_{M}^{\ominus}-RT\ln\left\{
M\right\} \nonumber \\ 
& = & \Delta G^{\ominus}+RT\ln\frac{\left\{M^{z+}\right\} }{\left\{ M\right\} }+z\Delta\mu\_{e}
\label{eq:N6}
\end{aligned}$$
</div>

where $\Delta G^{\ominus}=\mu\_{M^{z+}}^{\ominus}+z\mu\_{e}^{\ominus}-\mu\_{M}^{\ominus}$.

The electron chemical potential $\mu_{e}^{\ominus}$ is not defined uniquely by
the standard conditions. Thus we will add the condition that the system be in
equilibrium; this condition can always be met by providing enough $M$ and
$M^{z+}$ under standard conditions such that the electron reservoir (electrode)
is charged to the point that equilibrium is established. Note that this means
that, provided the electrode is metallic and sufficiently inert, it does not
matter what material is chosen. Once we reach equilibrium, we have $\Delta
G^{\ominus}=0$, and hence

<div>
$$\mu_{e}^{\ominus}=\frac{1}{z}\left(\mu_{M}^{\ominus}-\mu_{M^{z+}}^{\ominus}\right)\label{eq:N7}$$
</div>

This corresponds to the standard electrode potential $E^{\ominus}$ through
$\mu\_{e}^{\ominus}=-FE^{\ominus}$, where $F$ is a Faraday.  

Rearranging Eq.
\[eq:N6\] we then get the Nernst equation 

<div>
$$\begin{aligned}
    \mu_{e} & = & \mu_{e}^{\ominus}-\frac{RT}{z}\ln\frac{\left\{ M^{z+}\right\} }{\left\{ M\right\} }\label{eq:N8}\\
    E & = & E^{\ominus}-\frac{RT}{zF}\ln\frac{\left\{ M\right\} }{\left\{ M^{z+}\right\} }\label{eq:N8.1}\end{aligned}$$
</div>

### The Standard Hydrogen Electrode (SHE)

The Standard Hydrogen Electrode is characterized by the equilibrium
$H^{+}+e^{-}\rightleftharpoons\frac{1}{2}H\_{2}$ with pH 0, $P\_{H\_{2}}=1$ bar,
and $T=298$ K. Thus $\mu\_{e}=\frac{1}{2}\mu\_{H\_{2}}-\mu\_{H^{+}}$. 

The corresponding potential is in the range 4.44 V to 4.85 V relative to
vacuum.

Consider two half reactions 

<div> 
$$\begin{aligned} M_{1}^{z_{1}+}+z_{1}e^{-} & \rightleftharpoons
& M_{1}\nonumber \\ M^{z_{2}+}+z_{2}e^{-} & \rightleftharpoons
& M_{2}\label{eq:N9}\end{aligned}$$ 
</div>

with associated standard electrode potentials $E\_{1}$ and $E\_{2}$.  Now suppose
we allow electrons to flow from the electrode for $M\_{1}$ to the electrode for
$M\_{2}$. The free energy change per mole of electrons is then $\Delta
G=F\left(E\_{1}-E\_{2}\right)$. If $E\_{1}>E\_{2}$ then $\Delta G>0$, and it is
favourable for the electrons to flow the other way (from 2 to 1). Similarly, if
$E\_{1}<E\_{2}$ it is energetically favourable for the electrons to flow from
1 to 2. In short, electrons flow from the electrode with more negative
potential to the one with more positive (as expected).  Applying Le Chatelier’s
principle, that means coupling two electrodes will cause the reaction with the
more negative potential to proceed in the oxidising direction (mnemonic: NO),
while the one with the more positive potential will proceed in the reducing
direction (mnemonic: PR).

### Pourbaix Diagrams
These are phase diagrams displaying the most stable species as
a function of electrode potential ($\mu\_{e}=-FE$) and pH.  The phase boundary
lines are derived from the equation of chemical equilibrium. For example, for
the equilibrium $Mg^{++}+2H^{+}+4e^{-}\rightleftharpoons MgH\_{2}$ we have
$\mu\_{Mg^{++}}+2\mu\_{H^{+}}+4\mu\_{e}=\mu\_{MgH\_{2}}$. 

Hence,

<div>
$\mu\_{e}=\frac{1}{4}\left(\mu\_{MgH\_{2}}-\mu\_{Mg^{++}}\right)-\frac{1}{2}\mu\_{H^{+}}\\

\approx\frac{1}{4}\left(\mu\_{MgH\_{2}}-\mu\_{Mg^{++}}-2\mu\_{H^{+}}^{\ominus}\right)+\frac{2.303}{2}RTpH$.
</div>

The voltage is given by $\mu\_{e}=\mu\_{e,ref}-FE$.

Kinetics
========

The **Butler-Volmer** equation:

<div>
$i=i_{0}\left\{ \exp\left(\frac{\alpha_{a}zF\eta}{RT}\right)-\exp\left(-\frac{\alpha_{c}zF\eta}{RT}\right)\right\}$
</div>

For large positive (or negative) overpotential we get the **Tafel** equation

<div>
$$\begin{aligned} i & \approx
& i_{0}\exp\left(\frac{\alpha_{a}zF\eta}{RT}\right)\\ \Rightarrow\ln
i & \approx & \ln i_{0}+\left(\frac{\alpha_{a}zF}{RT}\right)\eta\end{aligned}$$
</div>

**Faraday’s law** $$\frac{m}{M}=\frac{Q}{nF}$$ where $m$ is the mass of substance
produced at an electrode, $Q$ is the total charge delivered to the system, $F$
is Faraday’s constant, $M$ is the molar mass of the substance, and $n$ is the
charge per ion.

At fixed overpotential, the total measured current must equal the net rate of
electron transfer to or from the electrode (to avoid a change in net charge).

Potentials
==========

Galvani potential $\phi$
: Electric potential inside the conductor

Volta potential $\psi$
: Electric potential at point $p$ just outside the interface, in vacuum.

Dipole potential $\chi$
: Electric potential difference between the point $p$ and inside: $\chi=\phi-\psi$

Chemical potential $\mu$
: $\mu=\mu^{0}+kT\ln a$

Electrochemical potential $\tilde{\mu}$
: Work done in taking particle from infinity to the interior of the phase. $\tilde{\mu}=\mu+q\phi$

Real potential $\alpha$
: Work done in taking particle from inside the phase to point $p$ just outside.
$\alpha=\tilde{\mu}-q\psi=\mu+q\chi$. Also $\alpha=\alpha^{0}+kT\ln a$ where $\alpha^{0}=\mu^{0}+q\chi$

Work function $W$
: $W=\tilde{\mu}^{g,0}-\tilde{\mu}^{0}=\mu^{g,0}-\alpha^{0}=\mu^{g,0}-\mu^{0}-q\chi$

Potential of Zero Charge
: The value of the electrode potential such that the electrode surface has zero charge

$q$ is the charge of the particle.
Note that the point $p$ is always in vacuum.

H formation by Mg in aqueous solution
=====================================

Let a piece of pure Mg with a perfectly clean surface be placed in a
beaker of pure water. The Mg can dissolve into the water according to

<div>
$$Mg_{(s)}\rightleftharpoons Mg_{(aq)}^{++}+2e^{-}\label{eq:RMg}$$
</div>

This results in the accumulation of electrons in the solid Mg, lowering
its potential (making it more cathodic). The standard electrode
potential is -2.38 V. These electrons are free to participate in a
second reaction

<div>
$$2H_{2}O+2e^{-}\rightleftharpoons H_{2}+2OH^{-}\label{eq:RH}$$ 
</div>

Thus the
dissolution of Mg enables the reduction of water to form hydrogen gas.
The removal of electrons from the solid Mg by reaction \[eq:RH\] pulls
reaction \[eq:RMg\] to the right, resulting in further dissolution of
g. This in turn produces more electrons, pulling reaction \[eq:RH\] to
the right as well. Thus the two reactions support each other, resulting
in the steady formation of hydrogen and dissolution of Mg.

The hydroxide ions can combine with Mg ions to form insoluble magnesium
hydroxide which has the hexagonal hP3 structure (space group
P$\bar{3}$m1 No. 164, lattice constants a = 0.312 nm, c = 0.473 nm)

<div>
$$Mg_{(aq)}^{++}+2OH_{(aq)}^{-}\rightleftharpoons Mg(OH)_{2(s)}\label{eq:RMgOH2}$$
</div>

This removes both $Mg^{++}$ and $OH^{-}$ from solution, further
encouraging the forward reactions, unless the hydroxide forms a
passivating layer.

We can quantify the above somewhat by reference to Eq. \[eq:N5\]we

<div>
$$\begin{aligned}
\left\{ Mg_{(aq)}^{++}\right\}  & = & \frac{K_{Mg}\left\{ Mg_{(s)}\right\} }{\left\{ e^{-}\right\} ^{2}}\label{eq:E1}\\
\left\{ OH^{-}\right\} ^{2} & = & \frac{K_{H}\left\{ H_{2}O\right\} ^{2}\left\{ e^{-}\right\} ^{2}}{\left\{ H_{2}\right\} }\label{eq:E2}\\
\left\{ Mg_{(aq)}^{++}\right\} \left\{ OH^{-}\right\} ^{2} & = & \frac{K_{Mg}K_{H}\left\{ H_{2}O\right\} ^{2}\left\{ Mg_{(s)}\right\} }{\left\{ H_{2}\right\} }\label{eq:E3}\\
 & = & \frac{\left\{ Mg\left(OH\right)_{2(s)}\right\} }{K_{Mg(OH)_{2}}}\label{eq:E4}\end{aligned}$$
 </div>

From Eq. \[eq:N4\] we have

<div>
$$\left\{ e^{-}\right\} =\exp\left(\frac{\mu_{e}-\mu_{e}^{\ominus}}{RT}\right)\doteq\exp\left(\frac{-FE}{RT}\right)\label{eq:mue}$$
</div>

Substituting Eq. \[eq:mue\] into Eqs. \[eq:E1\] and \[eq:E2\] then gives

<div>
$$\begin{aligned}
\left\{ Mg_{(aq)}^{++}\right\}  & = & K_{Mg}\left\{ Mg_{(s)}\right\} \exp\left(\frac{2FE}{RT}\right)\\
\left\{ OH^{-}\right\} ^{2} & = & \frac{K_{H}\left\{ H_{2}O\right\} ^{2}}{\left\{ H_{2}\right\} }\exp\left(\frac{-2FE}{RT}\right)\end{aligned}$$
</div>

from which we see that a more positive potential (anodic) encourages
formation of $Mg^{++}$ while a more negative potential (cathodic)
encourages $OH^{-}$ formation.

In the negative difference effect we find more hydrogen gas being
produced at anodic potentials, which contradicts the results above. From
Eq. \[eq:E3\] we see that increasing 

<div>
$\left\{ Mg\_{(aq)}^{++}\right\}$
</dev>

will decrease 

<div>
$\left\{ OH^{-}\right\}$
</div>

as the solid hydroxide
precipitates out. This in turn will pull reaction \[eq:RH\] to the right
(there will be more $H^{+}$ ions in solution), resulting in more
hydrogen production.

