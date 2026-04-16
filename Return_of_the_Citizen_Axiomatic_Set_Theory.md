# Return of the Citizen: An Axiomatic Treatment

## Introduction

### by Patrick Suppes

The application of axiomatic methods to domains beyond pure mathematics is by now a familiar enterprise. Since the pioneering work of Hilbert on geometry, and the subsequent axiomatizations of probability by Kolmogorov and of utility theory by von Neumann and Morgenstern, it has been increasingly clear that the rigor of formal systems need not be confined to the objects of mathematical intuition. The present work extends this program to a domain that may at first appear unlikely: the theory of citizenship as developed in Michael P. Suppes and William P. Schulz's *Return of the Citizen*.

I should say at the outset that what follows is not a formalization in the strict sense that one finds in metamathematics. We do not here establish completeness or decidability results. Rather, what we offer is an axiomatization in the sense that has proved fruitful in the empirical sciences: a precise statement of primitive notions, a finite list of axioms from which the principal claims of the theory may be derived as theorems, and a set of definitions that make explicit the logical relationships among the concepts employed. The aim is clarity of structure, not mechanical proof.

The reader familiar with my *Axiomatic Set Theory* (1960) will recognize the method. We begin with certain primitive notions that are not themselves defined within the system but whose intended interpretation is given informally. We then state axioms governing these primitives---axioms that are not themselves proved but are taken as the foundational commitments of the theory. From these, we derive definitions and theorems in the usual way.

What makes the work of Suppes and Schulz particularly amenable to this treatment is that it already possesses, in literary form, the structure of an axiomatic theory. The four traditions of political philosophy that they survey---liberal, republican, communitarian, and post-liberal---function as competing axiom systems for the concept *citizen*. Their synthesis, which they call Republican Liberalism, is in effect the proposal of a new axiom system that preserves the consistency of liberalism's rights-commitments while incorporating the republicans' formation-thesis and the communitarians' critique of the unencumbered self. The diagnostic chapters of Volume II establish empirical boundary conditions---constraints that any adequate axiom system must satisfy. And the practices of Volume III are, in our terms, constructive existence proofs: demonstrations that the objects whose existence the axioms assert can in fact be exhibited.

I confess a particular satisfaction in seeing my son Michael's name on this volume. That a philosopher trained in the analytic tradition and a political theorist trained in the civic republican tradition should find in axiomatic method a common language is, I think, no accident. The method does not dictate conclusions; it clarifies the commitments from which conclusions follow. If Michael and William have sometimes disagreed about which axioms to adopt, they have never disagreed about the value of stating those axioms plainly. That is the family business.

I have taken certain liberties with the formalism where strict fidelity to set-theoretic notation would obscure rather than illuminate the political content. In particular, I have freely used ordered pairs, functions, and relations as primitive or near-primitive, rather than constructing them from the empty set in the usual Kuratowski fashion. This is a concession to readability that I trust the working mathematician will forgive and the political theorist will appreciate.

The result, I hope, is a document that makes the logical architecture of *Return of the Citizen* fully explicit---that shows precisely which claims depend on which, and where the real points of controversy lie. If the axioms are accepted, the theorems follow. If a theorem is rejected, one knows exactly which axiom must be surrendered. This is the permanent contribution of the axiomatic method to any domain of inquiry: not certainty, but transparency.

Stanford, California

---

## Part I: Primitive Notions and Axioms of Foundation

### 1. Primitive Notions

We take the following as **primitive** (undefined within the system):

| Symbol | Intended Interpretation |
|--------|------------------------|
| **P** | The set of all persons |
| **C** | The set of all communities |
| **S** | The set of all states (political institutions of sovereign authority) |
| **R** | A relation of *formation*: for *p* in **P** and *c* in **C**, *R(p, c)* holds iff *c* is formative of *p* |
| **D** | A relation of *domination*: for entities *x, y*, *D(x, y)* holds iff *x* holds arbitrary power over *y* |
| **A** | A function of *attention*: *A(p, q)* for *p, q* in **P** denotes the willed, patient regard of *p* toward *q* |

### 2. Axioms of Foundation

We state six axioms governing the primitive notions. These constitute the foundational commitments of the theory.

**Axiom 1** (Non-Empty Person). The set **P** is non-empty.

$$\mathbf{P} \neq \varnothing$$

*Remark.* This is the axiom of political realism. A theory of citizenship without persons is vacuous. Unlike certain post-structuralist accounts, we insist that the domain of discourse contains actual individuals.

**Axiom 2** (Formation). For every person *p* in **P**, there exists at least one community *c* in **C** such that *R(p, c)* holds.

$$(\forall p \in \mathbf{P})(\exists c \in \mathbf{C})[R(p, c)]$$

*Remark.* No person is unencumbered. This is the communitarian insight formalized: persons are never pre-social. The set of communities formative of a given person may be large or small, but it is never empty.

**Axiom 3** (Non-Reduction of Person to Community). For every person *p* in **P**, *p* is not identical to the set of communities that formed her.

$$(\forall p \in \mathbf{P})\left[p \neq \{c \in \mathbf{C} : R(p, c)\}\right]$$

*Remark.* This is the liberal insight formalized. Though every person is formed by communities (Axiom 2), no person is merely the sum of those formations. The irreducibility of the person to her formative communities is what grounds rights held against both community and state.

**Axiom 4** (State as Proper Subset). Every state *s* in **S** is a structured subset of **P** $\times$ **C**, never coextensive with the whole.

$$(\forall s \in \mathbf{S})\left[s \subset \mathbf{P} \times \mathbf{C} \;\wedge\; s \neq \mathbf{P} \times \mathbf{C}\right]$$

*Remark.* The state is a trust, not a totality. It organizes a relationship between persons and communities but never exhausts either. This formalizes the Lockean constraint: there is always a remainder of personhood and community life that the state does not and may not encompass.

**Axiom 5** (Liberty). A person *p* is free if and only if two conditions jointly obtain: (i) no entity interferes with *p*'s action without justification, and (ii) no entity holds arbitrary power over *p*.

Let $I(x, p)$ denote unjustified interference of *x* with *p*. Then:

$$\text{Free}(p) \iff \neg(\exists x)[I(x, p)] \;\wedge\; \neg(\exists x)[D(x, p)]$$

*Remark.* This is the central axiom of the synthesis. Classical liberalism affirms only the first conjunct (negative liberty, non-interference). Classical republicanism affirms only the second (positive liberty, non-domination). The theory requires both. A benevolent master who never interferes still dominates; an anarchic order with no domination may still permit constant interference. The citizen requires protection from both.

**Axiom 6** (Intermediate Necessity). For any person *p* and any state *s*, the free citizenship of *p* within *s* requires the existence of at least one community *c* such that *c* is neither identical to *p* (considered as singleton) nor to *s*.

$$(\forall p \in \mathbf{P})(\forall s \in \mathbf{S})\left[\text{Citizen}(p, s) \implies (\exists c \in \mathbf{C})\left[R(p, c) \;\wedge\; c \neq \{p\} \;\wedge\; c \neq s\right]\right]$$

*Remark.* Between the isolated individual and the nation-state, there must exist intermediate associations---family, congregation, neighborhood, union, voluntary association. Without these, both atomization and tyranny result. This is the Tocquevillian axiom: associations are the "schools of self-government."

---

## Part II: Definitions

From the primitives and axioms, we construct the following definitions.

**Definition 1** (Citizen). A person *p* is a *citizen* of state *s* if and only if:
1. *p* is free (in the sense of Axiom 5),
2. there exists an intermediate community satisfying Axiom 6,
3. *p* stands in a relation of reciprocal obligation with *s*, and
4. *p* possesses the capacity for civic virtue (Definition 3 below).

$$\text{Citizen}(p, s) \iff \text{Free}(p) \;\wedge\; (\exists c \in \mathbf{C})[R(p,c) \wedge c \neq \{p\} \wedge c \neq s] \;\wedge\; O(p, s) \;\wedge\; O(s, p) \;\wedge\; V(p)$$

where $O(x, y)$ denotes that *x* bears obligation toward *y*, and $V(p)$ denotes that *p* possesses civic virtue.

*Remark.* The citizen is an individual who belongs. This definition synthesizes four conditions that the four traditions each emphasize separately: freedom (liberal), formation (communitarian), obligation (republican), and virtue (classical).

**Definition 2** (Social Capital). Let **C**$_p$ = $\{c \in \mathbf{C} : p \in c\}$ denote the set of communities to which person *p* belongs. We distinguish two subsets:

- *Bonding capital* of *p*: $B(p) = \{c \in \mathbf{C}_p : (\forall q \in c)[q \approx p]\}$, where $\approx$ denotes social similarity.
- *Bridging capital* of *p*: $\text{Br}(p) = \{c \in \mathbf{C}_p : (\exists q \in c)[q \not\approx p]\}$, where members cross lines of social difference.

The *total social capital* of *p* is $\Sigma(p) = B(p) \cup \text{Br}(p) = \mathbf{C}_p$.

*Remark.* The Putnam thesis is that $|\Sigma(p)|$ has declined across the population, and that $|\text{Br}(p)|$ has declined faster than $|B(p)|$. When bridging capital vanishes, political identity becomes the sole organizing loyalty.

**Definition 3** (Civic Virtue). Let $\rho$ be a role (a function from situations to actions satisfying internal standards of excellence). Civic virtue is the disposition to act well in the role of citizen:

$$V(p) \iff (\exists \rho)[\rho = \text{citizen-role} \;\wedge\; p \text{ reliably instantiates } \rho]$$

*Remark.* Virtue is not moralism. It is the practiced capacity to meet the internal standards of a role. A carpenter has the virtue of craftsmanship; a citizen has the virtues of attention, deliberation, and accountability. This follows the Aristotelian understanding that virtue is a *hexis*---a stable disposition acquired through practice, not a feeling or an opinion.

**Definition 4** (Atomization). A person *p* is *atomized* if and only if the intermediate community condition fails:

$$\text{Atom}(p) \iff (\forall c \in \mathbf{C})\left[R(p, c) \implies (c = \{p\} \;\vee\; c = s)\right]$$

for the relevant state *s*. That is, the only communities that form *p* are the trivial ones: *p* alone, or the state itself.

*Remark.* Atomization is not solitude (which may be chosen and rich). It is the structural condition in which all intermediate associations have been emptied. The atomized person stands naked before the state.

**Definition 5** (Mass Movement). A mass movement *M* is a subset of **P** equipped with a function $\phi : M \to \mathcal{F}$, where $\mathcal{F}$ is a set of "total fictions" (comprehensive narratives that explain everything and predict nothing), satisfying eight closure conditions (the Lifton criteria):

1. *Milieu control*: $(\forall p \in M)[\text{information}(p) \subseteq \text{approved}(M)]$
2. *Mystical manipulation*: $(\exists e \in M)[\text{orchestrates-experiences}(e, M)]$
3. *Demand for purity*: $M$ admits a partition into $\text{Pure}(M)$ and $\mathbf{P} \setminus M$, with the boundary treated as absolute
4. *Cult of confession*: $(\forall p \in M)[\text{self-disclosure}(p) \text{ is mandatory}]$
5. *Sacred science*: $\phi$ is treated as unfalsifiable
6. *Loading the language*: $(\exists L \subset \text{Language})[L \text{ replaces ordinary discourse within } M]$
7. *Doctrine over person*: $(\forall p \in M)[\phi(p) \text{ overrides } p\text{'s experience}]$
8. *Dispensing of existence*: $(\forall q \notin M)[\text{humanity}(q) \text{ is conditional}]$

*Remark.* This definition applies symmetrically. It does not distinguish left from right, religious from secular, political from therapeutic. Any formation satisfying these eight conditions is a mass movement in the technical sense, whether it calls itself a party, a church, a wellness community, or a startup.

**Definition 6** (Institution-as-Mold). An institution *c* in **C** functions as a *mold* if the formation relation *R* satisfies a character-shaping condition:

$$\text{Mold}(c) \iff (\forall p \in c)\left[R(p, c) \implies (\exists \rho_c)[p \text{ is constrained toward } \rho_c]\right]$$

where $\rho_c$ is the role internal to institution *c*. The institution forms its members by holding them to the standards of the role.

**Definition 7** (Institution-as-Platform). An institution *c* functions as a *platform* if the formation relation is inverted:

$$\text{Platform}(c) \iff (\forall p \in c)\left[p \text{ uses } c \text{ for self-presentation rather than being formed by } c\right]$$

*Remark.* The Levin thesis: when institutions shift from molds to platforms, trust erodes and formation ceases. The doctor, journalist, legislator, or pastor who treats her institution as a stage for personal performance rather than a structure that shapes character has abandoned the formative function.

**Definition 8** (The Prism). Let $\Pi : \mathbf{P} \times \mathbf{P} \to \text{Perception}$ be the function that maps pairs of persons to their perception of each other. The *prism effect* is a systematic distortion:

$$(\forall p, q \in \mathbf{P})\left[\text{partisan}(p) \neq \text{partisan}(q) \implies \Pi(p, q) \gg \text{actual}(q)\right]$$

where $\gg$ denotes that the perceived extremity of *q* as seen by *p* significantly exceeds the actual position of *q*.

*Remark.* The perception gap. Each side sees a caricature of the other. The most politically engaged have the least accurate perceptions. The prism does not merely reflect polarization; it manufactures it from people with more moderate beliefs than either side supposes.

---

## Part III: Theorems

We now derive the principal claims of the theory.

**Theorem 1** (The Formation Theorem). *No person can be a citizen without having been formed by at least one non-trivial community.*

*Proof.* By Definition 1, $\text{Citizen}(p, s)$ requires $(\exists c \in \mathbf{C})[R(p,c) \wedge c \neq \{p\} \wedge c \neq s]$. This is precisely the intermediate community condition of Axiom 6. By Axiom 2, at least one formative community exists, but Axiom 6 further requires it to be non-trivial. Therefore citizenship presupposes non-trivial formation. $\square$

**Theorem 2** (The Irreducibility Theorem). *No citizen is identical to the communities that formed her.*

*Proof.* By Axiom 3, $p \neq \{c \in \mathbf{C} : R(p, c)\}$ for all *p* in **P**. Since every citizen is a person (Definition 1), the result follows. $\square$

*Remark.* Theorems 1 and 2 jointly establish the central structural claim: the citizen requires community for her formation (Theorem 1) but is not reducible to that formation (Theorem 2). The liberal and communitarian insights are not opposed; they are conjuncts in a single theorem.

**Theorem 3** (The Atomization--Mass Movement Theorem). *If a person is atomized, then that person satisfies a necessary condition for membership in a mass movement.*

*Proof.* Suppose $\text{Atom}(p)$. By Definition 4, $p$'s formative communities are restricted to $\{p\}$ and $s$. Then $|\Sigma(p)| \leq 2$ (only trivial memberships remain), and $|\text{Br}(p)| = 0$ (no bridging ties). By Definition 5, mass movements recruit from persons whose intermediate community structure has collapsed, since the total fiction $\phi$ offers a substitute for the belonging that intermediate communities formerly provided. The atomized person, possessing no formative associations to anchor identity, satisfies the structural precondition: availability for capture. $\square$

*Remark.* This is the Hoffer-Arendt thesis in set-theoretic dress. The mass movement does not recruit the politically engaged citizen with thick associational ties. It recruits the lonely, the stripped, the atomized. Atomization and mass capture are not opposites; they are the same phenomenon at different temporal moments.

**Theorem 4** (The Paradox of Neutrality). *A state that is neutral about the conditions of formation is not neutral.*

*Proof.* Suppose state *s* adopts the policy: $(\forall c \in \mathbf{C})[\text{state-indifference}(s, c)]$---that is, *s* takes no action regarding any community. By Axiom 6, citizenship requires intermediate communities. If *s* is indifferent to the conditions under which such communities arise, persist, or decay, then *s* is indifferent to a necessary condition of citizenship. But by Axiom 4, *s* organizes a relationship between persons and communities. Indifference to the conditions of that relationship is itself a policy---it is the policy of permitting the erosion of the conditions of citizenship. Therefore the apparently neutral stance is substantively non-neutral: it favors the dissolution of intermediate communities over their preservation. $\square$

*Remark.* This is the farmer metaphor formalized. A state that refuses to attend to the conditions of civic formation, on the grounds that it must not "impose" any particular conception of the good, thereby imposes one: the conception under which formation does not matter. Neutrality about ways of life does not entail neutrality about the conditions of choice.

**Theorem 5** (The Bridging Capital Theorem). *If bridging capital approaches the empty set across the population, then affective polarization increases without bound.*

*Proof.* Let $\text{Br}_{\text{total}} = \bigcup_{p \in \mathbf{P}} \text{Br}(p)$. Suppose $\text{Br}_{\text{total}} \to \varnothing$. Then no person belongs to a community containing members dissimilar to herself. By Definition 8, the prism function $\Pi$ is uncorrected---there exist no lived encounters across lines of difference to discipline perception toward accuracy. Without the corrective of actual cross-partisan experience, $\Pi(p, q) \gg \text{actual}(q)$ becomes self-reinforcing: each side's perception of the other grows more distorted, generating reciprocal hostility, which further reduces the probability of bridging encounters. The system has no equilibrium short of maximal polarization. $\square$

*Remark.* This is the connective tissue of the diagnosis. When unions, congregations, civic clubs, and neighborhood associations decline---when the bowling leagues empty and the Elks lodges close---there remain no spaces where a person of one partisan identity routinely encounters a person of another in a context not organized by partisanship. Politics becomes identity because no other cross-cutting identity remains.

**Theorem 6** (The Mold-Platform Theorem). *If all institutions in* **C** *become platforms, then civic virtue vanishes from* **P**.

*Proof.* By Definition 3, civic virtue requires reliable instantiation of a role $\rho$. By Definition 6, roles are maintained by institutions functioning as molds---institutions that constrain members toward role-internal standards. If all institutions become platforms (Definition 7), then no institution constrains any member toward any role. Without the constraint of role, $\rho$ is never reliably instantiated. Therefore $V(p)$ fails for all $p$, and by Definition 1, $\text{Citizen}(p, s)$ fails for all $p$ and $s$. $\square$

*Remark.* This is the Levin thesis as theorem. If every institution---legislature, newsroom, university, congregation---becomes a stage for personal performance rather than a structure that forms character through the discipline of role, then the practiced capacity for citizenship has no site of cultivation. Virtue is not self-generating; it requires institutions that function as molds.

**Theorem 7** (The Productive Tension Theorem). *The health of the republic requires that neither the Federalist axiom set nor the Anti-Federalist axiom set is exclusively adopted.*

*Proof.* Let $\mathcal{F}$ denote the Federalist axioms: large-scale representation, structural checks, ambition counteracting ambition. Let $\mathcal{A}$ denote the Anti-Federalist axioms: small-scale participation, civic virtue, face-to-face accountability.

Case 1: Suppose $\mathcal{F}$ is adopted and $\mathcal{A}$ is discarded. Then by $\mathcal{F}$, the republic operates through structural mechanism alone. But by Axiom 6, citizenship requires intermediate communities, which are precisely the local, participatory structures that $\mathcal{A}$ insists upon. Without $\mathcal{A}$, the structural mechanisms of $\mathcal{F}$ operate upon a population of non-citizens (by Theorem 1)---persons who have not been formed by participatory community. The result is what Tocqueville calls "soft despotism": an "immense tutelary power" administering a population of isolated individuals.

Case 2: Suppose $\mathcal{A}$ is adopted and $\mathcal{F}$ is discarded. Then the republic consists of small participatory communities without structural checks at scale. But by Axiom 5, freedom requires non-domination, and non-domination at scale requires structural protections against the tyranny of local majorities. Without $\mathcal{F}$, the small republics of $\mathcal{A}$ may each internally sustain civic virtue while externally producing sectionalism, exclusion, and the domination of minorities by local majorities.

In either case, at least one axiom of the system (Axiom 5 or Axiom 6) is violated. Therefore the republic requires both $\mathcal{F}$ and $\mathcal{A}$ as operative, and its health consists in maintaining the tension between them. $\square$

**Theorem 8** (The Feedback Loop). *Atomization, mass movement susceptibility, institutional decay, and polarization form a closed cycle with no stable equilibrium except at the extremes.*

*Proof.* We establish the cycle by showing each condition entails the next:

(i) $\text{Atom}(p) \implies$ susceptibility to mass movement (Theorem 3).

(ii) Mass movement membership further atomizes: by Definition 5, conditions (1) and (3) (milieu control and demand for purity) sever the member from all communities outside $M$, reducing $\mathbf{C}_p$ to $\{M, \{p\}\}$.

(iii) The remaining institutions, drained of members, shift from molds to platforms (Definition 7): with fewer members committed to role-internal standards, the institution's formative power declines, and self-presentation replaces formation.

(iv) By Theorem 6, civic virtue declines across the population. By Theorem 5, the loss of bridging capital accelerates polarization.

(v) Polarization produces further atomization: as political identity becomes the sole organizing identity (Theorem 5), persons who resist total identification are expelled from or withdraw from the remaining associational structures.

The cycle (i)$\to$(ii)$\to$(iii)$\to$(iv)$\to$(v)$\to$(i) is self-reinforcing. At no stage does the system generate endogenous corrective pressure. $\square$

*Remark.* This is the "connective tissue" of Volume II rendered as a formal cycle. All six of the diagnostic chapters describe aspects of a single self-reinforcing process. The cycle can be entered at any point---begin with atomization, or with institutional decay, or with polarization---and the same circuit results.

---

## Part IV: The Constructive Axioms (Practices)

The theorems of Part III are largely negative: they establish what fails, what decays, what spirals. The theory would be incomplete---indeed, it would be merely diagnostic---without a constructive component. We therefore introduce three additional axioms, corresponding to the three core practices of Volume III. These are *axioms of construction*: they assert the existence of operations by which the cycle of Theorem 8 may be interrupted.

**Axiom 7** (Attention). For any persons *p, q* in **P**, the attention function $A(p, q)$ is always defined; that is, any person can attend to any other.

$$(\forall p, q \in \mathbf{P})[\exists A(p,q)]$$

*Remark.* Attention is not agreement. It is the willed, patient regard of one person toward another---the foundational political discipline. It is always available as a capacity, though it may be unpracticed. This axiom asserts that no structural condition renders attention impossible, only difficult. The first practice of citizenship is the recovery of this capacity.

**Axiom 8** (Presumption of Good Faith). There exists a default mapping $G : \mathbf{P} \times \mathbf{P} \to \{0, 1\}$ such that $G(p, q) = 1$ (good faith presumed) unless and until evidence forces revision.

$$(\forall p, q \in \mathbf{P})[G(p, q) = 1 \;\text{by default}] \;\wedge\; [G(p, q) = 0 \text{ only if } \text{Evidence}(\neg\text{good-faith}(q))]$$

*Remark.* This is an axiom, not a theorem---it cannot be derived from the other axioms, and it is not forced by the evidence (which is equally compatible with universal suspicion). It is a *commitment*: the decision to treat other persons as fellow citizens attempting in good faith to understand, unless and until specific evidence defeats the presumption. The empirical justification (the More in Common research showing systematic misperception) supports but does not compel the commitment.

**Axiom 9** (The Work of the Common). There exists, for any community *c* in **C**, a set of maintenance operations $W(c)$ such that the persistence of *c* depends on the regular performance of $W(c)$ by members of *c*.

$$(\forall c \in \mathbf{C})(\exists W(c) \neq \varnothing)\left[\text{Persist}(c) \implies (\exists p \in c)[p \text{ performs } W(c) \text{ regularly}]\right]$$

*Remark.* Communities do not maintain themselves. Roads, schools, courts, parks, libraries, congregations, neighborhoods---all require work. The work is mostly boring: planning committees, zoning debates, food bank shifts, PTA phone trees. It is not heroic. It is not glorious. It is done in slow time, with actual neighbors, on actual Tuesdays. This axiom asserts that the work exists and that it is non-empty for every community. The question is only whether anyone does it.

---

## Part V: The Existence Theorem

We are now in a position to state and prove the central result of the theory.

**Theorem 9** (Existence of the Citizen). *If Axioms 1--9 obtain, then for any state s in* **S**, *there exist persons p in* **P** *such that* Citizen(*p, s*).

*Proof.* By Axiom 1, **P** is non-empty. Let *p* be a person in **P**.

By Axiom 2, *p* is formed by at least one community. By Axiom 9, if members of that community perform $W(c)$, the community persists. By Axiom 6, the persisting community provides the intermediate structure required for citizenship.

By Axiom 7, *p* can attend to other persons. By Axiom 8, *p* can presume good faith. By Definition 3 and Axiom 9, the regular practice of attention (Axiom 7), good faith (Axiom 8), and common work (Axiom 9) within the mold-institution (Definition 6) cultivates civic virtue $V(p)$.

By Axiom 5, if the state does not permit domination or unjustified interference, $\text{Free}(p)$ holds.

Since all four conditions of Definition 1 are satisfiable---freedom, intermediate community, reciprocal obligation, civic virtue---$\text{Citizen}(p, s)$ holds. $\square$

*Remark.* This is a constructive existence proof. It does not merely assert that citizens exist; it exhibits the operations by which they are produced. The citizen is not a natural kind found in the wild. The citizen is constructed---by communities that form, institutions that mold, and practices that sustain. The existence of the citizen is conditional on the performance of the work.

---

## Part VI: The Incompleteness Observation

We close with an observation that is not a theorem but a reflection on the limits of the formalism.

No axiom system for citizenship can be both complete and consistent in the Godelian sense. The concept *citizen* involves self-reference (the citizen is a person who governs and is governed, who forms institutions that in turn form her), temporal change (the citizen is formed over time by practices that themselves change), and irreducible judgment (the citizen must determine, in each concrete situation, what attention, good faith, and common work require). These features resist total formalization.

What the axiomatic treatment achieves is not completeness but *transparency*. We now see precisely which commitments the theory requires (Axioms 1--9), which results follow from those commitments (Theorems 1--9), and which commitments are genuinely axioms---not provable from anything more basic, but adopted as the starting points of a form of life.

The citizen has not disappeared. The axioms still admit models. The existence theorem still holds. But existence is conditional. Whether the citizen returns depends on whether the axioms are *instantiated*---whether actual persons, in actual communities, perform the actual work.

The question is not whether the theory is true. The question is whether we will make it true.

$\square$

---

## Appendix: Summary of Axioms

| Axiom | Name | Content |
|-------|------|---------|
| 1 | Non-Empty Person | **P** $\neq \varnothing$ |
| 2 | Formation | Every person is formed by at least one community |
| 3 | Non-Reduction | No person is identical to her formative communities |
| 4 | State as Proper Subset | The state never exhausts the person-community relation |
| 5 | Liberty | Freedom = non-interference $\wedge$ non-domination |
| 6 | Intermediate Necessity | Citizenship requires non-trivial intermediate community |
| 7 | Attention | Attention between any two persons is always possible |
| 8 | Good Faith | Good faith is the default presumption toward other persons |
| 9 | Work of the Common | Every community requires non-empty maintenance work |

## Appendix: Summary of Theorems

| Theorem | Name | Content |
|---------|------|---------|
| 1 | Formation | No citizen without non-trivial community formation |
| 2 | Irreducibility | No citizen is identical to her formative communities |
| 3 | Atomization--Mass Movement | Atomization is a necessary condition for mass capture |
| 4 | Paradox of Neutrality | Neutrality about formation conditions is non-neutral |
| 5 | Bridging Capital | Loss of bridging capital produces unbounded polarization |
| 6 | Mold-Platform | Universal platform-institutions eliminate civic virtue |
| 7 | Productive Tension | Republic requires both Federalist and Anti-Federalist axioms |
| 8 | Feedback Loop | Atomization-capture-decay-polarization form a closed cycle |
| 9 | Existence of the Citizen | Under all nine axioms, citizens exist constructively |
