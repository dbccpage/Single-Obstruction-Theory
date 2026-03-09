# Changelog: Paper 000 -- Single Obstruction Theory

**Paper:** *Single Obstruction Theory: Projection Nonlinearity, l^1 Rigidity, and Density Scaling*
**Author:** Jeremy Carroll (ooutwire)
**Current Version:** v1.0 (preprint) -- file `v019/single_obstruction_theory_v019.md`
**Archive:** `.archive/` (v001--v018, plus original v0.5 snapshot)

---

## Version Map

The archive uses sequential folder numbering (v001--v018) which does NOT correspond 1:1 to the internal paper version numbers (v0.2--v1.7). The mapping is:

| Folder | Internal Version | Status | Lines |
|--------|-----------------|--------|-------|
| `single_obstruction_theory.md` | v0.5 | RGB Team Passed (snapshot) | ~146 |
| `single_obstruction_theory_v001.md` | v0.5 | 12 changes from v0.4 documented | ~146 |
| v002 | v0.2 | Post-RGB Round 3 | -- |
| v003 | v0.3 | Axiom terminology refined | -- |
| v004 | v0.4 | Structure tightened | -- |
| v005 | v0.5 | Examples + structure arc | ~146 |
| v006 | v0.6 | RGB Round 4 (major expansion) | ~311 |
| v007 | v0.7 | External RT Pass 1 | ~345 |
| v008 | v0.8 | External RT Pass 2 (coordinate-free) | ~340 |
| v009 | v0.9 | External RT Pass 3, LOCKED | ~332 |
| v010 | v1.0 FINAL | Journal submission candidate | ~332 |
| v011 | v1.1 | Enhanced abstract | -- |
| v012 | v1.2 | Minor refinements | -- |
| v013 | v1.3 | Uniqueness language, Lean4 refs removed from abstract | -- |
| v014 | v1.3+ | Continued polish | -- |
| v015 | v1.4 | Compressed abstract, Kan extension (section 2.3) | -- |
| v016 | v1.4 | Continued v1.4 polish | -- |
| v017 | v1.7 | Expanded intro, labeled structural theorems | -- |
| v018 | v1.7 | Final v1.7 polish | -- |
| **v019** | **v1.0 (preprint)** | **Current published version** | ~330 |

---

## Phase 1: Core Development (v0.2--v0.5)

### v0.2 -- Initial Draft (Feb 2026)

- First formal write-up of the three core theorems
- Established the projection nonlinearity / l^1 rigidity / density scaling structure
- Basic Banach space framework with C*-algebra context

### v0.3 -- Axiom Terminology (Feb 2026)

- Refined axiom naming conventions
- Tightened mathematical notation
- Clarified the role of the obstruction cocycle

### v0.4 -- Structure Pass (Feb 2026)

- Reorganized theorem presentation order
- Strengthened proof sketches
- 12 changes documented in v001 companion file:
  - Axiom 2 renamed "Obstruction Non-Triviality" (was "Axiom 2")
  - Added explicit H^1 cocycle class notation
  - Clarified projection vs. conditional expectation distinction
  - Tightened density scaling exponent bounds
  - Added Kadison inequality reference
  - Strengthened uniqueness claim language
  - Added "why this matters" paragraph to introduction
  - Fixed notation inconsistency (pi vs. P for projections)
  - Added cross-references to Papers 001--004
  - Clarified finite-dimensional vs. infinite-dimensional scope
  - Added remark on connection to Connes embedding
  - Fixed bibliography formatting

### v0.5 -- RGB Team Passed (Feb 2026, ~146 lines)

- **Milestone: First complete version to pass all three RGB team reviews**
- Final RGB Team stamp: "PASSED"
- Added worked examples (section 4)
- Added structure arc connecting all three theorems
- Clean theorem-proof-remark flow established
- This version archived as both `single_obstruction_theory.md` and `single_obstruction_theory_v001.md`

---

## Phase 2: Adversarial Hardening (v0.6--v0.9)

### v0.6 -- RGB Round 4 (Mar 2026, ~311 lines)

- **Major expansion: 146 to 311 lines (+113%)**
- Added discussion section connecting to broader program
- Added Lean4 formalization references
- Added appendices (proof details, computation examples)
- Strengthened connection to Paper 001 (Kan extension framework)
- Added explicit density scaling computation walkthrough
- Discussion of implications for quantum information theory

### v0.7 -- External Red Team Pass 1 (Mar 2026, ~345 lines)

- **Red Team: Gemini Oracle (external model adversarial review)**
- Red team identified Hahn-Banach triangle vulnerability
- Response: Added C_0 semigroup class specification to close the gap
- Koopman operator interpretation sealed (no longer open to misinterpretation)
- Added Lieb-Robinson bound corollary (connecting to quantum lattice systems)
- Tightened all quantifier scopes in theorem statements
- 311 to 345 lines (+11%)

### v0.8 -- External Red Team Pass 2 (Mar 2026, ~340 lines)

- **Key upgrade: Coordinate-free reformulation of Theorem 3.1**
- Eliminated basis-dependent notation from the density scaling theorem
- This was the single most important mathematical improvement in the paper's history
- Theorem now stated in terms of intrinsic Banach space geometry
- Slight line reduction (345 to 340) due to notation compression
- All proofs verified consistent with coordinate-free statement

### v0.9 -- External Red Team Pass 3 + LOCKED (Mar 2026, ~332 lines)

- **Milestone: Paper LOCKED for journal submission**
- 5 surgical polish fixes (no structural changes):
  1. Abstract tightened (removed redundant clause)
  2. Theorem 2.1 quantifier order standardized
  3. Bibliography: added 2 missing references
  4. Appendix A: fixed off-by-one in computation example
  5. Acknowledgments section added
- 340 to 332 lines (net reduction from tightening)
- Status: LOCKED -- no further structural changes permitted

---

## Phase 3: Journal Submission Polish (v1.0--v1.7)

### v1.0 FINAL -- Journal Submission Candidate (Mar 3, 2026, ~332 lines)

- **Milestone: First journal-ready version**
- Softened "intrinsic" claim in Theorem 3.1 (changed from "the unique intrinsic" to "a canonical")
- Simplified cancellation argument in Theorem 2.1 proof
- Added stress test companion document (separate file, not in paper)
- Minor formatting for journal style compliance
- Detailed transition documented in `v010/CHANGELOG_v009_to_v010.md`

### v1.1 -- Enhanced Abstract (Mar 2026)

- Rewrote abstract for broader accessibility
- Added one-sentence summary of each theorem in abstract
- No changes to theorem statements or proofs

### v1.2 -- Minor Refinements (Mar 2026)

- Copy-editing pass
- Consistent use of "projection nonlinearity" (not "projection non-linearity")
- Fixed 3 minor typos in proof of Theorem 2.1

### v1.3 -- Uniqueness Language (Mar 2026)

- **Important clarification: "unique (up to positive scalar)"**
- Theorem 2.1 (l^1 Rigidity) now states uniqueness qualification explicitly
- Removed Lean4 formalization references from abstract (moved to appendix)
- Lean4 content preserved in body text but not foregrounded in abstract

### v1.4 -- Kan Extension Content (Mar 2026)

- **Compressed abstract** (shorter, more direct)
- Added section 2.3: Kan extension interpretation
- Connected single obstruction theory to Paper 001's categorical framework
- Kan extension provides the universal property perspective on l^1 rigidity
- Two archive folders (v015, v016) contain v1.4 iterations

### v1.5--v1.6 -- Intermediate Polish (Mar 2026)

- Transitional versions between v1.4 and v1.7
- No archived snapshots found (changes folded into v1.7)

### v1.7 -- Structural Theorems (Mar 2026)

- **Expanded introduction with labeled structural theorems**
- Each of the three main results now has a named label in the introduction:
  - Structural Theorem A: Projection Non-Dilability (existence of obstruction)
  - Structural Theorem B: l^1 Rigidity (uniqueness of measurement)
  - Structural Theorem C: Density Scaling (persistence under limits)
- l^1 described as "free additive faithful contractive seminorm" (precise characterization)
- Two archive folders (v017, v018) contain v1.7 iterations
- Final pre-publication polish

---

## Phase 4: Publication (v019)

### v1.0 (preprint) -- Current Published Version (Mar 2026)

- **File:** `v019/single_obstruction_theory_v019.md`
- Published as preprint
- Version number reset to v1.0 for publication (distinct from internal v1.0 at folder v010)
- Incorporates all changes from v0.2 through v1.7
- Three core theorems in final form:
  1. **Projection Non-Dilability** -- Projections in infinite-dimensional C*-algebras generate non-trivial H^1 obstruction cocycles that cannot be removed by dilation
  2. **l^1 Rigidity** -- The l^1 seminorm is the unique (up to positive scalar) free additive faithful contractive measurement of obstruction magnitude
  3. **Density Scaling** -- Obstruction density scales predictably under limits, connecting finite-dimensional approximations to the infinite-dimensional theory

---

## Companion Files

| File | Location | Purpose |
|------|----------|---------|
| `readme.md` | `.archive/` | Lean 4 proof correspondence table |
| `red_team_analysis_v002.md` | `.archive/` | Gemini Oracle Red Team report (Hahn-Banach triangle analysis) |
| `CHANGELOG_v009_to_v010.md` | `.archive/v010/` | Detailed v0.9 to v1.0 transition with full version history table |
| Stress test companion | `.archive/v010/` | Adversarial stress test of v1.0 claims |

---

## Review History

| Round | Type | Reviewer | Result | Key Finding |
|-------|------|----------|--------|-------------|
| RGB 1--3 | Internal | RGB Team (Red/Green/Blue) | Passed | Core theorems sound |
| RGB 4 | Internal | RGB Team | Passed | Major expansion approved |
| External RT 1 | Adversarial | Gemini Oracle | Passed (with fixes) | Hahn-Banach triangle gap -- fixed via C_0 semigroup class |
| External RT 2 | Adversarial | External model | Passed (with upgrade) | Coordinate-free reformulation of Theorem 3.1 |
| External RT 3 | Adversarial | External model | Passed + LOCKED | 5 surgical fixes, paper locked |

---

## Statistics

- **Total versions:** 19 archived snapshots (v001--v018 + original v0.5)
- **Line count evolution:** ~146 (v0.5) -> 311 (v0.6) -> 345 (v0.7) -> 340 (v0.8) -> 332 (v0.9) -> ~330 (v019)
- **Peak expansion:** v0.6 (+113% from v0.5)
- **Review rounds:** 4 internal RGB + 3 external Red Team = 7 total adversarial passes
- **Most significant change:** v0.8 coordinate-free reformulation of Theorem 3.1
- **Development period:** February--March 2026

---

*Generated: March 9, 2026*
