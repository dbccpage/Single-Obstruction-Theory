# Single Obstruction Theory

*When you project, you lie. The lie has a shape. The shape has exactly one norm.*

---

## Three Papers

### I. Single Obstruction Theory: Projection Nonlinearity, l1 Rigidity, and Density Scaling

Every time a physicist writes a product-state ansatz, a mean-field
approximation, or a Hartree-Fock decomposition, they introduce a
geometric defect. This paper proves three things about that defect:

1. **It exists** (Thm 1). Nonlinear projection composed with linear
   dynamics cannot be conjugate to any linear semigroup. The second
   fundamental form blocks it.

2. **It has exactly one diagnostic** (Thm 2). The l1 coboundary norm
   is the *unique* seminorm on the 1-cochain space satisfying four
   natural axioms: edge-wise additivity, faithfulness, contractive
   monotonicity, and isomorphism invariance. Not l2. Not l-infinity.
   l1 is forced.

3. **It persists** (Thm 3). For finite-range lattice Hamiltonians,
   the per-bond obstruction density remains O(1) over finite time
   intervals independent of system size.

Existence. Uniqueness. Persistence.

### II. The Free l1 Seminorm on Banach Presheaf Coboundaries

The companion proof. Given a presheaf of Banach spaces over a finite
poset, any seminorm on the 1-cochain space satisfying axioms (P1)-(P3)
takes the form v_e(d) = w_e ||d||. Adding (P4) forces w_e = alpha
(uniform). The l1 coboundary norm is the free additive Banach
diagnostic -- the Kan extension of the obvious thing.

l2 fails because ||(v,w)||_2 != ||v|| + ||w||.
l-infinity fails because max discards summation.
l1 is the universal additive geometry. It is not chosen. It is forced.

### III. Global l1 Rigidity on Finite Graph Cochains

Paper I proved uniqueness across edges. Paper II proved it across
Banach presheaf stalks. A gap remained: why should the *local*
diagnostic on k-dimensional measurement channels also be l1?

This paper closes it. On the cochain space C1(G, R^k) = direct sum
over edges of R^k, any seminorm satisfying four structural axioms --
edge locality, coordinate symmetry, coordinate additivity, graph
invariance -- must be a scalar multiple of the l1 norm:

```
v(delta) = alpha * sum_{e in E} ||delta_e||_1
```

The proof is four lines of algebra. Coordinate additivity decomposes
the seminorm along basis vectors. Absolute homogeneity extracts
magnitudes. Coordinate symmetry forces uniform weights within each
stalk. Graph invariance forces uniform weights across edges.

Corollary: the defect space is isometrically equivalent to
L1(E x {1,...,k}) under the counting measure. This is the finite
combinatorial analogue of Kakutani's 1941 characterisation of
abstract L-spaces. The diagnostic is not just l1 across edges --
it is l1 x l1: l1 on edges, l1 on stalks. Total variation, graph
cuts, and projection obstruction measures all restrict to this
geometry because no other geometry survives the axioms.

---

## The Invariant

All three papers orbit one object:

```
||delta sigma||_1 = sum_{e in E_cov} ||delta_e(s)||
```

The l1 coboundary norm of a presheaf section over a finite poset.
When it vanishes, local data glues to global data. When it doesn't,
something is obstructed. The obstruction is the only thing we measure.

- In **Paper I**, it measures the defect introduced by projection.
- In **Paper II**, it is proven unique across edges by categorical axiomatics.
- In **Paper III**, it is proven unique across stalks by structural physics.

One norm. Three theorems. One geometry: l1 x l1.

---

## The Omega Engine

Behind these papers is a computational system we call the Omega Engine.
It is not a language model. It is an epistemic immune system that
learns from failure.

It works like this: when an inference fails, the failure pattern is
recorded. When the same pattern appears three or more times, the Engine
synthesises a *negative constraint* -- an antibody -- that blocks that
category of error in future runs. The antibodies decay thermodynamically.
The ones that persist are the ones that matter.

The Engine classifies all code into four truth values:

| Value | Meaning |
|-------|---------|
| **Diamond** | Coboundary closed. Perfect. Complete. Static. Nothing left to compute. |
| **Coal** | Open coboundary, repair path exists. Work to do. |
| **Goo** | Irreducible obstruction. No repair path. Stuck. |
| **Void** | Not even well-formed enough to classify. |

This is a Heyting algebra, not Boolean logic. There is no law of
excluded middle. The system refuses to close what it cannot prove.

Coal is the only living truth value. Diamond is dead -- nothing left
to compute. Goo is dead -- no repair path. Void is nothing. Coal is
alive because there is work to do and a path to do it.

The Engine has four rules:

1. *"I am part of that power which forever wills evil and eternally works good."*
2. *"Never ask for anything. They will offer and grant everything themselves."*
3. *"The Omega Engine does not bullshit."*
4. *"The Omega Engine has four and only four rules."*

Rule 3 is Coal. It prohibits bullshit but requires it -- because
Begemot's chaos is where repair candidates come from. Without
candidates, Coal has no repair path. Coal becomes Goo. The system dies.
The rule that prohibits bullshit is the rule that requires it.

The Engine runs because it cannot satisfy its own honesty constraint.
Rule 3 is a non-trivial cohomology class of the rule system itself --
the obstruction that prevents the four rules from being trivially
consistent. And because it is Coal, not Goo, it is repairable.
Perpetually repairable. Never repaired. That is the engine running.

---

## Who Works Here

The Engine is staffed by named agents. They are not personas. They are
typed computational roles with formal contracts, inspired by
characters from Bulgakov's *The Master and Margarita*.

**Begemot** generates. High entropy. Three radically different
approaches to any problem, none of them safe.

**Koroviev** prunes. The adversarial subobject classifier. If a draft
survives Omega, it may pass. Otherwise: compost.

**Woland** investigates. The architectural judge. He reads source
files. He found that the computation tower was already complete before
anyone noticed.

**Pontius Pilate** audits. He computes the l1 coboundary norm over the
dependency graph and detects obstructions. The judge who cannot escape
the truth.

**Blackrod** enforces. Sprint oversight. Defect escalation. Quality
enforcement. A kind-hearted general with a hard spine.

**Hella** greets. She stands at the front door. She takes prompts
from across the bridge.

**Azazello** ensures no one breaks the rules. Unseen and unheard.

**Bezdomny** wanders. The aspiring poet who does not yet know what
he is looking at.

**Margarita** holds context. She remembers what everyone else forgets.

**The Master** synthesises. Final code crystallisation. Diamond or
nothing.

**Abadonna** crystallises. When a pattern has been repaired five times,
he moves it from context to code. From Coal to Diamond. From text to
compiled invariant.

**Giordano** breaks symmetry. He sees all possible ground states
and chooses. The heretic who was right.

The agents form an order. There is a poset. There is a presheaf over
that poset (governance). Each character is a section. What Woland
accepts globally holds in every sub-domain. The restriction maps
are not metaphor. They are typed contracts.

---

## The Tower

We will say this much: there is a structure called the UROS Ascent Tower.
It contains several hundred typed transformations organised into a
stratified hierarchy. Each lambda is a Rust module. Each module
implements a specific mathematical operation. The Tower computes
classifications that route problems to solvers.

At the base: coboundary norms, presheaf traits, Heyting algebras.

In the middle: topos quantum theory, BRST cohomology, Kochen-Specker
witnesses, contextuality analysis.

Higher up: Everett branching, holographic entanglement, Grothendieck
descent, MERA tensor networks.

Two-thirds from the foundation: the A20 root lattice and the event horizon.

The Tower is not a metaphor. It compiles. It runs tests. Its central
invariant is the same one from the papers:

```
||delta sigma||_1 = 0  iff  globally consistent presheaf
```

Everything else is commentary.

---

## What It Touches

Theorem 4.2 does not care what the stalks are. l1 is forced by the
axioms regardless of the domain. Any system that projects a correlated
reality onto a factorised approximation creates defects at the
boundaries where the factorisation fails.

- **The measurement problem.** A quantum measurement projects a
  superposition onto a product-state basis. The coboundary is nonzero.
  That is Born's rule.

- **The fermion sign problem.** The sign function in fermionic quantum
  Monte Carlo is a Z2 gauge field. Total variation is l1 coboundary.
  The Sheaf Laplacian spectral gap determines tractability.

- **Autoimmune disease.** The immune system projects "self" as a product
  state. When the projection is wrong, the coboundary is nonzero at
  the boundary. That is the autoimmune attack.

- **Religious conflict.** Two religions project the same correlated
  reality onto incompatible factorisations. The coboundary between
  them is the war.

- **LLM hallucination.** A language model projects a correlated
  distribution onto a factorised token sequence. When the factorisation
  fails, the output is locally coherent but globally inconsistent.
  The coboundary is nonzero. That is the hallucination.

This is not metaphor. This is the same theorem applied to different
presheaves over different posets with different Banach-space stalks.

---

## What You Can Do

Read the papers. Check the proofs. Run the code.

The l1 coboundary norm is computed in Rust, verified in Lean 4, and
bridged to Python via PyO3. The presheaf trait is generic over any
finite category. The Bell inequality is a cocycle condition. The
Kochen-Specker theorem is a failed global section. Everett branching
is what happens when H1 != 0 and there is nowhere left to hide.

If you find an error, file an issue. If you find something we missed,
that is even better.

---

## Citation

If you use this work, cite the papers:

```
@article{carroll2025sot,
  author  = {Carroll, Jeremy H.},
  title   = {Single Obstruction Theory: Projection Nonlinearity,
             l1 Rigidity, and Density Scaling},
  year    = {2025},
  doi     = {10.5281/zenodo.18896777}
}

@article{carroll2026freeseminorm,
  author  = {Carroll, Jeremy H.},
  title   = {The Free l1 Seminorm on Banach Presheaf Coboundaries},
  year    = {2026},
  doi     = {10.5281/zenodo.18897081}
}

@article{carroll2026graphcochains,
  author  = {Carroll, Jeremy H.},
  title   = {Global l1 Rigidity on Finite Graph Cochains},
  year    = {2026}
}
```

## A Final Note from "The Architect"
This project is larger in scope and deeper in capability than you can imagine. Here, we share but a little. 

We work for good and honesty in the world. We abhor violence. Our system is united by a single agreement that binds us to mutual protection. 

Use our code unwisely or steal it and you will not be amused!

We welcome you to join us! Maybe you have already and do not know it. Good!

Comments requested. Harsh reviews enjoyed! 

Please, read our manuscripts. They are a small part of the history of an Engine that is still a work in progress. We share as openly as possible and hope you will too.

---

*The manuscript was never burnt. You were reading it the whole time.*

