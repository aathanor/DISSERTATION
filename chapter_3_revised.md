---
title: "Chapter 3 — From Russell to Kripke: The Argument for Rigid Designation"
subtitle: "Revised draft, aligned with Ch. 2 originality audit"
author: Florin Cojocariu
status: draft_v2
date: 2026-04-22
---

# From Russell to Kripke: The Argument for Rigid Designation

## Overview

Chapter 2 closed at the point where the necessity-of-identity formula, applied to names, presupposed that names exhibit the same reference-invariance across worlds that variables have under assignment. That presupposition is a substantive metasemantic claim; the formula does not establish it. 

This chapter presents the independent arguments Kripke makes for the rigidity of names, lays out the received view on why descriptions cannot supply this rigidity, and reconstructs a dialectical path on which Bertrand Russell first identified the correct cognitive mechanism and then declined to generalize it. 

Finally, the chapter evaluates the leading cognitive implementations of direct reference—Evans, Recanati, and Devitt. It argues that while each identifies a genuine desideratum, they all share a representational "template" architecture that treats reference as a form of algorithmic pattern-matching. 

The gap this critique identifies is the one Chapters 4 and 5 close by modeling reference as attractor-basin resonance under the Pattern-Recognition Unity (PRU) framework.

## Rigid Designation: Kripke's Independent Argument

Kripke’s thesis is that proper names are rigid designators: a proper name designates the same individual in every possible world in which that individual exists. The thesis is defended in *Naming and Necessity* by three converging arguments, none of which depends on the necessity-of-identity formula. The formula regiments the modal consequence once rigidity is granted; the case for rigidity runs separately.

The modal argument turns on counterfactual intuition. Aristotle could have died in infancy, never taught Alexander, and never written the *Nicomachean Ethics*. In that counterfactual scenario, it is Aristotle who failed to do these things, not someone else. The name "Aristotle" tracks the individual across counterfactual variation, even when every description we associate with him fails. If "Aristotle" abbreviated "the teacher of Alexander who wrote the *Nicomachean Ethics*," then in a world where no one satisfied that description the name would refer to no one. If it referred to whoever did satisfy it, the counterfactual claim would be about someone else. Both readings clash with the intuition that the counterfactual is about the man Aristotle himself.

The epistemic argument turns on ignorance and error. A competent user of the name "Feynman" may know only that Feynman was a physicist, or may believe things about him that are factually wrong. On a descriptivist theory, such a user either fails to refer or refers to whoever fits her associated description—which, in cases of error, will be someone other than Feynman. Yet speakers manage to refer to Feynman regardless. 

The sharpest version of this is the Gödel/Schmidt thought experiment: suppose, counterfactually, that the incompleteness proof we attribute to Gödel was actually discovered by a man named Schmidt, and Gödel merely stole it. On a descriptivist theory built around "the prover of the incompleteness of arithmetic," "Gödel" would refer to Schmidt. Our intuition is that "Gödel" still refers to Gödel. Reference runs through the name, not through the descriptions attached to it.

The semantic argument targets substitutivity in modal contexts. "Necessarily, Benjamin Franklin is Benjamin Franklin" is true; "Necessarily, the inventor of bifocals is the inventor of bifocals" is also true; but "Necessarily, Benjamin Franklin is the inventor of bifocals" is false—he might never have invented them. The name and the description share an actual-world referent but differ in modal profile. They cannot be synonyms. 

These three arguments motivate the distinction between *de jure* rigidity (characteristic of proper names, rigid by grammatical stipulation) and *de facto* rigidity (attaching to descriptions whose satisfiers are necessarily the same across worlds, such as "the least prime"). Names are rigid by how they function as designators, not by what they happen to pick out.

## Why Descriptions Cannot Supply Rigidity

Descriptions pick out satisfiers world by world. "The inventor of bifocals" picks out whoever, in any given world, invented bifocals. Different worlds can have different inventors; the description tracks whichever individual happens to satisfy it. 

This world-relative behavior is constitutive of descriptions: they specify a condition, and the reference is wherever the condition is met. No accumulation of conditions changes this. "The stout inventor of bifocals who was a Postmaster General" still picks out a satisfier world by world; adding conditions narrows the range of worlds where the description is satisfied but does not make the reference invariant across them.

The formal expression of this is the scope problem. In a sentence like $\Box \, F(\iota x\, G x)$, the description $\iota x\, G x$ can take scope inside or outside the modal operator. 
*   Read with narrow scope (primary occurrence), "necessarily, `$F$` of whoever is `$G$`" requires that in every world the satisfier of `$G$` in that world is also `$F$`. 
*   Read with wide scope (secondary occurrence), "of whoever is actually `$G$`, necessarily `$F$`" requires that the actual-world satisfier of `$G$` is `$F$` in every world. 

The wide-scope reading behaves modally as if the description were rigid: the referent is fixed in the actual world and held constant. But the rigidity is positional, not constitutive—it is achieved by choice of scope, not by anything intrinsic to the description. A description with wide scope and a rigid designator share modal profiles in simple cases but come apart on more complex constructions.

The same point applies to David Kaplan’s $\text{dthat}$ operator. $\text{dthat}(\iota x\, F x)$ takes a description and converts it into a directly referring term whose reference is fixed in the actual world and held constant across worlds. $\text{dthat}$ does the same logical work as wide-scope $\iota x\, F x$, but it does the work through rigidification rather than scope manipulation—and it makes the rigidification intrinsic to the designator rather than dependent on how the designator is positioned relative to a modal operator. 

Names differ from rigidified descriptions in a further respect: for names, wide scope is the only reading, because the name has no descriptive structure that could generate a narrow-scope reading in the first place. "Aristotle" does not pick out whoever happens to be Aristotle in each world, because "being Aristotle" is not a condition the name imposes.

The core reason descriptions cannot generate rigidity is architectural. In the vocabulary of the PRU framework, descriptions operate through **pattern-matching** (PRU §4.2). They function as templates: the cognitive system compares an input against a stored set of properties and evaluates the fit. Because this process is algorithmic and comparative, it must run anew in every counterfactual world, yielding different satisfiers in different environments. Rigidity requires an entirely different cognitive operation.

## Russell's Mechanism and His Retreat

If descriptions cannot supply rigidity, we must look for a non-descriptive cognitive operation that can. In a passage from *The Philosophy of Logical Atomism* quoted by Kripke, Bertrand Russell identifies this primitive operation but declines to generalize it:

> "If we want to reserve the term 'name' for things which really just name an object without describing it, the only real proper names we can have are names of our own immediate sense data, objects of our own immediate acquaintance. The only such names which occur in language are demonstratives like 'this' and 'that.'"

Two distinct claims are joined in this passage. They must be separated.

The first is the identification of a **mechanism**. Russell isolates a specific kind of designator—the demonstrative—and characterizes it by what it does not do: it does not describe. The demonstrative "just names an object," without descriptive intermediary. The reference is established by the demonstrative act itself, not by a description the speaker has in mind. 

In the vocabulary developed in Chapter 4, this is **local rigidity**: direct, non-descriptive coordination with an experienced particular. Russell is naming the cognitive operation that the rigid-designation thesis presupposes but does not itself describe.

The second is the **retreat**. Having identified the mechanism, Russell restricts it to "immediate sense data"—the subset of cases in which the reference is exempt from Cartesian doubt. The restriction is epistemological, driven by a foundationalist demand for certainty. Under Russell's standard, even "this chair" is not a genuine name, because one could be hallucinating the chair. 

The dialectical position this dissertation exploits begins here. Russell’s mechanism—demonstrative grounding—is the exact mechanism the rigid-designation literature needs to explain how a term can hold its referent fixed without descriptive mediation. But by restricting it to incorrigible cases, Russell makes the mechanism unavailable for ordinary, public proper names. 

This restriction is unnecessary. Russell collapsed a crucial distinction: the distinction between **directness** and **infallibility**. He assumed that if a cognitive operation is fallible, it must be mediated by descriptions, and therefore cannot be direct.

Neural attractor dynamics show that directness and infallibility are distinct (PRU §3.2). 
*   A Pattern-Constellation $\\{X\\}$ is an attractor basin in neural space. 
*   Falling into an attractor basin is mathematically and cognitively direct: it is a resonance event (pattern-recognition), not an algorithmic comparison (pattern-matching) (PRU §4.2). 
*   Yet the process is fallible: sensory noise, contextual shifts, or neurological changes can cause the system to misfire, fall into the wrong basin, or gradually resculpt the basin's boundaries (PRU §3.2).

Directness does not require infallibility. It requires **stability**. Demonstrative tracking is direct because it is a resonance event, but it remains fallible because the attractor landscape is dynamic. 

By dropping Russell’s Cartesian requirement of infallibility while keeping his demonstrative mechanism, we can generalize local rigidity beyond momentary sense data to physical objects.

## Baptism and the Causal Chain

Kripke’s positive picture of how ordinary names attach to their referents runs through baptism and causal-historical transmission. 

At some initial act—the baptism—a name is attached to its bearer, either by ostension ("let us call this child 'Feynman'") or by a reference-fixing description ("let 'Jack the Ripper' denote whoever committed these murders"). From this origin, the name propagates through a chain of communication: each speaker acquires the name from an earlier speaker, intending to use it with the same reference. The speaker at the end of the chain refers to the original bearer even if she knows nothing about him beyond the name.

Kripke is explicit that this is a "better picture" rather than a systematic theory:

> "I'm not, in fact, trying to give any sort of necessary and sufficient conditions for reference… in any rigorous sense."

The picture describes the external, social constraints of reference. It tells us what reference looks like from the outside, but it does not describe the cognitive operations that realize this picture in actual speakers.

The picture has two parts. The baptism fixes the reference. The causal chain preserves it across uses, speakers, and time. 

Kripke distinguishes reference-fixing from meaning-giving. A description used in a baptism—"let 'Jack the Ripper' denote the perpetrator of these crimes"—fixes the reference of the name but does not become its meaning. The name, once fixed, is rigid; the description is not. What is inherited down the chain is the designator and its rigidity, not the descriptive route by which the reference was originally established.

This picture successfully accounts for speaker ignorance and error. A child can learn "Aristotle" from a parent and refer to Aristotle with no descriptive content beyond the name. 

What the picture leaves open is the cognitive level. It asserts that baptism fixes reference and the chain transmits it, but it does not explain how a brain performs these operations.

## The Explanatory Gap

The post-Kripkean literature widely acknowledges what Joseph LaPorte characterizes as the "promissory note" structure of the causal-historical picture: it gestures at cognitive and psychological mechanisms it does not supply. This explanatory gap consists of three connected omissions.

First, **the tracking gap**: no account is given of what constitutes rigid tracking at the cognitive level. Names are said to be rigid; the rigidity is explained semantically as designation of the same individual across worlds; but the cognitive capacity that allows a speaker to use a name as rigid—to deploy it in modal contexts where descriptions fail—is not characterized. 

Second, **the baptism gap**: no account is given of the cognitive mechanism of baptism. Baptism is described as reference-fixing, but what a speaker actually does when she baptizes—especially in the ostensive case—is left unanalyzed. Pointing at an object and saying "let us call this 'X'" presupposes a prior cognitive capacity to segment the perceptual field and hold *this* particular fixed, a capacity that semantic theory takes for granted.

Third, **the transmission gap**: no account is given of how the causal chain is psychologically realized. A causal chain of uses requires, at each link, that a speaker take up the name from an earlier speaker in a way that preserves reference. What the speaker acquires cognitively when she learns the name—and how that acquisition preserves the reference without relying on a shared set of descriptions—is left unspecified.

These three gaps are three symptoms of a single missing element: the primitive tracking capacity that lets a speaker single out a particular and continue to track that same particular over time, through change, and under counterfactual variation. 

Rigid tracking is this capacity exercised at the modal level; baptism is this capacity exercised in attaching a name to a particular; the causal chain is this capacity exercised in taking up a name from another speaker and continuing to apply it to that particular.

## Existing Cognitive Implementations

Several philosophers have attempted to fill this explanatory gap. Three leading implementations illustrate the state of the art: Gareth Evans’s discriminating-conception account, François Recanati’s mental-files account, and Michael Devitt’s causal-descriptive account. 

While each identifies a genuine cognitive desideratum, all three share a structural limitation: they retain a representational "template" architecture that treats reference as a form of algorithmic pattern-matching.

### Evans: The Discriminating Conception
Evans defended a Russellian constraint: singular thought about an object requires that the thinker possess a "discriminating conception" of that object—a way of singling it out that distinguishes it from all other things. 

While Evans is careful to distinguish this from descriptivism, his account remains propositional: to have a discriminating conception of `$a$` is to be able to think, of `$a$`, that it is the unique satisfier of some condition the thinker grasps. The limit of this account is its propositional framing: the discriminating conception is modeled as a set of thoughts a thinker can have, rather than as a sensory-motor tracking capacity that supports those thoughts.

### Recanati: Mental Files
Recanati models the grasp of a singular term as a "mental file"—a cognitive container that collects information about a referent, supports updating, and underwrites the capacity to think about the referent in its absence. 

While files are not propositional in Evans's sense, the container metaphor retains a representational template. The file is an internal representation the speaker has; the referent is what the file is about. The act of opening a file presupposes a capacity to single out a particular and start a file on it. That capacity is the precondition for the file, not something the file architecture itself explains.

### Devitt: Causal-Descriptivism
Devitt offers a causal-descriptivist hybrid, supplementing Kripke's causal chain with a descriptive component to handle cases of reference-shift. 

The architecture remains representationalist: reference is a relation between an internal representational state (the speaker's causal-descriptive complex) and a referent. The descriptive component continues to do the sorting and matching work, leaving the account vulnerable to Kripke's original anti-descriptivist objections.

### The Shared Limitation: Pattern-Matching

These three proposals treat reference as a relation between an internal representational state (a conception, a file, or a causal-descriptive state) and a referent. Each account attempts to loosen the descriptive requirement, but they all preserve the template architecture: reference is something the speaker *has* (a representation); the referent is what that representation is *about*. 

This architecture forces them to model reference-evaluation as **pattern-matching** (PRU §4.2). The cognitive system must take the stored representation (the file or conception) and match it against the world to determine reference. 

This generates the **historical reference paradox**: 
*   If the contemporary speaker’s connection to an absent object (like Aristotle) is mediated by descriptions and files, and these files are evaluated via pattern-matching, then the contemporary speaker's reference should suffer from the same world-relative modal failures as standard descriptions. 
*   If we try to avoid this by asserting that the file is rigid by "categorial stipulation," we have returned to semantic fiat, bypassing the cognitive mechanism.

The PRU framework resolves this paradox in Chapters 4 and 5 by splitting the cognitive architecture into two non-interchangeable operations (PRU §8.4):

1.  **R-Grounding ($\mathcal{R}(\{X\}, \langle x \rangle)$):** Direct, sensory-motor pattern-recognition. This is local rigidity, where the word-sound is integrated directly into an active, experienced attractor basin.
2.  **A-Grounding ($\mathcal{A}(\mathcal{D}, N^c)$):** Value-fixing through structures internal to the linguistic system. 

When a contemporary speaker refers to Aristotle, they do not perform `$R$-grounding`; they have no sensory access to him. They operate through `$A$-grounding`. 

Crucially, the descriptions (`$\mathcal{D}$`) they possess do not function as satisfaction templates to match candidates in counterfactual worlds. Instead, `$\mathcal{D}$` acts as a historical coordinate within the collective linguistic pattern-constellation $\langle \text{Aristotle} \rangle$. 

The purpose of the descriptions is to retrieve and activate the name-concept `$N^c$`. Because `$N^c$` is a tracking device that inherits its scope-ambiguity-free character from the original baptismal $\mathcal{R}(h^o, N^c)$, the modal evaluation runs on the retrieved historical channel (`$N^c$`), not on the descriptions (`$\mathcal{D}$`). 

The contemporary speaker refers rigidly not because they possess a direct tracking relation to Aristotle, but because their `$A$-grounding` uses descriptions to *trace* a historical tracking channel, rather than to *match* a counterfactual satisfier.

## Summary and Transition

This chapter has established three points:

1.  Kripke’s independent arguments establish that names are rigid, but define a semantic property rather than explaining the cognitive operation that produces it.
2.  Descriptions cannot generate rigidity because they are structurally bound to a pattern-matching architecture that evaluates satisfiers world-by-world.
3.  Russell identified the correct cognitive primitive—direct demonstrative tracking—but mistakenly restricted it to momentary sense data because he demanded Cartesian infallibility.

By separating directness from infallibility through neural attractor dynamics, we can reclaim Russell's demonstrative mechanism for physical objects. 

This primitive tracking capacity is **local rigidity**. Baptism and the causal chain are best understood as the social stabilization of local rigidity across absence. 

Chapter 4 introduces the formal analytical vocabulary of this positive thesis: the object-mode/concept-mode distinction ($x^o/x^c$), the formal development of `$R$-grounding` and `$A$-grounding`, and the proof of how this distinction resolves the puzzle of the necessary *a posteriori* and *de re* modality.