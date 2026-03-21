# Changelog: Projection Obstruction Theory (Paper 000)

---

## v028 / v4.0.1 --- External review polish

- **Title**: Changed "Single Obstruction Theory" → "Projection Obstruction Theory" throughout (YAML header, main heading). More accurately describes the paper's content: the obstruction arises from projection, not from being a single object.
- **Theorem 4.2**: Added clarifying clause "in the sense that any other such seminorm factors uniquely through $I$ up to a positive scalar" to make the category-theoretic "initial object" terminology accessible to non-specialists.
- **Appendix A disclaimer**: Added italic disclaimer "This appendix outlines a broader research program and is not required for the results of this paper" at the top of Appendix A to clearly separate speculative material from the proven results.
- **Theorem 4.2 proof sketch**: Added explicit sentence "Concretely, edge-exchange symmetry implies that all edge weights $w_e$ are equal, since any permutation of edges that preserves graph structure must leave $J$ invariant" to make the weight-equalization step transparent.

---

## v028 / v4.0 --- Quad pre-print hardening

- **YAML header**: Replaced project-internal metadata (status, invariance_level, logic_system, substrate) with standard academic fields (title, author, date, version, keywords, license, doi_series).
- **Changelog extracted**: Removed inline changelog from the paper body; moved all historical entries to this separate `changelog.md` file.
- **Version string**: Updated from "v3.3 (preprint)" to "v4.0 (Pre-print)".
- **Duplicate Section 1.3 title**: Renamed Section 1.3 from "Observer-Theoretic Justification of Axioms" (duplicate of Section 1.2) to "Observer-Theoretic Derivation --- Expanded".
- **Removed project-internal code references**: Deleted all `.rs` file references (`derivation_chain.rs`, `fourier_born.rs`) from the paper body and from Appendix cross-references.
- **Removed internal paper labels**: Replaced "Paper 039", "Paper 018", "Paper 042" references with "(forthcoming)" throughout.
- **Reference [18] updated**: Changed from "in preparation, 2026" to proper Zenodo format: `J. H. Carroll, "Hodge Structure and Gauge Equivalence of l1 Defect Fields," Zenodo, 2026.`
- **Observer-theoretic remarks consolidated**: Reduced four redundant remarks after Theorem 4.2 to two: one mathematical remark about conditionality, one observer-theoretic interpretation. Removed the "forced in any universe" remark and the duplicate "Prior Observer-Theoretic Interpretation" remark. Kept the dependency paragraph referencing companion papers.
- **Appendix B merged into Appendix A**: Absorbed the cross-reference table from Appendix B as a paragraph in A.3. Deleted Appendix B entirely to eliminate duplication.
- **Orphan reference [042] fixed**: Replaced `[042] S 10.3` in the formal chain (A.2) with "(forthcoming)".
- **Orphan references removed**: Deleted 10 never-cited references: Grothendieck [4], Troyer-Wiese [2], Abramsky-Brandenburger [8], Pestov [9], Isidori [10], Jakubczyk-Respondek [11], Lang [12], Calabrese-Cardy [13], Kim-Huse [14], Audenaert [15], Golubitsky-Guillemin [16]. Renumbered surviving references [1]--[8] and updated all in-text citations to match.
- **Observer language softened**: Changed "see the computational demonstration in the Axiomatic Gap paper, Section 8, and the Rust implementation in `derivation_chain.rs`" to "see the axiom relaxation analysis in the companion work (forthcoming)".
- **ell^2 description corrected**: Changed "where positive and negative defects can cancel" to "where the Euclidean norm does not aggregate additively over independent components".
- **Notation convention added**: Added "Conventions" paragraph after the Scope paragraph specifying norm and absolute value notation.
- **Acknowledgments section added**: Inserted "No external funding. No conflicts of interest." before References.

### Reference renumbering map (v027 -> v028):
| v027 | v028 | Reference |
|------|------|-----------|
| [1]  | [1]  | Lieb-Robinson (1972) |
| [3]  | [2]  | Mac Lane (1971) |
| [5]  | [3]  | Klassen-Terhal (2019) |
| [6]  | [4]  | Nachtergaele-Sims (2006) |
| [7]  | [5]  | Bravyi-Hastings-Verstraete (2006) |
| [17] | [6]  | Carroll, Paper 001 (2026) |
| [18] | [7]  | Carroll, Paper 003 (2026) |
| [19] | [8]  | Carroll, Paper 002 (2026) |
| [2], [4], [8]--[16] | --- | Removed (never cited) |

---

## v027 / v3.3 --- Observer-theoretic justification of axioms

- Added Section 1.2 (Observer-Theoretic Justification of Axioms): derives Axioms 1--4 as minimal structural conditions for consistent local observers, grounding the l1 diagnostic in an operational criterion rather than unmotivated mathematical assumptions.
- Added Section 1.3 (Observer-Theoretic Justification of Axioms --- Expanded): explicit four-point operational derivation with failure modes for each axiom relaxation, referencing the Axiomatic Gap paper (Section 8).
- Added observer-theoretic interpretation remark after Theorem 4.2 proof sketch.
- Updated Abstract to reference the observer-theoretic grounding (Section 1.2).
- Renumbered former Section 1.2 (Conceptual Overview) to Section 1.4.
- Added Appendix B (The Complete Derivation Chain): connects observer existence (Layer 0) through l1 uniqueness (Layer 1) to quantum mechanics emergence (Layer 2), with explicit cross-references to companion papers.
- Conditionality of all results preserved.

## v026 / v3.2 --- Three-paper escalation ladder alignment

- Rewrote Section 1.1 (Relation to Companion Work) to establish the full three-paper escalation ladder: combinatorics [19] -> functional analysis [17] -> dynamics (this paper).
- Sharpened dependency sentence after Theorem 4.2 to reference both preceding papers.
- Added Reference [19] (Paper 002 concept DOI).
- Unified terminology with companion papers: "local additivity", "structural compatibility (functoriality)", "l1 coboundary norm."

## v025 / v3.1 --- Cross-paper alignment

- Added "Relation to Companion Work" subsection (Section 1.2) explicitly establishing that the l1 diagnostic is structurally forced by the companion classification paper, not introduced ad hoc.
- Added dependency chain sentence in Section 4 linking Theorem 4.2 to the companion paper's classification result.
- Added Reference [17] DOI for companion paper.
- Unified vocabulary with companion paper: "coboundary defect" consistently used.

## v024 / v3.0 --- Structural revision per external review

- Rewrote Abstract to remove hype; foregrounded conditionality of l1 uniqueness.
- Rewrote Introduction for reviewer-focused clarity; added explicit scope disclaimer.
- Theorem 3.1: removed informal "genericity" remark; added explicit C2 smoothness requirement on the conjugating embedding.
- Theorem 4.2: reframed as conditional universality; downgraded philosophical weight; clarified that the real content is additive aggregation of independent defects.
- Theorem 5.1: made constant dependence explicit; tightened cancellation argument via Lieb-Robinson causal structure; specified time window as O(1/J).
- Example 6.1: corrected "diagnosing entanglement" to "witnessing non-product structure".
- Discussion: rewrote opening paragraph; added explicit scope limitation.

## v023 / v2.1 --- Errata corrections

- Corrected Example 6.2: initial rate expression now matches Lemma 5.2.
- Removed redundant qualifier "connected" from commutator notation in Section 5.1.
- Added explicit citation of Reference [5] (Klassen-Terhal) in context.

## v022 / v2.0 --- Major revisions per peer review

- Replaced "projection" with C2 retraction throughout (terminological correction).
- Removed incorrect unique continuation argument (previous Lemma 3.3).
- Strengthened Theorem 3.1: replaced curvature-based non-degeneracy with explicit non-constancy of the full Jacobian DB(m).
- Clarified definition of projected semigroup S_t = Pi . T_t|_M.
- Corrected two-qubit example to a genuinely entangling Hamiltonian.
- Refined categorical formulation of l1 rigidity and clarified its dependence on additivity and symmetry axioms.
- Clarified density scaling argument with explicit use of Lieb-Robinson bounds.
- Addressed all identified structural and mathematical issues from prior version.
- Minor notation and clarity improvements throughout.
