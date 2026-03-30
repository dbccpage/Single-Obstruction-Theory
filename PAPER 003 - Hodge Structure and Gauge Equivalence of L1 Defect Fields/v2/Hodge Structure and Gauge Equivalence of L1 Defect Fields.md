
# Hodge Structure and Gauge Equivalence of $\ell^1$ Defect Fields

**Author:** Jeremy H. Carroll
**Date:** March 2026
**Version:** v3.0 (Pre-print)

---

## Classification of Results

This paper separates rigorous mathematics from original constructions and speculative analogies. Each result is annotated with its epistemic layer:

| Layer | Status | What it contains |
|-------|--------|------------------|
| **A: Theorems** | Established mathematics | Standard results from discrete algebraic topology and discrete $\ell^2$ Hodge theory on finite graphs without 2-cells [1, 7, 8]. |
| **B: Construction** | Original to this paper | The Cohomological $\ell^1$ Norm $\Phi$ (terminology adopted here for the $\ell^1$ quotient norm on graph cohomology), the proof of its sparsity bias, LP cut-duality, and the inflation quantification. |
| **C: Analogy** | Speculative | The structural parallel to anisotropic total variation (graph-TV) denoising in image processing [2, 13]. |

---

## Abstract

The preceding works [14, 15, 16] establish that additive, structure-preserving diagnostics on coboundary spaces uniquely induce an $\ell^1$ geometry under explicit axioms. Given this constraint, a natural question is how to define a gauge-invariant measure of the irreducible component of a defect field.

On finite graphs, classical discrete Hodge theory provides an $\ell^2$-orthogonal decomposition separating exact and harmonic components. However, this decomposition is not compatible with the $\ell^1$ metric: the $\ell^2$-orthogonal projection onto the harmonic space does not, in general, minimize $\ell^1$ cost within a cohomology class.

We study the functional
$$
\Phi([\delta]) = \min_{f \in C^0} \|\delta - d_0 f\|_1,
$$
which is the standard $\ell^1$ quotient norm on $C^1 / \operatorname{im}(d_0)$ (the minimum is attained; see Proposition 7.1). While this optimization problem is classical (appearing in total variation minimization and minimum homologous chain problems [12]), we show that, under the structural constraints identified in [14--16], it is **unique among norms induced via the quotient from the forced $\ell^1$ structure on $C^1$** (Theorem 7.2, Remark 7.7).

We further relate $\Phi$ to discrete Hodge decomposition, prove that $\ell^2$ projection generically inflates $\ell^1$ cost (with an explicit ratio of $3 - 2/n$ on cycle graphs $C_n$), and characterize $\Phi$ via linear programming duality as the dual norm of bounded divergence-free circulations. This provides a unified interpretation connecting cohomology, $\ell^1$ optimization, and network flows, without introducing new optimization machinery.

---

## METHODOLOGICAL NOTE: L1-NATIVE COHOMOLOGY AND DUALITY

**The ℓ² Structure is an Optional Scaffold; The True Theory is Convex-Geometric**

### 1. The Category Shift: From Orthogonality to Duality

This version completes the realization that $\ell^1$ cohomology is a closed, independent mathematical object. The $\ell^2$ Hodge decomposition is strictly **demoted** to an optional analytic coordinate chart. It is not required to parameterize, define, or optimize the defect fields. We have replaced the classical linear decomposition of vector spaces with an **optimization structure on equivalence classes**.

**Key distinction:**
- **Classical (ℓ²):** Subspaces, inner products, orthogonal projections, and dense harmonic representatives.
- **Intrinsic (ℓ¹):** Polyhedral structure, convex duality, LP minimizers, and sparse cycle localization.

### 2. The $\ell^1$-Native Decomposition

The true canonical decomposition intrinsic to this geometry is not orthogonal splitting but **Linear Programming Duality** (Section 10). For any $\delta$, we possess a primal-dual pair derived strictly from the quotient norm $\Phi$:
- **Primal Splitting:** $\delta = d_0 f^* + r^*$, dividing the field into a removable gauge artifact $d_0 f^*$ and an $\ell^1$-minimal irreducible topological obstruction $r^*$.
- **Dual Witness:** Certified by a bounded divergence-free circulation $\phi^*$ ($B^T \phi^* = 0$, $\|\phi^*\|_\infty \leq 1$) that explicitly pairs with $r^*$.

This structure replaces the $\ell^2$ Hodge Decomposition. The inflation ratio ($3 - 2/n$ on cycle graphs, Section 6) quantifies the **geometric misalignment** between $\ell^2$ projection (which spreads mass) and $\ell^1$ optimization (which concentrates mass). This measurable, empirical invariant demonstrates precisely why $\ell^2$ coordinates fail to align with the underlying discrete geometry.

---

## 1. Introduction

The preceding papers in this series isolated the exact geometric magnitude of interaction defects generated when correlated systems are projected onto locally factorized manifolds. Paper 002 [16] established that coordinate-wise additivity forces an $\ell^1$ geometry on finite graph cochains. Paper 001 [15] generalized this to Banach presheaves via functoriality under bounded linear maps. Paper 000 [14] applied this geometric rigidity to show that projecting dynamics onto a product-state manifold creates an $\ell^1$-measurable curvature obstruction that persists at finite density.

A natural next question arises: given a defect field $\delta \in C^1(G)$, how should one decompose it into removable (exact) and irremovable (cohomological) components? The classical tool is the discrete Hodge decomposition, which operates in $\ell^2$. But given the $\ell^1$ structure established in [14--16] as the baseline diagnostic geometry, a tension emerges.

Throughout, we assume the $\ell^1$ geometry established in [14--16]; this paper studies its consequences. Any decomposition or invariant associated with defect fields must therefore be compatible with this geometry. The central problem addressed here is thus not to choose a convenient norm, but to determine the canonical cohomological structure naturally induced by the $\ell^1$ metric.

**Classical Hodge decomposition does not generally hold in $L^1$ Banach spaces**, as they lack the inner-product structure necessary to define orthogonal projections. We do not construct an $\ell^1$ Hodge decomposition. Instead, we present the **$\ell^1$-Native Decomposition** driven purely by convex duality and linear programming. While earlier drafts utilized the $\ell^2$ Hodge decomposition as an algebraic coordinate system, we now establish that it is entirely superseded by the primal-dual optimization structure. The $\ell^2$ frame is demoted to a mere analytic reference, highlighting the internal completeness of the convex-geometric approach.

We demonstrate that the $\ell^1$ quotient norm determines intrinsic magnitude and defines the canonical splitting into gauge-removable and irreducible components. To capture the true physical penalty, we construct the **Cohomological $\ell^1$ Norm**: a well-defined functional $\Phi : H^1(G, \mathbb{R}) \to \mathbb{R}_{\geq 0}$ that evaluates the topological defect not by orthogonal projection, but by infimal $\ell^1$ gauge cost and maximum dual flow pairing.

**Scope and Relation to Existing Work.** We emphasize that the optimization problem $\min_f \|\delta - d_0 f\|_1$ is not new. It appears in several established contexts, including anisotropic total variation on graphs [2, 13], $\ell^1$ regression over incidence matrices [4], the minimum homologous chain problem [12], and is related to Gromov's bounded cohomology [11] in the infinite-dimensional setting. Compressed sensing and basis pursuit [5] exploit the same $\ell^1$ sparsity structure, and shortest cycle basis algorithms [6] address the underlying combinatorial structure. The contribution of this paper is not to introduce a new optimization framework, but to identify this functional as unique among norms induced via the quotient from the forced $\ell^1$ structure on $C^1$. Accordingly, the results here should be understood as a structural interpretation and organization of known optimization objects within a cohomological framework, rather than as the introduction of new algorithms or complexity results.

**Recall (Papers 001--002).** The $\ell^1$ coboundary norm $I(s) = \sum_e \|\delta_e(s)\|$ is the unique (up to positive scalar) edge-additive, faithful, functorial seminorm on the 1-cochain space $C^1(P, F)$ [15, 16]. In the presheaf language of [15], the coboundary is $\delta_e(s) = r_{b,a}(s(b)) - s(a)$. When the Banach presheaf $F$ is the constant sheaf $\mathbb{R}$ on a graph $G$, this reduces to $(d_0 f)(e) = f(v) - f(u)$, the total norm $I(s)$ becomes $\|d_0 f\|_1$, and the quotient norm $\Phi([\delta]) = \min_f I(s - d_0 f)$ measures the irreducible cost after gauge optimization. This paper develops the structure of $\Phi$.

**Notation bridge.** The following dictionary connects the presheaf notation of [14, 15] to the graph notation used in the remainder of this paper:

| Presheaf notation (Papers 000--001) | Graph notation (this paper) |
|-------------------------------------|----------------------------|
| Poset $P$, covering relations $E_{\mathrm{cov}}(P)$ | Graph $G = (V, E)$ |
| Banach presheaf $F$, stalks $F(x)$, restrictions $r_{b,a}$ | Constant sheaf $\mathbb{R}$, identity restrictions |
| Coboundary $\delta_e(s) = r_{b,a}(s(b)) - s(a)$ | Discrete derivative $(d_0 f)(e) = f(v) - f(u)$ |
| $\ell^1$ coboundary norm $I(s) = \sum_e \lVert\delta_e(s)\rVert$ | $\lVert d_0 f \rVert_1 = \sum_e \lvert (d_0 f)_e \rvert$ |

**Conventions.** Throughout this paper, $G = (V,E)$ denotes a finite, connected, undirected graph. Each edge is assigned an arbitrary but fixed orientation, used only for algebraic bookkeeping; all results are independent of this choice. We work over the scalar field $\mathbb{R}$. Norms are denoted $\lVert \cdot \rVert$ with appropriate subscripts ($\ell^1$, $\ell^2$, $\ell^\infty$); absolute values of scalars are denoted $|\cdot|$. The extension to vector-valued defects $\delta \in C^1(G, \mathbb{R}^k)$ proceeds component-wise and is discussed in Section 10.

---

## 2. Gauge Equivalence **(Layer A/B)**

Before constructing the decomposition machinery, we introduce the central physical notion that motivates the entire analysis.

A defect field $\delta \in C^1(G)$ records the local projection error across each edge. However, the absolute value of $\delta$ on any single edge is not physically meaningful: it depends on the choice of local reference state at each vertex. A **gauge transformation** is a reassignment of these local reference states, parameterized by a vertex function $f \in C^0(G) = \mathbb{R}^{|V|}$. We use "gauge equivalence" in the sense of equivalence under reassignment of local reference frames, analogous to the gauge freedom of electromagnetic potentials $A \mapsto A + d\Lambda$.

**Definition 2.1 (Gauge Equivalence).** Two defect fields $\delta, \delta' \in C^1(G)$ are **gauge equivalent** if their difference is an exact gradient:
$$ \delta \sim \delta' \iff \delta - \delta' \in \operatorname{im}(d_0) $$

where $d_0 : C^0 \to C^1$ is the discrete exterior derivative defined in Section 3. The equivalence class $[\delta] = \delta + \operatorname{im}(d_0)$ is the **gauge class** of $\delta$.

The physically meaningful quantity is not $\delta$ itself but its gauge class $[\delta]$. The natural gauge-invariant magnitude of an obstruction is therefore:

$$ \operatorname{Cost}(\delta) = \min_{f \in C^0} \|\delta - d_0 f\|_1 $$

This is precisely the $\ell^1$ quotient norm on $C^1 / \operatorname{im}(d_0)$. It represents the minimal $\ell^1$ cost achievable over all gauge-equivalent representatives. We will show that this quantity defines a norm on the first cohomology group $H^1(G, \mathbb{R})$ and admits a clean dual formulation connecting it to the topological cycle structure of $G$.

---

## 3. The Discrete de Rham Complex **(Layer A)**

Let $C^0 = \mathbb{R}^{|V|}$ denote the space of **$0$-cochains** (vertex functions) and $C^1 = \mathbb{R}^{|E|}$ denote the space of **$1$-cochains** (edge fields). Each edge $e$ carries its fixed orientation $e = (u,v)$.

**Definition 3.1 (Discrete Exterior Derivative).** The operator $d_0 : C^0 \to C^1$ is the graph difference operator:
$$ (d_0 f)(e_{uv}) = f(v) - f(u) $$

Its matrix representation is the signed incidence matrix $B \in \mathbb{R}^{|E| \times |V|}$, with $B_{e,v} = +1$, $B_{e,u} = -1$ for each oriented edge $e = (u,v)$.

**Definition 3.2 (Discrete Codifferential / Divergence).** The adjoint $d_0^* : C^1 \to C^0$ is defined with respect to the standard $\ell^2$ inner products on $C^0$ and $C^1$:
$$ \langle d_0 f, \omega \rangle_{\ell^2} = \langle f, d_0^* \omega \rangle_{\ell^2} $$

Explicitly, $d_0^* = B^T$ and the **divergence** of a $1$-cochain $\omega$ at a vertex $u$ is the net signed flow:
$$ (d_0^* \omega)(u) = \sum_{e \text{ incoming at } u} \omega(e) - \sum_{e \text{ outgoing from } u} \omega(e) $$

The discrete de Rham complex for a graph without $2$-cells is:
$$ C^0 \xrightarrow{d_0} C^1 \xrightarrow{0} 0 $$

---

## 4. The Hodge Laplacian and Harmonic Cochains **(Layer A)**

Following Eckmann [1], Horak--Jost [7], and Lim [8], the full $1$-form Laplacian on a simplicial complex is:

$$ \Delta_1 = d_0 \, d_0^{*} + d_1^{*} \, d_1 $$

**Remark 4.1 (Convention and Missing 2-Cells).** For a graph (a 1-dimensional simplicial complex), there are no $2$-cells. Consequently $d_1 \equiv 0$, and the Laplacian collapses to:

$$ \Delta_1 = d_0 \, d_0^* \quad \text{(graphs without 2-cells)} $$

**Definition 4.2.** A $1$-cochain $\omega \in C^1$ is **harmonic** if $\Delta_1 \omega = 0$: $\mathcal{H}^1(G) = \ker \Delta_1$.

**Proposition 4.3.** *For a graph without $2$-cells, $\ker \Delta_1 = \ker d_0^*$.*

*Proof.* $\ker d_0^* \subseteq \ker \Delta_1$ is immediate. Conversely, $\Delta_1 \omega = 0$ implies $0 = \langle d_0 d_0^* \omega, \omega \rangle_{\ell^2} = \|d_0^* \omega\|_{\ell^2}^2$, so $d_0^* \omega = 0$. $\blacksquare$

**Proposition 4.4.** *If $G$ is connected, $\dim \mathcal{H}^1(G) = \beta_1(G) = |E| - |V| + 1$.*

---

## 5. The Discrete Hodge Decomposition **(Layer A)**

On a general continuous manifold, the Hodge theorem splits any 1-form into three orthogonal components: $\omega = d\alpha + \delta \beta + h$ (exact, coexact, and harmonic). However, because our state space is a finite graph with no 2-cells, $d_1 = 0$, its adjoint $d_1^* = 0$, and the coexact term vanishes entirely. The decomposition reduces to exactly two functional pieces.

**Theorem 5.1 (Bipartite Hodge Decomposition).** *Every $\delta \in C^1(G)$ decomposes algebraically uniquely as:*
$$ \delta = \delta_{\text{ex}} + \delta_{\text{harm}}, \quad \delta_{\text{ex}} \in \operatorname{im}(d_0), \quad \delta_{\text{harm}} \in \ker d_0^*, \quad \delta_{\text{ex}} \perp_{\ell^2} \delta_{\text{harm}} $$

*Proof.* By the orthogonal complement theorem in finite dimensions, $C^1 = \operatorname{im}(d_0) \oplus (\operatorname{im}(d_0))^\perp$. Since $\langle d_0 f, h \rangle_{\ell^2} = \langle f, d_0^* h \rangle_{\ell^2}$ for all $f, h$, we have $(\operatorname{im}(d_0))^\perp = \ker(d_0^*)$. Therefore $C^1 = \operatorname{im}(d_0) \oplus \ker(d_0^*)$ with the two summands $\ell^2$-orthogonal. $\blacksquare$

**Remark 5.2 (Finite-Dimensional Availability).** This theorem explicitly relies on the finite-dimensionality of the graph. Infinite-dimensional $L^1$ spaces lack the inner-product structure necessary to define orthogonal projections, making $L^1$ Hodge theory structurally different from the $L^2$ case (cf. Kakutani's characterization of abstract $L$-spaces [17]). We do not attempt an $\ell^1$ Hodge decomposition. Instead, we use the $\ell^2$ Hodge decomposition as an algebraic coordinate system on $C^1(G)$ --- guaranteed to exist in finite dimensions --- and then evaluate its components under the $\ell^1$ norm. The resulting mismatch reflects the incompatibility between orthogonal projection in $\ell^2$ and sparsity structure in $\ell^1$.

**Remark 5.3 (Topological Interpretation).** Under this framework, $\operatorname{im}(d_0)$ corresponds to potential difference relationships (gauge transformations), while $\ker d_0^*$ captures network circulations. The harmonic component $\delta_{\text{harm}}$ is the gauge-invariant core, unchanged under $\delta \mapsto \delta - d_0 g$. For trees ($\beta_1 = 0$), all defects are exact and trivially gauge-removable. For graphs with loops ($\beta_1 > 0$), any non-zero harmonic component constitutes an irreducible topological obstruction.

---

## 6. The $\ell^1 / \ell^2$ Tension **(Layer A/B)**

**Remark 6.1 (Layer A).** $\|x + y\|_1 \leq \|x\|_1 + \|y\|_1$, with equality iff $x_e y_e \geq 0$ for all $e$. This is the standard triangle inequality.

**Remark 6.2 (Layer A).** Applying the triangle inequality to the Hodge decomposition: $\|\delta\|_1 \leq \|\delta_{\text{ex}}\|_1 + \|\delta_{\text{harm}}\|_1$, with equality iff there is edgewise sign compatibility between the exact and harmonic components.

**Remark 6.3.** Generic sign conflicts make the inequality strict. Thus, the $\ell^2$ algebraic Hodge projection operator generically yields strictly larger $\ell^1$ component sums except in sign-compatible cases.

**Proposition 6.4 (Failure of $\ell^2$ Hodge Minimization for $\ell^1$ Cost) (Layer B).** Let $\delta \in C^1(G)$ and let $\delta = \delta_{\mathrm{ex}} + \delta_{\mathrm{harm}}$ be its $\ell^2$ Hodge decomposition. Then:

1. The harmonic component does not, in general, minimize $\ell^1$ cost over the cohomology class $[\delta]$:
   $$\|\delta_{\mathrm{harm}}\|_1 \geq \Phi([\delta]),$$
   with strict inequality for generic $\delta$.

2. Equality holds if and only if $\delta_{\mathrm{harm}}$ is already an $\ell^1$-optimal representative of its cohomology class, which requires sign compatibility between the harmonic component and any exact correction.

In particular, the $\ell^2$-orthogonal projection onto $\ker d_0^*$ is not an $\ell^1$-optimal representative of the cohomology class.

*Proof.* By definition, $\Phi([\delta]) = \min_{f \in C^0} \|\delta - d_0 f\|_1 \leq \|\delta_{\mathrm{harm}}\|_1$ since $\delta_{\mathrm{harm}} = \delta - d_0 f_{\ell^2}$ for some $f_{\ell^2}$. Strict inequality holds whenever a different gauge representative achieves lower $\ell^1$ cost. By the crosspolytope geometry of the $\ell^1$ ball, the $\ell^2$-optimal representative (which minimizes Euclidean distance to $\ker d_0^*$) generically diffuses mass across coordinates, while the $\ell^1$-optimal representative concentrates mass on minimal support. These coincide only when the harmonic projection is already sparse (sign-compatible). The examples below demonstrate strict inequality on all cycle graphs $C_n$, $n \geq 3$. $\blacksquare$

### 6.1 Triangle Graph **(Layer B)**

**Example 6.5.** On $C_3$ with $\beta_1 = 1$, cycle vector $c = (1,1,1)^T$. A sparse local defect $\delta = (1,0,0)^T$ resolves via $\ell^2$ projection to:
- $\delta_{\text{harm}} = \frac{1}{3}(1,1,1)^T$, $\quad \delta_{\text{ex}} = \frac{1}{3}(2,-1,-1)^T$
- $\|\delta_{\text{ex}}\|_1 + \|\delta_{\text{harm}}\|_1 = \frac{4}{3} + 1 = \frac{7}{3} > 1 = \|\delta\|_1$
- Inflation ratio: $7/3 \approx 2.33$

### 6.2 Square Cycle **(Layer B)**

**Example 6.6.** On $C_4$ with $\delta = (1,0,0,0)^T$:
- $\delta_{\text{harm}} = \frac{1}{4}(1,1,1,1)^T$, $\quad \delta_{\text{ex}} = \frac{1}{4}(3,-1,-1,-1)^T$
- $\|\delta_{\text{harm}}\|_1 = 1$, $\quad \|\delta_{\text{ex}}\|_1 = \frac{3}{4} + \frac{1}{4} + \frac{1}{4} + \frac{1}{4} = \frac{6}{4} = \frac{3}{2}$
- $\|\delta_{\text{ex}}\|_1 + \|\delta_{\text{harm}}\|_1 = \frac{5}{2} > 1 = \|\delta\|_1$
- Inflation ratio: $5/2 = 2.5$

### 6.3 Inflation Ratio on Cycle Graphs **(Layer B)**

**Proposition 6.7 ($\ell^2$ Inflation Ratio on $C_n$).** *For a single-edge defect $\delta = \mathbf{e}_1 = (1, 0, \ldots, 0)^T$ on the cycle graph $C_n$ ($n \geq 3$), the $\ell^2$ Hodge decomposition inflation ratio is:*

$$ \frac{\|\delta_{\text{ex}}\|_1 + \|\delta_{\text{harm}}\|_1}{\|\delta\|_1} = 3 - \frac{2}{n} $$

*Proof.* The harmonic space of $C_n$ is $\ker(d_0^*) = \operatorname{span}(\mathbf{1})$, where $\mathbf{1} = (1,1,\ldots,1)^T$. The $\ell^2$-orthogonal projection onto $\ker(d_0^*)$ gives:
$$\delta_{\text{harm}} = \frac{\langle \delta, \mathbf{1} \rangle}{\langle \mathbf{1}, \mathbf{1} \rangle} \mathbf{1} = \frac{1}{n}\mathbf{1}$$
$$\delta_{\text{ex}} = \delta - \delta_{\text{harm}} = \left(\frac{n-1}{n}, \frac{-1}{n}, \ldots, \frac{-1}{n}\right)$$

Computing the $\ell^1$ norms:
$$\|\delta_{\text{harm}}\|_1 = n \cdot \frac{1}{n} = 1$$
$$\|\delta_{\text{ex}}\|_1 = \frac{n-1}{n} + (n-1) \cdot \frac{1}{n} = \frac{2(n-1)}{n}$$

The inflation ratio is:
$$\frac{\|\delta_{\text{ex}}\|_1 + \|\delta_{\text{harm}}\|_1}{\|\delta\|_1} = \frac{\frac{2(n-1)}{n} + 1}{1} = \frac{2n - 2 + n}{n} = \frac{3n - 2}{n} = 3 - \frac{2}{n}$$

This grows monotonically with $n$ and approaches 3 as $n \to \infty$. This inflation reflects the incompatibility between $\ell^2$ projection and $\ell^1$ geometry, rather than an intrinsic property of the defect field. $\blacksquare$

**Remark 6.8 (Crosspolytope Bias).** There is a geometric reason why the $\ell^2$ harmonic projection generically increases $\ell^1$ magnitude. The mismatch stems from the fundamental difference between Euclidean balls ($\ell^2$) and crosspolytopes ($\ell^1$) in high dimensions. The $\ell^2$ orthogonal projection minimizes Euclidean distance but naturally diffuses mass across coordinates uniformly (e.g., $1/3, 1/3, 1/3$). The $\ell^1$ cost, dictated by the crosspolytope geometry, privileges sparse, extreme configurations (corners). When mapping a sparse exact defect onto the harmonic cycle space, $\ell^2$ projection destroys its sparsity -- an inflation directly proportional to the loss of corner-localization.

---

## 7. The Cohomological $\ell^1$ Norm **(Layer B)**

This section develops the **Cohomological $\ell^1$ Norm**, a term we adopt for the $\ell^1$ quotient norm on $C^1/\operatorname{im}(d_0)$. The quotient norm construction is standard in functional analysis [4, 9]; the $\ell^1$ quotient norm on homology classes appears in the bounded cohomology literature [11] and the minimum homologous chain problem [12]. The contribution here is not the optimization framework itself, but the identification, under the additivity and functoriality assumptions established in [14--16], of $\Phi$ as the unique gauge-invariant norm on $H^1(G)$ induced by the forced $\ell^1$ geometry (Remark 8.6).

### 7.1 The $\ell^1$ Quotient Norm

As established in Section 2, the scalar magnitude invariant under arbitrary local reference rescalings is the **$\ell^1$ quotient norm** on the space of cochains modulo exact gradients $C^1 / \operatorname{im}(d_0)$:
$$ \operatorname{Cost}(\delta) = \min_{f \in C^0} \|\delta - d_0 f\|_1 $$

### 7.2 Descent to Cohomology

The gauge class $[\delta] = \delta + \operatorname{im}(d_0)$ is an affine subspace of $C^1(G)$. By linear programming duality, the minimum $\ell^1$ norm on this affine space is attained by a representative intimately linked to the cycle structure of the graph. The optimization:

$$ \operatorname{Cost}(\delta) = \min_{r \in [\delta]} \|r\|_1 $$

evaluates to a purely cohomological constraint. It depends only on the cohomology class $[\delta] \in H^1(G, \mathbb{R})$, abandoning the need for any $\ell^2$ harmonic reference coordinate.

### 7.3 The Cohomological Norm

**Proposition 7.1 (Existence of Minimizers).** *The minimum $\min_{f \in C^0} \|\delta - d_0 f\|_1$ is attained for every $\delta \in C^1(G)$.*

*Proof.* The objective $f \mapsto \|\delta - d_0 f\|_1$ is continuous and coercive on $C^0 / \ker(d_0) \cong \mathbb{R}^{|V|-1}$ (since $\ker(d_0) = \operatorname{span}(\mathbf{1})$ for connected $G$, the restriction $d_0|_{\operatorname{span}(\mathbf{1})^\perp}$ is injective, and by equivalence of norms on finite-dimensional spaces there exists $c > 0$ with $\|d_0 f\|_1 \geq c\|f\|_2$ for all $f \perp \mathbf{1}$, hence $\|d_0 f\|_1 \to \infty$ as $\|f\|_2 \to \infty$ on this quotient). A continuous coercive function on a finite-dimensional space attains its infimum [9]. $\blacksquare$

*Every minimizer $r^* = \delta - d_0 f^*$ satisfies the first-order optimality condition $B^T s^* = 0$ where $s^* \in \partial\|\cdot\|_1(r^*)$ is a subgradient [9, Section 23]. That is, $s^*$ is a divergence-free flow bounded entrywise by 1.*

**Theorem 7.2 (Cohomological $\ell^1$ Norm).** *The functional*

$$ \Phi : H^1(G, \mathbb{R}) \to \mathbb{R}_{\geq 0}, \qquad \Phi([\delta]) = \min_{r \in [\delta]} \|r\|_1 $$

*is a norm on $H^1(G, \mathbb{R})$.*

*Proof.*
**Positive definiteness.** If $\Phi([\delta]) = 0$, then by Proposition 7.1 the minimum is attained: there exists $f^*$ with $\|\delta - d_0 f^*\|_1 = 0$, hence $\delta = d_0 f^*$, so $[\delta] = 0$. Conversely, $[\delta] = 0$ gives $\delta \in \operatorname{im}(d_0)$, so $\Phi([\delta]) = 0$.

**Absolute homogeneity.** For $\lambda \neq 0$: $\Phi([\lambda \delta]) = \min_f \|\lambda \delta - d_0 f\|_1 = \min_f \|\lambda(\delta - d_0(f/\lambda))\|_1 = |\lambda| \min_g \|\delta - d_0 g\|_1 = |\lambda| \Phi([\delta])$, where $g = f/\lambda$. For $\lambda = 0$: $\Phi([0]) = 0$.

**Triangle inequality.** Let $f^*, g^*$ be minimizers for $[\delta]$ and $[\delta']$ respectively (existing by Proposition 7.1). Choosing $f = f^* + g^*$ in the minimization for $[\delta + \delta']$:
$$\Phi([\delta + \delta']) = \min_f \|\delta + \delta' - d_0 f\|_1 \leq \|(\delta - d_0 f^*) + (\delta' - d_0 g^*)\|_1 \leq \|\delta - d_0 f^*\|_1 + \|\delta' - d_0 g^*\|_1 = \Phi([\delta]) + \Phi([\delta'])$$
$\blacksquare$

### 7.4 Sparsity Bias

**Remark 7.3 (Geometric Sparsity Bias).** $\ell^1$ minimization inherently contacts the bounding faces of the crosspolytope geometry on low-dimensional faces (minimizing support). Consequently, optimization concentrates defects onto minimal edge cycles rather than expanding them as uniform fractional obstructions like the $\ell^2$ harmonic projection inevitably does.

### 7.5 Structure on Cycle Bases and Minimum Weight Combinations

While minimizing $\ell^1$ cost generally necessitates linear programming, the structural geometry of the cycle space allows for a direct evaluation on the graph's loops under favorable conditions.

**Theorem 7.4 (Evaluation on Vertex-Disjoint Cycle Bases).** *Suppose $G$ admits a cycle basis $\{C_1, \ldots, C_{\beta_1}\}$ for $H^1(G)$ in which the cycles are pairwise vertex-disjoint (and therefore edge-disjoint). Given the cohomology class $[\delta] = \sum_{i=1}^{\beta_1} a_i [C_i]$, the cohomological norm is:*

$$ \Phi([\delta]) = \sum_{i=1}^{\beta_1} |a_i| \|C_i\|_1 $$

*Proof.* Since the cycles are vertex-disjoint, their vertex sets $V_i$ are pairwise disjoint. The potential $f \in C^0$ decomposes as $f = \sum_i f_i$ where $f_i$ is supported on $V_i$. The exact form $d_0 f$ restricted to edge set $E_i$ depends only on $f_i$ (vertices outside $V_i$ contribute zero to edges in $E_i$). Therefore:

$$\min_f \|\delta - d_0 f\|_1 = \sum_{i=1}^{\beta_1} \min_{f_i \in \mathbb{R}^{V_i}} \sum_{e \in E_i} |a_i (C_i)_e - (d_0 f_i)_e|$$

On each component, the cohomology class $[a_i C_i]$ is one-dimensional, and any exact correction on a single cycle changes the representative by $d_0 f_i$ for $f_i$ supported on $V_i$. Since $C_i$ is a single cycle, the minimum $\ell^1$ representative of the class $[a_i C_i]$ has cost $|a_i| \|C_i\|_1$ (any exact correction on a cycle merely redistributes, never reduces, the total absolute circulation). $\blacksquare$

**Remark 7.5 (Existence of Vertex-Disjoint Cycle Bases).** A vertex-disjoint cycle basis exists precisely for *cactus graphs* (connected graphs in which every 2-edge-connected component is a single cycle). For general graphs---including $K_4$, whose $\beta_1 = 3$ independent cycles necessarily share vertices---no vertex-disjoint cycle basis exists, and the general case requires the linear program to resolve interactions, corresponding to the **minimum weight homologous chain** [12]. When cycles share vertices but not edges, the decomposition may still hold, but the proof requires a more delicate LP analysis showing that the shared-vertex coupling constraints are independently satisfiable.

**Remark 7.6 (Geometry of the Cycle Polytope).** Under the $\Phi$ functional, the metric geometry of $H^1(G)$ behaves structurally as a polyhedral metric space whose unit locus mirrors the network's bounded cycle polytope ($\operatorname{conv}\{\pm C_1, \ldots, \pm C_{\beta_1}\}$).

**Remark 7.7 (Uniqueness of $\Phi$).** The norm $\Phi$ is unique among norms obtained via the standard quotient construction from the $\ell^1$ norm on $C^1$ through the quotient map $C^1 \to C^1/\operatorname{im}(d_0)$. This follows from the standard construction: the quotient norm $\|[x]\| = \inf\{\|y\| : y \in [x]\}$ is the largest norm on the quotient space making the projection non-expansive [9, Section 2]. Since [14--16] establish $\ell^1$ as the uniquely forced norm on $C^1$, the quotient construction uniquely determines $\Phi$. Choosing any other gauge-invariant norm on $H^1$ (e.g., the $\ell^2$ norm on harmonic representatives) would break compatibility with the induced $\ell^1$ geometry.

---

## 8. Total Variation Denoising and Fast Algorithms **(Layer C)**

The gauge optimization $\min_f \|\delta - B f\|_1$ exhibits structural isomorphism to **anisotropic total variation (TV) denoising** extensively developed in image filtering [2, 13]. Although the optimization is formally identical to graph total variation minimization, its role here is different: it arises as the quotient norm induced by the uniquely determined $\ell^1$ geometry on coboundary spaces [14--16], rather than as a regularization principle or signal recovery objective. Setting the mapping between computational models:

| Imaging                 | Defect Topology                |
|-------------------------|--------------------------------|
| Image Signal            | Vertex Potential ($f$)          |
| Image Gradient ($\nabla$)| Exterior Derivative ($d_0 = B$)  |
| Observed Gradient ($y$)  | Source Defect Field ($\delta$)   |
| TV Residual ($y - \nabla u$)| Topological Obstruction ($r$) |

Consequently, the optimization objective directly mirrors **graph total variation (graph-TV)**. Where classical TV identifies structural borders (sparse semantic image edges), the framework localizes purely topological features (**sparse cycle contradictions**).

**Computational Remark.** This overlap permits the use of algorithms designed for large-scale imaging tasks. Rather than utilizing generic $O(|E|^3)$ interior point bounds, the $\ell^1$ quotient norm is computable using splitting protocols (Chambolle--Pock primal-dual [2], Split Bregman, ADMM), which admit per-iteration complexity scaling linearly in $|E|$. Whether these methods achieve comparable convergence rates in the graph cohomology setting is an empirical question not addressed here; we note only the formal structural correspondence.

---

## 9. Cut Duality and Flow Circulation **(Layer B)**

We establish that the topological magnitude of the norm is strictly characterized by valid internal network configurations.

**Theorem 9.1 (Cut Duality).**
$$ \Phi([\delta]) = \max_{\phi} \left\{ \langle \phi, \delta \rangle : \|\phi\|_\infty \leq 1, \; d_0^* \phi = 0 \right\} $$

*Proof.* The primal problem $\min_{f} \|\delta - B f\|_1$ is reformulated as a linear program by introducing auxiliary variables $t_e \geq 0$:

$$\text{Primal: } \min_{f, t} \sum_e t_e \quad \text{subject to} \quad -t_e \leq \delta_e - (Bf)_e \leq t_e, \quad t_e \geq 0$$

Let $\phi^+_e, \phi^-_e \geq 0$ be the dual variables for the upper and lower bound constraints respectively. Setting $\phi_e = \phi^+_e - \phi^-_e$, the dual problem becomes:

$$\text{Dual: } \max_{\phi} \langle \phi, \delta \rangle \quad \text{subject to} \quad B^T \phi = 0, \quad |\phi_e| \leq 1 \text{ for all } e$$

The constraint $B^T \phi = d_0^* \phi = 0$ requires $\phi$ to be divergence-free (a circulation). The bound $|\phi_e| \leq 1$ constrains $\phi \in B_\infty$. Strong duality holds because both the primal and dual are feasible finite-dimensional LPs: the primal is feasible ($f = 0$ is feasible) with objective bounded below by zero, and the dual is feasible ($\phi = 0$ satisfies $B^T \phi = 0$ and $\|\phi\|_\infty = 0 \leq 1$) [4, Chapter 5]. $\blacksquare$

**Remark 9.2 (Dual Norm of Bounded Circulations).** The $d_0^* \phi = 0$ condition fixes $\phi \in Z_1(G)$, the cycle space. The bounded infinity constraint yields:

$$ \Phi([\delta]) = \max_{\phi \in Z_1(G) \cap B_\infty} \langle \phi, \delta \rangle $$

Hence, $\Phi$ resolves as the exact **dual norm of bounded circulations**. Within the network interpretation, it isolates the maximal potential flow pairing compatible with the measured contradiction field $\delta$. In contrast to $\ell^2$ Hodge theory, which decomposes via orthogonal projection, the $\ell^1$ cohomological structure is governed by convex duality between defect fields and bounded circulations.

---

## 10. The $\ell^1$-Native Decomposition **(Layer B)**

Because the unique geometry of the coboundary space is dictated by $\ell^1$, the true canonical decomposition is not orthogonal, but derived strictly from primal-dual optimality. This decomposition replaces the role of the classical Hodge splitting as the canonical structure in this geometry, requiring identically zero reliance on an inner product.

**Definition 10.1 (Primal Minimizer).** The primal minimization problem $\min_{f \in C^0} \|\delta - d_0 f\|_1$ yields an optimal vertex potential $f^*$.

**Definition 10.2 (Dual Witness).** The dual maximization problem from Theorem 9.1 yields an optimal bounded circulation $\phi^* \in Z_1(G) \cap B_\infty$.

**Remark 10.2a ($\ell^2$-Independence of the Dual Constraint).** While we defined $d_0^* = B^T$ via the $\ell^2$ adjoint relationship in Section 3, the dual constraint $B^T \phi = 0$ is purely algebraic: it characterizes $\phi \in \ker(B^T)$, the cycle space $Z_1(G)$, and does not depend on the adjoint interpretation. The entire primal-dual framework of this section uses only the incidence matrix $B$, its transpose $B^T$, the $\ell^1$ norm on $C^1$, and convex optimization---no inner product is required.

**Theorem 10.3 ($\ell^1$-Native Decomposition).** *Every defect field $\delta \in C^1(G)$ admits an intrinsically $\ell^1$ decomposition:*
$$ \delta = \delta_{\text{exact}} + \delta_{\text{irr}} $$
*where:*
1. $\delta_{\text{exact}} = d_0 f^*$ *for some primal minimizer $f^* \in C^0$ of $\|\delta - d_0 f\|_1$.*
2. $\delta_{\text{irr}} = \delta - d_0 f^*$ *is an $\ell^1$-minimal representative of $[\delta]$, satisfying* $\|\delta_{\text{irr}}\|_1 = \Phi([\delta])$.

*This optimal decomposition is certified by a dual witness $\phi^*$ satisfying:*
$$ d_0^* \phi^* = 0, \quad \|\phi^*\|_\infty \leq 1, \quad \langle \phi^*, \delta_{\text{irr}} \rangle = \|\delta_{\text{irr}}\|_1 $$

*The $\ell^1$-minimal representative $\delta_{\text{irr}}$ may not be unique: the set of optimal representatives $\{r \in [\delta] : \|r\|_1 = \Phi([\delta])\}$ forms a convex polytope (as a level set of the convex objective on an affine subspace). However, the value $\Phi([\delta]) = \|\delta_{\text{irr}}\|_1$ is uniquely determined.*

**Remark 10.4 (Sparsity vs. Diffusion).** In $\ell^2$, the splitting $\delta = d_0 \alpha + h$ is a linear projection where $h$ diffuses uniformly to minimize the sum of squares. In the $\ell^1$-native decomposition, the splitting pairs a primal exact correction with a polyhedral dual flow. Because $\ell^1$ minimization inherently seeks the bounding faces of the crosspolytope, $\delta_{\text{irr}}$ naturally concentrates mass on minimal cycle supports (sparsity). The mismatch between this sparse concentration and the dense diffusion of the $\ell^2$ harmonic projection is precisely what the inflation ratio ($3 - 2/n$) quantifies.

---

## 11. Extension to Vector-Valued Defects **(Layer A/B)**

For $\delta \in C^1(G, \mathbb{R}^k)$, define the separable $\ell^1$ norm $\|\delta\|_1 = \sum_{e \in E} \sum_{j=1}^k |\delta_{e,j}|$ (i.e., $\ell^1$ over edges, then $\ell^1$ over components). Under this norm, the decomposition and cohomological norm extend component-wise: $\Phi([\delta]) = \sum_{j=1}^k \Phi([\delta^{(j)}])$.

---

## 12. Discussion

### 12.1 What This Paper Establishes

Once $\ell^1$ is forced at the cochain level (Paper 002), the canonical cohomological measurement compatible with the induced $\ell^1$ geometry is the $\ell^1$ quotient norm $\Phi$, governed entirely by convex duality rather than orthogonal decomposition. The framework is now mathematically closed: there are no dangling dependencies on $\ell^2$ structure for defining cohomology classes. The $\ell^1$-Native Decomposition provides the canonical decomposition compatible with the $\ell^1$ geometry, in contrast to the $\ell^2$ Hodge decomposition.

The conceptual progression is:
1. **Convex-Geometric Cohomology** (Sections 2-4): Establishes the topological framework.
2. **$\ell^1/\ell^2$ Misalignment** (Section 6, Layer B): Quantifies the geometric incompatibility between Euclidean projection and the intrinsic crosspolytope geometry, measuring $\ell^2$ cost inflation at an empirical ratio of $3 - 2/n$ on cycle graphs.
3. **Cohomological norm** (Theorem 7.2, Layer B): Formalizes $\Phi([\delta]) = \min_r \|r\|_1$ as the $\ell^1$ quotient norm evaluating the defect's cycle space structure.
4. **Primal-Dual Native Decomposition** (Section 10, Layer B): Elevates Cut Duality (Theorem 9.1) to define the canonical $\ell^1$ decomposition of a defect field into a removable potential and an irreducible, algorithmically sparse topological obstruction, permanently replacing the role of classical Hodge theory within this geometry.
5. **Image processing parallelism** (Section 8, Layer C): Notes the structural correspondence to TV denoising methods.

### 12.2 Relation to Prior Work

The discrete de Rham complex on graphs is due to Eckmann [1]. The bipartite Hodge decomposition on graphs without 2-cells is standard (see Lim [8] for a modern treatment). The LP duality formulation of $\Phi$ connects to classical network flow theory (Ford--Fulkerson [3]) and the coarea formula for graph total variation (Chambolle et al. [2]). The $\ell^1$ quotient norm on cohomology is related to Gromov's bounded cohomology [11], though the finite-dimensional setting here avoids the subtleties of the infinite-dimensional theory. The quotient norm construction itself is standard in functional analysis [9]. The discrete calculus framework is developed systematically in [10].

### 12.3 Position in the Unified Program

This paper completes the structural program initiated in the preceding works by resolving the final open question: given that $\ell^1$ is the uniquely forced geometry on coboundary defects, what is the canonical gauge-invariant decomposition and measurement of such defects?

The progression is now complete:

1. **Combinatorial Level (Paper 002)** [16]: Local additivity over disjoint coordinate supports and edge separability force $\ell^1$ geometry on finite cochains.
2. **Functional Level (Paper 001)** [15]: Structural compatibility (functoriality under bounded linear maps) extends this rigidity to Banach presheaves.
3. **Dynamical Level (Paper 000)** [14]: Projection of linear dynamics onto nonlinear manifolds generates intrinsic coboundary defects measured in this geometry, persisting at non-vanishing density.
4. **Cohomological Level (this paper)**: The forced $\ell^1$ geometry induces a canonical quotient norm $\Phi$ on $H^1$, providing the unique representation among norms induced via the quotient from the forced $\ell^1$ structure on $C^1$ (Remark 7.7). The $\ell^2$ Hodge decomposition provides a linear parameterization of cohomology classes; $\Phi$ measures their true intrinsic magnitude.

Thus, the $\ell^1$ structure is not an isolated phenomenon but persists across combinatorial, functional, dynamical, and topological layers. The measurement, decomposition, and optimization of defect fields are not independent choices, but are constrained by a single underlying geometric requirement.


### 12.4 Limitations and Future Work

The inflation analysis in Section 6 is restricted to cycle graphs $C_n$ with a single-edge localized defect. A complete characterization of the inflation factor for general graphs remains open. The TV denoising analogy in Section 8 is structural rather than rigorous; formalizing the correspondence and establishing convergence rates is left to future work. The restriction to graphs without 2-cells means the coexact term vanishes. Appendix A provides the complementary combinatorial perspective via the discrete coarea formula, establishing that the $\ell^1$ geometry decomposes into level-set cuts. Extending the analysis to simplicial 2-complexes, where the full tripartite Hodge decomposition $\delta = d\alpha + \delta\beta + h$ is active, is a natural next step.

### 12.5 Closing Remark

The results of this paper do not introduce new optimization problems or algorithms; rather, they identify the structural role of an existing $\ell^1$ minimization within a cohomological framework. When combined with the preceding classification results [14--16], this shows that the measurement, decomposition, and optimization of defect fields are not independent choices, but are constrained by a single underlying geometric requirement. The $\ell^1$ quotient norm $\Phi$ thus serves as the consistent endpoint of this structure, linking local defect aggregation, global topology, and convex optimization in a common framework.

---

## Acknowledgments

No external funding. No conflicts of interest.

---

## References

[1] B. Eckmann, "Harmonische Funktionen und Randwertaufgaben in einem Komplex," *Commentarii Mathematici Helvetici* **17** (1944/45), 240--255.

[2] A. Chambolle and T. Pock, "A first-order primal-dual algorithm for convex problems with applications to imaging," *J. Math. Imaging Vision* **40** (2011), 120--145.

[3] L. R. Ford and D. R. Fulkerson, *Flows in Networks*, Princeton University Press, 1962.

[4] S. Boyd and L. Vandenberghe, *Convex Optimization*, Cambridge University Press, 2004.

[5] E. J. Cand\`es and T. Tao, "Decoding by linear programming," *IEEE Trans. Inform. Theory* **51** (2005), 4203--4215.

[6] J. D. Horton, "A polynomial-time algorithm to find the shortest cycle basis of a graph," *SIAM J. Comput.* **16** (1987), 358--366.

[7] D. Horak and J. Jost, "Spectra of combinatorial Laplace operators on simplicial complexes," *Adv. Math.* **244** (2013), 303--336.

[8] L.-H. Lim, "Hodge Laplacians on Graphs," *SIAM Review* **62** (2020), 685--715.

[9] R. T. Rockafellar, *Convex Analysis*, Princeton University Press, 1970.

[10] R. Grady and A. Polimeni, *Discrete Calculus*, Springer, 2010.

[11] M. Gromov, "Volume and bounded cohomology," *Publications Math\'ematiques de l'IH\'ES* **56** (1982), 5--99.

[12] T. K. Dey, A. N. Hirani, and B. Krishnamoorthy, "Optimal homologous cycles, total unimodularity, and linear programming," *SIAM J. Comput.* **40** (2011), 1026--1044.

[13] L. I. Rudin, S. Osher, and E. Fatemi, "Nonlinear total variation based noise removal algorithms," *Physica D: Nonlinear Phenomena* **60** (1992), 259--268.

[14] J. H. Carroll, "Projection Obstruction Theory - Retraction Nonlinearity, l1 Rigidity, and Density Scaling," Zenodo, 2026. https://doi.org/10.5281/zenodo.19151803

[15] J. H. Carroll, "The Free $\ell^1$ Seminorm on Banach Presheaf Coboundaries," Zenodo, 2026. https://doi.org/10.5281/zenodo.19152115

[16] J. H. Carroll, "Coordinate-Wise Additivity and the $\ell^1$ Norm on Finite Graph Cochains," Zenodo, 2026. https://doi.org/10.5281/zenodo.19152599

[17] S. Kakutani, "Concrete representation of abstract $(L)$-spaces and the mean ergodic theorem," *Annals of Mathematics* **42** (1941), 523--537.

---

## Appendix A: Cut Decomposition and $\ell^1$ Duality on Finite Graphs

*Absorbed from the archived companion paper "Cut Decomposition and $\ell^1$ Duality on Finite Graphs: The Combinatorial Architecture of Total Variation" (J.H. Carroll, March 2026).*

### A.1 Level Sets and Graph Cuts

The total variation (the discrete $\ell^1$ gradient norm) connects directly to the coboundary operator:
$$ \operatorname{TV}_G(v) = \|d_0 v\|_1 = \sum_{(x,y) = e \in E} |v_x - v_y| $$

We parameterize the scalar field into level sets via a threshold $\tau \in \mathbb{R}$:
$$ V_\tau = \{ x \in V \mid v_x > \tau \} $$

The boundary of any level set $V_\tau$ is a graph cut — the set of edges with exactly one endpoint in $V_\tau$.

### A.2 The Discrete Coarea Formula

**Theorem A.1 (Discrete Coarea Formula).** *For any $v \in \mathbb{R}^V$ on a graph $G$:*
$$ \operatorname{TV}_G(v) = \int_{-\infty}^{\infty} |\partial V_\tau| \, d\tau $$

*Proof.* For a single edge $e = (x,y)$ with $v_x > v_y$:
$$ |v_x - v_y| = \int_{-\infty}^{\infty} \mathbf{1}_{\tau \in [v_y, v_x)} \, d\tau = \int_{-\infty}^{\infty} \mathbf{1}_{e \in \partial V_\tau} \, d\tau $$
Summing over all edges and exchanging the (finite) sum and integral:
$$ \operatorname{TV}_G(v) = \int_{-\infty}^{\infty} |\partial V_\tau| \, d\tau $$
$\blacksquare$

**Corollary A.2 (Discrete Summation Form).** *If $v$ takes $r$ distinct values $v_{(1)} < v_{(2)} < \cdots < v_{(r)}$, then:*
$$ \operatorname{TV}_G(v) = \sum_{j=1}^{r-1} (v_{(j+1)} - v_{(j)}) \, |\partial V_{v_{(j)}}| $$

### A.3 The $\ell^1$ Specificity

**Proposition A.3 ($\ell^1$ Specificity of the Linear Coarea Decomposition).** *For $p > 1$, there exists no function $g_p : \mathbb{R} \to \mathbb{R}_{\geq 0}$ such that*
$$ |a - b|^p = \int_{-\infty}^{\infty} g_p(\tau) \, \mathbf{1}_{\tau \in [\min(a,b), \max(a,b))} \, d\tau $$
*for all $a, b \in \mathbb{R}$.*

*Proof.* Setting $a = L > 0$ and $b = 0$ gives $L^p = \int_0^L g_p(\tau) \, d\tau$ for all $L > 0$. By the Fundamental Theorem of Calculus, $g_p(\tau) = p \tau^{p-1}$ a.e. on $(0, \infty)$. For general $a > b \geq 0$: $\int_b^a p \tau^{p-1} \, d\tau = a^p - b^p \neq (a - b)^p$ when $b > 0$ and $p > 1$. Contradiction. $\blacksquare$

### A.4 TV-Cut Relaxation Tightness and Max-Flow Duality

**Theorem A.4 (TV-Cut Relaxation Tightness).** *For distinguished vertices $s, t \in V$ and $\mathcal{F}_{s,t} = \{ v : V \to [0,1] \mid v_s = 1, v_t = 0 \}$:*
$$ \min_{v \in \mathcal{F}_{s,t}} \operatorname{TV}_G(v) = \min_{\substack{S \subseteq V \\ s \in S, \, t \notin S}} |\partial S| $$

*Proof.* Binary indicators $v = \mathbf{1}_S$ achieve $\operatorname{TV}_G(\mathbf{1}_S) = |\partial S|$, giving $\leq$. For $\geq$: by the coarea formula, $\operatorname{TV}_G(v) = \int_0^1 |\partial V_\tau| \, d\tau$, and each $V_\tau$ is a valid $s$-$t$ cut. $\blacksquare$

By the Ford-Fulkerson max-flow/min-cut theorem:
$$ \min_{v \in \mathcal{F}_{s,t}} \operatorname{TV}_G(v) = \min_S |\partial S| = \max_{f \in \operatorname{Flow}(s,t)} \operatorname{val}(f) $$

### A.5 Connection to the Cohomological Norm

Applying the discrete coarea formula to the cohomological $\ell^1$ norm $\Phi$:
$$ \Phi([\delta]) = \min_{f \in C^0} \int_{-\infty}^{\infty} |\partial V_\tau(\delta - d_0 f)| \, d\tau $$

The cohomological norm $\Phi$ evaluates as a minimization over gauge-equivalent representatives, where each representative's $\ell^1$ cost decomposes into a superposition of thresholded cycle cuts. The optimal defect pattern concentrates on domain-wall-like structures — minimal separating surfaces that distinguish rigid regions of the network.

### Appendix A References

[A1] A. Chambolle, "An algorithm for total variation minimization and applications," *J. Math. Imaging Vision* **20** (2004), 89--97.

[A2] Y. Boykov and V. Kolmogorov, "An experimental comparison of min-cut/max-flow algorithms for energy minimization in vision," *IEEE Trans. PAMI* **26** (2004), 1124--1137.

[A3] W. H. Fleming and R. Rishel, "An integral formula for total gradient variation," *Archiv der Mathematik* **11** (1960), 218--222.

[A4] C. Villani, *Optimal Transport: Old and New*, Springer, 2009.
