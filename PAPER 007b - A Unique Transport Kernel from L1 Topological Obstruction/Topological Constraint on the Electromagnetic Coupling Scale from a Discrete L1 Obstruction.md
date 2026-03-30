# Topological Constraint on the Electromagnetic Coupling Scale from a Discrete $\ell^1$ Obstruction

**Author:** Jeremy H. Carroll
**Version:** v1.0 (Pre-Print)
**Date:** March 2026

---

## Abstract

We present a topological constraint on the electromagnetic coupling scale derived from a single geometric seed: a sign contradiction on a minimal graph. The $\ell^1$ coboundary norm measures the contradiction. Subdivision heals it into a 3-node lattice. From this lattice, we derive the discrete Fourier transform as the unique diagonalizing basis, the Born rule as Parseval's identity, and the cyclic shift operator as the transport mechanism. The transport amplitude across one edge of the resulting 2-simplex is shown to be uniquely determined: the measure is Haar (by uniqueness of shift-invariant measures), the observable is $\cos\theta$ (by linearity and symmetry constraints), and the domain is $[-\pi/6, \pi/6]$ (by Voronoi bisection of the eigenvalue partition). The resulting amplitude $a = \sin(\pi/6)/(\pi/6) = 3/\pi$ yields a unitarity deficit $D = 1 - 9/\pi^2$, from which a candidate bare coupling scale follows. The Casimir bridge to $SU(3)$ and one-loop renormalization group flow produce a candidate UV coupling consistent with $\alpha_{\mathrm{em}}^{-1}(0) \approx 137$ at the infrared scale. A formal representation theorem, grounded in the Riesz--Markov--Kakutani theorem, establishes that the operator class is not sampled but exhausted. The derivation establishes uniqueness within the admissible operator class defined by $\ell^1$ stability; whether physical reality is strictly restricted to this class remains an open question. The derivation chain contains no free parameters and no imported physics prior to the renormalization group stage. This work derives necessity, not completeness: it shows what a minimal consistency condition forces, not that it accounts for all of physics.

---

## 1. Introduction

The fine structure constant $\alpha_{\mathrm{em}} \approx 1/137.036$ has resisted first-principles derivation since its identification by Sommerfeld in 1916. It enters the Standard Model as a free parameter, and no existing framework--including string theory, loop quantum gravity, or asymptotic safety--computes its value from internal structure alone.

This work takes a different approach. Rather than beginning with a quantum field theory and searching for a vacuum that reproduces $\alpha$, we begin with the minimal computable structure: a graph with a sign contradiction. We then show that resolving this contradiction, under the requirement that the resolution be stable, forces a unique chain of algebraic and geometric structures that produces a constrained candidate consistent with observed scaling. The only foundational requirement is that local corrections to inconsistency must reduce, not increase, global inconsistency. Everything else follows as theorem.

**Scope.** This work derives necessity, not completeness. We show what a minimal consistency condition uniquely forces; we do not claim that this single seed accounts for all of physics. The derivation boundary--what is derived versus what is imported--is explicitly delineated in Section 10.

The derivation proceeds in stages:

1. **The seed** (Section 3): A 2-node graph with sections $s(A) = +1$, $s(B) = -1$ has $\ell^1$ coboundary tension $\|\delta s\|_1 = 2$. Subdivision heals this to a 3-node lattice.

2. **Wave mechanics** (Section 4): The cyclic shift operator on the 3-node lattice is diagonalized uniquely by the discrete Fourier transform. Parseval's identity forces the Born rule $P = |\psi|^2$.

3. **The transport operator** (Section 5): The eigenvalue partition of $S^1$ defines Voronoi cells. Edge-sharing bisects each cell. The transport amplitude is the Haar average of $\cos\theta$ over the edge sector $[-\pi/6, \pi/6]$, yielding $a = 3/\pi$.

4. **Uniqueness** (Section 6): A representation theorem proves the operator space collapses to a single element under four requirements (bounded, linear, local, single-step), each derived from $\ell^1$ stability axioms.

5. **The coupling constant** (Section 7): The unitarity deficit $D = 1 - (3/\pi)^2$ and the Casimir bridge to $SU(3)$ yield $\alpha_{\mathrm{GUT}}^{-1} \approx 25.54$. Renormalization group flow to the infrared scale produces $\alpha_{\mathrm{em}}^{-1} \approx 137$.

6. **Geometric Symmetry** (Section 8): The equilateral 2-simplex tiles $\mathbb{R}^2$ uniquely as the exactly flat $\{3,6\}$ lattice. This is presented as a suggestive geometric observation, not a cosmological model.

Section 9 addresses the relation to holographic and multiverse frameworks. Section 10 delineates what is derived from what is imported. Section 11 discusses open problems.

---

## 2. Notation and Conventions

| Symbol | Definition |
|--------|-----------|
| $\|\delta s\|_1$ | $\ell^1$ coboundary norm: $\sum_{\text{edges}} |s(v) - s(w)|$ |
| $N$ | Number of lattice nodes (derived: $N = 3$) |
| $S$ | Cyclic shift operator on $N$ nodes |
| $w_k$ | Eigenvalue of $S$: $w_k = e^{2\pi i k/N}$ |
| $\Omega$ | Edge sector (Voronoi half-cell): $[-\pi/6, \pi/6]$ |
| $a$ | Transport amplitude: $\mathrm{sinc}(\pi/6) = 3/\pi$ |
| $D$ | Unitarity deficit: $1 - a^2 = 1 - 9/\pi^2$ |
| $C_2(\mathrm{adj}), C_2(\mathrm{fund})$ | Quadratic Casimir invariants of $SU(3)$ |

---

## 3. The $\ell^1$ Obstruction and Its Resolution

### 3.1 The Minimal Contradiction

Consider the simplest non-trivial graph: two vertices $A, B$ connected by a single edge, with a section $s: V \to \{+1, -1\}$ assigning opposite signs. The $\ell^1$ coboundary measures the disagreement:

$$\|\delta s\|_1 = |s(A) - s(B)| = 2$$

This is the minimal topological obstruction: $H^1 \neq 0$ on the graph. The section cannot be made globally consistent.

### 3.2 Subdivision Healing

The obstruction is resolved by iterative subdivision. When the tension across an edge exceeds a threshold (set to 1), a new vertex is inserted at the midpoint with interpolated value. Starting from $[+1, -1]$:

- Iteration 1: $[+1, 0.0, -1]$. Tensions: $|1 - 0| = 1$, $|0 - (-1)| = 1$. Healed.

The process terminates at $N = 3$ nodes. This is deterministic: the same seed always produces the same lattice. The subdivision threshold is fixed by normalization of the $\ell^1$ defect unit; any rescaling $\tau \mapsto \lambda\tau$ is equivalent to a change of units and does not alter the fixed point $N = 3$.

### 3.3 Why $\ell^1$ and Not Another Norm

The foundational requirement is not the $\ell^1$ norm itself, but the existence of a stable, monotone defect diagnostic---one under which every local repair monotonically reduces the global obstruction measure. The $\ell^1$ coboundary norm is the unique structure satisfying this requirement.

**Formal result.** Any norm on $C^1(G, \mathbb{R})$ allowing cancellation between positive and negative edge defects cannot guarantee monotone defect detection on frustrated cycles. Specifically: let $\delta_e = s(v) - s(w)$ be the edge defect. A norm $\|\cdot\|$ that satisfies $\|x + y\| < \|x\| + \|y\|$ for some sign-opposing $x, y$ (strict triangle inequality, as in $\ell^2$) necessarily admits configurations where a single edge flip reduces the norm while increasing the number of frustrated faces. Under $\ell^1$, every edge flip that reduces a local defect reduces the global diagnostic monotonically, because $\|\cdot\|_1 = \sum |\delta_e|$ decomposes as a sum of independent non-negative terms.

This is established formally at three levels of generality in the companion papers:

- **Paper 000** (Theorem 4.2, $\ell^1$ Additive Universality): The $\ell^1$ coboundary norm is the initial object in the category of faithful seminorms satisfying locality, additivity, symmetry, and non-degeneracy. Any such diagnostic is proportional to $\ell^1$.
- **Paper 001** (Theorem 2.2, Free Seminorm Classification): The result extends to Banach presheaf coboundaries under functoriality. The $\ell^1$ norm is unique up to positive scalar among edge-additive, faithful, functorial seminorms.
- **Paper 002** (Theorem 2.1, Cochain Classification): Coordinate-wise additivity over disjoint supports on finite graph cochains forces $\ell^1$ geometry. This is the minimal combinatorial case.

Computationally, the stability argument is verified on $N = 15$ frustrated rings (`execute_25`): $\ell^1$ observers remain stable while $\ell^2$ and $\ell^\infty$ observers drift past stability thresholds. The norm inequality $\|\cdot\|_1 \geq \|\cdot\|_2 \geq \|\cdot\|_\infty$ ensures $\ell^1$ is maximally sensitive.

---

## 4. Wave Mechanics from Graph Structure

### 4.1 The Discrete Fourier Transform as Unique Diagonalization

The $N$-node lattice from Section 3 admits a cyclic shift operator $S$ (the translation-by-one-site map). The constraint that independent subsystems factorize under this shift requires diagonalization. The unique basis diagonalizing the cyclic convolution on $N$ nodes is the discrete Fourier transform (`execute_09`). This is a theorem of representation theory: the irreducible representations of the cyclic group $\mathbb{Z}_N$ are exactly the characters $e^{2\pi i k n / N}$.

Alternative bases (real-valued wavelets, random orthogonal matrices, identity basis) are tested and fail to recover the convolution structure (`execute_09_02`).

### 4.2 The Born Rule as Parseval's Identity

The DFT satisfies Parseval's identity: $\sum_n |s_n|^2 = \sum_k |\hat{s}_k|^2$. An observer who lacks access to the global $\ell^1$ phase origin (gauge ignorance) must integrate over this unknown phase. The unique translation-invariant measure on $U(1)$ is the Haar measure, and the resulting expectation value is $|\psi|^2$.

The Born rule is therefore not an axiom of the framework. It is a theorem, derived at `execute_11` from the DFT (which is derived at `execute_09` from the lattice, which is derived at `execute_00` from the obstruction). Probability enters the derivation chain downstream of the seed, not before it.

### 4.3 Complex Phase Necessity

The shift operator $S$ on a directed cycle is asymmetric (non-symmetric real matrix). By the spectral theorem, its eigenvalues are generically complex. The complex plane is not imported; it is forced by the directedness of causal transport on the lattice (`execute_10`). Real-valued diagonalization fails for asymmetric circulant matrices.

---

## 5. The Transport Operator and the Sinc Kernel

### 5.1 Eigenvalue Partition of $S^1$

The eigenvalues $w_k = e^{2\pi i k / N}$ for $k = 0, 1, \ldots, N-1$ partition the unit circle into $N$ equal arcs. For $N = 3$, the eigenangles are $0, 2\pi/3, 4\pi/3$.

The Voronoi cell of each eigenvalue is the arc of angles closer to it than to any other. For $N$ equally-spaced points, each cell has width $2\pi/N$. The cell of $w_0 = 1$ is $\theta \in [-\pi/3, \pi/3]$.

### 5.2 Edge-Sharing Bisection and the Locality Constraint

The eigenvalue partition defines the full Voronoi cell $[-\pi/3, \pi/3]$. However, an edge is not a vertex. Transport is fundamentally an edge-local operation. In a cycle graph $C_3$, each vertex is incident to exactly two edges (degree $d = 2$). 

If we assigned the full vertex Voronoi cell $[-\pi/3, \pi/3]$ to both incident edges, the edges would double-count the phase space surrounding the vertex. This explicitly violates the strict independence and additivity of the $\ell^1$ norm. To preserve $\ell^1$ additivity and avoid double counting, the vertex measure must be partitioned equally across its incident edges. 

For degree 2, this forces the unique edge-local domain:
$$h = \frac{\pi/3}{1} = \frac{\pi}{3}, \quad \text{half-sector} = \frac{h}{2} = \frac{\pi}{6}$$

The edge sector $\Omega = [-\pi/6, \pi/6]$ is therefore not a geometric coincidence. Any domain larger than $[-\pi/6, \pi/6]$ double-counts vertex measure; any smaller domain breaks symmetry. Thus $[-\pi/6, \pi/6]$ is the unique admissible edge-local domain. This partition is the unique measure-preserving decomposition of the vertex Voronoi cell compatible with $\ell^1$-additive edge independence.

### 5.3 The Forced Observable

The transport operator $T = e^{i\theta}$ is a unitary phase rotation. To extract a real-valued amplitude compatible with the $\ell^1$ lattice (which evaluates real integer defects), we require the observable $f(\theta)$ to satisfy:

1. **Linear in $T$**: $f(T) = \mathrm{Re}(cT)$ for some $c$, since $T$ is the single-edge operator.
2. **Real-valued**: The $\ell^1$ lattice is real.
3. **Normalized**: $f(0) = 1$ (identity transport has unit amplitude).
4. **Even**: $f(\theta) = f(-\theta)$ (the edge sector is symmetric about $\theta = 0$).

Starting from $f(\theta) = c \cdot e^{i\theta} + d \cdot e^{-i\theta}$ with 4 real parameters, these constraints reduce:
- Real $\Rightarrow$ 2 parameters
- Normalized $\Rightarrow$ 1 parameter
- Even $\Rightarrow$ 0 parameters

The unique survivor is $f(\theta) = \cos\theta = \mathrm{Re}(e^{i\theta})$.

### 5.4 The Haar Measure

The integration measure over $\Omega$ must be shift-invariant (the transport does not privilege any phase within the sector). By Haar's theorem (1933), the unique such measure on a compact group is the uniform (Lebesgue) measure.

### 5.5 The Transport Amplitude

Combining the unique measure, observable, and domain:

$$a = \frac{1}{|\Omega|} \int_{-\pi/6}^{\pi/6} \cos\theta \, d\theta = \frac{\sin(\pi/6)}{\pi/6} = \frac{1/2}{\pi/6} = \frac{3}{\pi} \approx 0.9549$$

This is the sinc function evaluated at $\pi/6$. The result contains no free parameters.

---

## 6. The Uniqueness Theorem

### 6.1 Exhaustive Falsification

Eight combinations of alternative observables ($\cos\theta$, $\cos 2\theta$) and domains ($[-\pi/12, \pi/12]$, $[-\pi/6, \pi/6]$, $[-\pi/3, \pi/3]$, $[-\pi, \pi]$) are tested. Only $\cos\theta$ over $[-\pi/6, \pi/6]$ yields $3/\pi$. The coincidence that $\cos 2\theta$ over $[-\pi/12, \pi/12]$ also gives $3/\pi$ numerically is explained by the identity $\mathrm{sinc}(x) = \mathrm{sinc}(2 \cdot x/2)$, but this combination is doubly excluded: $\cos 2\theta = \mathrm{Re}(T^2)$ is quadratic in $T$ (violating linearity), and $[-\pi/12, \pi/12]$ has no topological derivation.

### 6.2 Higher Harmonics Exclusion

The observable $\cos(n\theta) = \mathrm{Re}(T^n)$ corresponds to the $n$-edge transport operator, not the single-edge operator. The per-edge amplitude uses $\langle k | S | k \rangle = w_k$, not $\langle k | S^n | k \rangle = w_k^n$. Higher harmonics conflate multi-edge holonomy with single-edge transport.

Computationally: the average $\langle \cos(n\theta) \rangle_\Omega \neq a^n$ for $n > 1$, confirming these are distinct physical quantities.

### 6.3 The Representation Theorem

**Theorem.** Let $T: \mathcal{H} \to \mathbb{R}$ be a transport functional satisfying:
- **(R1) Bounded**: $|T[\psi]| \leq C \|\psi\|$ for some finite $C$.
- **(R2) Linear**: $T[\alpha\psi_1 + \beta\psi_2] = \alpha T[\psi_1] + \beta T[\psi_2]$.
- **(R3) Local**: $T$ depends only on the state within the edge sector $\Omega$.
- **(R4) Single-step**: $T$ measures the amplitude for one edge traversal.

Then $T$ is uniquely representable as:

$$T[\psi] = \int_\Omega \psi(\theta) \, d\mu(\theta)$$

with $\mu = $ Haar measure, $\psi = \cos\theta$, $\Omega = [-\pi/6, \pi/6]$.

**Proof sketch.**
1. (R1) + (R2) imply $T$ is a bounded linear functional on $C(\Omega)$, the space of continuous functions over the compact domain $\Omega$. By the Riesz--Markov--Kakutani representation theorem (1909/1938/1941), $T$ is representable as an integral against a unique regular Borel measure.
2. This integral has the form $(\text{measure}, \text{integrand}, \text{domain}) = (M, O, D)$.
3. $M$ is unique by Haar's theorem (Section 5.4).
4. $O$ is unique by the constraint analysis of Section 5.3.
5. $D$ is unique by the Voronoi bisection of Section 5.2.

**Escape routes closed:**
- *Nonlocal kernels*: violate (R3). The Voronoi sectors are disjoint; cross-sector coupling means transport across edge $e$ depends on states at distant edge $e'$.
- *Distributional operators*: the transport amplitude is a scalar in $[0, 1]$, not a distribution.
- *Nonlinear functionals*: violate (R2), which is forced by the DFT-derived Hilbert space structure.
- *Path-dependent operators*: violate (R4). The shift operator $S$ is Markov; multi-step transport decomposes as iterated single-step.
- *Full-support weighted operators*: Haar uniqueness forces uniform measure; only $h = \pi/6$ yields $3/\pi$.

### 6.4 Axiom Justification

The requirements R1--R4 are not external assumptions. They are the operator-language translations of four $\ell^1$ stability axioms, each proven independently necessary (`execute_24`):

| Operator Requirement | $\ell^1$ Axiom | Failure Mode if Violated |
|---------------------|---------------|------------------------|
| R1 Bounded | Faithfulness | Unbounded $\Rightarrow$ unfaithful diagnostic |
| R2 Linear | Coproduct compatibility | Nonlinear $\Rightarrow$ defect cancellation |
| R3 Local | Locality | Nonlocal $\Rightarrow$ missed distributed defects |
| R4 Single-step | Contractive monotonicity | Multi-step $\Rightarrow$ amplifying corrections |

The $\ell^1$ norm itself is forced by observer stability (Section 3.3). Therefore: the derivation chain from obstruction to $\alpha$ contains no free axioms. Every requirement is derived from the one before it.

---

## 7. The Coupling Constant

### 7.1 The Unitarity Deficit

The transport amplitude $a = 3/\pi < 1$ implies that traversing one edge of the 2-simplex is contractive. The unitarity deficit per edge is:

$$D = 1 - a^2 = 1 - \frac{9}{\pi^2} \approx 0.08860$$

For the full triangular loop, the operator $T_\triangle = T_1 T_2 T_3$ has spectrum $\mathrm{Spec}(T_\triangle^\dagger T_\triangle) = \{a^6, a^6, a^6\}$, and the scalar deficit $D_\triangle = 1 - a^6 \approx 0.2417$ is gauge-invariant under $SU(3)$ transformations (`execute_33`).

### 7.2 The Casimir Bridge

The 2-simplex has 3 oriented edges, making the boundary cochain $C^1 \cong \mathbb{C}^3$. The cyclic transport generates a $\mathbb{Z}_3$ center, and $\det = 1$ (conservation). By Lie algebra classification, these constraints strongly single out $SU(3)$ as the minimal consistent candidate.

#### 7.2.1 Uniqueness of $SU(3)$

A referee may ask why not $SU(2) \times U(1)$ or a larger group. The transport structure acts on a 3-dimensional complex cochain space ($C^1 \cong \mathbb{C}^3$) with a $\mathbb{Z}_3$ phase symmetry and a global conservation law. The representation must therefore satisfy all of the following geometrically-derived constraints:

1. **Faithful representation on $\mathbb{C}^3$**: The group must act faithfully on the 3 oriented complex edges. This excludes groups whose lowest faithful representation is higher-dimensional, and excludes $SU(2)$ which lacks a 3D fundamental representation. It also excludes $SO(3)$ which is real, not complex.
2. **Center containing $\mathbb{Z}_3$**: The cyclic shift $S$ on 3 nodes enforces eigenvalues containing $e^{2\pi i/3}$. The group center must contain this symmetry. This excludes $SU(2)$ (center $\mathbb{Z}_2$) and $Sp(n)$ (center $\mathbb{Z}_2$).
3. **Determinant-preserving ($\det = 1$)**: The $\ell^1$ subdivision healing explicitly conserves the total section mass, translating to a determinant of 1. This excludes $U(3)$ (which has $\det \in U(1)$) and $GL(3)$ (not unitary).
4. **Non-abelian**: The 2-simplex enforces correlated transport across edges to close the loop holonomy ($S^3 = I$). An abelian product like $U(1)^3$ cannot enforce edge-to-edge correlation and curvature.
5. **Irreducible**: The 2-simplex is a single, indecomposable connected face. Realizing the group via a block-diagonal (reducible) representation like $SU(2) \times U(1)$ violates this geometric indecomposability.

By Cartan's classification of compact Lie groups, these constraints leave exactly one minimal admissible solution: $SU(3)$. Larger groups would introduce extraneous generators and degrees of freedom unsupported by the exact dimension of the 2-simplex topology. $SU(3)$ is not just mathematically natural; it is uniquely forced as the minimal closed solution.

The mapping from edge transport to face curvature is not an arbitrary choice—it corresponds to the the coboundary lift $d^1: C^1 \to C^2$. The fundamental defining action resides on the edges (the fundamental representation, $\dim 3$), while the closed loop holonomy measures curvature, taking values in the Lie algebra (the adjoint representation, $\dim 8$). 

When translating the amplitude deficit $D$ from the fundamental representation on the edge to the adjoint representation on the face, the geometric scaling factor is exactly the ratio of their quadratic Casimir invariants. This scaling is a theorem of Lie algebra representations dictating how traces scale when lifting an algebraic structure from its fundamental defining space to its adjoint bracket space. It is not an imported QFT axiom, but a structural scaling ratio:

$$\frac{1}{\alpha_{\mathrm{GUT}}} = \frac{C_2(\mathrm{adj})}{C_2(\mathrm{fund})} \times \frac{1}{D} = \frac{3}{4/3} \times \frac{\pi^2}{\pi^2 - 9} = \frac{9}{4} \times \frac{1}{D} \approx 25.54$$

### 7.3 Renormalization Group Flow

**Note on imported quantities.** The RG flow from $\alpha_{\mathrm{GUT}}^{-1} \approx 25.54$ to the infrared scale requires beta-function coefficients, which encode the matter content of the theory. For the MSSM ($N_g = 3$, $N_h = 2$), the one-loop coefficients are $\beta_1 = 33/5$, $\beta_2 = 1$, $\beta_3 = -3$.

These coefficients are not derived from the $\ell^1$ obstruction in this work. They represent the interface between the topological derivation (Sections 3--6) and phenomenology. The derivation of gauge group representations from $\ell^1$ topology is allocated to the Grand Unification program (Paper 009).

The derivation provides a candidate UV coupling $\alpha_{\mathrm{GUT}}^{-1} \approx 25.54$ consistent with $\alpha_{\mathrm{em}}$ under RG flow; the IR value $\alpha_{\mathrm{em}}^{-1} \approx 137$ depends on matter content, which remains to be derived from $\ell^1$ topology in subsequent work.

With this caveat, the one-loop RG flow yields:

$$\alpha_{\mathrm{em}}^{-1}(M_Z) \approx 128, \qquad \alpha_{\mathrm{em}}^{-1}(0) \approx 137$$

consistent with experimental measurement.

---

## 8. The Infinite Tiling and Geometric Symmetry

### 8.1 The $\{3,6\}$ Tiling

The 2-simplex from Section 3 is equilateral (forced by $\mathbb{Z}_3$ edge equivalence, `execute_29`). Equilateral triangles tile the Euclidean plane uniquely as the $\{3,6\}$ Schlafli tiling: 6 triangles meet at each vertex.

The Regge deficit at every vertex is:

$$\epsilon = 2\pi - 6 \times \frac{\pi}{3} = 0$$

This is zero identically, not approximately. The tiling is exactly flat.

### 8.2 A Suggestive Geometric Observation

The $\{3,6\}$ tiling identifies an exactly flat underlying continuous structure. While an initially perfectly flat discrete geometry is structurally encouraging given observed cosmic flatness, we explicitly classify this as a suggestive geometric observation, not a cosmological model. It does not contain dynamics, expansion, or perturbation modeling, and determining whether this fundamentally relates to the physical universe's flatness problem lies strictly outside the scope of this paper's claims.

---

## 9. Relation to Alternative Frameworks

### 9.1 Prior Probability and the Landscape

Frameworks that begin with a probability distribution over possible universes (the string landscape, eternal inflation with a measure problem, Tegmark's Level IV multiverse) presuppose a mathematical structure---probability---that is not available at the foundational level of this derivation.

In the $\ell^1$ pipeline, the Born rule $P = |\psi|^2$ is derived at Section 4.2 from Parseval's identity, which requires the DFT (Section 4.1), which requires the $N$-node lattice (Section 3.2), which requires the obstruction (Section 3.1). Probability enters the derivation chain downstream of the seed. Any framework that invokes probability at the foundational level uses a tool that does not yet exist at the point where the selection would occur.

### 9.2 The Everett Interpretation

Everett's many-worlds interpretation (MWI) requires three elements: (E1) a Hilbert space, (E2) unitary evolution, and (E3) branch weights given by the $\ell^2$ norm.

The $\ell^1$ pipeline derives (E1) at Section 4.1 and (E2) as an emergent infrared limit. However, it denies (E3): the $\ell^2$ norm is not fundamental but derived from $\ell^1$ via the gauge-ignorance functor (Parseval's identity). Observers using $\ell^2$ defect accounting are unstable on frustrated graphs (`execute_25`), and the $\ell^1$ healing is deterministic with a unique fixed point ($N = 3$).

MWI correctly identifies the Hilbert space but incorrectly elevates the derived $\ell^2$ norm to foundational status. Everett's branches are epistemic (observer-relative projections of a single $\ell^1$ structure), not ontic (independently existing universes).

### 9.3 Holography and AdS/CFT

The AdS/CFT correspondence and related holographic frameworks operate within a continuous $L^2$ Hilbert space and explore a broad class of consistent quantum field theories and gravitational duals. These approaches have achieved remarkable success in characterizing strongly coupled systems and establishing deep mathematical dualities.

The present work takes a different foundational approach. Rather than assuming a Hilbert structure, it derives the underlying space from a discrete $\ell^1$ topological obstruction. The focus is not on classifying all consistent theories, but on determining whether a minimal consistency condition uniquely fixes physical structure.

Several structural features distinguish the two approaches:

1. **Geometry**: The $\ell^1$ tiling yields exactly flat ($\epsilon = 0$) Euclidean geometry. AdS/CFT requires negative cosmological constant (negative curvature). The pipeline forces vertex valence $k = 2\pi/(\pi/3) = 6$, yielding the $\{3,6\}$ tiling. The hyperbolic $\{3,7\}$ tiling required for AdS-like geometry is not accessible.

2. **Discreteness**: The holographic principle (Bekenstein bound, Ryu--Takayanagi formula) presupposes a smooth manifold with well-defined areas. The $\ell^1$ lattice is fundamentally discrete; information content is the coboundary norm on edges, not an area-entropy relationship.

3. **Information structure**: In holographic frameworks, information on a $(d-1)$-dimensional boundary encodes a $d$-dimensional bulk. In the $\ell^1$ framework, information lives on edges (1-cells). There is no higher-dimensional bulk for a lower-dimensional boundary to encode.

4. **Methodology**: AdS/CFT is a duality relating two descriptions of the same physics, both assuming extensive prior structure. The $\ell^1$ pipeline is a derivation from a single seed. These are complementary approaches: holographic frameworks characterize what is *possible*; this construction investigates what is *necessary*.

---

## 10. Derivation Boundary: What Is Derived and What Is Imported

Intellectual honesty requires a clear delineation.

### 10.1 Derived from the $\ell^1$ Obstruction (No External Input)

| Structure | Source | Section |
|-----------|--------|---------|
| $N = 3$ lattice | Subdivision healing | 3.2 |
| DFT as unique basis | Representation theory of $\mathbb{Z}_N$ | 4.1 |
| Born rule $P = |\psi|^2$ | Parseval's identity | 4.2 |
| Complex phase | Asymmetric shift operator | 4.3 |
| Voronoi partition | Metric geometry on $S^1$ | 5.1 |
| Edge sector $[-\pi/6, \pi/6]$ | Bisection by vertex degree | 5.2 |
| Observable $\cos\theta$ | Linearity + symmetry constraints | 5.3 |
| Haar measure | Uniqueness of shift-invariant measure | 5.4 |
| $a = 3/\pi$ | Sinc kernel | 5.5 |
| $D = 1 - 9/\pi^2$ | Unitarity deficit | 7.1 |
| $SU(3)$ gauge group | Lie algebra classification | 7.2 |
| $\alpha_{\mathrm{GUT}}^{-1} \approx 25.54$ | Casimir scaling | 7.2 |
| Euclidean flatness | Regge calculus on $\{3,6\}$ | 8.1 |
| Representation theorem | Riesz--Markov--Kakutani + $\ell^1$ axioms | 6.3--6.4 |

### 10.2 Imported from Phenomenology

| Structure | Status | Section |
|-----------|--------|---------|
| MSSM beta-function coefficients | Input (matter content) | 7.3 |
| Couplings at $M_Z$ | Experimental boundary condition | 7.3 |
| $M_{\mathrm{Planck}}$ | External gravitational scale | 7.3 |
| $U(1) \times SU(2)$ gauge structure | Not derived from $\ell^1$ in this work | 7.3 |

### 10.3 Honest Assessment

The genuine achievement of this work is the derivation of $a = 3/\pi$ and $D = 1 - 9/\pi^2$ from a single topological seed with zero free parameters (Sections 3--6). The Casimir bridge to $SU(3)$ (Section 7.2) is structurally clean. The RG flow to $1/137$ (Section 7.3) requires phenomenological inputs that are not yet derived from $\ell^1$ topology.

The derivation of the full Standard Model gauge structure ($U(1) \times SU(2) \times SU(3)$, generation count, Higgs sector) from the $\ell^1$ obstruction is an open problem allocated to the Grand Unification program (Paper 009).

---

## 11. Open Problems

1. **Derive the electroweak sector.** The $SU(3)$ gauge group is forced by the 2-simplex structure. The $U(1) \times SU(2)$ sector and its breaking pattern are not yet derived from $\ell^1$ topology.

2. **Derive the beta-function coefficients.** The matter content (3 generations, 2 Higgs doublets) enters as an input to the RG flow. A first-principles derivation would eliminate the last imported quantities.

3. **Derive gravity.** The Regge deficit is identically zero on the $\{3,6\}$ tiling. Curvature (gravity) requires defects in the tiling. The mechanism by which $\ell^1$ defects source geometric curvature is not yet formalized.

4. **Experimental predictions.** The framework predicts that Planck-scale physics is non-unitary (Section 4.3), with unitarity emerging as an infrared limit. Observable consequences at accessible energies remain to be identified.

5. **The origin of distinction.** The derivation begins at the first computable condition: the existence of a sign contradiction on a graph. Why such a distinction exists lies outside the domain of physical theory and enters metaphysics. The pipeline is complete within the scope of computable structure.

---

## 12. Conclusion

We have presented a computational derivation chain from a single topological seed (a sign contradiction on a minimal graph) to a topological constraint on the electromagnetic coupling scale, passing through the emergence of wave mechanics, the Born rule, complex phase, the sinc transport kernel, and the $SU(3)$ Casimir bridge.

The central result is the transport amplitude $a = \mathrm{sinc}(\pi/6) = 3/\pi$, proven unique by a representation theorem grounding the operator classification in the Riesz--Markov--Kakutani theorem, with requirements derived from $\ell^1$ stability axioms rather than imposed externally.

The derivation contains zero free parameters from seed to $\alpha_{\mathrm{GUT}}^{-1} \approx 25.54$. The RG flow to $\alpha_{\mathrm{em}}^{-1} \approx 137$ requires phenomenological inputs (beta-functions, scale matching) that represent the current interface between topological derivation and Standard Model phenomenology.

Under the requirement of $\ell^1$-stable observer consistency, the admissible operator space collapses to a single solution. The derivation establishes uniqueness within the admissible operator class defined by $\ell^1$ stability; whether physical reality is strictly restricted to this class remains an open question. This leads to a topological constraint, in contrast to frameworks that admit large theory spaces or rely on anthropic selection. This distinction reflects a difference in foundational perspective: holographic and landscape approaches characterize what is possible, while the present construction investigates what is necessary.

The complete derivation chain, including all computational proofs and falsification tests, is available in the companion script `master_l1_derivation.py`.

---

## References

1. Haar, A. (1933). Der Massbegriff in der Theorie der kontinuierlichen Gruppen. *Annals of Mathematics*, 34(1), 147--169.
2. Riesz, F. (1909). Sur les operations fonctionnelles lineaires. *Comptes Rendus*, 149, 974--977.
3. Kakutani, S. (1941). Concrete representation of abstract (M)-spaces. *Annals of Mathematics*, 42(4), 994--1024.
4. Regge, T. (1961). General relativity without coordinates. *Il Nuovo Cimento*, 19(3), 558--571.
5. Maldacena, J. (1999). The large-$N$ limit of superconformal field theories and supergravity. *International Journal of Theoretical Physics*, 38(4), 1113--1133.
6. Everett, H. (1957). "Relative state" formulation of quantum mechanics. *Reviews of Modern Physics*, 29(3), 454--462.
7. Shannon, C. E. (1948). A mathematical theory of communication. *Bell System Technical Journal*, 27(3), 379--423.
8. Carroll, J. H. (2026). *Projection Obstruction Theory: Retraction Nonlinearity, $\ell^1$ Rigidity, and Density Scaling.* (Paper 000). Zenodo. https://doi.org/10.5281/zenodo.19151803
9. Carroll, J. H. (2026). *The Free $\ell^1$ Seminorm on Banach Presheaf Coboundaries.* (Paper 001). Zenodo. https://doi.org/10.5281/zenodo.19152115
10. Carroll, J. H. (2026). *Coordinate-Wise Additivity and the $\ell^1$ Norm on Finite Graph Cochains.* (Paper 002). Zenodo. https://doi.org/10.5281/zenodo.19152599
11. Carroll, J. H. (2026). *Hodge Structure and Gauge Equivalence of $\ell^1$ Defect Fields.* (Paper 003). Zenodo. https://doi.org/10.5281/zenodo.19152799
12. Carroll, J. H. (2026). *Universal Obstruction Theory: The $\ell^1$ Topological Framework.* (Paper 004). Zenodo. https://doi.org/10.5281/zenodo.19154775
13. Carroll, J. H. (2026). *Autopoietic Cohomology: Iterative Obstruction Repair on Causal Posets.* (Paper 005). Zenodo. https://doi.org/10.5281/zenodo.19155011

---