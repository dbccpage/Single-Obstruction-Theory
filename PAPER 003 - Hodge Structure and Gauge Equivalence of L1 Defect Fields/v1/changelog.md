# Changelog — Hodge Structure and Gauge Equivalence of ℓ¹ Defect Fields

## v015 / v4.0 (March 2026) — R/G/B Pre-print Hardening

Red Team (adversarial audit), Blue Team (structural integrity), Green Team (synthesis) findings applied:

### CRITICAL fixes
- **Norm notation**: Unified `|·|_1` → `‖·‖_1` throughout (Abstract, Proposition 6.4). Single bars reserved for scalar absolute values.
- **Proposition 7.1 (Existence of Minimizers)**: Promoted from unproven assertion to proven Proposition with explicit coercivity argument and citation [9].
- **Theorem 7.2 (Cohomological Norm) proofs**: Positive definiteness now explicitly depends on Proposition 7.1. Triangle inequality now exhibits the explicit witness `f = f* + g*`. Absolute homogeneity now shows the substitution `g = f/λ`.
- **Theorem 7.4 (Edge-Disjoint Cycles)**: Strengthened hypothesis from "edge-disjoint" to "edge-disjoint and vertex-disjoint" to close a genuine mathematical gap (vertex-sharing couples the LP). Added full proof replacing the sketch. Added Remark 7.5 discussing the vertex-sharing case.
- **Uniqueness claim**: Formalized as Remark 7.7 with precise definition: Φ is the unique norm on H¹(G) *induced by the ℓ¹ norm via the quotient map*. Cited [9] for the quotient norm characterization.
- **Orphan references**: All 5 orphan references ([5] Candès-Tao, [6] Horton, [9] Rockafellar, [10] Grady-Polimeni, [17] Kakutani) now cited in the text.

### MAJOR fixes
- **Changelog**: Moved from paper body to separate file (this file).
- **Example 6.6 arithmetic**: Corrected intermediate display from `3/4 + 3/4` to `3/4 + 1/4 + 1/4 + 1/4` (all 4 terms shown).
- **Abstract**: Changed `inf` to `min` with parenthetical referencing Proposition 7.1 for attainment. Added precision to uniqueness claim.
- **"Coined" → "adopted"**: Toned down novelty claim for "Cohomological ℓ¹ Norm" terminology.
- **Section 7.3 heading**: Renamed from "General Formula" to "Inflation Ratio on Cycle Graphs" (scope-accurate).
- **YAML header**: Replaced project-internal metadata with standard academic fields.

### MINOR fixes
- **Section 6 merged into Section 5**: Former Section 6 (Topological Interpretation, 5 lines) absorbed as Remark 5.3.
- **Section renumbering**: Sections renumbered after merge (old 7→6, 8→7, 9→8, 10→9, 11→10, 12→11).
- **"Epistemic Guide" → "Classification of Results"**: More conventional heading.
- **Notation convention**: Added explicit statement that `‖·‖` denotes norms and `|·|` denotes scalar absolute values.
- **Notation bridge table**: Added explicit presheaf-to-graph dictionary table in Introduction.
- **Complexity claim softened**: "linearly accessible" → "per-iteration linear complexity (convergence rates are an empirical question not addressed here)".
- **Strong duality citation**: Added explicit reference [4, Chapter 5] for LP strong duality.
- **Rockafellar [9]**: Now cited for quotient norm, coercivity, and subdifferential optimality.
- **Grady-Polimeni [10]**: Now cited in Section 11.2 (Relation to Prior Work).
- **Candès-Tao [5]**: Now cited in Scope and Relation to Existing Work paragraph.
- **Horton [6]**: Now cited in Scope and Relation to Existing Work paragraph.

## v014 / v3.2 (March 2026) — Observer-theoretic grounding
- Added remark at end of Section 12.3 giving the observer-theoretic interpretation of the four-level escalation ladder.
- Forward-references Paper 000 Section 1.2; cross-references Papers 001 Section 6.4 and 002 Section 3.3.

## v014 / v3.1 (March 2026) — Referee-hardened revision per external review
- Rewrote Abstract: acknowledged optimization is classical; repositioned contribution.
- Added dependency chain paragraph to Introduction.
- Added "Scope and Relation to Existing Work" paragraph.
- Promoted ℓ²/ℓ¹ incompatibility to formal Proposition.
- Fixed Hodge language throughout.
- Added TV structural-role sentence.
- Tightened "canonical" claims to be conditional on prior axioms [14–16].
- Rewrote Section 12.3 with full four-level escalation ladder.

## v012 / v3.0 (March 2026) — R/G/B Structural Revision
- Restored v010 as base (v011 regression abandoned).
- Added epistemic layer annotations (A/B/C).
- Added explicit C_n inflation ratio proof.
- Corrected Definition 3.2: "adjoint with respect to ℓ² inner products".
- Added cross-references to Papers 000–002 with DOIs.
- Added notation bridge.

## v010 / v2.1 (March 2026) — Final adversarial polish
- Signaled ℓ² projection as coordinate choice.
- Justified existence of optimizers in Theorem 8.1.
- Tempered complexity claims.

## v009 / v2.0 (March 2026) — Major revisions per peer review
- Clarified ℓ¹ quotient norm depends on cohomology class.
- Toned down Theorem 5.1 framing.
- Justified strong duality.

## v008 (March 2026) — Initial preprint submission.
