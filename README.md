# Quantum Simulation Toolkit

A Python-based simulation toolkit for exploring quantum systems such as:

- Single/Two qubit dynamics
- Spin chains
- Quantum phase transitions
## Overview of Simulations
--Single Qubit Driven by Oscillating Field + Decoherence

Time-dependent Hamiltonian: H(t) = H₀ + cos(ωt) σₓ

Simulates Rabi oscillations with and without:

T1 decay (relaxation)

T2 dephasing

#Figure: fig0 — Excited state probability over time

--Bloch Sphere Trajectory

3D visualization of the qubit state’s evolution on the Bloch sphere

Colored by Bloch vector length (purity)

Figure: fig1

--Fidelity with |0⟩ Over Time

Fidelity calculated as overlap with the |0⟩ state

Useful to quantify how close the system stays to the ground state

Figure: fig2

--Rotating Frame Analysis

Projects state onto the rotating |0(t)⟩ basis

Highlights how the rotating frame can simplify dynamics

No saved figure (use .savefig() if needed)

--Two-Qubit Driven System

Coupled 2-qubit Hamiltonian with interaction: J * σₓ ⊗ σₓ

Decoherence applied independently to each qubit

Observables:

⟨1|⟩ projection on each qubit

Von Neumann entropy of reduced density matrix

Figures:

fig3 — Population of each qubit

fig4 — Entropy of qubit 1

--XXZ Spin Chain Dynamics

Simulates a 10-site chain under:

XXZ interactions: σₓσₓ + σᵧσᵧ + Δσ_zσ_z

Local transverse and longitudinal fields

Tracks:

⟨σ_z⟩ per qubit

Entanglement entropy (site 0)

Figures:

fig5 — Time evolution of ⟨σ_z⟩

fig6 — 3D surface of ⟨σ_z⟩ vs qubit & time

--Transverse Ising Model (Dynamics + Ground State)

Hamiltonian: -J Σ σ_z σ_z + h Σ σ_x

Time evolution from random product state

Also calculates mutual information from the ground state

Figures:

fig7 — Mutual info between qubit 0 and others

fig8 — ⟨σ_z⟩ time evolution

--Quantum Phase Transition Detection

Scans transverse field h ∈ [0, 2] for 8-qubit Ising chain

Tracks:

Average magnetization ⟨σ_z⟩, ⟨σ_x⟩

Entanglement entropy of half-chain

Mutual information between qubit 0 and 1

Figures:

fig9 — Magnetization vs h

fig10 — Entropy peak near critical point

fig11 — Mutual information vs h
## Requirements
Python, matplotlib, numpy, qutip
