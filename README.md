# Ferdin Joe John Joseph, Ph.D. — Quantum Computing, built from the maths up

**Quantum Research · Quantum Software Development · Quantum Pre-sales & Solutions Architecture**

| Reach me | |
|---|---|
| **Email** (fastest, and preferred) | [ferdinjoe@gmail.com](mailto:ferdinjoe@gmail.com) |
| **LinkedIn** | [linkedin.com/in/ferdinjoe](https://www.linkedin.com/in/ferdinjoe/) |
| **Phone** | available on request — send an email or a LinkedIn message and I will send it straight back |

> **For the recruiter or hiring manager reading this in a queue of profiles:** every claim in this
> repository is a number produced by code in the same file, checked against an independent library
> where one exists, and re-verified on 9 November 2026 in two modes — all fifteen notebooks run with
> the reference libraries **blocked** (15/15 clean, 4,077 self-test assertions passing) and with them
> **installed** (15/15 clean, 4,182 assertions passing, zero failures in both). There are no
> screenshots, no pre-baked outputs and no library call presented as an achievement. If your quantum
> programme needs someone who can prototype an algorithm, price it against a real device's error
> budget, and then stand in front of the
> customer's technical team and explain what the number means — that is the three-part profile this
> portfolio is built to demonstrate, and I would like 30 minutes to show it live.

*Keywords for searching: quantum computing, quantum algorithms, Grover, Shor, QFT, quantum phase
estimation, VQE, QAOA, Max-Cut, QUBO, Ising Hamiltonian, quantum chemistry, Jordan–Wigner, ansatz,
parameter-shift, quantum machine learning, quantum kernels, QNN, QGAN, BB84, quantum key distribution,
QEC, stabiliser codes, surface code, NISQ, randomised benchmarking, gate-set tomography, error
mitigation, hybrid quantum-classical, trapped-ion QPU, IonQ, quantum application engineering, proof of
value, classical baseline comparison, Qiskit, PennyLane, PySCF, dimod, scikit-learn, NumPy, Python,
Google Colab, cloud architecture, solutions architecture, pre-sales, technical account management.*

---

## Where to start

| You have | Open |
|---|---|
| 60 seconds | This page, then [Bell_Inequality.ipynb](Bell_Inequality.ipynb) — scroll to its recap. |
| 15 minutes | [The three-minute version](#the-three-minute-version-by-what-you-are-hiring-for), then [the portfolio table](#the-portfolio). |
| A live technical screen | Any notebook + `Runtime ▸ Run all`. The last cell prints its own verdict. |

---

## Why this repository exists

Fifteen self-contained notebooks that build the working parts of a quantum stack from first
principles in plain NumPy — statevector engines, gates, oracles, cost Hamiltonians, ansätze,
gradient rules, noise channels, decoders, key-sifting protocol machinery, a gate-level instruction
list that compiles down to a trapped-ion device's native operations — and then check every one of
them against an independent reference implementation (Qiskit, PennyLane, PySCF, dimod,
scikit-learn) where a reference exists.

Nothing here is a tutorial wrapper around a library. Every quantity a reader might want to argue
about is *computed* in this repository, printed with its tolerance, and asserted. Where a reference
library and my code disagree, the notebook says so and quantifies the disagreement instead of
quietly rounding it away.

**The measure of the work, counted mechanically across the fifteen files:**

| What | Measured |
|---|---|
| Notebooks | 15 |
| Cells | 602 (264 explanatory markdown / 338 code) |
| Code lines, all hand-written | 23,923 (every line of every code cell, blanks included; 21,621 of them are non-blank) |
| Figures generated | 120 on the library-free path, 123 when the reference libraries are present |
| Self-test assertions that pass | **4,077** library-free, **4,182** with the reference libraries present (each notebook's own suite; the external-library comparisons are counted separately in the table below) |
| Self-test assertions that fail | **0** in either mode |
| External dependency required to run the core | **none** — NumPy and matplotlib only |
| Runtime | `Runtime ▸ Run all` in Google Colab; each file is a single `.ipynb`, no data files, no setup |
| Slowest measured full run (library-free core path) | `Noise_Benchmarking` 131.5 s, then `Quantum_GAN` 81.5 s, `QAOA_MaxCut` 73.8 s, `IonQ_QAOA_MaxCut` 62.8 s, `Bell_Inequality` 49.3 s, `Quantum_Neural_Network` 45.3 s; the other nine all finish inside 30 s and two inside 3 s. Measured serially, one notebook at a time, with nothing else running, by executing every code cell of the delivered file. Repeat passes on this machine agree to about ±5% (the pass before this one put Noise at 129.0 s and IonQ at 60.9 s), so read these as this laptop's timings, not a specification. The whole fifteen-notebook batch runs end-to-end in **553 s (9.2 min)** of code-cell time library-free and **592 s (9.9 min)** with the reference libraries installed; Colab adds package-install time on top for the optional cross-check sections. Five notebooks (`Hybrid_Quantum_Cloud`, `Noise_Benchmarking`, `Quantum_GAN`, `Quantum_Kernel_SVM`, `VQE_Molecular_Ground_State`) print their own elapsed time; the other ten are timed by the harness around them |

Every notebook ships with its output cells stripped, so what you see when you run it is the run, not
a screenshot of one.

### Portfolio at a glance

**Areas:** quantum algorithms (Grover, Shor, QFT/QPE, QAOA, VQE) · quantum machine learning
(parameter-shift, quantum kernels, QNN, QGAN) · quantum communication (BB84, privacy amplification,
information-theoretic security) · error correction and mitigation (stabiliser/CSS codes, syndrome
decoding, surface-code thresholds, ZNE, readout mitigation) · NISQ device characterisation (randomised
benchmarking, gate-set tomography, RBE, `T1`/`T2`/readout error budgets) · hybrid quantum-classical
platform engineering (job queues, retries, provider SDK abstraction, cost accounting) · quantum
chemistry (Gaussian integrals, Hartree–Fock, Jordan–Wigner transform, Pauli strings, frozen orbitals) ·
QPU application engineering (business problem → QUBO → cost Hamiltonian → native gate payload →
ideal / noisy / hardware tiers → price and latency per answer → verdict against a classical
baseline).

**Tools and libraries this code is verified against:** Python, NumPy, SciPy, matplotlib, Qiskit,
qiskit-ionq, PennyLane, PySCF, dimod, scikit-learn, Google Colab. Primary language for the
from-scratch core: NumPy only.

**What a reviewer should take away:** I build the thing before I use the library, I measure the
agreement between the two, and I publish the number that is less flattering.

### For a non-technical reader

You do not need to follow the maths to check the claim. Open any notebook in Google Colab, press
**Run all**, and look for the line that says how many self-tests passed. Fifteen notebooks, more than
four thousand such checks, zero failures — and every external library comparison is printed with its
error, including the ones that were not perfect. If you are matching against a job description, the
table under *The portfolio* names the sub-field each file covers, so the JD keywords map one to one.

### If you are matching a job description

Hand me the JD and I will do this properly, but the short map is:

| Your requirement | The evidence |
|---|---|
| Quantum algorithm design / implementation | `Grovers_Search`, `QFT_Phase_Estimation`, `Shors_Algorithm`, `QAOA_MaxCut` |
| Quantum chemistry or optimisation applications | `VQE_Molecular_Ground_State`, `QAOA_MaxCut`, `IonQ_QAOA_MaxCut` |
| Real-device (QPU) application engineering, PoC scoping against hardware | `IonQ_QAOA_MaxCut` — QUBO → cost Hamiltonian → native gate payload → ideal / noisy / hardware tiers, priced per answer |
| Error correction, fault tolerance, logical qubits | `Quantum_Error_Correction` |
| Device characterisation, NISQ performance claims | `Noise_Benchmarking`, and the noise sections inside every other notebook |
| Quantum machine learning | `Quantum_Neural_Network`, `Quantum_GAN`, `Quantum_Kernel_SVM` |
| Quantum security / QKD | `BB84_Quantum_Key_Distribution`, `Bell_Inequality` |
| Hybrid quantum-classical platform or cloud integration | `Hybrid_Quantum_Cloud` |
| Customer-facing technical work, proposals, PoC scoping | all fifteen, plus the professional background at the end of this file |

---

## Run it in sixty seconds (no install, no account setup beyond Google)

1. Go to [colab.research.google.com](https://colab.research.google.com/) ▸ **Upload notebook** ▸
   drag in any `.ipynb` from this folder.
2. **Runtime ▸ Change runtime type ▸ Hardware accelerator: None** ▸ **Runtime ▸ Run all**.
3. Scroll to the last code cell: it prints the self-test tally (e.g. `all 94 checks passed`,
   `self-tests: 282 passed, 0 failed`). If anything failed, the cell would have raised instead.

The explanatory markdown is interleaved, so a non-running reader can still follow the argument cell
by cell — every figure and number quoted in prose is produced by the cell above it.

---

## The three-minute version, by what you are hiring for

**Hiring a research scientist?** Start with
[`Bell_Inequality.ipynb`](Bell_Inequality.ipynb) and
[`VQE_Molecular_Ground_State.ipynb`](VQE_Molecular_Ground_State.ipynb). Bell is not a demo of
`cos²θ`; it derives the CHSH operator from coincidence projectors, finds the violating settings per
Bell state by search, and then shows that `Ŝ > 2` proves nothing on its own — a local source sitting
exactly on the bound lands above it in about half of all runs at *any* shot count, while the
significance `(Ŝ−2)/σ` grows with `N` only when there is a real violation. VQE goes from Gaussian
integrals to a measured molecular ground state and cross-checks the Hamiltonian against **two**
independent chemistry engines, with the residual gap attributed rather than hidden.

**Hiring a quantum software engineer?** Open
[`QAOA_MaxCut.ipynb`](QAOA_MaxCut.ipynb), [`Grovers_Search.ipynb`](Grovers_Search.ipynb) and
[`Quantum_Error_Correction.ipynb`](Quantum_Error_Correction.ipynb). These contain the things that
break in production: exact parameter-shift gradients versus finite differences versus the "textbook"
formula that is actually wrong for non-commuting terms (`1.78e-09` against finite differences,
`1.225` for the textbook version — a real trap, demonstrated rather than mentioned); multi-controlled
gate decomposition with an honest two-qubit-gate count; a decoder whose logical error rate is
measured against its own threshold model.

**Hiring for pre-sales, solutions architecture or customer-facing technical work?**
[`Hybrid_Quantum_Cloud.ipynb`](Hybrid_Quantum_Cloud.ipynb) and
[`Noise_Benchmarking.ipynb`](Noise_Benchmarking.ipynb) are written for exactly that conversation.
The first simulates a hybrid quantum-classical platform — job queue, batching, retries, injected
provider faults, cost accounting — and proves the orchestrator returns the same energy as the
local simulator to `4.44e-16` while absorbing 22 retryable backend failures. The second is the
deck you take into a customer meeting: randomised benchmarking, gate-error tomography, readout
mitigation, device-specific error budgets, and what a `T1`/`T2` table actually costs a circuit you
want to run. [`IonQ_QAOA_MaxCut.ipynb`](IonQ_QAOA_MaxCut.ipynb) is the whole engagement in one file:
a customer's rostering problem turned into a QUBO, compiled to a trapped-ion device's native gate
set, priced per answer under two real billing models, and then reported as *no practical value over
the classical baseline on this instance* — with the three conditions that would flip that verdict.
Alongside that, I work as a cloud/AI solutions architect and teach, so translating a quantum result
into a customer's decision is the part I do for a living rather than the part I hope to learn.

---

## The portfolio

| # | Notebook | Built from scratch | Headline measured result | Independent reference |
|---|---|---|---|---|
| 1 | [`Quantum_Circuit.ipynb`](Quantum_Circuit.ipynb) | Statevector engine, tensor-product gate application, H/X/Y/Z/S/T/CNOT/CZ/CCZ, Bloch spheres, measurement histograms, entanglement entropy | 88 assertions pass; `H·Z·H = X` verified as a matrix identity, global-phase stripping demonstrated | Qiskit `Statevector` / `Operator` |
| 2 | [`Bell_Inequality.ipynb`](Bell_Inequality.ipynb) | Bell states, coincidence-projector correlations `E(a,b)`, CHSH search, local hidden-variable model, Kraus channels, finite-shot sampler | `S = 2√2` quantum vs `2.000000` classical over a dense angle scan; white-noise threshold `p* = 1 − 1/√2 ≈ 0.293`, readout threshold `ε* ≈ 0.0796`; CHSH game `75.0%` classical vs `cos²(π/8) ≈ 85.4%` | Qiskit `Statevector`, `DensityMatrix.evolve(Kraus)`, `Pauli` stabilisers |
| 3 | [`Grovers_Search.ipynb`](Grovers_Search.ipynb) | Real oracles compiled from predicates (subset-sum, 2-CNF, 3-SAT), phase and bit-flip oracles, diffusion as both a matrix and `Hⁿ(2\|0⟩⟨0\|−I)Hⁿ`, closed-form `P(t)`, depolarising noise on the circuit | `N = 256, M = 1`: `t* = 12`, success `0.999947`; measured log-log slope of queries-to-50% vs `N` over `N = 4 … 2²⁰` is **0.485** against the theoretical `0.5`; `p = 0.002` noise pushes the best attainable `P` under a coin flip | Qiskit `QuantumCircuit.mcx`, `Statevector`, `Operator` |
| 4 | [`Shors_Algorithm.ipynb`](Shors_Algorithm.ipynb) | Modular-exponentiation unitary built entry by entry, QFT from twiddles, order extraction with continued fractions, classical post-processing, failure modes audited | 159 assertions; all order-finding peaks land at multiples of `r`, `φ(r)/r = 0.5000` success per shot; factor-vs-order oracle equivalence verified with **0** mismatches; the classical side is benchmarked honestly (trial division beat the simulator by ~3000× at small `N`) | — *(no library cross-check; the verification is internal and adversarial)* |
| 5 | [`QFT_Phase_Estimation.ipynb`](QFT_Phase_Estimation.ipynb) | QFT with and without swaps, exact Fourier columns, iterative and textbook QPE, eigenstate prep, phase-collapse under noise | Single-shot accuracy `P(\|err\| ≤ 2⁻⁴) = 0.954973`, **1.000000** with majority vote over the same shots; dyadic phases peak at exactly `1.0` while generic phases lose mass in the documented pattern | NumPy `expm` and analytic Fourier columns, plus Qiskit `Statevector` / `Operator` in the optional section |
| 6 | [`QAOA_MaxCut.ipynb`](QAOA_MaxCut.ipynb) | Max-Cut cost Hamiltonian from the cut table, mixer, angle search (grid, Nelder–Mead, COBYLA, pattern search), exact shift-rule gradient, shot-level sampling | `K₃,₃` at `p = 1` reaches the analytic ceiling `F = 6.232050808` = `0.69245·\|E\|`; `p = 2` reaches **0.89108** of `OPT`; gradient vs finite difference `1.78e-09` | Own `expm` reference, closed-form `p=1` ceiling, Qiskit circuit simulation in the optional section |
| 7 | [`VQE_Molecular_Ground_State.ipynb`](VQE_Molecular_Ground_State.ipynb) | Jordan–Wigner transform, Pauli-string decomposition, frozen-orbital reduction, a hardware-efficient `Ry` ansatz, Nelder–Mead written from scratch, gradient descent on exact parameter-shift gradients, a symmetry-adapted single rotation solved in closed form, shot sampling, Kraus noise, the whole potential-energy curve, plus a **determinant-basis full-CI engine** and a from-scratch Gaussian-integral + RHF engine as the no-library references | VQE reaches the exact ground energy to `−2.2e-16 Ha`; Hamiltonian agrees with PySCF to `3.0e-11 Ha` and with PennyLane to `1.87e-08 Ha`; the pure-NumPy integral engine matches PySCF's integrals to `2.8e-11 Ha` and its RHF energy to `9.7e-13 Ha` | PySCF (`FCI`, integrals), PennyLane (`qchem` + VQE engine), Qiskit `Statevector` |
| 8 | [`Quantum_Kernel_SVM.ipynb`](Quantum_Kernel_SVM.ipynb) | Feature-map circuits, kernel matrix from state overlaps, SVM dual solved by hand, PAC-learning angle on why the quantum kernel separates | Parity `p = 2` test accuracy **quantum 0.806 / RBF 0.833 / linear 0.639**; quantum-vs-`sklearn` train accuracy identical at `0.9500 / 0.9500` | scikit-learn `svm.SVC` and `model_selection.train_test_split` |
| 9 | [`Quantum_Neural_Network.ipynb`](Quantum_Neural_Network.ipynb) | Parameter-shift rule derived and implemented, layers, barren-plateau scan, hardware-efficiency accounting (circuit executions per gradient entry) | 282 assertions; `iris` and `breast_cancer` honest test accuracies reported at the best-loss epoch; under depolarising noise `p ≤ 0.40` accuracy holds at `1.0000` while the readout range collapses `1.9914 → 1.0962` | PennyLane parameter-shift / `default.qubit` |
| 10 | [`Quantum_GAN.ipynb`](Quantum_GAN.ipynb) | Generator/critic as parameterised statevectors, full Hermitian vs diagonal-only score, adversarial loop with stability instrumentation, capacity sweep | 762 assertions library-free (795 with PennyLane present), whole notebook in `81.5 s`; critic BCE `1.38 → 0.02` with a full Hermitian critic vs `1.39 → 1.39` (no learning) with a diagonal-only one — the coherence term is where the capacity lives | PennyLane, plus analytic reference distributions |
| 11 | [`Quantum_Error_Correction.ipynb`](Quantum_Error_Correction.ipynb) | Bit-flip and phase-flip codes, syndrome extraction circuits, Shor fault-tolerant ancilla, CSS construction, depolarising decoding | 274 assertions; surface-code budget computed from the threshold model — `p = 0.002 → d = 15 (225 qubits)`, `p = 0.008 → d = 103 (10,609 qubits)`, `p ≥ 0.010 → no distance below 201 works` | Qiskit `QuantumCircuit` / `quantum_info` (state and Pauli checks) in the optional section |
| 12 | [`BB84_Quantum_Key_Distribution.ipynb`](BB84_Quantum_Key_Distribution.ipynb) | Basis preparation and sifting, parameter estimation, privacy-amplification threshold from mutual information, intercept-resend and optimal-cloning attacks, finite-key accounting | 238 assertions; information-equivariance threshold `Q* = 0.146447`, `1 − 2h(Q) = 0` abort point `Q = 0.110028`, optimal cloner fidelity `0.833333 = 5/6` measured | Qiskit (state simulation), independent `h(Q)` computation |
| 13 | [`Hybrid_Quantum_Cloud.ipynb`](Hybrid_Quantum_Cloud.ipynb) | Simulated quantum provider SDK, job queue with batching, retry/fault injection, cost and latency accounting, hybrid optimisation loop against a local simulator, all on a transverse-field Ising ring as the target problem | 270/270 assertions in `8.6 s`; analytic SDK energy vs dense local `4.441e-16`; ground energy recovered at `−4.402569` against exact `−4.402568723`; **22 retryable provider failures absorbed** without changing the answer | Own deterministic reference simulator, plus Qiskit as an optional third backend |
| 14 | [`Noise_Benchmarking.ipynb`](Noise_Benchmarking.ipynb) | RB sequences with Clifford grouping, interleaved RB, gate-set tomography lite, RBE from `T1`/`T2`/readout, error-mitigation zero-noise extrapolation, readout-mitigation matrix | 457 assertions in `131.5 s`; mean fidelity across five circuits `0.75928` over 101 two-qubit gates; `QFT\|13⟩` vs exact Fourier column `1.855e-15`; CHSH violation disappears at `p = 0.2103` | Qiskit `Statevector` (amplitude difference measured at `0.000e+00`), plus `qiskit_aer`'s `NoiseModel` where that package is available |
| 15 | [`IonQ_QAOA_MaxCut.ipynb`](IonQ_QAOA_MaxCut.ipynb) | A customer's crew-shift contention matrix → QUBO → Ising cost Hamiltonian → one gate-level IR (`h`/`rx`/`zz`/`gpi`/`gpi2`/`ms`) with three backends (exact statevector, exact density matrix through Pauli-twirl channels, Pauli-trajectory Monte Carlo) → IonQ native payload, routing accounting, shot-level pricing and a classical-baseline verdict | `W_total = 72`, exact optimum cut `68` (contention `4.0` min/day), best *balanced* rota `62` — the balance demand costs `8.8%` of the optimum. QUBO vs brute force `0.000e+00` over all 256 rosters. Ideal QAOA `p=4` ratio `0.9091`, `P(opt) = 0.60960`; at published Forte noise (`2.00e-4` 1q / `4.64e-3` 2q / `5.00e-3` SPAM) `0.8648` / `0.49526`. `14` entangling gates per layer on an all-to-all chain vs `48` (`×3.43`) if routed onto a path graph. 56 two-qubit gates, `39.1 ms` gate time, `$327.98` (Braket) / `$284.08` (Azure) at 4096 shots, `$0.70` for the 5 shots that see the optimum once at 95%. Multi-start local search: `1.0000` of the optimum in `7.8–13.7 ms` (the spread over four serial passes on this machine) for `$0.00` → **no practical value over the classical baseline on this instance**, and `9 of 12` hardware-tier cells left `UNKNOWN`. 59 assertions library-free / 62 with libraries, whole notebook in `62.8 s`; 6 of 6 negative controls caught | Qiskit 2.6.2 `Statevector` — L1 `6.363e-16` once the q0 bit order is reconciled, `1.627` if it is not; dimod 0.12.23 `to_ising()` spectrum and `ExactSolver` — `0.000e+00` over 256 rosters, constant term differing by exactly `W_total = 72` as the cut-vs-contention bookkeeping; plus a dense-matrix build inside the notebook that needs no library at all |

---

### Worst disagreement measured against an external library

Same code paths, run 9 November 2026 with Qiskit 2.6.2, PennyLane 0.45.1, PySCF 2.15.0,
dimod 0.12.23 and scikit-learn 1.9.1 importable. These are the numbers a reviewer should actually care about, because
they are the ones that could have been fudged:

| Notebook | Agreement with the external implementation |
|---|---|
| `Quantum_Circuit` | `0.00e+00` worst statevector discrepancy over 4 circuits |
| `Bell_Inequality` | worst printed difference `3.33e-16` across state vectors, `E(a,b)`, `S`, the stabiliser expectation values and the noisy `Kraus` channels |
| `Grovers_Search` | operators and states to `~1e-15`; ray overlaps `1.000000000000` after the little-endian flip |
| `Shors_Algorithm` | *no library comparison claimed* — internal and adversarial verification only |
| `QFT_Phase_Estimation` | worst of 11 comparisons: `2.30e-15` |
| `QAOA_MaxCut` | worst of 37 comparisons: `7.77e-16`; shift-rule gradient vs finite difference `1.78e-09` |
| `VQE_Molecular_Ground_State` | integrals vs PySCF `3.01e-11 Ha`, energy `1.44e-11 Ha`; operator vs PennyLane `1.87e-08 Ha`, energy `1.22e-09 Ha`; PennyLane's own VQE engine `2.48e-12 Ha`; Qiskit statevector exact |
| `Quantum_Kernel_SVM` | train accuracy identical to scikit-learn `0.9500 / 0.9500` |
| `Quantum_Neural_Network` | PennyLane parameter-shift: readout `3.3e-16`, gradients `6.7e-16`; own PCA vs scikit-learn PCA `1.21e-12` |
| `Quantum_GAN` | trained distribution `5.20e-18`, Jacobian `5.55e-17`, critic expectation `8.88e-16` |
| `Quantum_Error_Correction` | Qiskit `Kraus` evolution vs our Kraus sums: `1.11e-16` |
| `BB84_Quantum_Key_Distribution` | probe-coupling attack `0.000e+00`; cross-check flag `ran: True` |
| `Hybrid_Quantum_Cloud` | 9/9 agreement items, worst `1.665e-16` |
| `Noise_Benchmarking` | statevector amplitudes `0.000e+00`; the `qiskit_aer` noise-model branch prints its own skip reason when that package is absent |
| `IonQ_QAOA_MaxCut` | statevector vs Qiskit `Statevector` L1 `6.363e-16` **after** reconciling bit order — `1.627e+00` before, and the notebook keeps both numbers to show what the trap looks like; `zz(θ)` vs `rzz(2θ)` `0.000e+00`; `zz(θ)` vs IonQ `ZZ(θ/π)` `2.483e-16`; Ising spectrum vs dimod `to_ising()` `0.000e+00` over 256 rosters with the constant term differing by exactly `W_total = 72`; `qiskit-ionq` was absent in this runtime, so no backend transpilation is claimed |

Both verification modes ran clean across all fifteen: **15/15 `all code cells ran` with the libraries
blocked, and 15/15 with them present, zero failing cells and zero failed assertions either way**
(4,077 assertions library-free, 4,182 with the libraries). That is twice over: once as a batch audit
and once again as a serial timing pass, one notebook per process, and the two passes agree on every
per-notebook assertion count and figure count.

---

## Suggested reading path

A reviewer's time is short, so the notebooks are ordered so that each one can be read alone. But if
you want the argument in one pass:

**Fifteen minutes — "can he actually build the thing?"**
1. `Quantum_Circuit.ipynb`, Parts 1–4 — the engine, gate by gate.
2. `Bell_Inequality.ipynb`, Parts 2–4 — correlations from coincidence projectors, then CHSH.
3. `Grovers_Search.ipynb`, Part 5 — the closed form `P(t) = sin²((2t+1)θ)` and the sweep that proves it.

**One hour — "would I put him in front of a customer?"**
4. `VQE_Molecular_Ground_State.ipynb`, sections 1–3 and 7 — Jordan–Wigner, then three engines agreeing.
5. `QAOA_MaxCut.ipynb` — the gradient section especially; it is the cleanest illustration of finding a
   wrong formula that everyone copies, and proving it wrong numerically.
6. `Noise_Benchmarking.ipynb` and `Hybrid_Quantum_Cloud.ipynb` — the device-reality and platform-reality halves.
7. `IonQ_QAOA_MaxCut.ipynb`, Parts 9–10 — the same circuit priced per answer under two public rate
   cards, the scoreboard with its `UNKNOWN` cells left in, and the verdict against the classical baseline.

**Deep dive — "would he be a good colleague on a hard problem?"**
Read the **last markdown cell of any notebook**. Each one ends with a recap of what was measured, a
set of exercises that extend the work, and a "where this shows up in the real world" note. Those
sections are the most honest signal of how the notebooks were written: every claim in them is a
number the code above actually printed.

---

## How the claims in this file are verified

This matters more than the results, so it is stated plainly.

1. **A self-test suite in every notebook.** 4,077 assertions across the fifteen files when the
   reference libraries are absent, 4,182 when they are present, each checking
   a mathematical property (Hermiticity, trace preservation, commutation, unitarity), a numerical
   identity (my matrix against my closed form), or a physical limit (classical bound never exceeded
   by a classical model). They raise on failure and print their count when they pass. The tolerances
   are measured, not assumed — a check is only asserted once the observed gap is known.
2. **Cross-checked against reference libraries, and reported when they disagree.** Where Qiskit,
   PennyLane, PySCF or scikit-learn implement the same object, the notebook compares them and prints
   the gap in scientific notation (verified against Qiskit 2.6.2, PennyLane 0.45.1, PySCF 2.15.0,
   dimod 0.12.23 and scikit-learn 1.9.1 on 9 November 2026). If the gap is larger than expected, the notebook explains
   *why* instead of loosening the tolerance. Two examples I would happily be quizzed on: PennyLane's
   `qchem` only accepts `sto-3g`, so that comparison is run in `sto-3g` on **both** sides and labelled
   — comparing a `sto-3g` operator against a `sto-6g` one would be a basis-set difference dressed up
   as an agreement; and PennyLane's residual `1.87e-08 Ha` was chased down (elementwise gap ÷
   spectral gap `= 1.000`, coordinate drift measured at exactly `0.0e+00`, `conv_tol` swept over four
   orders of magnitude) before being attributed to its own integral engine.
3. **The no-library proof.** The claim "runs without a quantum library" is not taken on faith. All
   fifteen notebooks were executed with `pyscf`, `pennylane`, `qiskit`, `qiskit-ionq`, `qiskit-aer`,
   `openfermion`, `dimod`, `networkx`, `cvxpy`, `braket` and `aws` made
   **unimportable** and `get_ipython()` disabled — the state of a fresh Colab runtime where the
   optional installs have not happened — and every code cell in all fifteen ran, with the optional
   sections printing why they skipped instead of raising. Re-run across the whole batch on
   9 November 2026: **15/15 `all code cells ran`, zero failing cells, 4,077 self-test assertions
   passing.** This protocol is what caught
   two real bugs that a normal local run cannot see: with the libraries preinstalled, the fallback
   branch is dead code, so a bare `%pip` line inside an `except ImportError` block (invalid in
   IPython) and an unguarded reference import both survived for weeks while looking green.
4. **Notebooks are clean artefacts.** No stored outputs, no execution counts, no filesystem writes,
   one `.ipynb` per project, valid `nbformat` with a Python 3 / Colab kernel spec.
5. **Vendor numbers are quoted, dated, and left blank when they are not published.** Every IonQ
   fidelity, gate time, shot limit and price in `IonQ_QAOA_MaxCut.ipynb` comes from a `VENDOR` table
   that carries its source string and `ACCESS_DATE = 2026-11-09`, and anything that could not be
   confirmed at a source is stored as `None` and printed as `UNKNOWN` rather than estimated — the
   IonQ direct per-shot price is one of those cells. Nothing in any notebook reads, prints or stores
   a credential: the hardware section tests for the *presence* of `IONQ_API_KEY` and stops with a
   written reason if it is absent, so no claim in that notebook is dressed up as a device result.

---

## Honest limitations

A portfolio that only lists wins is not worth reading, and a pre-sales engineer who oversells the
technology loses the room anyway.

- **Classical simulation scales as `2ⁿ`.** Everything here runs on amplitudes in NumPy. Statevectors
  stay tractable to roughly `n ≈ 20`; the circuits in these notebooks are 2–9 qubits, chosen so that
  exact references are computable in the same file, while the resource tables extrapolate honestly to
  key-size regimes. **Nothing has been run on real quantum hardware** — this repository demonstrates
  algorithmic and numerical understanding, not device access. `IonQ_QAOA_MaxCut.ipynb` builds the
  whole trapped-ion workflow (native gate payload, shot and depth accounting, two public rate cards,
  a replay harness that a real distribution can be pasted into) but submits no job, so nine of its
  twelve hardware-tier cells are printed as `UNKNOWN` rather than filled with a simulated number.
- **The vendor facts in that notebook are a snapshot.** Its error rates, gate times, shot limits and
  prices carry a source string and `ACCESS_DATE = 2026-11-09`; IonQ's direct per-shot price is not
  published and is deliberately left as `None`. Re-check the rate card before quoting a customer, and
  note that the gate-time latency model excludes queueing, retries and calibration failures, which on
  a real device dominate turnaround.
- **Chemistry results are basis-limited, not algorithm-limited.** The VQE notebook models H₂ at
  0.7319 Å in `sto-6g` (and compares operators in `sto-3g` where PennyLane's `qchem` requires it);
  the hybrid-cloud notebook's target problem is a 4-qubit transverse-field Ising ring. The basis set
  dominates: switching H₂ from `sto-3g` to `sto-6g` moves the full-CI energy by **8.68 mHa**, while
  the numerical VQE error is `2.2e-16 Ha` — thirteen orders of magnitude smaller, so the impressive
  decimal is the least interesting number on the page and the notebooks say so.
- **`Shors_Algorithm.ipynb` has no library cross-check.** Its verification is internal and adversarial
  (all peaks, all failure modes, versus brute-force orders) — flagging that asymmetry is deliberate.
- **Small-data ML.** The kernel-SVM, QNN and QGAN notebooks use 2-D/`iris`/`breast_cancer`-scale
  problems. They are demonstrations of the gradient machinery, the noise behaviour, and where a
  quantum kernel genuinely helps versus an RBF one — not competitive models.
- **The noise models are models.** Depolarising, amplitude-damping and readout-error channels with
  published `T1`/`T2` ranges approximate a device; they are not a trace of one. Correlated crosstalk
  and leakage are out of scope of these notebooks.
- **The QPU verdict is measured on an instance inside brute force's reach.** Eight crews, 256 rosters:
  a single-flip local search finds the exact optimum in `7.8–13.7 ms` across four separate serial
  passes, so `IonQ_QAOA_MaxCut.ipynb`'s
  conclusion — no practical value over the classical baseline *here* — is a statement about this
  problem size, not about QAOA. The notebook lists the three conditions that would flip it and does
  not test any of them: instances large and structured enough that the classical climb stalls in a
  local optimum; hard side constraints handled by the hardware rather than by a penalty term (only
  the penalty route was tried, and its `mu` sweep is what a native route would retire); and a deeper
  ansatz at a fixed error rate — the measured `p`-ladder gains `+0.188` of the ratio from `p=1` to
  `p=4`, while each added layer costs 14 more two-qubit gates, so quality and noise move in opposite
  directions on the same dial. It also states plainly that the noisy simulation is a *floor* on the
  damage, not an estimate of it: no crosstalk, no `T1`/`T2`, no correlated or leakage errors.

---

## Background, and how to reach me

I work as a **Senior Training Advisor and AI / Generative-AI Solutions Architect at Alibaba Cloud**
and teach **machine learning and data science** as an assistant professor — a research record of
around 39 publications, 900+ citations and an H-index of 18, in deep learning, computer vision,
time-series forecasting and IoT before quantum became the interesting part. I am based in Singapore
and have worked across India, Thailand and Singapore. That combination is why this portfolio is
deliberately three things at once:

* **research credibility** — derivations, closed forms, thresholds and error budgets that a quantum
  scientist can interrogate, because every one of them is asserted in code;
* **engineering credibility** — from-scratch simulators, ansätze, decoders, gradient rules and a
  simulated hybrid-cloud platform, verified against Qiskit, PennyLane, PySCF and scikit-learn rather
  than trusted;
* **commercial credibility** — the ability to hold the customer's side of the conversation: what to
  promise, what a `T1`/`T2` table really costs, where the classical baseline still wins, and how to
  say so without losing the deal.

If you are a **recruiter, talent-acquisition partner or hiring manager** looking at a quantum
requirement — research team, quantum software group, or a pre-sales / solutions role where the
candidate has to survive both the lab and the customer meeting — the most useful thing you can do is
send me the job description. I will tell you honestly which parts of it this portfolio evidences,
which parts it does not, and what I would need to ramp on. I would rather be placed accurately than
placed quickly.

**Write to me at [ferdinjoe@gmail.com](mailto:ferdinjoe@gmail.com)** — a subject line of
`Quantum role — <your company>` is enough, and you will normally hear back the same day.
**Or connect on LinkedIn: [linkedin.com/in/ferdinjoe](https://www.linkedin.com/in/ferdinjoe/).**
**Phone number:** available on request by email or LinkedIn message.

Happy to do a live 30-minute walkthrough of any single number in this file: the cell that produced
it, the tolerance it was checked against, the library it was checked with, and what would have to
change for it to move.
