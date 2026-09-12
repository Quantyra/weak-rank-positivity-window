# Sources and attribution

The external source results below are credited imports and comparisons. This note does not claim their machinery as original. Links identify primary works; no source text or figures are redistributed.

## Functional being analyzed

Garlik, Gryaznov, Ren, and Tzameret, *The Weak Rank Principle: Lower Bounds and Applications*, [ECCC TR26-133](https://eccc.weizmann.ac.il/report/2026/133/) and [arXiv:2608.08760v1](https://arxiv.org/abs/2608.08760v1), August 2026.

The relevant contract is Section 6.1, Definitions 6.5--6.6, Lemma 6.7, and the functional R in the proof of Lemma 6.4. The ECCC text places these on printed pages 69--71; arXiv v1 has different pagination (Definition 6.5 on printed page 66). The full local law is uniform on odd X rows and odd Y columns, each augmented frame independent with the all-ones vector, with all selected cross dot products prescribed. U is assigned its actual prefix parity. With no Y columns selected this reduces to the X-only law analyzed in v1. The functional's domain is monomialwise row-degree at most n-2, not one common row support for an entire polynomial. Consistency is imported from the source.

The source's discussion in Section 2.2 of extending the bamboo-tree method to SoS concerns a different construction from its existing perfect-matching SoS results (Theorems 2.3/5.18). Version 2.0.0 analyzes full X/Y/U square positivity of this specified bamboo-tree functional; it does not import the different perfect-matching SoS theorem or assert a SoS lower-bound corollary.

## Comparisons retained for the v1 X-only result

- Janson, Konstantopoulos, and Yuan, [arXiv:1410.1777v3](https://arxiv.org/abs/1410.1777v3), Theorem 1 and Example 2(i): signed mixtures for finite exchangeable laws. The fixed-character signed-law mechanism is familiar; this reference does not identify the weak-rank X-only window.
- Kunisky and Moore, [arXiv:2203.05693](https://arxiv.org/abs/2203.05693), Definition 1.3 and Theorems 1.4--1.5: symmetric-difference pseudomoment matrices and spectral analysis. Their degree-dependent moments differ from the constant negative even moments used for the witness here.
- Kunisky, [arXiv:2009.07269](https://arxiv.org/abs/2009.07269), Theorem 1.12 and equations (14)--(16) in Theorem 1.14: particular positive higher-degree extensions under quantitative conditions. This does not establish positivity of an arbitrary prescribed higher-moment functional.
- Kothari and Lin, [arXiv:2608.18048v1](https://arxiv.org/abs/2608.18048v1), Theorems 1.2/2.2 and 1.3/2.1: distinctions between SA local positivity, SoS positivity, and exact or approximate Cauchy--Schwarz. Merely finding nonpositivity in a locally positive functional is not a new general phenomenon.

These comparisons came from a bounded AI-agent primary-source audit. They neither certify priority nor establish that this application has not appeared elsewhere. These v1 comparisons concern the preserved X-only calculation. The full-variable proof uses the additional comparisons below; its general tools are established.

## Comparisons for the full-variable proof

- Chastaing, Gamboa, and Prieur, [arXiv:1112.1788v3](https://arxiv.org/abs/1112.1788v3), Section 2.2 and Theorem 1: conditional/Hoeffding decompositions for dependent inputs under a positive lower-domination assumption on a joint law. That assumption fails already for one source X/Y pair, because the product of odd marginals gives positive mass to forbidden dot parity. We do not import their decomposition theorem. The finite-dimensional local-complement argument in FULL-NOTE.md is proved directly from the source laws.
- Vinh, [arXiv:0711.4427](https://arxiv.org/abs/0711.4427), Section 2: finite-field point--hyperplane incidence spectral methods. This is a methodological precedent, not an identified spectrum of the present arbitrary-separator, rank-excluded mixed-frame source fiber.
- Phuong, Pham, and Vinh, [arXiv:1510.03481](https://arxiv.org/abs/1510.03481): plane-incidence results in an odd-prime-power field setting. No direct characteristic-two theorem is imported into this proof.
- [arXiv:1709.09011](https://arxiv.org/abs/1709.09011), Section 7: bilinear-forms association schemes and rank-shell spectral machinery. Finite Fourier analysis and rank counting are standard. The proof here supplies its own affine-fiber reduction, deletion estimates and probability normalizations.

The full conditional-correlation argument needs no junction-tree or global-law construction. The source's local consistency is credited, while the conditional rank estimates, total-covariance reduction and all-context positivity argument are written in the note.

This was a bounded AI-agent primary-source applicability audit, not an exhaustive priority search. No novelty or priority certification is claimed for the theorem or its method. The exact underlying derivation is pinned in [REVIEW.md](REVIEW.md). The v2.0.0 artifact has a separate review process recorded there.

## Version 2.1.0: exact certificate-degree consequence

[COROLLARY.md](COROLLARY.md) additionally uses source Definition 4.3's ordinary, unreduced SoS certificate-degree convention and Definition 6.1's complete simple bamboo clause list, including the boundary restriction immediately before Section 6.1. Boolean equations are expressly included; optional literal twins are eliminated by complements without degree increase. Source local satisfaction, normalization and consistency annihilate each bounded-degree axiom multiple. The v2 full-square theorem handles every square root. The positive-functional contradiction is standard; this extraction contributes exact encoding and degree accounting, not a new proof-complexity mechanism.

The source's Lemma 6.4 gives an SA row-degree lower bound for the same restricted encoding. Its Theorem 6.11 uses a separate SA size argument. Theorems 2.3/5.18 already give exponential SoS size hardness for the distinct PMRank perfect-matching encoding, using the matching-extension reduction in Lemma 5.17. Those extension variables are not the present prefix U variables. No reduction to that encoding or to the z-extended BTRank system is supplied here. The narrow comparison neither certifies novelty nor imports a size lower bound into the corollary.

The preceding v2.0.0 discussion remains historical attribution for the unchanged positivity proof. Version 2.1.0 adds the explicit corollary; no SoS size, general SAT, circuit, or complexity-class consequence is claimed.
