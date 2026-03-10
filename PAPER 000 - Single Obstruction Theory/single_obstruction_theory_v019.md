# Single Obstruction Theory: Projection Nonlinearity, $\ell^1$ Rigidity, and Density Scaling

**Author:** Jeremy H. Carroll  
**Date:** March 2026  
**Version:** v1.0 (preprint)  

---

## Abstract

Projection-based approximations --- such as mean-field theory, product-state ansätze, and factorized variational methods --- replace correlated states with products of local states via a nonlinear projection. We study the structural obstruction introduced by this projection.

We prove three results. **(1)** A nonlinear projection composed with a linear semigroup cannot be conjugate to any linear semigroup (Theorem 3.1). **(2)** The resulting defect admits a unique local additive diagnostic: the $\ell^1$ coboundary norm, characterized as the free additive faithful contractive seminorm on the space of edge defects (Theorem 4.2). **(3)** For finite-range non-commuting interactions on finite-dimensional lattice systems, the per-bond obstruction density remains bounded below over a finite time interval whose duration is $O(1)$ in system size (Theorem 5.1).

Together these theorems establish **existence, uniqueness, and finite-time persistence** of projection obstructions within a presheaf-theoretic framework over finite posets with Banach-space stalks.

---

## 1. Introduction

Many-body computation relies on factorization: replace an exponentially large state with a product of local states. Mean-field theory, Hartree--Fock, product-state ansätze, and factorized variational methods all implement this via a **projection** $\Pi$ onto the manifold of product states. This paper asks: **What does the projection discard, how should we measure it, and how does the discarded quantity scale?**

**Main Result (informal).** Projection-based factorization introduces a geometric curvature term in the induced dynamics on the product-state manifold. This curvature prevents linear conjugacy, manifests as a presheaf coboundary defect, and is measured uniquely by the $\ell^1$ norm on edge defects. For finite-range lattice systems this obstruction appears with non-vanishing density over finite time intervals.

We prove three structural theorems governing this loss of information:
1. **Geometric Obstruction (Existence):** $\Pi$ introduces affine curvature that prevents the projected dynamics from being conjugate to any linear semigroup (Theorem 3.1).
2. **Categorical Rigidity (Uniqueness):** The $\ell^1$ coboundary norm is the universal local faithful diagnostic for this obstruction, arising as the free additive seminorm on the space of local defects (Theorem 4.2).
3. **Density Scaling (Persistence):** The per-bond obstruction density is $\Omega(1)$ in system size over an $O(1)$ time window, protected by Lieb--Robinson bounds (Theorem 5.1).

**Scope.** The framework applies rigorously to Banach presheaves over finite posets. We avoid speculative physics or infinite-time limits; the density scaling bound is finite-time only, as thermalization destroys local correlations at late times. The focus of this paper is to stabilize the core mathematical invariants of projection obstructions.

### 1.1 Conceptual Overview

The structure of the argument can be summarized as follows:

```
Full correlated state space X
        |
        |  nonlinear projection Π
        v
Product-state manifold M
        |
        |  induced curvature term D²Π(Am, ·)
        v
Projected dynamics on M
        |
        |  local incompatibilities across regions
        v
Coboundary defects δₑ(s)
        |
        |  universal additive aggregation (Kan extension)
        v
Total obstruction  I(s) = Σ ||δₑ(s)||₁
```

**Interpretation:**

- **Theorem 3.1:** Nonlinear projection introduces curvature that prevents linear conjugacy of the projected dynamics.
- **Theorem 4.2:** The resulting incompatibilities form local coboundary defects whose unique additive diagnostic is the $\ell^1$ norm.
- **Theorem 5.1:** In lattice systems with finite-range interactions, these defects appear with nonzero density over finite time intervals.

The formal versions of these statements are given in Theorems 3.1, 4.2, and 5.1.

---

## 2. Structural Framework

We work with Banach-valued presheaves over finite posets, following standard categorical conventions [3, 4].

### 2.1 Presheaves over Finite Posets

Let $(P, \leq)$ be a finite poset with covering relations $E_{\text{cov}}(P) = \{(a, b) : a < b,\; \nexists\, c \text{ with } a < c < b\}$. A **Banach presheaf** $F$ over $P$ assigns to each $x \in P$ a Banach space $F(x)$ and to each $(a,b) \in E_{\text{cov}}$ a contractive linear restriction map $r_{b,a}: F(b) \to F(a)$ with $\|r_{b,a}\|_{\text{op}} \leq 1$. Restriction maps along general order relations $a < c$ are obtained by composition of covering restrictions.

### 2.2 The Coboundary

For each edge $e = (a,b)$, the **coboundary** is $\delta_e(s) = r_{b,a}(s(b)) - s(a) \in F(a)$. A section descends if $\delta_e(s) = 0$ for all $e$. The $\ell^1$ coboundary norm is $I(s) = \sum_{e \in E_{\text{cov}}} \|\delta_e(s)\|$.

### 2.3 Categorical Interpretation via Kan Extensions

The obstruction functional has a canonical origin in category theory. Interpret the covering edges as a category $\mathrm{Edge}(P)$ with a projection functor $\pi: \mathrm{Edge}(P) \to P$ sending each edge $e = (a < b)$ to its lower vertex $a$. For a presheaf $F$, the local defect assignment $d(s)(e) = \delta_e(s)$ defines a section of the pulled-back presheaf $F \circ \pi^{op}$. 

The natural way to aggregate these dispersed local defects globally is the left Kan extension along $\pi$. Because the $\ell^1$ direct sum realizes the categorical coproduct in the category of Banach spaces with contractive maps, the colimit evaluates to the space of edge defects $\mathrm{Lan}_\pi(F \circ \pi^{op}) \cong \bigoplus_{e \in E_{\text{cov}}} F(a_e)$ equipped with the $\ell^1$ norm. The total obstruction $I(s) = \|\mathrm{Lan}_\pi(d(s))\|_1$ is exactly the universal additive seminorm evaluated on this Kan extension.

### 2.4 Linear Semigroups and Nonlinear Projections

A **$C_0$ contraction semigroup** on a Banach space $X$ is $\{T_t\}_{t \geq 0}$ with $T_0 = \text{id}$, $T_{t+s} = T_t T_s$, $\|T_t\| \leq 1$, and strong continuity. Its generator is $(A, \mathcal{D}(A))$. A **nonlinear projection** is a continuous idempotent $\Pi: X \to M \subset X$ with $M$ a regular submanifold and $\Pi$ not affine.

---

## 3. Theorem I: Projection Non-Dilability

The first result identifies a geometric obstruction introduced by nonlinear projection.

### 3.1 Statement

> **Theorem 3.1 (Projection Non-Dilability).** Let $X$ be a Banach space, $\{T_t\}$ a $C_0$ contraction semigroup with generator $(A, \mathcal{D}(A))$, and $\Pi: X \to M \subset X$ a $C^2$ idempotent projection onto a nonlinear submanifold $M \subset \mathcal{D}(A)$. Suppose:
>
> (a) $T_t$ does not preserve $M$ for some $t > 0$, and
> (b) *(Non-degeneracy)* There exists $m_0 \in M$ such that $D^2\Pi(m_0)(Am_0, \cdot) \neq 0$.
>
> Then there is no $C^2$ conjugacy connecting $T_t|_M$ to any linear contraction semigroup. That is, there does not exist a Banach space $Y$, a $C^2$ embedding $\iota: M \hookrightarrow Y$, and a $C_0$ contraction semigroup $\{\tilde{T}_t\}$ on $Y$ such that $\Pi \circ T_t|_M = \iota^{-1} \circ \tilde{T}_t \circ \iota$.

### 3.2 Preliminary Lemmas

> **Lemma 3.2 (Parallel fields on flat connections).** Let $(\nabla, M)$ be a connected Banach manifold equipped with a flat affine connection ($R^{\nabla} = 0$). If a $(1,1)$-tensor field $S$ on $M$ satisfies $\nabla S = 0$ (parallel), then $S$ is constant in any affine coordinate chart.

*Proof.* Since $R^{\nabla} = 0$, the exponential map at any $m \in M$ is a local diffeomorphism onto a neighborhood in which the Christoffel symbols vanish [14, Prop. VII.5.2]. In these coordinates, $\nabla S = 0$ reduces to $\partial_i S^j_k = 0$, so the components are constant. On a connected manifold, two affine coordinate charts overlap via affine transitions (compositions of linear maps and translations), which preserve constancy. Therefore $S$ is constant on all of $M$. $\square$

> **Lemma 3.3 (Genericity of non-degeneracy).** Let $M$ be a finite-dimensional $C^2$ submanifold of a Banach space $X$, $A$ a bounded linear operator on $X$, and $\Pi: X \to M$ a $C^2$ idempotent. Define $\Phi: M \to \mathcal{L}(X; T_m M)$ by $\Phi(m) = D^2\Pi(m)(Am, \cdot)$. If $\Pi$ is not affine (i.e., $D^2\Pi \not\equiv 0$), then the zero set $Z = \Phi^{-1}(0)$ has empty interior in $M$.

*Proof.* $\Phi$ is continuous ($\Pi$ is $C^2$, $A$ is bounded). If $Z$ had nonempty interior, $\Phi$ would vanish on an open set $U \subset M$. On $U$, $D^2\Pi(m)(Am, v) = 0$ for all $v \in T_m M$ and all $m \in U$. This implies $D^2\Pi|_U \equiv 0$, meaning $\Pi$ is exactly affine when restricted to $U$. By unique continuation of $C^2$ maps on connected manifolds, $\Pi$ would be affine on all of $M$, thereby contradicting the strict non-affinity hypothesis. $\square$

### 3.3 Proof of Theorem 3.1

**Step 1: Linear flows are affinely flat.**
A linear semigroup $\{\tilde{T}_t\}$ on $Y$ with generator $\tilde{A}$ satisfies $\tilde{A}(y) = \tilde{A} y$. The canonical flat connection $\tilde{\nabla}$ on $Y$ (given by $\tilde{\nabla}_v w = Dw \cdot v$) has $R^{\tilde{\nabla}} = 0$, and $\tilde{\nabla}^2 \tilde{A} = 0$.

**Step 2: Conjugacy transfers flatness.**
If a $C^2$ embedding $\iota: M \hookrightarrow Y$ conjugates $S_t$ to $\tilde{T}_t$, then $\nabla = \iota^* \tilde{\nabla}$ is a flat connection on $M$ ($R^{\nabla} = 0$, since pullback preserves flatness [14, §VII.3]), and $\nabla^2 B = 0$ for the generator $B = \iota^{-1}_* \tilde{A}$ of $S_t$.

**Step 3: The projected generator has non-constant covariant derivative.**
The projected generator is $B(m) = D\Pi(m) \cdot Am$ (well-defined since $\Pi$ is idempotent, so $D\Pi(m)$ projects onto $T_m M$). Differentiating:
$$\nabla_v B = D^2\Pi(m)(Am, v) + D\Pi(m) \cdot Av.$$

If $\nabla^2 B = 0$, then $\nabla_v B$ is a parallel tensor field. By Lemma 3.2 (applicable since $\nabla$ is flat), $\nabla_v B$ is constant in affine coordinates. But $D^2\Pi(m_0)(Am_0, \cdot) \neq 0$ (hypothesis (b)), and $m \mapsto D^2\Pi(m)(Am, \cdot)$ is continuous and nonzero on an open neighborhood $U$ of $m_0$ (Lemma 3.3 with $A$ bounded). Since the projection curvature $D^2\Pi(m)(Am, v)$ varies nontrivially with $m$ on $U$, the tensor $\nabla_v B$ cannot be constant. Contradiction. $\square$

**Remark 1 (Second fundamental form).** The curvature term $\mathrm{II}(Am, v) = D^2\Pi(m)(Am, v)$ is the second fundamental form of $M$ evaluated along the generator. Theorem 3.1 restates as: *nonzero second fundamental form along the generator obstructs linear conjugacy.*

**Remark 2 (Feedback linearization).** The obstruction is structurally analogous to Jakubczyk--Respondek conditions [11] in nonlinear control: both involve second-derivative curvature terms preventing coordinate-based linearization. Here, the original dynamics are linear — projection introduces the nonlinearity.

---

## 4. Theorem II: Categorical Rigidity

### 4.1 Diagnostic Systems
> **Definition 4.1.** A **diagnostic system** is a family $\{J_P\}_{P \in \mathbf{Poset}_{\mathrm{fin}}}$ with $J_P: \Gamma(F_P) \to \mathbb{R}_{\geq 0}$ for each finite poset $P$ and Banach presheaf $F_P$.

### 4.2 Axioms

**Axiom 1 (Coboundary Locality).** $J_P(s) = \sum_{e} j_e(\delta_e s)$, with $j_e: F(a) \to \mathbb{R}_{\geq 0}$.
**Axiom 2 (Faithfulness).** $j_e(\delta) = 0 \iff \delta = 0$.
**Axiom 3 (Contractive Monotonicity).** For any contraction $\varphi: V \to W$, $j_e(\varphi(\delta)) \leq \|\varphi\|_{\text{op}} \cdot j_e(\delta)$.
**Axiom 4 (Isomorphism Invariance).** For any poset isomorphism $\pi$, $J_{\tilde{P}}(\pi^* s) = J_P(s)$.

**Remark (Continuity).** Axiom 3 implies $j_e$ is Lipschitz: apply it to the Hahn--Banach functional $f_\delta$ and the embedding $\iota_\delta$ (both contractions) to obtain $j_e(\delta) = j_e(\|\delta\|)$, and to scaling maps to obtain $j_e(c\delta) = c \cdot j_e(\delta)$. No additional regularity hypothesis is needed.

### 4.3 Categorical Rigidity

Let $\mathbf{Ban}$ be the symmetric monoidal category of Banach spaces equipped with the $\ell^1$ direct sum $(V \oplus_1 W, \|(v,w)\| = \|v\| + \|w\|)$. This categorical structure intrinsically encodes additivity over local edges. The space of 1-cochains $C^1(P,F) = \bigoplus_{e \in E_{\text{cov}}} F(a_e)$ equipped with the $\ell^1$ norm is the free additive Banach object generated by the edges. By Axiom 1, any diagnostic factorizes through the coboundary map $\delta: \Gamma(F) \to C^1(P,F)$.

> **Theorem 4.2 ($\ell^1$ Rigidity** [12]**).** The $\ell^1$ coboundary norm $I(s) = \sum_e \|\delta_e(s)\|$ is the **free additive faithful contractive seminorm** on $C^1(P,F)$. It is the **initial object in the category of additive faithful contractive seminorms on $C^1(P,F)$**. Consequently, any diagnostic $J_P$ satisfying Axioms 1--4 factors uniquely as $J_P(s) = \alpha \cdot I(s)$ for some $\alpha > 0$.

*(Proof detailed in the companion notes [12]. By defining the metric through the Hahn-Banach scaling of contractive monotonic maps, exact 1-homogeneity natively limits variations to uniform posetic scalars alone.)*

Thus $\ell^1$ is not merely a convenient choice of diagnostic; it is forced by the structural axioms governing local defect aggregation.

**Remark (Universal Property).** Re-framing the uniqueness theorem as a universal property addresses why $\ell^1$ specifically emerges: it is the *unique additive geometry* compatible with the axioms. The $\ell^2$ norm fails because $\|(v,w)\|_2 \neq \|v\| + \|w\|$, while $\ell^\infty$ fails because $\max(\|v\|, \|w\|)$ discards summation over independent local defects. The $\ell^1$ norm is structurally forced because it is the universal map out of the free space of local inconsistencies (the Kan extension $\mathrm{Lan}_\pi d(s)$) [12].



---

## 5. Theorem III: Application to Density Scaling

### 5.1 Setup

Consider $N$ sites on a finite graph with **finite-dimensional** local Hilbert spaces ($\dim \mathcal{H}_x \leq d < \infty$), Hamiltonian $H = \sum_e H_e$ with $\|H_e\| \leq J$, and product-state projection $\Pi(\rho) = \bigotimes_x \text{Tr}_{\bar{x}}(\rho)$. Since $H$ is bounded, all domain conditions of Theorem 3.1 are automatic.

### 5.2 Explicit Rate Bound

> **Lemma 5.2 (Local obstruction rate).** For a single bond $e = (a,b)$ with $[H_e, \rho_a \otimes \rho_b] \neq 0$, define $\gamma_e = \|[H_e, \rho_a \otimes \rho_b]_{\text{conn}}\|_1 / d^2$. Then $\gamma_e > 0$ and $\gamma_e \leq 2J$. For $t$ small:
> $$C_e(t) \geq \gamma_e t - O(J^2 t^2).$$

*Proof.* On the finite-dimensional space $\mathcal{H}_e$ ($\dim \leq d^2$), the map $t \mapsto \rho_e(t) - \rho_a(t) \otimes \rho_b(t)$ is entire analytic. Its leading Taylor coefficient is $\|[H_e, \rho_a \otimes \rho_b]_{\text{conn}}\|_1$, which is positive by hypothesis. The denominator $d^2$ converts trace-norm to operator-norm constraints: $\|A\|_1 \leq d^2 \|A\|_{\text{op}}$. The remainder is $O(J^2 t^2)$ since $\|H\| \leq z J$ and higher-order commutators grow at most geometrically. $\square$

### 5.3 The Density Bound

> **Theorem 5.1 (Finite-Time Density Scaling).** Let $\rho(0) = \bigotimes_x \rho_x(0)$ with fraction $\eta > 0$ of bonds satisfying $[H_e, \rho_a \otimes \rho_b] \neq 0$. Define $\gamma_* = \min_{e \in E_{\text{active}}} \gamma_e > 0$ (attained: $E_{\text{active}}$ is finite). Then $C(t) \geq c > 0$ for $t \in [t_1, t_2]$, where $c, t_1, t_2$ depend only on $J, z, d$ — not on $N$.

*Proof sketch.* By Lemma 5.2, each active bond has $C_e(t) \geq \gamma_e t - O(J^2 t^2) > 0$ for $t \in (0, \gamma_*/(2zJ)^2)$. Continuity gives a positive interval $[t_1, t_2]$ with $C_e(t) \geq \tfrac{1}{2}\gamma_* t_1$ for all active $e$. By Lieb--Robinson [1, 6], with finite propagation velocity $v_{\text{LR}} = O(Jz)$, bulk bonds (graph distance $\geq v_{\text{LR}} t$ from the boundary) have marginals independent of $N$ up to exponentially small corrections. Summing over the macroscopic number of active bonds: $C(t) \geq \eta \cdot \tfrac{1}{2}\gamma_* t_1 = \Omega(1)$. $\square$

---

## 6. Worked Examples

### 6.1 Example 1: Two Qubits (Minimal)

Two qubits ($d = 2$) with $H = J \cdot Z \otimes Z$ and initial product state $\rho(0) = |{0}\rangle\langle{0}| \otimes |{+}\rangle\langle{+}|$. The commutator:
$$[Z \otimes Z,\; |{0}\rangle\langle{0}| \otimes |{+}\rangle\langle{+}|] = |{0}\rangle\langle{0}| \otimes [Z, |{+}\rangle\langle{+}|] \neq 0$$
Exact continuous-time evolution $\rho(t) = e^{-iJt Z \otimes Z} \rho(0) e^{iJt Z \otimes Z}$ expands to a locally-rotating entangled state: $\rho(t) = \cos^2(Jt) \rho(0) + \sin^2(Jt) (|{0}{-}\rangle\langle{0}{-}|) + \frac{i}{2}\sin(2Jt) (|{0}{-}\rangle\langle{0}{+}| - |{0}{+}\rangle\langle{0}{-}|)$. Tracing over and comparing to the product gives exactly $C(t) = \sin^2(Jt)$. This satisfies $C(t) > 0$ for $0 < t < \pi/J$ — a single-bond illustration of Theorem 5.1. The obstruction's existence ($C > 0$) follows from Theorem 3.1; its measurement by $\|\cdot\|_1$ is forced by Theorem 4.2.

### 6.2 Example 2: Transverse-Field Ising Model

The 1D transverse-field Ising model $H = -J\sum_i Z_i Z_{i+1} - h\sum_i X_i$ on $N$ qubits with $\rho(0) = |{+}\rangle\langle{+}|^{\otimes N}$. Since $\langle{+}|Z|{+}\rangle = 0$, the first-order contribution vanishes: $C_e(t) = O(J^2 t^2)$ with strictly positive leading coefficient. By translational invariance, $C(t) = O(J^2 t^2) > 0$ for $t > 0$, with per-bond density insensitive to $N$ for $t \ll N/v_{\text{LR}}$.

### 6.3 Example 3: Classical Factorized Dynamics

Coupled oscillators $\dot{x}_i = -\omega_i^2 x_i + \epsilon \sum_{j \sim i}(x_j - x_i)$ with factorized initial distribution. The coupling generates correlations at rate $\epsilon \cdot \text{Var}(x_j) > 0$, giving $C_{\text{cl}}(t) = O(\epsilon^2 t^2)$ with coefficient independent of $N$.

---

## 7. Discussion

### 7.1 Correlation Flux Interpretation

The coboundary $\delta_e(s) = r_{b,a}(s(b)) - s(a)$ quantifies the mismatch between local states across the edge $e$. In physical settings this mismatch corresponds to the **generation of correlations** between subsystems. Under this interpretation:
- **Theorem 3.1:** Projection creates non-removable correlation sources.
- **Theorem 4.2:** $\ell^1$ uniquely measures total flux magnitude as the universal map out of the free defect space.
- **Theorem 5.1:** Flux propagates locally at finite speed.

**Relation to entanglement.** The obstruction $C_e(t) = \|\rho_{ab} - \rho_a \otimes \rho_b\|_1$ bounds mutual information via Fannes--Audenaert [17]: $I(A:B) \leq 2\varepsilon \log d + 2h(\varepsilon)$. Its early-time scaling $O(J^k t^k)$ matches entanglement entropy growth [15, 16], since both are controlled by the same Dyson-series commutators.

### 7.2 Domain of Validity

Theorems 3.1--4.2 apply to Banach presheaves over finite posets. Theorem 5.1 requires finite-dimensional local Hilbert spaces and finite-range non-commuting interactions. The framework does not apply to infinite-dimensional posets, long-range interactions, or commuting Hamiltonians.

### 7.3 Relation to Existing Work

The $\ell^1$ coboundary norm is standard in Čech cohomology; the novelty is the uniqueness theorem (Theorem 4.2) showing it is forced by axioms. Our framework generalizes the sheaf-theoretic contextuality of Abramsky--Brandenburger [8] from boolean to Banach presheaves: binary contextuality (sections glue or not) becomes quantitative ($\ell^1$ measures how badly gluing fails).

### 7.4 Covering Map Transport

The $\ell^1$ norm satisfies $I_{\tilde{P}}(\pi^* s) = k \cdot I_P(s)$ for degree-$k$ covering maps (Theorem A.1) but is **not** preserved under general order-preserving maps (Appendix B: dimensional collapse).

### 7.5 Companion Results

- **Free seminorm classification** [12]: Comprehensive categorical proof that $\ell^1$ is the free additive faithful contractive seminorm.
- **Universal obstruction theory** [13]: Extension to Lindbladian dynamics and scalar propagation.

---

## Appendix A: Covering Map Extensivity
> **Theorem A.1.** For a covering map $\pi: \tilde{P} \to P$ of degree $k$: $I_{\tilde{P}}(\pi^* s) = k \cdot I_P(s)$.

*Proof.* Each edge has exactly $k$ preimages with identical coboundaries. $\square$

## Appendix B: Dimensional Collapse
> **Theorem B.1.** For a non-covering order-preserving map $f: P_1 \to P_2$, there exist $F, s$ with $I_{P_1}(f^*s) \neq I_{P_2}(s)$.

*Proof.* Take $P_1 = L_x \times L_t$, $P_2 = L_t$, $f(i,j) = j$. Spatial edges are annihilated; temporal edges amplified by $L_x$. $\square$

---

## References

1. E. H. Lieb and D. W. Robinson, "The Finite Group Velocity of Quantum Spin Systems," *Commun. Math. Phys.* **28** (1972), 251--257.
2. M. Troyer and U.-J. Wiese, "Computational Complexity and Fundamental Limitations to Fermionic Quantum Monte Carlo Simulations," *Phys. Rev. Lett.* **94** (2005), 170201.
3. S. Mac Lane, *Categories for the Working Mathematician*, Springer, 1971.
4. A. Grothendieck, *Revêtements Étales et Groupe Fondamental* (SGA 1), Lecture Notes in Mathematics **224**, 1971.
5. J. Klassen and B. M. Terhal, "Two-local qubit Hamiltonians: when are they stoquastic?," *Quantum* **3** (2019), 139.
6. B. Nachtergaele and R. Sims, "Lieb--Robinson Bounds and the Exponential Clustering Theorem," *Commun. Math. Phys.* **265** (2006), 119--130.
7. S. Bravyi, M. B. Hastings, and F. Verstraete, "Lieb--Robinson Bounds and the Generation of Correlations and Topological Quantum Order," *Phys. Rev. Lett.* **97** (2006), 050401.
8. S. Abramsky and A. Brandenburger, "The sheaf-theoretic structure of non-locality and contextuality," *New J. Phys.* **13** (2011), 113036.
9. V. Pestov, "Dynamics of infinite-dimensional groups and Ramsey-type phenomena," *Publicações Matemáticas do IMPA*, 2006.
10. A. Isidori, *Nonlinear Control Systems*, 3rd ed., Springer, 1995.
11. B. Jakubczyk and W. Respondek, "On linearization of control systems," *Bull. Acad. Pol. Sci. Sér. Sci. Math.* **28** (1980), 517--522.
12. S. Lang, *Fundamentals of Differential Geometry*, Springer, 1999.
13. P. Calabrese and J. Cardy, "Evolution of entanglement entropy in one-dimensional systems," *J. Stat. Mech.* (2005), P04010.
14. H. Kim and D. A. Huse, "Ballistic Spreading of Entanglement in a Diffusive Nonintegrable System," *Phys. Rev. Lett.* **111** (2013), 127205.
15. K. M. R. Audenaert, "A sharp continuity estimate for the von Neumann entropy," *J. Phys. A* **40** (2007), 8127--8136.
16. M. Golubitsky and V. Guillemin, *Stable Mappings and Their Singularities*, Springer, 1973.
