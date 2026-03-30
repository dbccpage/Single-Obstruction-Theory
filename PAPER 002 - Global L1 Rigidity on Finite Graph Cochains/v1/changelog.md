# Changelog — Paper 002: Coordinate-Wise Additivity and the l1 Norm on Finite Graph Cochains


This document traces the evolution of **Publication 002** from its initial drafts through the rigorous adversarial review process, resulting in the final frozen `v021` preprint.

## Evolution Summary
The core mathematical journey of this paper involved moving from conceptually sound but physically underspecified axioms (which inadvertently allowed pathological norm geometries like $\ell^\infty$ and $\ell^2$) to a rigorous formalization of structural independence via **Coordinate Additivity**. The final result isolates the unique $\ell^1 \otimes \ell^1$ metric structure of the defect field and formally establishes its isometric equivalence to a discrete $L^1$ space.

---

### v018 - v021: Final Polish and Metric Formalization (The Frozen Preprint)
*   **v021:** Final formatting and publication polish. Repaired LaTeX encoding corruptions in Corollary 2.2. Corrected citations to include precise Zenodo DOIs for prior works and added Rockafellar (1970) for formal convex analysis context. Adjusted title to *Global ℓ¹ Rigidity on Finite Graph Cochains*. References ordered by humility.
*   **v020:** Introduced *Corollary 2.2*, formally proving that the cochain space equipped with the diagnostic seminorm is isometrically equivalent to $L^1(E \times \{1,\dots,k\})$ under the counting measure. Corrected the theorem to strictly require $\alpha > 0$.
*   **v019:** Journal reformatting. Decompressed the multi-section axiom bloat into a crisp, single-theorem structure. Complete excision of obsolete projection monotonicity references. 
*   **v018:** Mathematical compaction. The proof was structurally cleaned and tightened around the formal explicit axioms, producing a concise and mathematically sound note.

### v013 - v017: The Adversarial Review & Coordinate Additivity
*   **v017:** A critical theoretical breakthrough. Addressed the referee's identification of the $\ell^\infty$ loophole by formally introducing **Coordinate Additivity** (**Axiom 5**). This explicitly formalized the structural independence of measurement channels, forcing linear accumulation and uniquely determining the $\ell^1$ stalk geometry without relying on hidden assumptions.
*   **v016:** Attempted a "pre-emptive strike" against the accusation of hidden coordinate additivity by leaning heavily on subadditivity and projection monotonicity, but failed to logically force equality over upper bounds (still permitting $\ell^\infty$).
*   **v014 - v015:** Structural reorganization under hostile referee criteria. Concepts were robust, but logical gaps remained regarding the step from single-coordinate components to full-vector summation. The proof was still vulnerable to pathological metric choices. 
*   **v013:** Initial major review version. Defined the goal of classifying the diagnostic seminorm $\nu(\delta) = \alpha \sum_e |\delta_e|_1$ using locality, symmetry, and projection monotonicity.

### v001 - v012: Conceptual Foundation
*   Established the conceptual necessity of classifying the metric geometry of the $k$-dimensional measurement channels (the stalks) over the graph's edges.
*   Iteratively stripped away physical jargon to reveal the underlying mathematical skeleton.
*   Experimented with metric compatibility axioms and projection-based constraints before realizing the necessity of orthogonal coordinate independence.
