# Projection Obstruction for Factorized States: Nonlinear Dynamics, Additive ℓ¹ Structure, and Finite-Time Defect Bounds

**Author:** Jeremy H. Carroll
**Date:** March 2026
**Version:** v5.0 (Pre-Print)

---

## Abstract

Projection-based approximations --- such as mean-field theory, product-state ansatze, and factorized variational methods --- replace correlated states with product states via a nonlinear retraction. This induces a structural discrepancy between the true dynamics and the projected dynamics.

We analyze this discrepancy in a Banach presheaf framework and establish three results. **(1)** For a ^2$ retraction $\Pi$ onto a submanifold $, the induced dynamics  = \Pi \circ T_t|_M$ is, under a non-degeneracy condition on the Jacobian of the projected generator, not conjugate to any linear semigroup (Theorem 3.1). **(2)** Under strict locality, additivity, and symmetry axioms (Axioms 1--4), the $\ell^1$ norm of the presheaf coboundary is the canonical additive diagnostic for this discrepancy, characterized as the initial object in an appropriate category of seminorms (Theorem 4.2). **(3)** For finite-range, finite-dimensional lattice systems with non-commuting interactions, the induced defect exhibits non-vanishing density over a finite time interval independent of system size, as constrained by Lieb--Robinson bounds (Theorem 5.1).

Axioms 1–4 characterize a class of local, additive, and symmetry-respecting defect diagnostics. Within this class, the ℓ¹ coboundary norm is uniquely determined up to a global scalar.

These results formalize the geometric, categorical, and dynamical structure of projection-induced errors in factorized many-body approximations. The framework is finite-dimensional and finite-time; no claims are made regarding asymptotic or thermodynamic limits.

--- such as mean-field theory, product-state ansatze, and factorized variational methods --- replace correlated states with product states via a nonlinear retraction. This induces a structural discrepancy between the true dynamics and the projected dynamics.

We analyze this discrepancy in a Banach presheaf framework and establish three results. **(1)** For a $C^2$ retraction $\Pi$ onto a submanifold $M$, the induced dynamics $S_t = \Pi \circ T_t|_M$ is, under a non-degeneracy condition on the Jacobian of the projected generator, not conjugate to any linear semigroup (Theorem 3.1). **(2)** Under strict locality, additivity, and symmetry axioms (Axioms 1--4), the $\ell^1$ norm of the presheaf coboundary is the canonical additive diagnostic for this discrepancy, characterized as the initial object in an appropriate category of seminorms (Theorem 4.2). **(3)** For finite-range, finite-dimensional lattice systems with non-commuting interactions, the induced defect exhibits non-vanishing density over a finite time interval independent of system size, as constrained by Lieb--Robinson bounds (Theorem 5.1).

We further observe that Axioms 1--4 are not arbitrary: they characterize the minimal structural conditions under which a local agent can consistently detect, aggregate, and act upon defects (Section 1.2). This grounds the $\ell^1$ diagnostic in an operational criterion --- the existence of consistent local observers --- rather than in unmotivated mathematical assumptions.

These results formalize the geometric, categorical, and dynamical structure of projection-induced errors in factorized many-body approximations. The framework is finite-dimensional and finite-time; no claims are made regarding asymptotic or thermodynamic limits.

---

## 1. Introduction

Projection-based approximations are central to many-body physics and computation. Methods such as mean-field theory, Hartree--Fock, and product-state variational ansatze replace a correlated state with a product of local states, thereby reducing an exponentially large description to a tractable one. This replacement is implemented by a nonlinear map --- formally, a retraction --- onto a low-dimensional manifold of factorized states. While the practical success of these methods is well established, the structural effect of this retraction on the underlying dynamics is less clearly understood: what information is systematically discarded, how it propagates, and how it should be measured in a representation-independent way.

In this work, we isolate and analyze the discrepancy introduced by projection as a geometric and combinatorial object. We show that composing a linear many-body evolution with a nonlinear retraction produces dynamics that --- under a non-degeneracy condition --- cannot be reduced to any linear flow, and that the resulting local inconsistencies assemble into a presheaf coboundary with a canonical additive structure. Under natural locality and symmetry conditions, this leads to a distinguished $\ell^1$ diagnostic for projection-induced defects, and for finite-range systems we prove that this defect persists with non-vanishing density over a finite time interval independent of system size.

The goal is not to propose a new physical theory, but to provide a precise structural account of the error introduced by factorization.

We prove three structural theorems:
1. **Geometric Obstruction (Theorem 3.1):** The projected dynamics is not $C^2$-conjugate to any linear semigroup when the projected generator has non-constant Jacobian.
2. **Additive Universality (Theorem 4.2):** Subject to Axioms 1--4, the $\ell^1$ coboundary norm is the uniquely determined diagnostic, up to a global scalar. Relaxing these axioms admits alternative norms (e.g. $\ell^2$).
3. **Density Persistence (Theorem 5.1):** The per-bond obstruction density is $\Omega(1)$ in system size over a time window $O(1/J)$, with constants depending only on local dimension, interaction strength, and active bond fraction.

**Scope.** The framework applies rigorously to Banach presheaves over finite posets. We avoid speculative physics or infinite-time limits; the density scaling bound is finite-time only.

**Conventions.** Norms are denoted $\lVert \cdot \rVert$ with appropriate subscripts; scalar absolute values are denoted $|\cdot|$.

### 1.1 Relation to Companion Work

The additive diagnostic used throughout this paper --- the $\ell^1$ coboundary norm --- is not introduced ad hoc. It is the terminal output of a two-stage classification program establishing $\ell^1$ rigidity at progressively richer structural levels:

* **Stage 1 (combinatorial):** In "Coordinate-Wise Additivity and the $\ell^1$ Norm on Finite Graph Cochains" [8], local additivity over disjoint coordinate supports and edge separability on finite graph cochains already force an $\ell^1$ geometry. No Banach space structure or dynamics are required.
* **Stage 2 (functional-analytic):** In "The Free $\ell^1$ Seminorm on Banach Presheaf Coboundaries" [6], the same rigidity persists when the cochain spaces are replaced by Banach presheaves and coordinate additivity is replaced by structural compatibility (functoriality under bounded linear maps).

By the classification results of these preceding papers, any diagnostic satisfying locality, additivity over disjoint supports, and structural compatibility with the underlying linear maps must be proportional to the $\ell^1$ coboundary norm. Accordingly, the defect quantity analyzed here is not chosen, but structurally determined by these constraints.

The present paper (Stage 3, dynamical) builds on that classification by showing that projection-induced dynamics naturally generate nontrivial coboundary defects, and that these defects persist with non-vanishing density under finite-range evolution. Together, the three papers establish that additive, structure-preserving measurements of local defects are uniquely forced to be $\ell^1$ across combinatorial, functional, and dynamical settings, and that projection dynamics generically produce nonzero instances of such defects.

### Conceptual Overview

```text
Full correlated state space X
        |
        |  C^2 retraction Pi
        v
Product-state manifold M
        |
        |  induced curvature term D^2Pi(Am, .)
        v
Projected dynamics S_t = Pi . T_t|_M
        |
        |  local incompatibilities across regions
        v
Coboundary defects delta_e(s)
        |
        |  additive aggregation (Axioms 1-4)
        v
Total obstruction  I(s) = Sum ||delta_e(s)||
```

---

## 2. Structural Framework

We work with Banach-valued presheaves over finite posets, following standard categorical conventions [2].

### 2.1 Presheaves over Finite Posets

Let $(P, \leq)$ be a finite poset with covering relations $E_{\text{cov}}(P) = \{(a, b) : a < b,\; \nexists\, c \text{ with } a < c < b\}$. A **Banach presheaf** $F$ over $P$ assigns to each $x \in P$ a Banach space $F(x)$ and to each $(a,b) \in E_{\text{cov}}$ a contractive linear restriction map $r_{b,a}: F(b) \to F(a)$.

### 2.2 The Coboundary

For each edge $e = (a,b)$, the **coboundary** is $\delta_e(s) = r_{b,a}(s(b)) - s(a) \in F(a)$. A section descends if $\delta_e(s) = 0$ for all $e$. The $\ell^1$ coboundary norm is $I(s) = \sum_{e \in E_{\text{cov}}} \|\delta_e(s)\|$.

### 2.3 Linear Semigroups and Projected Dynamics

A **$C_0$ contraction semigroup** on a Banach space $X$ is $\{T_t\}_{t \geq 0}$ with generator $(A, \mathcal{D}(A))$. A **$C^2$ retraction** is a $C^2$ idempotent $\Pi: X \to M \subset X$ with $M$ a regular $C^2$ submanifold. If $\{T_t\}$ does not preserve $M$, we define the **projected semigroup** $S_t = \Pi \circ T_t|_M$ mapping $M \to M$ locally.

---

## 3. Theorem I: Nonlinear Obstruction to Linear Conjugacy

### 3.1 Statement

> **Theorem 3.1 (Projection Non-Dilability).** Let $X$ be a Banach space, $\{T_t\}$ a $C_0$ contraction semigroup with generator $(A, \mathcal{D}(A))$, and $\Pi: X \to M \subset X$ a $C^2$ retraction onto a $C^2$ submanifold $M \subset \mathcal{D}(A)$. Suppose:
>
> (a) *(Non-invariance)* There exists $t > 0$ such that $T_t(M) \not\subset M$.
>
> (b) *(Non-degeneracy)* The induced vector field $B(m) = D\Pi(m)Am$ has non-constant Jacobian $DB(m)$ in any affine coordinate chart compatible with a flat connection.
>
> Then there does not exist a Banach space $Y$, a $C^2$ embedding $\iota: M \hookrightarrow Y$, and a $C_0$ contraction semigroup $\{\tilde{T}_t\}$ on $Y$ such that $S_t = \iota^{-1} \circ \tilde{T}_t \circ \iota$. All arguments are local in affine coordinate charts induced by the ambient Banach space; global flatness of $M$ is not required.

### 3.2 Preliminary Lemma

> **Lemma 3.2 (Parallel fields on flat connections).** Let $(M, \nabla)$ be a connected Banach manifold equipped with a flat affine connection ($R^{\nabla} = 0$). If a $(1,1)$-tensor field $S$ on $M$ satisfies $\nabla S = 0$, then $S$ is constant in any affine coordinate chart.

*Proof.* Since $R^{\nabla} = 0$, the exponential map provides local affine coordinates where the Christoffel symbols vanish. In these coordinates, $\nabla S = 0$ reduces to $\partial_i S^j_k = 0$, making components constant. Affine transitions preserve this constancy globally. $\square$

### 3.3 Proof of Theorem 3.1

**Step 1: Linear flows are affinely flat.**
A linear semigroup $\{\tilde{T}_t\}$ with generator $\tilde{A}$ satisfies $\tilde{A}(y) = \tilde{A} y$. The canonical flat connection $\tilde{\nabla}$ on $Y$ has $R^{\tilde{\nabla}} = 0$, and $\tilde{\nabla}^2 \tilde{A} = 0$.

**Step 2: Conjugacy transfers flatness.**
Suppose $\iota: M \hookrightarrow Y$ is a $C^2$ embedding conjugating $S_t$ to $\tilde{T}_t$. The pullback connection $\nabla = \iota^* \tilde{\nabla}$ is flat on $M$ (since $\iota$ is $C^2$, the pullback preserves the vanishing of curvature), and $\nabla^2 B = 0$ for the generator $B = \iota^{-1}_* \tilde{A}$ of $S_t$.

**Step 3: The projected generator has non-constant derivative.**
The projected generator is $B(m) = D\Pi(m)Am$. Differentiating yields:
$$\nabla_v B = D^2\Pi(m)(Am, v) + D\Pi(m)Av$$

If $\nabla^2 B = 0$, then $\nabla_v B$ would be a parallel tensor field on $(M, \nabla)$, and by Lemma 3.2, it would be constant in any affine coordinate chart. But Hypothesis (b) states that $DB(m)$ is non-constant in every such chart. This is a contradiction. $\square$

---

## 4. Theorem II: Additive Universality of the $\ell^1$ Diagnostic

Theorem 3.1 demonstrates that geometric nonlinearity is inevitably produced by the retraction. The next question is how to measure the resulting defect. Theorem 4.2 establishes that, given Axioms 1--4, the $\ell^1$ norm is the uniquely forced diagnostic. The conclusion is conditional on these axioms; relaxing them admits other norms.

### 4.1 Diagnostic Systems and the Category of Seminorms

Let $C^1(P, F) = \bigoplus_{e \in E_{\text{cov}}} F(a_e)$ be the space of edge defects. We consider seminorms $J: C^1(P,F) \to \mathbb{R}_{\geq 0}$ satisfying:

**Axiom 1 (Coboundary Locality).** $J_P(s) = \sum_{e} w_e \|\delta_e s\|$, with local weights $w_e > 0$.

**Axiom 2 (Faithfulness).** $J_P(s) = 0 \iff s \text{ descends}$.

**Axiom 3 (Contractive Monotonicity).** For local contractions, the norm weakly decreases.

**Axiom 4 (Symmetry and Coproduct Compatibility).** Edge weights are uniform by edge-exchange symmetry, and the norm splits linearly over disjoint graph unions.

### 4.2 Statement

> **Theorem 4.2 ($\ell^1$ Additive Universality).** The $\ell^1$ coboundary norm $I(s) = \sum_e \|\delta_e(s)\|$ is the initial object in the category of faithful seminorms on $C^1(P,F)$ satisfying Axioms 1--4 (with morphisms given by monotone seminorm contractions), in the sense that any other such seminorm factors uniquely through $I$ up to a positive scalar. Consequently, any diagnostic satisfying these axioms is proportional to $I$:
> $$J(s) = c \sum_e \|\delta_e(s)\|$$
> for some constant $c > 0$.

*Proof Sketch.* Any diagnostic $J_P$ satisfying the axioms must assign constant weights to local defects due to edge-exchange isomorphism (Axiom 4). Concretely, edge-exchange symmetry implies that all edge weights $w_e$ are equal, since any permutation of edges that preserves graph structure must leave $J$ invariant. The Kan extension $\mathrm{Lan}_\pi d(s)$ realizes the universal space of local defects. Additivity over disjoint unions (Axiom 4) forces the seminorm to decompose as a sum over edges, excluding $\ell^2$ or $\ell^\infty$ alternatives, which do not decompose additively over disjoint unions. Thus $\ell^1$ is uniquely selected. $\square$

*Remark.* The $\ell^1$ norm is uniquely selected **given Axioms 1--4**, which may or may not be physically appropriate depending on context. The structural content of the theorem is that $\ell^1$ corresponds to additive aggregation of independent defects. In settings where defect channels are not independent, alternative diagnostics may be appropriate.

By the classification results of the preceding papers [8, 6] --- first at the combinatorial level (local additivity over disjoint supports) and then at the Banach level (functoriality under bounded linear maps) --- any diagnostic satisfying locality, additivity, and structural compatibility must be proportional to the $\ell^1$ coboundary norm. Accordingly, the defect quantity analyzed here is not chosen, but structurally determined by these constraints.

---

## 5. Theorem III: Finite-Time Density Persistence

### 5.1 Setup

Consider $N$ sites on a finite graph $\Lambda$ with local Hilbert spaces ($\dim \mathcal{H}_x \leq d < \infty$), bounded Hamiltonian $H = \sum_e H_e$ with $\|H_e\|_{\text{op}} \leq J$, and retraction $\Pi(\rho) = \bigotimes_x \text{Tr}_{\bar{x}}(\rho)$. Local Hamiltonians satisfying the non-commutativity requirement below are generic in the space of two-local interactions [3].

Define the commutator:
$$[H_e, \rho_a \otimes \rho_b] = H_e(\rho_a \otimes \rho_b) - (\rho_a \otimes \rho_b)H_e$$

### 5.2 Explicit Rate Bound

> **Lemma 5.2 (Local obstruction rate).** For a single bond $e = (a,b)$ with $[H_e, \rho_a \otimes \rho_b] \neq 0$, let $\gamma_e = \|[H_e, \rho_a \otimes \rho_b]\|_1 / d^2$. Then $\gamma_e > 0$. For $t$ small:
> $$C_e(t) \geq \gamma_e t - O(J^2 t^2).$$

*Proof.* On finite-dimensional spaces, the map $t \mapsto \rho(t) - \Pi(\rho(t))$ is analytic. Expanding to first order, the leading term is $-it[H_e, \rho_a \otimes \rho_b]$, whose trace norm is $\gamma_e d^2 / d^2 = \gamma_e$. The remainder is bounded by $O(J^2 t^2)$ via the operator norm bound $\|H_e\|_{\text{op}} \leq J$. Since $\gamma_e > 0$ by hypothesis, the linear term dominates for $t < \gamma_e / (KJ^2)$ where $K$ is a computable constant depending only on $d$. $\square$

### 5.3 The Density Bound

> **Theorem 5.1 (Finite-Time Density Persistence).** Let $\Lambda$ be a finite graph with $N$ sites and finite-dimensional local Hilbert spaces ($\dim \leq d$). Let $H = \sum_e H_e$ be a bounded finite-range Hamiltonian with $\|H_e\|_{\text{op}} \leq J$, and suppose a fraction $\eta > 0$ of edges satisfy $[H_e, \rho_a \otimes \rho_b] \neq 0$ for an initial product state $\rho(0) = \bigotimes_x \rho_x$.
>
> Then there exist constants $c > 0$ and $t_0 > 0$, depending only on local dimension $d$, interaction strength $J$, and active fraction $\eta$ (but not on system size $N$), such that
> $$\frac{C(t)}{N} \geq c \quad \text{for all } t \in [t_1, t_2] \subset (0, t_0]$$
> where $t_0 = O(1/J)$.

*Proof sketch.* By Lemma 5.2, each active bond $e$ generates a trace-norm defect $C_e(t) \geq \gamma_e t - O(J^2 t^2)$ for small $t$. By the Lieb--Robinson bound [1, 4, 5], for times $t < R / v_{\text{LR}}$ (where $R$ is the interaction range and $v_{\text{LR}}$ the Lieb--Robinson velocity), the reduced density matrix on any bond is approximated by its isolated evolution up to an error exponentially small in $(v_{\text{LR}} t - R)$. Concretely, the trace-norm error from truncating the causal cone satisfies $\|\rho_e^{\text{exact}}(t) - \rho_e^{\text{local}}(t)\|_1 \leq C_{\text{LR}} e^{-\mu(R - v_{\text{LR}} t)}$ for constants $C_{\text{LR}}, \mu > 0$ depending on the lattice geometry.

Within this causal window, each bond's defect $C_e(t)$ is controlled by the local evolution and cannot be canceled by correlations from distant bonds, because such correlations have not yet propagated to the bond. Summing over the $\eta N$ active bonds and noting that $\gamma_e \geq \gamma_{\min} > 0$ (where $\gamma_{\min}$ depends on $J$ and $d$), we obtain $C(t) \geq \eta N (\gamma_{\min} t - KJ^2 t^2)$ for $t \in (0, \gamma_{\min}/(2KJ^2))$. Dividing by $N$ gives $C(t)/N \geq \eta \gamma_{\min} t / 2 > 0$ on a non-trivial interval, with all constants independent of $N$. $\square$

*Remark on the time window.* The interval $[t_1, t_2]$ scales as $O(1/J)$: the defect appears immediately (linear growth at rate $\gamma_e$), dominates the quadratic correction for $t \ll 1/J$, and the Lieb--Robinson causal cone remains localized for $t \ll R/v_{\text{LR}} \sim 1/J$. Beyond this window, many-body correlations propagate across bonds and the argument does not apply.

---

## 6. Worked Examples

### 6.1 Example 1: Two Qubits (Entangling)

Consider two qubits with $H = J(X \otimes X)$ and initial state $|{00}\rangle$. The commutator $[H, |00\rangle\langle00|]$ is strictly non-zero. The full evolution yields:
$$|\psi(t)\rangle = \cos(Jt)|{00}\rangle - i\sin(Jt)|{11}\rangle$$
$$\rho(t) = \cos^2(Jt)|{00}\rangle\langle{00}| + \sin^2(Jt)|{11}\rangle\langle{11}| + (\text{off-diagonal terms})$$

The product retraction isolates marginals:
$$\rho_A(t) = \rho_B(t) = \cos^2(Jt)|{0}\rangle\langle{0}| + \sin^2(Jt)|{1}\rangle\langle{1}|$$
$$(\Pi\rho)(t) = \cos^4(Jt)|{00}\rangle\langle{00}| + \sin^4(Jt)|{11}\rangle\langle{11}| + \cos^2(Jt)\sin^2(Jt)(|{01}\rangle\langle{01}| + |{10}\rangle\langle{10}|)$$

The trace norm defect $C(t) = \|\rho - \Pi\rho\|_1 > 0$ for $t > 0$. This witnesses non-product structure in $\rho(t)$: the true state cannot be written as a tensor product of marginals, and the defect quantifies this failure.

### 6.2 Example 2: Transverse-Field Ising Model

The 1D Ising model $H = -J\sum_i Z_i Z_{i+1} - h\sum_i X_i$ with $|{+}\rangle^{\otimes N}$ produces strictly positive initial rates $C_e(t) = \gamma_e t + O(J^2 t^2) > 0$, consistent with the linear-in-$t$ scaling established by Lemma 5.2. By translational invariance, per-bond density is insensitive to $N$ for $t \ll N/v_{\text{LR}}$.

---

## 7. Discussion

This work isolates a structural feature common to projection-based approximations: the act of restricting a linear many-body evolution to a nonlinear manifold introduces an intrinsic obstruction that is both geometrically unavoidable and locally detectable. The three results established here --- nonlinear non-dilability of the projected flow, additive universality of the $\ell^1$ coboundary diagnostic under symmetry and locality constraints, and finite-time persistence of defect density in finite-range systems --- together provide a coherent description of how information is lost under factorization and how that loss propagates. Importantly, these statements are finite-dimensional and finite-time, and rely only on structural properties of the retraction and locality of interactions, rather than on model-specific features. In this sense, the framework does not compete with existing approximation methods, but rather clarifies the limits they necessarily obey.

Looking ahead, just as differential forms decompose into local and global topological pieces, resolving $C^1(P, F)$ defects suggests a generalized **Hodge decomposition** for dynamical lattice models:
$$ \delta s = d\alpha + \delta\beta + h $$
where $d\alpha$ isolates removable trivial projection errors, $\delta\beta$ captures dynamical correlation flux, and $h$ localizes persistent obstruction invariants (harmonic forms). This decomposition, together with its duality structure, is developed in companion papers [6, 7].

---

## Acknowledgments

No external funding. No conflicts of interest.

---

## References

1. E. H. Lieb and D. W. Robinson, "The Finite Group Velocity of Quantum Spin Systems," *Commun. Math. Phys.* **28** (1972), 251--257.
2. S. Mac Lane, *Categories for the Working Mathematician*, Springer, 1971.
3. J. Klassen and B. M. Terhal, "Two-local qubit Hamiltonians: when are they stoquastic?," *Quantum* **3** (2019), 139.
4. B. Nachtergaele and R. Sims, "Lieb--Robinson Bounds and the Exponential Clustering Theorem," *Commun. Math. Phys.* **265** (2006), 119--130.
5. S. Bravyi, M. B. Hastings, and F. Verstraete, "Lieb--Robinson Bounds and the Generation of Correlations and Topological Quantum Order," *Phys. Rev. Lett.* **97** (2006), 050401.
6. J. H. Carroll, "The Free $\ell^1$ Seminorm on Banach Presheaf Coboundaries," Zenodo, 2026. https://doi.org/10.5281/zenodo.18897080
7. J. H. Carroll, "Hodge Structure and Gauge Equivalence of $\ell^1$ Defect Fields," Zenodo, 2026.
8. J. H. Carroll, "Coordinate-Wise Additivity and the $\ell^1$ Norm on Finite Graph Cochains," Zenodo, 2026. https://doi.org/10.5281/zenodo.18945342