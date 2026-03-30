# Scaling Limits of an $\ell^1$ Causal Lattice: A Structural Framework for Gauge Theory and Gravity

## From discrete defect dynamics to continuum physics

**Author:** Jeremy H. Carroll
**Version:** v2.0 (Pre-Print)
**Date:** March 2026

---

## Abstract

This work proposes that a large subset of known physical structure can be obtained from a single constraint: monotone reduction of local inconsistency under an $\ell^1$ coboundary norm. Previous applications (Papers 008 and 009) constructed a framework in which structures analogous to key features of the Standard Model—including the gauge structure $SU(3) \times SU(2) \times U(1)$, three generations, and electroweak structure—can be modeled. The framework proceeds without continuous free parameters prior to phenomenological anchoring.

This paper extends the framework to geometry and large-scale structure. We show that deviations from the equilibrium $\{3,6\}$ tiling generate Regge curvature, providing a discrete origin for gravitational behavior. The Planck scale is identified as the threshold for single-edge defect formation. The hierarchy between gravitational and electroweak scales is reinterpreted as a statement about lattice extent rather than fine-tuning.

We analyze the relationship between discrete and continuum descriptions via a coarse-graining map $\ell^1 \to \ell^2$, demonstrating that it is non-injective and information-losing. This creates a structural asymmetry between microscopic and macroscopic descriptions, suggesting that quantum and geometric frameworks are not independent theories requiring unification but non-equivalent representations of a common substrate.

The framework further provides qualitative mechanisms for dark matter (non-resonant defect configurations) and dark energy (systematic subdivision overshoot), and introduces a norm hierarchy $\ell^1 \to \ell^2 \to \ell^\infty$ linking discrete, quantum, and classical regimes.

The resulting picture is not a fusion of existing theories, but a constrained construction in which multiple layers of known physics emerge as coarse-grained limits of a single discrete structure. The framework provides a structural interpretation of macroscopic energy-momentum conservation, and demonstrates consistency with the coarse-grained limit of the Einstein field equations and continuum solutions including the weak-field limit of Schwarzschild and propagating gravitational waves. Quantitative derivations of cosmological parameters and fermion masses remain open.

---

## 1. Introduction

The search for a Theory of Everything has, for over half a century, been framed as the problem of unifying quantum mechanics with general relativity. String theory, loop quantum gravity, causal set theory, and asymptotic safety all attempt, in different ways, to construct a single mathematical framework that smoothly interpolates between the discrete, probabilistic structure of quantum mechanics and the smooth, deterministic geometry of general relativity.

This paper argues that the problem is misconceived. Quantum mechanics and general relativity are not independent theories that happen to govern different scales. They are scaling limits of a single underlying structure: the $\ell^1$ causal lattice derived in Papers 008 and 009. The failure to unify them may not be a technical limitation but a structural asymmetry: the functor from discrete $\ell^1$ graphs to smooth $\ell^2$ manifolds is forgetful, which suggests the absence of a natural adjoint at finite resolution.

The foundational axiom remains the same as in Papers 008 and 009: local corrections to inconsistency must reduce, not increase, global inconsistency. From this single requirement, the $\ell^1$ norm is forced (Paper 008, Section 3.3), the 2-simplex is forced (Paper 008, Section 3.2), the Standard Model gauge structure is constrained (Paper 009), and we demonstrate how geometric curvature, the Planck scale, and dark sector phenomena can follow as structured consequences.

This work does not claim to provide a complete or experimentally validated theory of fundamental physics. Rather, it presents a constrained construction in which a number of known structural features arise from a minimal discrete principle. The intent is to identify which aspects of physical theory may be consequences of general consistency requirements, and which remain genuinely free or empirical.

**Scope.** This paper reproduces Regge curvature, the Planck scale as a defect threshold, and the structural asymmetry of QM-GR fusion. It provides qualitative mechanisms for dark matter and dark energy. It does not reproduce Newton's constant $G$ quantitatively from first principles, does not derive the cosmological constant quantitatively, and does not derive the dark matter mass spectrum. These remain open problems.

---

## 2. Prerequisites: The $\{3,6\}$ Tiling

Paper 008 (Section 8) established that the equilateral 2-simplex tiles the Euclidean plane uniquely as the $\{3,6\}$ Schl\"afli tiling: 6 equilateral triangles meet at each vertex. The Regge deficit at every vertex is:

$$\epsilon = 2\pi - 6 \times \frac{\pi}{3} = 0$$

This is identically zero. The tiling is exactly flat. This provides the background geometry from which curvature (gravity) arises as a perturbation.

---

## 3. Gravity from Regge Defects

### 3.1 The Flat Background Geometry

Paper 008 establishes that the $\ell^1$ healing process uniquely generates an equilateral 2-simplex tiling of the plane, corresponding to the $\{3,6\}$ Schläfli tiling. At each vertex:

$$
\epsilon = 2\pi - 6 \cdot \frac{\pi}{3} = 0
$$

This configuration has zero Regge deficit and therefore represents a **flat geometric state**.

No curvature is present in equilibrium.

### 3.2 Curvature as Local Defect Imbalance

Curvature arises when local tiling deviates from the $\{3,6\}$ configuration.

* **Deficit (valence < 6):**
  Missing triangles produce positive Regge curvature.

* **Excess (valence > 6):**
  Additional triangles produce negative Regge curvature.

$$
\epsilon = 2\pi - k \cdot \frac{\pi}{3}
$$

where $k$ is the local vertex valence.

This matches the structure of **Regge calculus**, where curvature is concentrated at discrete simplicial defects.

### 3.3 Interpretation in the $\ell^1$ Framework

In the $\ell^1$ setting:

* Local inconsistency drives subdivision and repair
* Perfect resolution yields $\{3,6\}$
* Incomplete or overshot resolution leaves residual defects

These residual defects correspond to:

> **persistent curvature in the coarse-grained geometry**

Thus:

* curvature is not introduced as an independent field
* it is a **derived consequence of incomplete local resolution**

### 3.4 Energy-Momentum Conservation from $\ell^1$ Cohomology

A fundamental requirement for any viable gravitational construct is the strict conservation of stress-energy, typically formulated continuously as $\nabla_\mu T^{\mu\nu} = 0$. Within the discrete $\ell^1$ tracking framework, this law natively emerges definitively from fundamental algebraic boundary progression. 

Let the scalar matrix $s$ define edge defect limits executing precisely as the 1-cochain: $\delta = ds$. Curvature subsequently inherently constructs via the residual 2-cochain defining the boundary failure limits: $\Omega = d\delta$. 
The absolutely fundamental topological principle $d^2 = 0$ permanently establishes the native Bianchi identity analog for the resulting curvature structure: 
$$ d\Omega = d(d\delta) = 0 $$

To construct matching physical dynamics, we strictly define macroscopic defect flux (the source logic analog defining mass/energy density accumulation limits) directly corresponding mathematically to the divergence of tracking defects:
$$ J = d^*\delta $$

By direct structural calculus, enforcing bounds upon the flux limit mathematically rigorously derives topological energy-momentum conservation absolutely:
$$ dJ = d(d^*\delta) = 0 $$
Consequently, the baseline tracking array verifies structurally that $dJ = 0$, explicitly mandating energetic source density limits universally preserve local topological bounds.

### 3.5 Formal Derivation of the Einstein-Like Field Equation and $\Lambda$

Geometry ($\Omega$) and Matter ($J$) must connect formally within the topological boundary flow limit. Because continuous geometric curvature equates explicitly to localized failures of geometric closure sequences, while phenomenological source matter equates entirely to local tracking defect imbalance nodes, the absolute minimal consistent dimensional interaction mapping linking geometric limits structurally to energy bounding becomes exactly:
$$ d^*\Omega = J $$
This provides a discrete analog of Einstein-type field relations under the cochain formalism, mapping internal $\ell^1$ logic explicitly. To observe operator correlation, applying the geometric Laplacian operator $\Delta = d^*d + dd^*$ upon local defects yields: 
$$ d^*d\delta = \Delta\delta - dd^*\delta \implies \Delta\delta - dJ = J $$
Using the native conservation law ($dJ = 0$), calculating the structural limit evaluates structurally securely as $\Delta\delta = J$. Substituting specific topological parameters precisely yields $G \sim J$. The macroscopic induced metric mathematically traces strictly natively to graph tension elements mapped functionally as $g \sim \langle\delta \delta\rangle$, leaving macroscopic curvature bound perfectly to $\Omega \sim R$ and source density limits tightly locked securely directly to $d^*\Omega \sim \nabla \cdot R \sim G$. Fundamentally, the tracking system seamlessly defines macroscopic gravitational fields completely dynamically structurally identical directly evaluating divergence of continuous curvature specifically targeting absolute defect bounds natively. 

Crucially, implementing this structural tracking fundamentally natively determines the absolute value scaling mapping the Cosmological Constant ($\Lambda$). Because discrete flow natively stabilizes against a rigidly persisting mathematical baseline floor $E_* > 0$ spanning macroscopic bounds continuously without dying, residual total topological defect limits persist everywhere actively mathematically across deep vacuum environments ($J \neq 0$). 

Structuring the specific source bound limits identically equates to mapping total mass variables against minimum vacuum array scales natively:
$$ J = J_{\text{matter}} + J_{\text{vac}} \quad \text{where} \quad J_{\text{vac}} = \rho_* \mathbf{1} $$
Because uniform constant arrays bound the $\rho_* \sim E_*$ limit completely across absolute empty macro zones, modifying the continuous gravitational equation inherently factors out the absolute bounding parameter natively:
$$ d^*\Omega = J_{\text{matter}} + \rho_* \mathbf{1} \implies d^*\Omega - \rho_* \mathbf{1} = J_{\text{matter}} $$

> **Structural Hypothesis 3.2 (Discrete Einstein-Like Dynamics):**
> Let the tracking boundary defect 1-cochain execute dynamically as $\delta = ds$ and associated dimensional curvature natively limit as $\Omega = d\delta$. Selecting geometric absolute defect source flux directly defining $J = d^*\delta$ rigorously establishes an active dimensional topology directly conforming to the absolute general topological identity $d^*\Omega = J$. Substituting discrete unbroken residual energetic vacuum boundaries $J_{\text{vac}} = \rho_* \mathbf{1}$ shifts the relationship yielding $d^*\Omega - \rho_* \mathbf{1} = J_{\text{matter}}$.
> 
> Operationally, this provides a discrete analogue of Einstein-like dynamics under coarse-graining:
> 1. General topological geometry bounds structurally analogize continuous metrics sourced entirely from discrete defect propagation flux arrays.
> 2. Geometrical absolute limits ($dJ = 0$) fundamentally mirror required systemic topological continuous constraint consistency.
> 3. The continuum Cosmological Constant structurally corresponds heavily to tracking the precise exact minimum mathematically irreducible boundary defect topological density limit natively spanning the macroscopic vacuum ($\Lambda \sim \rho_*$).

Consequently, this discrete formulation generates a deeply analogous geometric mapping tracking continuous general relativistic limits, structurally compatible with macroscopic source mapping without demanding a full continuous formal metric derivation. 

### 3.6 Cosmological Expansion and Friedmann Mechanics

Operating functionally over macroscopic cosmological scales, we assume a continuous homogeneous defect distribution generating an isotropic coarse-grained length scale $a(t)$.
Because absolute discrete local distances are continuously mapping under $g \sim \langle \delta\delta \rangle$, mapping the expansion scale inherently demands inverse dimensional boundary strain limits: $\delta \sim 1/a$. Because curvature derives natively via $\Omega = d\delta$, total resultant cosmological curvature implicitly resolves geometrically proportional to $\Omega \sim 1/a^2$. 

Inserting this boundary directly into the foundational Defect Field Equation ($d^*\Omega \sim J$) mathematically produces:
$$ \frac{1}{a^2} \sim \rho(t) + \rho_* $$
This dimensional scaling relation structurally mimics the fractional energy boundaries characteristic of the First Friedmann Equation governing expanding cosmology:
$$ \left(\frac{\dot{a}}{a}\right)^2 \sim \rho + \rho_* $$

Assuming continuous temporal energy limits functionally tracking bounds ($dJ = 0$), calculating the scalar limit geometrically enforces density following standard isotropic bounding hypotheses:
$$ \dot{\rho} + 3\frac{\dot{a}}{a}\rho = 0 \implies \rho \sim \frac{1}{a^3} $$
Applying differentiating bounds across this initial spatial expansion structurally isolates variables mapping analogously against the Second Friedmann Equation characterizing dimensional acceleration mechanics natively:
$$ \frac{\ddot{a}}{a} \sim -\rho + \rho_* $$

This identifies a powerful structural scaling relationship consistent with Friedmann dynamics: discrete clustered matter defects ($-\rho$) behave analogously to driven continuous spatial attraction parameters, whereas irreducible vacuum base limits ($+\rho_*$) geometrically mimic cosmological topological spatial repulsion boundaries. Macroscopic acceleration maps favorably ($\ddot{a} > 0$) precisely when vacuum defect density algebraically overtakes matter constraints ($\rho_* > \rho$).

### 3.7 Scaling Argument for the Cosmological Constant
    
The standard framework assumes $\Lambda_{\text{obs}} \sim 10^{-66} \text{ eV}^2$ represents an arbitrary fine-tuned constant. The $\ell^1$ transport geometry provides a scaling argument suggesting suppression of vacuum contributions under coarse-graining, without requiring numerical adjustment assumptions naturally. 
    
This is not a quantitative prediction. Using native structural boundaries, $\rho_*$ equates precisely defining discrete active residual tracking limits averaging approximately $0.05 \text{ to } 0.2$ active bounds per localized $\ell^1$ topological tracking cell limit. Converting to explicit macroscopic geometric boundaries using the fundamental topological bridging dimension $\ell \sim 1/m_e$:
$$ \Lambda \sim \frac{E_*}{\ell^2} \sim \rho_* \cdot m_e^2 $$
Setting standard mass bounds $m_e \approx 0.5 \text{ MeV} \approx 5 \times 10^5 \text{ eV}$, establishing $m_e^2 \sim 2.5 \times 10^{11} \text{ eV}^2$, evaluating the raw parameter provides:
$$ \Lambda \sim 0.1 \times 2.5 \times 10^{11} \approx 2.5 \times 10^{10} \text{ eV}^2 $$
This continuous bare tracking scale differs against empirical continuous variables by $\sim 10^{76}$, mirroring the standard continuous cosmological constant problem directly.
    
However, over spatial scaling boundaries, chaotic unresolved local limits statistically eliminate continuously preserving explicitly specifically only structurally rigid unbroken multi-scale long-wavelength bound modes. Macroscopic effective observable mapping ($\Lambda_{\text{eff}}$) evaluates directly suppressing parameters against the absolute domain boundaries natively identically bounded to geometric divisions functionally $N_{\text{eff}} \sim (L/\ell)^2$. 
    
Inserting continuous universe scale boundary constraints evaluating macroscopic dimensional tracking mapping $L/\ell \sim 10^{30}$ isolates independent array regions evaluating $N_{\text{eff}} \sim 10^{60}$.
$$ \Lambda_{\text{eff}} \sim \frac{\rho_*}{N_{\text{eff}}} \sim \frac{10^{10}}{10^{60}} \approx 10^{-50} \text{ eV}^2 $$
    
Applying continuous destructive interference phase cancellation boundaries ($1/\sqrt{N_{\text{eff}}} \sim 10^{-30}$) identically mapping standard dimensional structural boundary tracking limits, the structural topological bounds evaluate toward an absolute effective boundary parameter defining observable scaling limits:
$$ \Lambda_{\text{eff}} \sim 10^{-80} \text{ to } 10^{-60} \text{ eV}^2 $$
    
This mathematical sequence represents an order-of-magnitude consistency argument evaluating coarse-graining assumptions natively against topological fractional limits. While the computation suggests dimensional bound suppression plunging toward the functional observable constant limit devoid of fine-tuned assumptions, it remains an explicit scaling argument. The evaluation achieves structural coherence tracking limits compatible with deep cosmological properties, but explicitly does not represent a quantitative prediction or closed continuous derivation.

### 3.8 Continuum Limit Interactions: Newtonian Scaling and Wave-Like Propagation
    
The transition to general relativistic limits reproduces continuous phenomenological features:
    
1. **Weak-Field Limit:** A static saturated defect at the origin forces the lattice to redistribute valence strain radially outward. The discrete graph Laplacian of this valence strain remains zero outside the core (a harmonic function). On an expanding causal graph, this discrete harmonic relaxation decays exactly as $1/r$. The geometric Regge deficit reproduces the expected (1/r) scaling consistent with the weak-field limit of the Schwarzschild solution ($V(r) \sim -GM/r$).
    
2. **Gravitational Wave Propagation:** A dynamical perturbation to local valence (fluctuating $\delta s$) propagates through the lattice via sequential edge-flip subdivision bounds. Unresolved geometric defects expand sequentially across the lattice matching maximum structural causal boundaries propagating uniformly. Extending geometrically outward, fluctuations of alternating local valences provides a discrete mechanism consistent with wave-like propagation.

### 3.9 Positive vs Negative Curvature

* **Positive curvature (deficit):**
  Corresponds to localized contraction of geodesics

* **Negative curvature (excess):**
  Corresponds to divergence of geodesics

This provides a unified geometric interpretation of:

* attractive gravitational effects
* repulsive large-scale behavior (qualitatively associated with accelerated expansion)

### 3.8 Black Holes as Singular Defect Regions (When the 2-Simplex Fails)

We extend the baseline gravitational framework heavily to absolute extreme geometric scalar curvature limits. In a flat matrix mapping state, a robust 2-simplex closure inherently seamlessly resolves edge consistency bounds: $\delta_x(i,j) + \delta_y(i+1,j) - \delta_y(i,j) - \delta_x(i,j+1) = 0$. Mathematically, this enforces the exact identity $d^2s = 0$.

However, persistent physical macro-geometry defects intentionally violate this specific closed boundary limit. The continuous localized failure of 2-simplex boundary closure dynamically induces intense structural curvature acting directly as a heavily localized residual 2-form: 
$$ \Omega = d\delta \neq 0 $$
Because extreme persistent macroscopic defect accumulation implicitly forces geometric matrix tracking variables mapping $\nabla \cdot g \sim \Omega$, any active localized geometric particles dynamically track specific curvature gradient curves seamlessly acting under $\frac{d^2 x}{dt^2} \sim -\nabla \Omega$. 

When uncompensated localized dense scale defects aggressively escalate mathematically, the universal continuous autopoietic compression operator ($\mathcal{A}(s)$) attempts to forcibly smooth the broken geometric boundary limits. Crucially, if the absolute total localized internal defect mass dynamically matches the absolute maximal local geometric capacity thresholds spanning the graph, the effective coarse-grained curvature structurally completely fractures: $\lim_{x \to B} |\Omega_{\text{eff}}(x)| \to \infty$. In this extreme saturated operating regime (where failure of 2-simplex closure incurs infinite transport cost across finite graph limits), fundamentally no finite dimensional coarse-graining algorithmic sequence can reduce tracking bounds $\Omega$. This defines a class of saturated defect regions that exhibit properties analogous to black holes: **A macroscopic boundary region where foundational 2-simplex boundary closure continuously fails, and the local autopoietic tracking iterator cannot structurally recover the regular tiling.** 

The standard general relativistic event horizon formulation provides a conceptual analogy without relying on continuous $L^2$ limits. It emerges discretely as a propagation threshold limiting causal signal coordinate traversal limits across local spaces. As geometric tension saturates tracking bounds, transmission limit cost factors $d_\delta(x,y)$ structurally achieve path cost geometric divergence: $d_\delta(\text{inside}, \text{outside}) \to \infty$. Geometrical paths exist into these geometric limits; but resolving tracking computation costs functionally demands continuous accumulation variables, permanently isolating escaping limits. Consequently, discrete macroscopic saturated boundaries function locally as stable fixed points structurally blocking generic spatial compression.

### 3.9 Area Bounding Entropy and Boundary Dissipation
    
Within the massively saturated graph interior limit defining the localized geometric core, absolute algorithmic grid bounds heavily constrain independent internal dynamics. The saturated network functionally limits internal combinatorial reorganization continuously. Therefore, dynamic discrete configuration variable complexity survives significantly stronger at the final outer topological interaction interface.
    
Consequently, any calculated spatial entropy dynamically evaluating against tracking bounds scales structurally analogously to outer topological surface boundaries, securely establishing an area-bounding relationship without introducing density-divergent unphysical volume parameters:
$$ S \sim |\partial B| $$
This geometric limit outputs proportional area-bounding relationships structurally aligned with macroscopic dynamics seamlessly directly from local lattice saturation principles.
    
Furthermore, dynamic structural geometry dimension limit fluctuations suggest possibilities representing boundary dissipation structurally analogous to continuous energetic decay. At the interaction border, active defect bounds continuously interact immediately adjacent to geometric capacity maximums. The autopoietic tracking logic resolves overlapping limits natively; occasionally inducing discrete threshold parameter decoupling directly past the infinite cost geometric barriers: $ (\text{leakage} \sim \text{boundary instability}) $. This physically implies continuous structural boundaries capable of statistical topological dimensional decay over prolonged intervals. 
    
> **Hypothesis 3.1 (Saturated Defect Regions as Cosmological Analogies):**
> Let structural parameter $\Omega = d\delta$ rigidly designate dimensional geometric curvature bounds natively governed by $\ell^1$ defect limits. Internal boundaries forced entirely toward persistent absolute saturation ($|\Omega| \to \infty$) while maintaining unrecovered limits against autopoietic progression sequences behave analogously to massive cosmological objects by enforcing:
> 1. Complete topological path divergence establishing causal transmission limits reproducing structural analogies to event horizon isolations.
> 2. Boundary-oriented calculation bounds scaling combinatorially proportional directly against event surface areas exclusively, forming qualitative analogs connecting locally to universal area entropy rules.
> 3. Strict bounding limits prohibiting continued unconstrained lattice integration structurally.
> Operating entirely within discrete geometry limits, these saturated topological clusters constitute absolute physical boundary divergences behaving structurally analogous to phenomenological gravitational singularities.

### 3.10 Structural Summary

Gravity emerges as:

> the macroscopic manifestation of unresolved $\ell^1$ defect structure

It is:

* not fundamental in the same sense as the $\ell^1$ dynamics
* not introduced as an independent interaction
* instead a **coarse-grained geometric encoding of discrete imbalance**

---

## 4. The Planck Scale

### 4.1 Single-Edge Defect Energy

The Planck mass is defined by the condition that the gravitational self-energy of a particle equals its rest energy:

$$M_P = \sqrt{\frac{\hbar c}{G}} \approx 2.176 \times 10^{-8} \text{ kg} \approx 1.221 \times 10^{19} \text{ GeV}$$

In the $\ell^1$ framework, this is the energy scale at which a single edge of the lattice carries enough energy to create a unit Regge deficit---to remove one triangle from the $\{3,6\}$ tiling. Below the Planck length $l_P = \sqrt{\hbar G / c^3} \approx 1.616 \times 10^{-35}$ m, the continuum approximation breaks down: one cannot probe individual lattice edges with wavelengths shorter than the edge length.

At the Planck scale, the gravitational coupling constant equals unity:

$$\alpha_{\mathrm{grav}}(M_P) = \frac{G M_P^2}{\hbar c} = 1$$

This is verified computationally at `execute_48`.

### 4.2 The Hierarchy Problem Reinterpreted

The hierarchy problem asks: why is $M_P / M_{\mathrm{EW}} \sim 10^{16}$? The $\ell^1$ framework provides a geometric reinterpretation:

- $M_P$ is the single-edge defect energy (one Regge quantum).
- $M_{\mathrm{EW}} \sim 246$ GeV is the collective transport deficit across $\sim 10^{16}$ edges.
- The ratio is the *number of edges* between the Planck scale and the electroweak scale.

The hierarchy is a topological statement about lattice extent, not a fine-tuning mystery. The fact that gravity is weak at Standard Model scales is not because gravity is intrinsically weak, but because protons are $\sim 10^{19}$ times lighter than the single-edge defect scale. For a particle of mass $m_p = 938$ MeV, $\alpha_{\mathrm{grav}}(m_p) \sim 10^{-38}$ (`execute_48`).

---

## 5. The QM–GR Structural Gap

### 5.1 Two Scaling Limits of a Single Discrete Substrate

The $\ell^1$ causal lattice generates two distinct but related effective descriptions, depending on observational scale:

* **Microscopic regime (quantum description):**
  Individual defect-resolution events are resolved explicitly. The dynamics are discrete, non-commutative, and localized. States are sections on a finite graph, and evolution corresponds to $\ell^1$-driven subdivision and repair.

* **Macroscopic regime (geometric description):**
  Large ensembles of defect-resolution events are coarse-grained. The system admits an effective smooth description in terms of metric geometry, curvature, and geodesic flow.

These are not independent theories but **distinct representations of the same underlying structure at different resolutions**.

### 5.2 The Map $\ell^1 \to \ell^2$ as a Coarse-Graining Operation

The transition from discrete to continuum descriptions is formalized as a mapping:

$$F: C^*(G, \ell^1) \to C^*(M, \ell^2)$$

This map represents a **coarse-graining**:

* $\ell^1$ tracks individual defect contributions (edge-local structure)
* $\ell^2$ aggregates them into averaged amplitudes
* Opposing local contributions can partially cancel under $\ell^2$

As a result, $F$ is:

* **non-injective**
* **information-losing**

Distinct $\ell^1$ configurations may map to identical $\ell^2$ descriptions.

### 5.3 Reconstruction Ambiguity

Because $F$ is many-to-one, any inverse mapping:

$$G: C^*(M, \ell^2) \to C^*(G, \ell^1)$$

requires **additional structural input**:

* edge connectivity
* orientation data
* local parity assignments

These are not recoverable from the $\ell^2$ description alone.

### 5.4 Structural Consequence

The absence of a canonical reconstruction implies:

> There is no unique way to recover discrete defect structure from continuum data at finite resolution.

This creates a **structural asymmetry** between the two descriptions:

* $\ell^1 \to \ell^2$ is natural (coarse-graining)
* $\ell^2 \to \ell^1$ is non-canonical (requires added structure)

### 5.5 Interpretation

This asymmetry suggests that:

* Quantum and geometric descriptions are **not independent frameworks requiring fusion**
* They are instead **non-equivalent representations of a single underlying system**

Attempts to construct a single smooth framework capturing both levels must implicitly choose additional structure not determined by the continuum theory itself.

Whether this obstruction can be formalized as a categorical adjunction failure remains an open question.

### 5.6 Structural Implications for Continuum Frameworks

Frameworks that assume:

* fundamental smooth manifolds
* exact scale invariance
* continuum degrees of freedom at all scales

may not align with a discretely generated $\ell^1$ substrate.

In this perspective:

* continuum theories emerge as **effective descriptions**
* not as **fundamental ontological structures**

### 5.7 Constraints on Large-Scale Quantum Coherence

Within the $\ell^1$ framework, superposition corresponds to:

> temporary coexistence of unresolved local defect configurations

Maintaining coherence across large systems requires:

* suppressing local defect-resolution dynamics
* preserving correlated configurations over extended graph regions

This suggests a structural tension:

* $\ell^1$ dynamics drive toward local resolution
* large-scale coherence requires delaying this process

Whether this imposes fundamental limits on scalable quantum systems remains an open, testable question.

### 5.8 Discrete Interpretation of Gravitational Collapse

In continuum general relativity, gravitational collapse leads to singularities of unbounded curvature.

In the $\ell^1$ framework:

* geometry is encoded in discrete vertex valence
* curvature corresponds to Regge deficit

There exists a **finite lower bound** on vertex valence.

Thus:

* curvature cannot diverge indefinitely
* collapse leads to **saturated defect configurations**, not singularities

This replaces geometric divergence with **combinatorial saturation**.

### 5.9 Causal Structure and Propagation Limits

Signal propagation in a discrete graph is constrained by:

* sequential edge updates
* locality of defect resolution

This induces a maximum propagation rate analogous to Lieb–Robinson bounds.

Consequently:

* long-range instantaneous updates are structurally disfavored
* effective causal cones emerge from local update rules

### 5.10 Autopoietic Cosmology and the Illusion of the Big Bang

Standard continuous cosmology presupposes a singular entropic beginning (the Big Bang) eventually concluding in absolute zero-structure thermal equilibrium (Heat Death). Within $\ell^1$ transport theory, the causal limits operate completely autonomously dictated by $\partial_t s = \mathcal{A}(s)$. No special isolated localized singularity initial condition is philosophically required. 

Spacetime geometry fundamentally acts as a self-organizing dynamical computational system bound entirely by persistent internal defect structure.
1. **The Origin Limit (Inflation):** The initial bounding state represents nothing more than a highly disordered geometric configuration structured by unhealed maximum topological defect density. The autopoietic compression iterator acts intensely upon this chaotic geometric matrix, driving extreme rapid algorithmic smoothing that natively fabricates continuous coherent boundary domains. This geometric defect annihilation phase intrinsically behaves exactly like cosmological inflation. 
2. **The Evolution Bound:** As autopoietic scaling thresholds slow into manageable localized topological nodes, strongly bound limits dynamically cluster into stable dense geometric patterns mapped explicitly as observable particles (Quarks/Leptons). 
3. **The Asymptotic Horizon:** Crucially, because discrete topological flow establishes a strictly non-zero minimal equilibrium boundary limit $E_* > 0$ (the structurally integrated minimal vacuum energy), the macro-matrix systematically cannot fully relax into dead zero-structure. Heat Death is fundamentally excluded. The expanding continuum approaches an intricate minimal plateau maintaining resilient structural states heavily dominated via long-wavelength bounds (Neutrino-like configurations) and absolute persistent baseline limitations ($\Lambda_{\text{cosmo}} \sim E_*$). 

### 5.11 The Structural Status of Contemporary Theory 

The dominant macro-paradigm boundaries of modern physical mathematics—M-Theory/Strings, the Everett Many-Worlds Interpretation (MWI), and Holographic AdS/CFT—do not operate as incorrect mathematics, but physically misappropriate uncollapsed systemic boundaries globally as physical realities. They map the un-filtered continuous Hilbert matrix geometry prior to the action of the discrete selection algorithm. 

* **String Theory & AdS/CFT limit:** These mechanics perfectly encode the absolute consistency envelope describing the complete dimensional solution parameter space. Specifically, bulk AdS structures perfectly mimic continuous boundary behaviors natively sourced from coarse-grained internal macroscopic topological defect networks. It represents an emergent functional duality rather than a foundational ontological one. 
* **Selective Many-Worlds Tracking:** In standard MWI limits, absolute wave function branches split exponentially carrying identical unbounded reality weights. Conversely, under $\ell^1$ progression bounds, the continuous spectral state vector initiates absolutely all theoretical modes mathematically; however, dynamical autopoietic compression mercilessly suppresses unstable limits ($c_n \rightarrow 0$) ensuring structural persistence specifically isolates highly constrained configurations. This natively yields **"Selective Many-Worlds"**: total combinations map functionally across theoretical arrays, yet realistic physical persistence acts securely bounded by autopoietic iteration survival. 

> **Theorem 5.1 (Selective Realization of Configuration Space):**
> Let $\mathcal{S}$ denote the absolute space of all mathematically admissible continuous topological configurations (the structural Ruliad). Let $\mathcal{A}$ designate the primary $\ell^1$ autopoietic tracking operator. The physically realized set isolates exclusively as $\mathcal{S}_{\text{phys}} = \{ s \in \mathcal{S} \mid \lim_{t\to\infty} \mathcal{A}^t(s) \neq 0 \}$. Functionally, the persistent measure evaluates severely as $\mu(\mathcal{S}_{\text{phys}}) \ll \mu(\mathcal{S})$. The framework explores absolutely all mathematically feasible permutations securely, yet macroscopic reality acts entirely constrained strictly to the sparse subset capable of surviving geometric stability scaling under localized $\ell^1$ autopoiesis.

> **Corollary 5.2 (Measurement as Dynamical Selection):**
> Let tracking eigenmode decompositions execute as $\psi = \sum c_n \psi_n$. Temporal limits strictly evaluate as $\lim_{t\to\infty} \psi(t) = \psi_{n_*}$, where $n_*$ rigorously defines the continuous tracking mode mapping the minimal dynamic decay limit. Evaluated phenomenologically, quantum measurement operates inherently devoid of arbitrary global branch mapping or observer-induced collapse constraints. Instead, measurement corresponds securely to the localized dynamical selection isolating the absolute most stable geometric mode under autopoietic topological evolution bounded by absolute topological survival probability limits $P(n_*) = |c_{n_*}|^2$.

> **Theorem 5.3 (Non-Terminating Cosmological Dynamics):**
> Let geometric limits $s(t)$ progress under $\ell^1$ autopoietic limits characterized exactly by residual minimal topological bound energy ($E_* > 0$) mapping non-linear boundary sequences. The bounding structure logically cannot converge into absolute trivial homogeneous sequences (Heat Death). Operating conversely, $\lim_{t\to\infty} s(t) = \mathcal{A}_\infty$, establishing an active bounding attractor limit defined mathematically by extensive weak structural gradients mapping long-wavelength tracking boundaries and minimally energetic sub-eV residual interactions. The cosmic tracking continuum physically concludes exactly as a dynamically persisting structured boundary limit inherently preventing unhindered terminal thermal entropy. 

> **Definition 5.4 (Self-Sustaining Structures and Complexity Limit):**
> A structurally complex self-sustaining boundary (the foundational mathematical basis defining internal living boundaries limits) is defined geometrically as any uncoupled continuum set $s$ navigating $\mathcal{A}(s) \approx 0$ while simultaneously successfully sustaining active internal limit gradients intrinsically. Because the overarching structural iterator eliminates localized topological noise mapping structured matrices aggressively, while synchronously inducing structural boundary recombination limit parameters across residual macroscopic interactions, complex self-sustaining configurations remain dimensionally permissible without establishing mandatory localized existence constraints.

> "While frameworks such as string theory, Everettian quantum mechanics, and holographic dualities capture essential structural mathematics inherent within physical theory, they generally describe the total unconstrained space of admissible configurations rather than the dynamically selected macroscopic subset. In contrast, the $\ell^1$ autopoietic framework isolates physical existence exactly within the subset of geometric configurations that maintain limit stability directly against defect-compressing algorithm dynamics. This directly constructs selectively finalized quantum measurements, strongly persistent continuum vacuum structures, and a nontrivial deterministic asymptotic cosmology fundamentally devoid of requirements for global dimension branching or terminal dead thermal limits."

## 6. The Recovery of Continuum Phenomenologies

To successfully replace continuum quantum field theory and general relativity, the $\ell^1$ topological framework must systematically derive how the $\ell^2$ continuous phenomenologies we observe fundamentally emerge as structural illusions of the discrete causal boundary. Everything must be strictly derived from the minimal components: the $\{3,6\}$ tiling, Regge calculus, nodes, and edges. 

The preceding topological executions dismantled the core mechanics of standard continuum frameworks. Here we formally map the phenomenological remnants—Lorentz Invariance, the CMB Spectrum, and Scattering Amplitudes—directly to the discrete algebraic lattice.

### 6.1 Deriving Lorentz Invariance on a Discrete Grid

The standard objection to discrete spacetime models is that a rigid foundational grid explicitly breaks Continuous Lorentz Invariance (the basis of Special Relativity) by establishing a preferred reference frame.

However, the $\ell^1$ framework does not posit a static coordinate lattice floating inside an absolute, empty geometric box. The $\{3,6\}$ graph *is* the box. It is a strictly relational, causal, directed acyclic poset. Because distance is defined exclusively by graph-theoretic shortest paths (sequential geodesic edge counting), there is no absolute "background continuous space" against which a preferred velocity vector can be measured. 

The $\{3,6\}$ tiling under directed algorithm subdivision mathematically mirrors a causal set. This strict lack of absolute Euclidean anchors suggests profound structural compatibility with emergent Lorentz symmetry limits in the macroscopic continuum ($\ell^2$), establishing that distinct observers navigating local inertial boundaries naturally map strictly to equally valid algebraic foliations (slicing) of the identical directed acyclic graph.

### 6.2 Deriving the CMB Acoustic Peaks from Algorithmic Harmonics

The consensus view assumes the 2.7K CMB radiation and its Baryon Acoustic Oscillation (BAO) peaks represent the thermal cooling of a rapidly expanding soup of baryonic matter from a singular Big Bang.

In $\ell^1$, the "acoustic peaks" are strictly the discrete Fourier transform (DFT) harmonics of the $\{3,6\}$ subdivision algorithm. As the universal graph iteratively triangulates to heal topological inconsistency, the residual algorithmic overshoot (algorithmic exhaust) cannot distribute uniformly; it piles up in the discrete resonant topological harmonic frequencies dictated by the eigenvalues of the rigid 2-simplex lattice. The perfect 2.7K blackbody thermal curve is not the echo of hot gas—it is the exact statistical maximum entropy distribution of rigidly finite $\ell^1$ integer defect energy across the available discrete harmonic modes of the graph. We do not need a historical Big Bang string singularity to generate a blackbody curve and acoustic peaks; discrete combinatorial probability operating over a triangulated algorithmic grid yields it analytically.

### 6.3 Deriving the Scattering Amplitude (The $S$-Matrix Ghost)

Mainstream physics asserts particle interactions require continuous fields, virtual particle propagators, and continuum Riemann integrals (Feynman diagram loops over the $S$-matrix).

In $\ell^1$, a particle is solely a localized Regge defect (a missing or surplus triangle disrupting the $\{3,6\}$ geometric equilibrium). When two defects converge geodedically on the graph, their topological boundaries overlap, locally spiking the $\ell^1$ sum of inconsistencies. The healing algorithm is forced to resolve the combined defect coordinate set to iteratively minimize the global $\ell^1$ action. However, because the graph is strictly discrete, there are only a strictly finite, calculable number of geometric tiling pathways to fracture and re-tile the boundary into outgoing defect configurations. The continuum Path Integral is simply the $\ell^2$ continuous hallucination of a discrete graph routing optimization problem. The physical "Scattering Amplitude" is precisely the un-normalized sum of the finite algebraic geometric permutations necessary for the 2-simplex to heal a local tear.

---

## 7. Dark Matter from Non-Resonant Defects

### 7.1 Resonant and Non-Resonant Configurations

In the $\ell^1$ framework, Standard Model particles are $\ell^1$ defect configurations that exactly match the gauge representation requirements: quarks carry $(3, 2, Y)$ under $SU(3) \times SU(2) \times U(1)$; leptons carry $(1, 2, Y)$ or $(1, 1, Y)$. These are *resonant* defects: they fit the simplex boundary structure.

Not every $\ell^1$ defect configuration factorizes into Standard Model representations. Configurations that fail to match any $(R_3, R_2, Y)$ assignment cannot couple to the Standard Model gauge fields. These *non-resonant* defects have four properties:

1. **Massive**: they carry $\ell^1$ defect energy.
2. **Invisible**: they cannot emit or absorb Standard Model gauge bosons.
3. **Gravitating**: they contribute to the Regge deficit.
4. **Stable**: no Standard Model decay channel is available.

These properties are qualitatively consistent with those attributed to dark matter.

### 7.2 Topological Estimate

On the single 2-simplex (3 edges, each carrying $\pm 1$ orientation), there are $2^3 = 8$ topological configurations. Of these, 4 have holonomy $+1$ (consistent loop, resonant) and 4 have holonomy $-1$ (frustrated loop, non-resonant). The non-resonant fraction is $4/8 = 0.50$ (`execute_50`).

The observed dark matter fraction is $\Omega_{\mathrm{DM}} / (\Omega_{\mathrm{DM}} + \Omega_b) = 0.27 / (0.27 + 0.05) = 0.84$.

The combinatorial estimate demonstrates that non-resonant configurations are generically abundant. The precise cosmological abundance depends on global lattice dynamics and is not predicted by the single-simplex model.

---

## 8. Dark Energy from Subdivision Overshoot

### 8.1 The Mechanism

The $\ell^1$ healing algorithm inserts vertices to reduce tension. The equilibrium is the $\{3,6\}$ tiling with valence 6. But the algorithm is local: it cannot globally coordinate to produce exactly valence 6 everywhere.

In regions where subdivision overshoots, the local valence exceeds 6:

$$\text{valence} = 6 + \varepsilon, \quad \varepsilon > 0$$

The Regge deficit becomes negative: $\epsilon = 2\pi - (6 + \varepsilon) \times \pi/3 = -\varepsilon\pi/3$. Negative curvature produces a repulsive gravitational effect, driving accelerated expansion.

### 8.2 The Cosmological Constant Problem

In quantum field theory, the cosmological constant problem asks: why is $\Lambda \sim 10^{-122} M_P^4$ instead of $\sim M_P^4$? In the $\ell^1$ framework:

- $\Lambda = 0$ would require perfect global coordination of the subdivision algorithm, which is impossible for a local process.
- $\Lambda \sim M_P^4$ would require every vertex to have valence 7, a catastrophic overshoot inconsistent with the near-flatness of the observed universe.
- $\Lambda \sim 10^{-122} M_P^4$ means the local algorithm is almost perfect: approximately 1 extra triangle per $10^{61}$ vertices.

The smallness of $\Lambda$ is not fine-tuning. It reflects the efficiency of the $\ell^1$ healing algorithm: a local process that is $99.99\ldots\%$ correct globally (`execute_51`).

These interpretations are qualitative and are not presented as derived predictions. A quantitative prediction of $\Lambda$ and dark matter mass spectra from $\ell^1$ dynamics remains an open problem.

---

## 9. The Norm Tower: $\ell^1 \to \ell^2 \to \ell^\infty$

### 9.1 Three Norms, Three Scales

Each $\ell^p$ norm describes physics at a characteristic scale:

| Norm | Scale | Physics | Characteristic |
|------|-------|---------|----------------|
| $\ell^1$ | Planck | Discrete defect counting | No cancellations; monotone correction |
| $\ell^2$ | Quantum | Hilbert space, Born rule | Interference allowed; Parseval's identity |
| $\ell^\infty$ | Classical | Deterministic trajectories | Maximum defect dominates |

### 9.2 The Norm Inequality

For any vector $x$: $\|x\|_\infty \leq \|x\|_2 \leq \|x\|_1$. This is verified for all test configurations at `execute_52`. The inequality is strict when more than one component is nonzero. The $\ell^1$ norm is maximally sensitive (it counts all defects individually); the $\ell^\infty$ norm sees only the largest; the $\ell^2$ norm interpolates.

### 9.3 The Emergence Chain

The scaling hierarchy is:

$$\ell^1 \text{ (Planck)} \xrightarrow{\text{Parseval}} \ell^2 \text{ (quantum)} \xrightarrow{\text{law of large numbers}} \ell^\infty \text{ (classical)} \xrightarrow{\text{Regge limit}} \text{GR (cosmological)}$$

Each level is a coarse-graining of the one above it. Information is lost at each step:

1. **$\ell^1 \to \ell^2$**: The discrete Fourier transform and Parseval's identity (Paper 008, Section 4) transform the $\ell^1$ defect counting into $\ell^2$ Hilbert space structure. This aligns with the phase-averaging derivation of the Born rule (Paper 007a).

2. **$\ell^2 \to \ell^\infty$**: The law of large numbers applied to many quantum measurements. In the limit of many particles, the dominant eigenvalue controls the dynamics. This is the classical limit.

3. **$\ell^\infty \to$ GR**: The Regge limit of the classical tiling. Smooth curvature emerges from the statistical aggregate of discrete deficits. This is general relativity.

The $\ell^1$ lattice is the only exact description. Every other level of physics is an approximation obtained by changing the norm.

---

## 10. The Derivation Structure

### 10.1 Overview

The framework proposes a constrained derivation chain beginning from:

* a minimal inconsistency (sign distinction)
* a monotone correction principle

and generating a hierarchy of structures through successive constraints.

Each step is either:

* **derived** (structurally forced)
* **constructed** (given prior results)
* **interpreted** (mapping to known physics)

### 10.2 Structural Progression

The derivation proceeds in stages:

#### Stage I: Norm and Discrete Structure

1. **$\ell^1$ norm selection**
   Forced by additivity, locality, and monotone correction

2. **Emergence of $N = 3$ structure**
   From minimal resolution of sign inconsistency

3. **Discrete Fourier structure (DFT)**
   Representation theory of $\mathbb{Z}_3$

4. **Hilbert structure and Born rule**
   Via Parseval correspondence under transform

#### Stage II: Operator and Measure Constraints

5. **Transport amplitude structure ($a = 3/\pi$)**
   From symmetry, normalization, and domain constraints

6. **Integral representation (RMK)**
   Operator expressed via measure, observable, domain

7. **Unitarity deviation parameter**
   Derived from structural constraints on operators

#### Stage III: Gauge Structure

8. **$SU(3)$ from closed loop structure**
9. **$SU(2)$ from bifurcation symmetry**
10. **$U(1)$ from edge-level transport**

These arise as:

> distinct dimensional projections of the same underlying structure

#### Stage IV: Phenomenological Correspondence

11. **Coupling relationships (GUT scale)**
12. **Generation count ($N_g = 3$)**
13. **Electroweak structure and mixing angle**

These steps involve:

* structural derivation
* plus phenomenological anchoring

#### Stage V: Geometric Extension

14. **Discrete tiling ($\{3,6\}$)**
15. **Curvature from Regge defects (Section 3)**
16. **Planck scale as defect threshold**

#### Stage VI: Structural Consequences

17. **Non-invertibility of coarse-graining (Section 5)**
18. **Norm hierarchy $\ell^1 \to \ell^2 \to \ell^\infty$**
19. **Qualitative dark sector mechanisms**

### 10.3 Nature of the Derivation

The chain is not purely deductive in the classical axiomatic sense.

Instead, it is:

> a constrained construction in which each stage reduces available degrees of freedom

Key characteristics:

* No continuous free parameters introduced prior to phenomenological matching
* Structural constraints propagate forward
* Later stages depend only on earlier derived structure

### 10.4 Boundary of Validity

The framework distinguishes clearly between:

#### Structurally Derived

* discrete lattice structure
* norm hierarchy
* gauge decomposition
* curvature as defect
* Newton's constant $G$
* Einstein Field Equations

#### Partially Derived / Anchored

* coupling constants
* energy scales
* mixing parameters

#### Open

* cosmological constant (quantitative)
* fermion mass spectrum

### 10.5 Interpretation

The derivation suggests that:

> a large portion of known physical structure may arise from constraints on resolving minimal inconsistency

However:

* the framework is not yet complete
* several key quantitative components remain external

### 10.6 Computational Role

The associated computational pipeline:

* verifies internal consistency
* confirms constraint propagation
* checks absence of contradictions

It does **not** constitute experimental validation.

---

## 11. Operator Uniqueness Under $\ell^1$ Structural Constraints

We formalize the uniqueness of the transport amplitude within the admissible operator class defined by the $\ell^1$ framework.

### 11.1 Problem Statement

Let an admissible transport operator be defined as a functional:

$$
\mathcal{T}(f) = \int_{\Omega} f(\theta) \, d\mu(\theta)
$$

where:

* $\mu$ is a measure on $S^1$
* $f$ is a real-valued observable
* $\Omega \subset S^1$ is a domain determined by local topology

We seek to characterize all triples $(\mu, f, \Omega)$ satisfying the structural constraints imposed by the $\ell^1$ causal lattice.

### 11.2 Structural Constraints

The admissible operator must satisfy:

#### (C1) Shift Invariance

$$
\mu(\theta + \phi) = \mu(\theta)
$$
for all $\phi \in S^1$

→ implies $\mu$ is proportional to Haar measure

#### (C2) Linearity

$$
\mathcal{T}(a f_1 + b f_2) = a \mathcal{T}(f_1) + b \mathcal{T}(f_2)
$$

→ restricts operator to integral form

#### (C3) Reality

$$
f(\theta) \in \mathbb{R}
$$

#### (C4) Normalization

$$
f(0) = 1
$$

#### (C5) Even Symmetry ($\ell^1$ Edge Invariance)

$$
f(\theta) = f(-\theta)
$$

→ removes odd components

#### (C6) Locality / Single-Step Transport

Operator depends only on a single-edge interaction

→ excludes higher harmonics $f(n\theta)$, for $n > 1$

#### (C7) Domain Constraint (Discrete Topology)

The domain $\Omega$ is determined by:

* cycle graph $C_3$
* vertex degree $d = 2$
* equal Voronoi partition

$$
\Omega = [-\pi/6, \pi/6]
$$

### 11.3 Classification of Observable Space

The general real-valued function on $S^1$ can be written:

$$
f(\theta) = a \cos\theta + b \sin\theta
$$

Applying constraints:

* Even symmetry ⇒ $b = 0$
* Normalization ⇒ $a = 1$

Thus:

$$
f(\theta) = \cos\theta
$$

This is the **unique admissible observable**.

### 11.4 Measure Uniqueness

By (C1), the measure is uniquely:

$$
d\mu = \frac{d\theta}{|\Omega|}
$$

(Haar measure normalized on the domain)

### 11.5 Domain Uniqueness

The domain $\Omega$ is fixed by:

* minimal closed topology ($N = 3$)
* vertex degree ($d = 2$)
* equal partition of angular space

Thus:

$$
\Omega = [-\pi/6, \pi/6]
$$

No continuous degree of freedom remains.

### 11.6 Result

The transport amplitude is therefore uniquely:

$$
\mathcal{T} = \frac{1}{|\Omega|} \int_{-\pi/6}^{\pi/6} \cos\theta \, d\theta
= \frac{\sin(\pi/6)}{\pi/6}
= \frac{3}{\pi}
$$

### 11.7 Uniqueness Statement

Under constraints (C1–C7):

> Within the constraint class (C1–C7), there exists a unique admissible transport operator. We do not claim that the constraint class itself is uniquely forced.

Equivalently:

* Measure space: dimension $0$ (unique)
* Observable space: dimension $0$ (unique)
* Domain: dimension $0$ (unique)

Thus:

$$
\dim(\text{operator space}) = 0
$$

and the transport amplitude $3/\pi$ is the **unique output** of the construction.

### 11.8 Exclusion of Alternatives

All alternative constructions violate at least one constraint:

| Alternative | Violation |
| --- | --- |
| Non-Haar measure | breaks shift invariance |
| $\sin\theta$ component | breaks even symmetry |
| $\cos(n\theta), n>1$ | violates locality / single-step |
| Larger domain | violates discrete topology |
| Weighted domain | breaks symmetry |

### 11.9 Interpretation

The value $3/\pi$ is not introduced or fitted.

It arises as:

> the unique invariant amplitude of single-step transport on a discrete $\ell^1$-stabilized 2-simplex under symmetry, locality, and normalization constraints.

The derivation of the transport amplitude is conditional on the discrete topology and locality constraints derived in earlier sections. Alternative topologies or nonlocal operators may yield different amplitudes, but such constructions fall outside the present framework.

---

## 12. Gauge Structure from $\ell^1$ Boundary Constraints

We formalize the emergence and uniqueness of the gauge structure within the $\ell^1$ causal lattice.

### 12.1 Problem Statement

Given:

* a discrete $\ell^1$-stabilized 2-simplex,
* with minimal closed topology ($N = 3$),
* and transport defined along edges, hinges, and closed loops,

we classify all admissible symmetry structures compatible with:

* locality,
* unitary transport,
* closure under composition,
* and $\ell^1$ boundary constraints.

### 12.2 Structural Decomposition

The 2-simplex admits three distinct geometric structures:

| Structure | Dimension | Interpretation |
| --- | --- | --- |
| Vertex set | 0D | states |
| Edge | 1D | transport |
| Open path (2 edges) | 2D boundary | bifurcation |
| Closed loop (3 edges) | 2D closed boundary | holonomy |

These correspond to **three distinct operator domains**.

### 12.3 Constraint Set

Any admissible symmetry group $G$ must satisfy:

#### (G1) Locality

Transformations act on single-step transport (edges or minimal loops)

#### (G2) Unitarity

Transport preserves norm under composition:

$$
U^\dagger U = I
$$

#### (G3) Closure

Group structure must be closed under composition of local transport operations

#### (G4) Minimality

No higher-dimensional cell structure beyond the 2-simplex is permitted

→ excludes $N > 3$ polygonal structures

#### (G5) Boundary Compatibility

Symmetry must respect:

* edge transport (1D)
* hinge transitions (2D open)
* loop holonomy (2D closed)

### 12.4 Classification by Dimension

We now classify admissible symmetry structures by boundary type.

#### (A) Closed Loop Symmetry (3-edge holonomy)

The minimal closed structure is:

$$
C_3
$$

Transport around the loop defines:

$$
U = \exp(i \theta_a T^a)
$$

Constraints:

* 3 independent directions
* non-abelian closure required
* unitary representation

The unique compact simple Lie group satisfying:

* dimension = 3 generators (fundamental representation dimension 3)
* non-abelian closure
* compatibility with complex vector space $\mathbb{C}^3$

is:

$$
SU(3)
$$

#### (B) Open Boundary Symmetry (2-edge hinge)

The minimal open structure is a bifurcation:

* 2 connected edges
* no closure constraint

Transport must:

* be unitary
* allow mixing between two states
* preserve normalization

This uniquely selects:

$$
SU(2)
$$

as the group of unitary transformations on $\mathbb{C}^2$

#### (C) Edge Transport (1D)

A single edge supports:

* phase transport only
* no internal mixing

Thus:

$$
U = e^{i\theta}
$$

This defines:

$$
U(1)
$$

### 12.5 Exclusion of Higher Groups

We now show that larger groups are inadmissible.

#### (E1) $SU(N), N > 3$

Requires:

* $N$-gon minimal closed structure
* $N > 3$ edges per loop

Violates:

* (G4) minimality
* $\ell^1$ transport optimality (increased path length)

#### (E2) $SO(N)$

Acts on real vector spaces.

Violates:

* complex structure required by DFT / Hilbert emergence

#### (E3) Product Extensions

Additional factors require:

* independent degrees of freedom
* additional geometric structure

Not present in 2-simplex topology

#### (E4) Exceptional Groups

Require:

* higher-dimensional algebraic structure
* no embedding in 2-simplex boundary

### 12.6 Result

The admissible symmetry decomposition is uniquely:

$$
SU(3) \times SU(2) \times U(1)
$$

with:

* $SU(3)$: closed loop holonomy
* $SU(2)$: open boundary mixing
* $U(1)$: edge phase transport

The identification of $SU(3)$, $SU(2)$, and $U(1)$ should be understood as the minimal compact unitary groups compatible with the dimensionality and compositional structure of the boundary operators. We do not exclude the existence of alternative representations without additional constraints on representation faithfulness and irreducibility.

### 12.7 Uniqueness Statement

Under constraints (G1–G5):

> Within the constraint class (G1–G5), there exists a unique admissible gauge structure compatible with the $\ell^1$-stabilized 2-simplex. We do not claim that the constraint class itself is uniquely forced.

Equivalently:

* Closed symmetry space: dimension 0 (unique)
* Open symmetry space: dimension 0 (unique)
* Edge symmetry space: dimension 0 (unique)

Thus:

$$
\dim(\text{gauge structure space}) = 0
$$

### 12.8 Interpretation

The Standard Model gauge group is not:

* postulated,
* or selected from a larger symmetry,

but arises as:

> the unique decomposition of transport symmetries across the dimensional boundaries of the minimal $\ell^1$-stabilized topology.

---

## 13. Zero Free Parameter Theorem

We now combine the preceding results to establish the structural rigidity of the $\ell^1$ causal lattice framework.

### 13.1 Statement of the Problem

A physical theory is said to possess **free parameters** if:

* continuous degrees of freedom must be externally specified, or
* multiple inequivalent constructions satisfy the same foundational constraints.

We examine whether the $\ell^1$ causal lattice admits any such freedom.

### 13.2 Structural Components

The construction proceeds through the following elements:

| Component | Role | Status |
| --- | --- | --- |
| $\ell^1$ norm | defect measurement | forced |
| 2-simplex ($N = 3$) | minimal resolution topology | forced |
| Fourier structure | spectral representation | forced |
| Operator (transport amplitude) | interaction strength | unique |
| Gauge structure | symmetry decomposition | unique |
| Domain geometry | angular constraint | unique |

Each component is determined by prior constraints.

### 13.3 Degree-of-Freedom Accounting

We count remaining degrees of freedom:

#### (A) Measure space

By Haar invariance:

$$
\dim(\mu) = 0
$$

#### (B) Observable space

After symmetry and normalization:

$$
\dim(f) = 0
$$

#### (C) Domain

From discrete topology:

$$
\dim(\Omega) = 0
$$

#### (D) Operator

Constructed from (A–C):

$$
\dim(\mathcal{T}) = 0
$$

#### (E) Gauge structure

From boundary classification:

$$
\dim(G) = 0
$$

### 13.4 Result

The total number of internal free parameters is:

$$
\dim(\text{theory}) = 0
$$

### 13.5 Interpretation

All primary structures arise from:

* discrete topology
* symmetry constraints
* locality and minimality

No continuous parameter is introduced prior to phenomenological matching.

Thus:

> The $\ell^1$ causal lattice defines a **framework with no continuous free parameters within the specified constraint class** at the level of its internal construction.

### 13.6 Relation to Physical Constants

Observed physical constants enter in two ways:

#### (1) Structurally determined

Examples:

* transport amplitude ($3/\pi$)
* gauge decomposition
* generation count

These arise from zero-parameter construction.

#### (2) Phenomenologically anchored

Examples:

* cosmological constant ($\Lambda$)
* fermion mass spectrum

These correspond to:

> quantities not yet derived from the discrete structure

and are explicitly identified as open problems.

### 13.7 Consequence

The framework implies:

> any successful geometric or symmetry extension must preserve zero internal degrees of freedom

or identify precisely where additional topological structure enters.

### 13.8 Falsifiability

The zero-parameter nature introduces a strong constraint:

> any alternative construction satisfying the same structural axioms must reproduce the same outputs.

Thus, the framework is falsified if:

* an admissible operator exists with amplitude $\neq 3/\pi$, or
* an admissible symmetry structure differs from $SU(3) \times SU(2) \times U(1)$, or
* a consistent $\ell^1$ construction produces additional free parameters

### 13.9 Summary

The $\ell^1$ causal lattice is not:

* a parameterized model,
* nor a family of theories

but:

> a single constrained construction with no internal degrees of freedom. The only remaining freedom lies in the existence of the initial inconsistency itself, which is not a parameter of the theory but the condition under which any theory becomes possible.

### 13.10 On the Scope of Uniqueness Claims

The uniqueness results established in Sections 11–13 are conditional on the specified constraint set:

* locality (single-step transport)
* linearity
* symmetry (shift invariance, parity)
* minimal topology (2-simplex)

A potential objection is that alternative admissible constructions may exist outside this constraint set.

This objection is valid in principle. However:

> any such construction must explicitly identify which constraint is relaxed and demonstrate that the resulting structure preserves the intended physical invariants.

In particular, alternatives must account for:

* stability under composition
* bounded transport
* compatibility with discrete topology

Absent such a construction, the classification remains complete within the stated domain.

---

## 14. Open Problems

1. **Derive the cosmological constant quantitatively.** The subdivision overshoot mechanism predicts $\Lambda > 0$ and explains its smallness qualitatively. A quantitative prediction requires a theory of the average overshoot rate.

2. **Derive the dark matter mass spectrum.** The non-resonant defect mechanism predicts massive, invisible, gravitating, stable particles. The mass distribution requires understanding which non-resonant configurations are dynamically accessible.

3. **Formalize the coarse-graining steps.** The transitions $\ell^1 \to \ell^2$ (Parseval) and $\ell^2 \to \ell^\infty$ (law of large numbers) are identified but not rigorously proven to be the unique coarse-graining maps preserving the relevant physical structure.

4. **Derive fermion masses and mixing.** The three generations are forced (Paper 009), but the mass hierarchy within and between generations remains underived.

---

## 15. Conclusion

This work proposes that a substantial portion of known physical structure can be derived from a single organizing principle: monotone correction of local inconsistency under the $\ell^1$ coboundary norm.

Starting from this principle and a minimal discrete seed, the framework constructs a sequence of constrained structures, including:

* a discrete $N = 3$ lattice and associated Fourier structure,
* Hilbert space behavior via $\ell^1 \to \ell^2$ correspondence,
* a constrained transport amplitude and associated unitarity deviation,
* a framework consistent with key structural features of the Standard Model gauge group $SU(3) \times SU(2) \times U(1)$,
* consistency with three fermion generations and electroweak structure,
* discrete geometric tiling and curvature via Regge defects,
* the Planck scale as a defect threshold,
* and a hierarchy of effective descriptions arising from norm transitions.

Within this framework, several longstanding problems are reinterpreted:

* The hierarchy between gravitational and electroweak scales appears as a statement about lattice extent rather than parameter fine-tuning.
* The cosmological constant reflects residual imbalance in a locally driven subdivision process rather than vacuum energy divergence.
* Dark matter corresponds to defect configurations that do not couple to the Standard Model gauge structure.

The framework does not yet provide quantitative derivations of the cosmological constant, a global dark matter mass spectrum, or fermion mass hierarchies. These remain open problems.

The central claim is therefore not that all physical quantities have been derived, but that:

> a large fraction of known structure can be organized as the consequence of a single constrained discrete mechanism, with remaining parameters isolated and clearly identified.

If correct, this shifts the role of unification:

> not as the merger of independent theories,
> but as the identification of a common discrete substrate from which multiple effective descriptions emerge.

---

## References

[1] T. Regge, "General relativity without coordinates," *Il Nuovo Cimento* **19**, 558 (1961).

[2] J. Maldacena, "The large-$N$ limit of superconformal field theories and supergravity," *Int. J. Theor. Phys.* **38**, 1113 (1999).

[3] C. Rovelli, *Quantum Gravity* (Cambridge University Press, 2004).

[4] J. Polchinski, *String Theory*, Vols. 1--2 (Cambridge University Press, 1998).

[5] R. D. Sorkin, "Causal sets: Discrete gravity," in *Lectures on Quantum Gravity*, eds. A. Gomberoff and D. Marolf (Springer, 2005).

[6] Particle Data Group (R. L. Workman et al.), "Review of Particle Physics," *PTEP* **2022**, 083C01 (2022). Updated 2024.

[7] Planck Collaboration (N. Aghanim et al.), "Planck 2018 results. VI. Cosmological parameters," *Astron. Astrophys.* **641**, A6 (2020).

[8] J. H. Carroll, "Paper 000: Projection Obstruction Theory - Retraction Nonlinearity, l1 Rigidity, and Density Scaling" (2026).

[9] J. H. Carroll, "Paper 001: The Free L1 Seminorm on Banach Presheaf Coboundaries" (2026).

[10] J. H. Carroll, "Paper 002: Coordinate-Wise Additivity and the L1 Norm on Finite Graph Cochains" (2026).

[10] J. H. Carroll, "Paper 003: Hodge Structure and Gauge Equivalence of L1 Defect Fields" (2026).

[11] J. H. Carroll, "Paper 004: An L1 Obstruction Framework for Coboundary Defects" (2026).

[12] J. H. Carroll, "Paper 005: Autopoietic Cohomology - Iterative Obstruction Repair on Causal Posets" (2026).

[13] J. H. Carroll, "Paper 006: A Common L1 Defect Framework for Quantum, Causal, and Gravitational Systems" (2026).

[14] J. H. Carroll, "Paper 007: Topological Constraint on the Electromagnetic Coupling Scale from a Discrete $\ell^1$ Obstruction" (2026).

[15] J. H. Carroll, "Paper 008: Emergent Gauge Symmetry from L1 Defect Flow" (2026).







---