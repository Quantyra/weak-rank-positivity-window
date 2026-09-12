# Sources and attribution

The external source results below are credited imports and comparisons. This note does not claim their machinery as original. Links identify primary works. SIZE-NOTE.md restates the small restriction templates and exact mathematical contracts with attribution; no primary PDF or source figure is redistributed.

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

## Version 3.0.0: row-space positivity and explicit SoS size

[SIZE-NOTE.md](SIZE-NOTE.md) uses source Definition 4.3's exact size convention `sum_i ||f_i||||g_i||+sum_j ||h_j||`, with roots explicitly represented before squaring. It states the complete original Definition 6.1 clause-falsification encoding. Source Definitions 6.5--6.6 and Lemma 6.7 supply the residual complete-row local laws and consistency. Definition 6.8 supplies the exact independent row-type/parity-bit substitution, including both D/E templates, endpoints and boundary-prefix images; Lemma 6.9 supplies survival probability `(sqrt(7/8))^r` for the interior typed-row support r. Lemma 6.10 supplies the local semantic clause check, not an imported arbitrary-sign equality-ideal simulation. These are credited source results, not new restrictions invented here.

The input width is `N=8q+4`, the even residual width is `q>=1024`, and `m=q^2` is unchanged by restriction. The size theorem is `S >= (8/7)^((2 floor(q/(32 log_2 q))-1)/2) = exp(Omega(N/log N))`, not `exp(Omega(N))`. The additional argument proves bounded-row-space square positivity from the complete-row conditional estimates in FULL-NOTE.md and counts original multiplier/root monomials before any complement expansion. The previous ordinary-degree theorem alone does not imply this step.

The source's Theorem 6.11 already gives exponential SA size via the same restriction. Its Theorems 2.3/5.18 already give exponential SoS size for the distinct perfect-matching encoding. Version 3 neither claims those results as new nor transfers its theorem to that encoding or the z-extended encoding. Novelty and priority of the exact present result remain unknown. Earlier no-size-consequence statements in this file concern v2.0.0 and v2.1.0 only. Source provenance, template transcription corrections and AI-review limitations are recorded in REVIEW.md.

## Version 4.0.0: output-uniformity and the exact indexed map

[OUTPUT-NOTE.md](OUTPUT-NOTE.md) proves the arbitrary-output extension at
the same fixed parameters, rather than importing it from the identity
statement. The primary source already supplies arbitrary-output local
laws and restrictions. The additional check retains the actual augmented
pairing rank, affine right-hand sides, deletion counts and normalization
in the complete-row conditional estimates and all-context PSD assembly.
The final size argument keeps source Definition 4.3's explicit monomial
measure, including roots before squaring. The displayed D/E templates
retain the visually checked corrections disclosed in the v3 review.

The separate G_q corollary uses ordinary binary matrix multiplication,
rank factorization, prefix circuit encoding and parameter arithmetic.
These are established ingredients. Its seed length is 16q^3+8q^2 and
output length q^4=Theta(s_q^(4/3)) for seed length s_q, with
encoding-specific explicit SoS hardness for every nonrange output.
Neither a generic SoS generator nor an iterated-stretch theorem is
imported from the source's PCR results.

The bounded contribution audit checked the live ECCC record and arXiv
history on 12 September 2026: only arXiv:2608.08760v1 (9 August 2026)
was listed, and Section 2.2 still leaves the bamboo SoS direction
unpursued. This supports a source-relative extension description, not
priority certification or completion of that entire direction.

Additional primary comparisons examined in that audit were:

- Dikstein, Dinur, Filmus and Harsha,
  [arXiv:1804.08155v5](https://arxiv.org/abs/1804.08155v5), Theorems 3.2,
  4.6 and 6.2: decomposition and approximate orthogonality on measured
  complexes/expanding posets. These are methodological precedent, not an
  identified theorem for this unchanged union-law moment form.
- Dinur, Filmus, Harsha and Tulsiani,
  [arXiv:2009.05218v1](https://arxiv.org/abs/2009.05218v1), Theorem 1.1:
  explicit SoS-hard 3XOR from LSV complexes. This does not identify the
  bamboo family or supply its encoding transfer.
- Barak, Hopkins, Kelner, Kothari, Moitra and Potechin,
  [arXiv:1604.03084v2](https://arxiv.org/abs/1604.03084v2), Theorem 1.1
  and Sections 3, 6--7: pseudocalibration and model-specific PSD analysis
  for planted clique. This is not a general guarantee that an arbitrary
  prescribed consistent local functional is PSD.

No exact subsuming theorem was identified in that bounded comparison;
absence of a match does not establish novelty. The arbitrary-A extension
and G_q statement here were separately checked after that audit.
Known short matrix-identity proofs and their rational Hilbert-like IPS
simulation remain compatible with an explicit-monomial lower bound:
see [Hrubes--Tzameret](https://users.math.cas.cz/~hrubes/PDFs/DET.pdf) and
[Pitassi--Tzameret, Section 3.2](https://eccc.weizmann.ac.il/report/2016/101/download).
No unrestricted circuit-certificate lower bound is claimed.
