---
title: "Global $\\ell^1$ Rigidity on Finite Graph Cochains"
author: Jeremy H. Carroll
documentclass: amsart
abstract: |
  This paper proves a classification theorem for seminorms on graph cochains, showing that structural independence and symmetry constraints force $\ell^1$ geometry. Any seminorm on $C^1(G,\mathbb{R}^k)$ that connects independent measurements—acting locally across edges and additively across disjoint coordinates—under permutation symmetry must be a scalar multiple of the $\ell^1$ norm. This establishes that the defect field is isometrically equivalent to $L^1(E \times \{1,\dots,k\})$ under the counting measure. The resulting $\ell^1 \otimes \ell^1$ metric demonstrates why total variation, graph cuts, and projection obstruction correlation measures inevitably restrict to sparse $\ell^1$ aggregation.
---

## 1. Introduction

This paper completes a trilogy studying projection obstructions on presheaf coboundaries:

- **Paper 000** [6] establishes that projecting dynamics onto a product-state manifold creates a geometric curvature obstruction over correlation defects.
- **Paper 001** [7] demonstrates that aggregation across edges must follow an $\ell^1$ rule.

A central mathematical vulnerability remains: why should the local diagnostic norm itself, operating on the $k$-dimensional measurement channels (the stalks), assume an $\ell^1$ geometry?

Rather than engineering axioms to manufacture an $\ell^1$ result, we derive the full diagnostic form strictly from fundamental structural physics. When forced to respect both axes of separability—edges and coordinates—the diagnosis becomes globally rigid.

---

## 2. $\ell^1$ Characterization on Graph Cochains

**Theorem 2.1.** Let $G=(V,E)$ be a finite directed graph and consider the cochain space
$$ C^1(G,\mathbb{R}^k)=\bigoplus_{e\in E}\mathbb{R}^k. $$

Let $\nu:C^1(G,\mathbb{R}^k)\to\mathbb{R}_{\ge0}$ be a seminorm satisfying:

1. **Edge locality**
   $$ \nu(\delta)=\sum_{e\in E}\nu_e(\delta_e) $$
2. **Coordinate symmetry**
   $$ \nu_e(x_{\sigma(1)},\dots,x_{\sigma(k)}) = \nu_e(x_1,\dots,x_k) $$
   for every permutation $\sigma$.
3. **Coordinate additivity**
   If $x,y\in\mathbb{R}^k$ have disjoint coordinate support ($\mathrm{supp}(x) \cap \mathrm{supp}(y) = \varnothing$ where $\mathrm{supp}(x) = \{i : x_i \neq 0\}$), then
   $$ \nu_e(x+y)=\nu_e(x)+\nu_e(y). $$
4. **Graph invariance**
   For any graph isomorphism $\sigma:G\to G'$,
   $$ \nu_{G'}(\sigma_*\delta)=\nu_G(\delta). $$

Then there exists $\alpha > 0$ such that
$$ \nu(\delta)=\alpha\sum_{e\in E}\|\delta_e\|_1. $$

**Proof.**

By edge locality it suffices to classify the seminorm $\nu_e$ on $\mathbb{R}^k$.

Let $x=(x_1,\dots,x_k)$. Decompose
$$ x=\sum_{i=1}^k x_i \hat{e}_i. $$

The vectors $x_i \hat{e}_i$ have disjoint coordinate support, so coordinate additivity gives
$$ \nu_e(x)=\sum_{i=1}^k\nu_e(x_i \hat{e}_i). $$

Since $\nu_e$ is a seminorm, it is absolutely homogeneous, providing
$$ \nu_e(x_i \hat{e}_i)=|x_i|\nu_e(\hat{e}_i). $$

By coordinate symmetry,
$$ \nu_e(\hat{e}_i)=w_e $$
for all $i$.

Hence
$$ \nu_e(x)=w_e\sum_{i=1}^k |x_i|=w_e\|x\|_1. $$

Thus across the entire graph,
$$ \nu(\delta)=\sum_{e\in E} w_e\|\delta_e\|_1. $$

Finally, graph invariance implies all intrinsic weights coincide:
$$ w_e=\alpha. $$

Therefore
$$ \nu(\delta)=\alpha\sum_{e\in E}\|\delta_e\|_1. $$
$\square$

## Corollary 2.2 (Discrete $L^1$ Structure of the Defect Space)

Under the hypotheses of Theorem 2.1, the cochain space equipped with the diagnostic seminorm satisfies

$$
(C^1(G,\mathbb{R}^k),\nu)
\cong
L^1(E\times\{1,\dots,k\})
$$

with respect to the counting measure.

**Proof.**

By Theorem 2.1,

$$
\nu(\delta)
=
\alpha\sum_{e\in E}\|\delta_e\|_1.
$$

Writing $\delta_{e,i}$ for the $i$-th coordinate of $\delta_e$, we obtain

$$
\nu(\delta)
=
\alpha\sum_{e\in E}\sum_{i=1}^k |\delta_{e,i}|.
$$

Define

$$
f:E\times\{1,\dots,k\}\to\mathbb{R}
$$

by

$$
f(e,i)=\delta_{e,i}.
$$

Then

$$
\nu(\delta)
=
\alpha\|f\|_{L^1}.
$$

Thus the diagnostic space is isometrically equivalent to  
$L^1(E\times\{1,\dots,k\})$ under the counting measure.  
$\square$


---

## 3. Structural Consequences

### 3.1 Coarea Duality ($k = 1$)

For scalar signals, the classified norm has a distinguished topological property.

**Fact 3.1 (Discrete Coarea Formula** [2, 3]**).** For $v: V \to \mathbb{R}$:
$$ \text{TV}_G(v) = \int_{-\infty}^{\infty} |\partial V_t| \, dt $$
where $V_t = \{m : v_m > t\}$ and $|\partial V_t|$ counts edges crossing the boundary.

When boundary conditions force a binary partition ($v_a = 1, v_b = 0$), $\ell^1$ minimization recovers the minimum $s$-$t$ cut via max-flow/min-cut [5].

**Remark 3.2.** For $k > 1$, the total variation $\sum_e \|v_n - v_m\|_1$ decomposes (by Theorem 2.1) as a sum of $k$ independent scalar total variations, each individually satisfying the coarea formula.

### 3.2 The Geometry of the Defect Field

The explicit inclusion of **Coordinate Additivity** formally captures the physical independence of disparate measurement channels. Permutation symmetry and seminorm subadditivity alone permit pathological metrics like the $\ell^\infty$ maximum norm or the Euclidean $\ell^2$ norm. The strict structural requirement that physically isolated defect channels—the orthogonal coordinates—must accumulate their structural signatures linearly thereby forcing the $\ell^1$ stalk geometry.

Thus, the unique seminorm compatible with the stated structural principles of locality, measurement independence, and symmetry is the $\ell^1$ metric: $\ell^1 \otimes \ell^1$.

Conceptually, our theorem establishes that the defect space restricts to:
$$ C^1(G,\mathbb{R}^k) \cong L^1(E \times \{1,\dots,k\}) $$
whenever the diagnostic respects independent components. This serves as a finite combinatorial analogue of Kakutani's (1941) concrete characterization of abstract $L$-spaces [1]. Additivity across independent structural components forces the $\ell^1$ geometry over the counting measure. Defect fields thus behave strictly as discrete 1-forms whose absolute total variation tracks graph cuts and sparse obstructions [3].

---

## Acknowledgments

No external funding. No conflicts of interest.

---

## References

1. Kakutani, S. (1941). *Concrete representation of abstract $(L)$-spaces and the mean ergodic theorem*. Annals of Mathematics, 42(2), 523-537.
2. Fleming, W. H., & Rishel, R. (1960). *An integral formula for total gradient variation*. Archiv der Mathematik, 11(1), 218-222.
3. Chambolle, A., et al. (2010). *An introduction to total variation for image analysis.* In: Theoretical Foundations and Numerical Methods for Sparse Recovery. De Gruyter.
4. Rockafellar, R. T. (1970). *Convex Analysis.* Princeton University Press.
5. Ford, L. R., & Fulkerson, D. R. (1956). *Maximal flow through a network.* Canadian Journal of Mathematics, 8, 399–404.
6. Carroll, J. H. (2025). *Single Obstruction Theory: Projection Nonlinearity, $\ell^1$ Rigidity, and Density Scaling.* Zenodo. https://doi.org/10.5281/zenodo.18896777
7. Carroll, J. H. (2026). *The Free $\ell^1$ Seminorm on Banach Presheaf Coboundaries.* Zenodo. https://doi.org/10.5281/zenodo.18897081
