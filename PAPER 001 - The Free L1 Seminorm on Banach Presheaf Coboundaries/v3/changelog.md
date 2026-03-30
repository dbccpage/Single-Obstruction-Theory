# Changelog: v012 to v013
**Paper:** 001 - The Free $\ell^1$ Seminorm on Banach Presheaf Coboundaries
**Date:** March 2026

## Overview of Changes
The transition from v012 to v013 explicitly defines the boundaries and structural load-bearing capacity of Property (P3) (functoriality under bounded linear maps) in the classification theorem. This ensures the theorem accurately attributes the derivation of $\ell^1$ to the full algebra of bounded linear endomorphisms.

## Specific Modifications

### 1. Property (P3) Explicit Bounded Constraint
- **Target:** Section 1.3, Definition of (P3)
- **Change:** Adjusted the parenthetical description to explicitly broadcast the strength of the axiom: *"This condition is intentionally strong: functoriality under all bounded linear endomorphisms forces the seminorm to depend only on the underlying Banach norm, and is the key structural input driving the classification."*
- **Rationale:** Clarifies to the reader that (P3) is the fundamental operator engine that enforces symmetry under linear structure. This prevents any perception that $\ell^1$ emerges randomly; it is structurally dictated precisely by the allowance of all contractive endomorphisms. 

### 2. Discussion Constraints Re-scoped
- **Target:** Section 6.1 (What This Paper Proves)
- **Change:** Added structural concession: *"The uniqueness result is therefore contingent on allowing the full algebra of bounded linear maps; restricting to a smaller class of transformations would admit additional seminorms."*
- **Rationale:** Further defensive buffering against claims of "smuggling" the $\ell^1$ norm. The claim is now bounded perfectly within the axioms.

### 3. Hahn-Banach Terminology Alignment
- **Target:** Lemma 2.0 (1-Dimensional Compatibility)
- **Change:** Modified *"contractive surjection"* to *"bounded linear functional"*.
- **Rationale:** Directly aligns the phrasing strictly with the application of the Hahn-Banach theorem used recursively throughout the lemma, maintaining uncompromising formal consistency.
