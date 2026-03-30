# Changelog -- Paper 001: The Free l1 Seminorm on Banach Presheaf Coboundaries

## v012 / v5.1 -- Final Pre-print Polish
**Date:** March 2026
*   **Version Bump:** Officially incremented to v12.
*   **Markdown Standardization:** Cleaned up YAML headers for automated Pandoc/LaTeX conversions.
*   **Compilation:** Successfully stripped structural constraints and compiled into pure LaTeX format.

---

## v011 / v5.0 -- Quad pre-print hardening
**Date:** March 2026

### Critical fix
- **P3 endomorphism scope gap (Stages 2--3 proof simplification).** The previous proof applied axiom (P3) to the non-endomorphism map iota: R -> V in the Stage 2 lower bound, but (P3) is stated for endomorphisms phi: F(a_e) -> F(a_e). Eliminated the problematic Hahn-Banach upper/lower bound argument in Stage 2 and the scaling argument in Stage 3. The new proof uses Lemma 2.1 (direction independence) plus absolute homogeneity of the seminorm to derive nu_e(delta) = w_e ||delta|| directly. This is mathematically stronger: the proof now uses only endomorphisms in (P3), exactly as stated. Former Stage 4 renumbered to Stage 3.

### Mathematical corrections
- **Definition 1.1:** Changed "functional" to "function" (a seminorm is a function, not a functional in the Banach dual sense).
- **Lemma 2.1 proof wording:** Changed "Because Phi is an arbitrary bounded linear map on the stalk space" to "Because Phi is a bounded linear endomorphism of F(a_e)" to match (P3) scope.
- **P3 parenthetical rewritten:** Removed misleading claim about sufficiency of endomorphisms for full Banach compatibility. Replaced with precise statement: "Combined with Lemma 2.1, this forces the seminorm to depend only on the Banach norm."
- **Section 6.2:** Updated proof-stage reference from "Stage 2" to "Stage 1" and clarified that the mechanism is "direction independence" rather than the former Hahn-Banach reduction.

### Structural changes
- **YAML header:** Replaced project-internal metadata (status, invariance_level, logic_system, substrate) with standard academic fields (keywords, license, doi_series).
- **Changelog removed from paper body:** Moved full version history (v004--v010) to this separate changelog.md file.
- **Version updated:** "v4.1 (preprint)" -> "v5.0 (Pre-print)". Removed redundant "Status: Preprint (companion to...)" line.
- **Notation convention added:** After abstract, added conventions block specifying norm and absolute value notation.
- **Acknowledgments section added:** Before references.

### Reference cleanup
- Removed uncited references: [2] Mac Lane, [4] Bourbaki, [5] Godement.
- Renumbered remaining references.
- Added new reference [5]: J. H. Carroll, "Hodge Structure and Gauge Equivalence of l1 Defect Fields," Zenodo, 2026.
- Updated all in-text citations to match new numbering.

### Content updates
- **Section 6.3:** Changed "three-paper sequence" to "four-paper sequence". Updated item 4 from "Hodge Decomposition (future work)" to cite Paper 003 [5] with concrete description of quotient norm on H^1(G).
- **Section 6.4 (observer language):** Softened "they characterize the structural conditions" to "they correspond to the structural conditions".

---

## v010 / v4.2 (March 2026)
Observer-theoretic grounding:
- Added observer-theoretic interpretation paragraph in Section 6.4: (P1)--(P4) as minimal conditions for consistent local observers on Banach presheaf coboundaries.
- Cross-references Paper 000 Section 1.2 (full development) and Paper 002 Section 3.3 (combinatorial parallel).

## v010 / v4.1 (March 2026)
Cross-paper alignment per external review:
- Added Section 1.4 (Relation to the Combinatorial Classification) as backward anchor to Paper 002, explicitly stating that the present classification is a functional-analytic extension of the finite-dimensional result.
- Added Reference [7] (Paper 002 concept DOI).
- Unified terminology with companion papers: "local additivity", "structural compatibility (functoriality)", "l1 coboundary norm."
- Updated Section 6.3 numbering to reflect the three-paper sequence explicitly.

## v008 / v4.0 (March 2026)
Structural revision per external review:
- Rewrote Discussion Section 6.1 opening: removed hype; reframed result as "conditions under which no alternative exists" rather than "l1 is special."
- Added Section 6.4 (Connection to Dynamical Obstruction Theory): explicit forward-reference establishing that the companion paper's use of l1 is not a modeling choice but structurally forced by (P1)--(P4).
- Added cross-norm positioning sentence to Section 6.2 per Banach space literature awareness.
- Unified vocabulary with companion paper: "coboundary defect" (object), "1-cochain space" (space), "additive diagnostic" (measurement), "l1 coboundary norm" (result).
- Added Reference [6] (companion paper DOI).

## v007 / v3.1 (March 2026)
Erratum:
- Fixed P3-dropped counterexample in Section 4 necessity table: replaced invalid nu = sum_e ||delta_e||^2 (not a seminorm; fails absolute homogeneity) with nu_e(delta) = |x_1| + 2|x_2| on F(a_e) = R^2, a genuine direction-dependent seminorm violating P3.

## v006 / v3.0 (March 2026)
Final surgical edits for release:
- Clarified that the classification is conditional on axioms rather than a universal property of norms.
- Appended clarification that P3 functoriality on stalk endomorphisms suffices to force compatibility.
- Tightened single-edge presheaf isomorphism requirement to mandate compatible restriction maps.
- Downgraded Theorem 5.1 to Proposition 5.1 to correctly reflect its structural corollary status.

## v005 / v2.0 (March 2026)
Major revisions per peer review:
- Clarified that Property P3 (contractive monotonicity) functionally encodes compatibility with Banach geometry.
- Explicitly stated P3 applies to arbitrary bounded linear maps on stalks.
- Reinforced that P1 (additivity) is the primary structural driver forcing the l1 result.
- Reframed the category AFC as a mathematical consequence of the axioms rather than an ad-hoc constraint.
- Reordered the logical flow to emphasize the foundational nature of this manuscript within the overarching program.

## v004 (Final Polish & Structural Finalization)
*   **Stage 2 (Embedding Independence):** Clarified the Hahn-Banach reduction to 1-dimensional analysis. Explicitly noted that two embeddings mapping 1 to equal norms produce identical values of \nu_e, ensuring well-definedness.
*   **Stage 3 (Linearity):** Streamlined the 1-homogeneity argument to apply contractive monotonicity to scaling operations simultaneously in both directions.
*   **Stage 4 (Uniform Weights):** Formalized the isomorphism invariance using explicit restriction functors to single-edge posets, proving uniform weighting precisely.
*   **Categorical Context:** Softened the terminal object claim to "terminal up to positive scalar normalization."
*   **Literature Connections:** Expanded Section 6.3 to explicitly connect contractive monotonicity + Hahn-Banach arguments to classical uniqueness proofs for operator norms.
*   **Title/Abstract:** Added explicit $\ell^1$ references to the title ("The Free \ell^1 Seminorm...") and abstract for immediate theoretical clarity.

---

## v001 - v003 (Conceptual Development)
*   Formalized the 1-cochain space as the free additive Banach object generated by the edges of the poset.
*   Distilled the properties necessary to classify the diagnostic: (P1) Edge-wise Additivity, (P2) Faithfulness, (P3) Contractive Monotonicity, and (P4) Isomorphism Invariance.
*   Developed the central proof utilizing sequential stages: direction independence, factoring through norms, forcing exact linearity via functional bounds, and collapsing independent weights into a single universal scalar.
*   Separated the pure functional analysis from the physical dynamics of Single Obstruction Theory (SOT) to ensure the mathematics stood independently.
