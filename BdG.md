- [Cooper pairs in BCS](#cooper-pairs-in-bcs)
  - [Cooper Pair Operator Expression](#cooper-pair-operator-expression)
  - [BCS Ground State](#bcs-ground-state)
- [Bogoliubov Transformation](#bogoliubov-transformation)
  - [Intuition Behind It](#intuition-behind-it)
  - [Physical Meaning](#physical-meaning)
- [Entanglement](#entanglement)
  - [**Cooper pairs are entangled**, both **in spin** and **momentum**.](#cooper-pairs-are-entangled-both-in-spin-and-momentum)
    - [1. Spin Entanglement](#1-spin-entanglement)
    - [2. Momentum Correlation](#2-momentum-correlation)
    - [3. Overall Wavefunction](#3-overall-wavefunction)
      - [Summary](#summary)
  - [The **BCS condensate is entangled**, but the nature of the entanglement is subtle and depends on how you define and probe it.](#the-bcs-condensate-is-entangled-but-the-nature-of-the-entanglement-is-subtle-and-depends-on-how-you-define-and-probe-it)
    - [1. Entanglement Within a Cooper Pair](#1-entanglement-within-a-cooper-pair)
    - [2. Entanglement in the BCS Ground State](#2-entanglement-in-the-bcs-ground-state)
    - [3. Type of Entanglement](#3-type-of-entanglement)
      - [Summary](#summary-1)
  - [Superpositions of electron and hole states](#superpositions-of-electron-and-hole-states)
    - [Bogoliubov Quasiparticle States](#bogoliubov-quasiparticle-states)
    - [At the Fermi Wavevector $k = k\_F$](#at-the-fermi-wavevector-k--k_f)
    - [Physical Interpretation](#physical-interpretation)
    - [What Are Coherence Peaks?](#what-are-coherence-peaks)
    - [Origin of Coherence Peaks](#origin-of-coherence-peaks)
    - [Why "Coherence"?](#why-coherence)
      - [Summary](#summary-2)

# Cooper pairs in BCS
In BCS theory, a **Cooper pair** can be described using **creation and annihilation operators** in the second quantization formalism. Here's how it's typically represented:

---

## Cooper Pair Operator Expression

A Cooper pair consists of two electrons with opposite momenta and opposite spins. The **pair creation operator** is written as:

$$
b^\dagger_{\mathbf{k}} = c^\dagger_{\mathbf{k}\uparrow} c^\dagger_{-\mathbf{k}\downarrow}
$$

- $c^\dagger_{\mathbf{k}\uparrow}$: creates an electron with momentum $\mathbf{k}$ and spin up.
- $c^\dagger_{-\mathbf{k}\downarrow}$: creates an electron with momentum $-\mathbf{k}$ and spin down.

This operator creates a **Cooper pair** in the state $(\mathbf{k}, \uparrow; -\mathbf{k}, \downarrow)$.

---

## BCS Ground State

The BCS ground state is a **coherent superposition** of states with different numbers of Cooper pairs. It can be written as:

$$
|\text{BCS}\rangle = \prod_{\mathbf{k}} \left( u_{\mathbf{k}} + v_{\mathbf{k}} c^\dagger_{\mathbf{k}\uparrow} c^\dagger_{-\mathbf{k}\downarrow} \right) |0\rangle
$$

- $u_{\mathbf{k}}$ and $v_{\mathbf{k}}$ are variational parameters satisfying $|u_{\mathbf{k}}|^2 + |v_{\mathbf{k}}|^2 = 1$.
- $|0\rangle$ is the vacuum state (no electrons).
- The term $c^\dagger_{\mathbf{k}\uparrow} c^\dagger_{-\mathbf{k}\downarrow}$ creates a Cooper pair.

This form shows that the ground state is a **condensate of Cooper pairs**, with each pair being a quantum superposition of occupied and unoccupied states.

---
# Bogoliubov Transformation

The **Bogoliubov transformation** is a mathematical tool used in quantum many-body physics, especially in **BCS theory of superconductivity**, to describe how the system's elementary excitations (quasiparticles) are mixtures of electron and hole states.

## Intuition Behind It

In a superconductor, the ground state is not simply a filled Fermi sea of electrons. Instead, due to the pairing interaction, the true excitations are **quasiparticles** that are **superpositions of electron and hole states**. The Bogoliubov transformation allows us to diagonalize the BCS Hamiltonian and describe these quasiparticles.

---

Let’s denote:

- $c_{\mathbf{k}\uparrow}$: annihilation operator for an electron with momentum $\mathbf{k}$ and spin up.
- $c_{-\mathbf{k}\downarrow}^\dagger$: creation operator for an electron with momentum $-\mathbf{k}$ and spin down.

The Bogoliubov transformation introduces new quasiparticle operators:

$$
\begin{aligned}
\gamma_{\mathbf{k}\uparrow} &= u_{\mathbf{k}} c_{\mathbf{k}\uparrow} - v_{\mathbf{k}} c_{-\mathbf{k}\downarrow}^\dagger \\
\gamma_{-\mathbf{k}\downarrow}^\dagger &= v_{\mathbf{k}} c_{\mathbf{k}\uparrow} + u_{\mathbf{k}} c_{-\mathbf{k}\downarrow}^\dagger
\end{aligned}
$$

Here:

- $\gamma_{\mathbf{k}\uparrow}$ and $\gamma_{-\mathbf{k}\downarrow}^\dagger$ are **quasiparticle operators**.
- $u_{\mathbf{k}}$ and $v_{\mathbf{k}}$ are **coherence factors**, satisfying $|u_{\mathbf{k}}|^2 + |v_{\mathbf{k}}|^2 = 1$.

These coefficients depend on the energy of the state and the superconducting gap $\Delta$, typically:

$$
u_{\mathbf{k}}^2 = \frac{1}{2} \left( 1 + \frac{\xi_{\mathbf{k}}}{E_{\mathbf{k}}} \right), \quad
v_{\mathbf{k}}^2 = \frac{1}{2} \left( 1 - \frac{\xi_{\mathbf{k}}}{E_{\mathbf{k}}} \right)
$$

where:

- $\xi_{\mathbf{k}} = \epsilon_{\mathbf{k}} - \mu$ is the energy relative to the Fermi level.
- $E_{\mathbf{k}} = \sqrt{\xi_{\mathbf{k}}^2 + \Delta^2}$ is the quasiparticle energy.

---

## Physical Meaning

- The quasiparticles $\gamma$ are **not pure electrons or holes**, but **quantum mixtures**.
- This transformation is crucial for understanding how superconductors behave, especially how they respond to perturbations and how the energy gap arises.

---
# Entanglement

## **Cooper pairs are entangled**, both **in spin** and **momentum**.

### 1. Spin Entanglement
A typical Cooper pair in conventional superconductors (like in BCS theory) is in a **spin singlet state**, which is maximally entangled:

$$
|\psi_{\text{spin}}\rangle = \frac{1}{\sqrt{2}} \left( |\uparrow\rangle_1 |\downarrow\rangle_2 - |\downarrow\rangle_1 |\uparrow\rangle_2 \right)
$$

This state is antisymmetric under exchange and represents perfect quantum entanglement of the two electron spins.

### 2. Momentum Correlation
The electrons in a Cooper pair have **opposite momenta**: $\mathbf{k}$ and $-\mathbf{k}$. This correlation is also a form of entanglement in the momentum basis, though not necessarily maximal in the same sense as spin entanglement.

### 3. Overall Wavefunction
The total wavefunction of a Cooper pair is:

$$
|\Psi\rangle = \sum_{\mathbf{k}} \phi(\mathbf{k}) c^\dagger_{\mathbf{k}\uparrow} c^\dagger_{-\mathbf{k}\downarrow} |0\rangle
$$

This is a **superposition** over many momentum states, and the pairing amplitude $\phi(\mathbf{k})$ encodes the spatial and momentum structure of the entanglement.

---

#### Summary
- Cooper pairs are **entangled quantum states**.
- The entanglement is **essential** for superconductivity—it allows the pairs to form a coherent condensate.
- This entanglement is **nonlocal**, meaning the electrons can be spatially separated yet still correlated.

## The **BCS condensate is entangled**, but the nature of the entanglement is subtle and depends on how you define and probe it.

---

### 1. Entanglement Within a Cooper Pair

Each **Cooper pair** is formed by two electrons with opposite momenta and spins:

$$
|\psi_{\text{pair}}\rangle = \frac{1}{\sqrt{2}} \left( |\mathbf{k}, \uparrow; -\mathbf{k}, \downarrow\rangle - |\mathbf{k}, \downarrow; -\mathbf{k}, \uparrow\rangle \right)
$$

This is a **spin singlet state**, which is **maximally entangled** in spin. So **each Cooper pair is entangled** in spin and momentum.

---

### 2. Entanglement in the BCS Ground State

The full BCS ground state is:

$$
|\text{BCS}\rangle = \prod_{\mathbf{k}} \left( u_{\mathbf{k}} + v_{\mathbf{k}} c^\dagger_{\mathbf{k}\uparrow} c^\dagger_{-\mathbf{k}\downarrow} \right) |0\rangle
$$

This is a **many-body quantum state** that is a **coherent superposition** of different numbers of Cooper pairs. It exhibits **global entanglement** across momentum modes. The occupation of one mode is correlated with the occupation of its time-reversed partner.

This means:
- The state is **not separable** across momentum modes.
- It contains **quantum correlations** between different parts of the system.
- It is **entangled in the Fock space** representation.

---

### 3. Type of Entanglement

- **Mode entanglement**: Between $\mathbf{k}$ and $-\mathbf{k}$ modes.
- **Particle entanglement**: Between the two electrons in a Cooper pair.
- **Global entanglement**: Across the entire condensate.

---

#### Summary

- **BCS** condensate is entangled.
- **Each Cooper pair** is entangled in spin and momentum.
- The **BCS ground state** is a highly entangled many-body state, both in terms of particle and mode entanglement.

## Superpositions of electron and hole states

At the **Fermi wavevector** $k_F$, the **Bogoliubov quasiparticles** in BCS theory exhibit a particularly interesting character: they are **equal superpositions of electron and hole states**.

---

### Bogoliubov Quasiparticle States

The Bogoliubov quasiparticle operators are defined as:

$$
\gamma_{\mathbf{k}\uparrow} = u_{\mathbf{k}} c_{\mathbf{k}\uparrow} - v_{\mathbf{k}} c^\dagger_{-\mathbf{k}\downarrow} \\
\gamma_{-\mathbf{k}\downarrow} = u_{\mathbf{k}} c_{-\mathbf{k}\downarrow} + v_{\mathbf{k}} c^\dagger_{\mathbf{k}\uparrow}
$$

Here:
- $c_{\mathbf{k}\sigma}$: annihilates an electron with momentum $\mathbf{k}$ and spin $\sigma$
- $u_{\mathbf{k}}, v_{\mathbf{k}}$: coherence factors, satisfying $|u_{\mathbf{k}}|^2 + |v_{\mathbf{k}}|^2 = 1$

---

### At the Fermi Wavevector $k = k_F$

At the Fermi surface, the energy $\xi_{\mathbf{k}} = \varepsilon_{\mathbf{k}} - \mu$ vanishes, so:

$$
u_{k_F} = v_{k_F} = \frac{1}{\sqrt{2}}
$$

This means the quasiparticle becomes:

$$
\gamma_{k_F\uparrow} = \frac{1}{\sqrt{2}} \left( c_{k_F\uparrow} - c^\dagger_{-k_F\downarrow} \right)
$$

This is a **50/50 mixture of an electron and a hole**, i.e., a **maximally mixed quasiparticle**.

---

### Physical Interpretation

- **Electron-like far above $k_F$**: $u_k \to 1, v_k \to 0$
- **Hole-like far below $k_F$**: $u_k \to 0, v_k \to 1$
- **Equal mix at $k_F$**: quasiparticles are **neither purely electron nor hole**, but a **quantum superposition**.

This mixed character is crucial for phenomena like **Andreev reflection**, **tunneling spectroscopy**, and the **energy gap** in superconductors.

---

the **coherence peaks** observed in **scanning tunneling microscopy (STM)** of superconductors are directly related to the **Bogoliubov quasiparticles**, especially their behavior near the **Fermi wavevector**.

---

### What Are Coherence Peaks?

In STM measurements of a superconductor, the **differential conductance** $dI/dV$ as a function of bias voltage $V$ reflects the **local density of states (LDOS)**. In a conventional BCS superconductor, this LDOS shows:

- A **gap** around zero bias (no states between $-\Delta$ and $+\Delta$)
- **Sharp peaks** at energies $\pm \Delta$: these are the **coherence peaks**

---

### Origin of Coherence Peaks

These peaks arise from the **singularities in the density of states** due to the BCS quasiparticle dispersion:

$$
E_{\mathbf{k}} = \sqrt{\xi_{\mathbf{k}}^2 + \Delta^2}
$$

At the Fermi surface ($\xi_{\mathbf{k}} = 0$), the quasiparticle energy is exactly $\Delta$, and the **Bogoliubov quasiparticles** are **equal mixtures of electron and hole states**. This mixing leads to **enhanced tunneling probability**, which manifests as coherence peaks.

---

### Why "Coherence"?

The term "coherence" refers to the **quantum coherence** of the superconducting state:
- The quasiparticles are **not purely electron or hole**, but **coherent superpositions**.
- The peaks reflect the **constructive interference** in the tunneling process due to this coherence.

---

#### Summary

- Bogoliubov quasiparticles at the Fermi wavevector are responsible for the **coherence peaks** in STM.
- These peaks are a hallmark of the **superconducting gap** and the **quantum coherence** of the paired state.