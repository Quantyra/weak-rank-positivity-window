# Version 4.1.0: dimension-budget addendum review

Version 4.1.0, 12 September 2026. This section precedes the exact unchanged
v4 REVIEW bytes below. [DIMENSION-NOTE.md](DIMENSION-NOTE.md) is a modest
parameter-budget addendum to the same artifact, not a new lower-bound
method or separate generator construction. The old fixed-m theorem is
stronger at its own parameters and is retained. The near-quadratic indexed
output trades away part of its seed-normalized hardness exponent.

The mathematical source is formal-pvnp commit
`3d381934744c48f7afa913ac650037a477148a19`, note
`research/p-equals-np/2026-09-12-bamboo-dimension-budget.md`, 29436 bytes,
SHA256 `da37598d495efc1da7302fbc664f74b45302a8f6ec12a3de423b9ab1107f5676`,
Git blob `121e62bc15926696611baf8cb00dca6d4c16643d`.
The author supplied the full dimension derivation and separate indexed
implication. Source/complexity review supplied source-domain and cost
guidance; initial and fresh independent mathematical reviews supplied
actual-file verification without author repair. Separate scope review
checked claims and readiness. These were informal AI roles, not human
peer review, Lean verification or novelty certification.

| Internal source lens | Record in formal-pvnp research/p-equals-np/ | Verdict | SHA256 |
|---|---|---|---|
| Source/complexity | 2026-09-12-bamboo-dimension-source-review.md | PASS | `B90F6E5947C8FCBF4446CA238A1C818CD8AD782BEBFC6FFB16D9F088638428DC` |
| Initial independent mathematics | 2026-09-12-bamboo-dimension-proof-review.md | PASS; no repair | `57F076CABFE1883DE6BA20154C85B3F591063AC3BF8E4467ACB102E5AF1B5CF1` |
| Fresh independent mathematics | 2026-09-12-bamboo-dimension-fresh-review.md | PASS; no repair | `4D8D25243713E733DE96C633BBBC580ACB7B5E4151A01F8A505D59D359107C35` |
| Nonclaims/readiness | 2026-09-12-bamboo-dimension-nonclaims-review.md | Internal GO; public preparation required | `EC0FD5289903607BE31D70A4B53D6080DED633C24E2E06F6254234FF2B3F7905` |

Two independent significance assessments are integrated at source commit
`2c9aaef67bca05c17a1a3eb6ce50e77793f0b7c6`: dimension-significance
SHA256 `81fdf5ebea5438768a0696aa39e782db827d701136f23885143b126128c55947`
and dimension-significance-challenge SHA256
`d2aa7cb3b9aff87df787e4518fe4382a4abab0a00047c5227c1aefa2c2cc853b`.
Both recommended a modest existing-artifact update, not a standalone new
mechanism. A local cached-file locator in the second assessment was replaced
by a source description before integration; substantive text and verdict
were unchanged. These assessments are not additional correctness reviews.
They identify a legitimate wider quantitative statement, with unknown
priority and no claim of journal-level significance or P-versus-NP progress.

The extracted DIMENSION-NOTE has 30347 bytes, SHA256 `4b9acce60dd1eb328e711eb894e080b0fdbcee9b5ab1b1b3ee71f564524e2f4b`,
Git blob `e37400ab3f45a751e8472f8052ddf5bab6e539e0`. The mathematical body matches the committed source
from 'Statements and exact conventions' through the complete indexed proof,
except removing the 'author claim' label from the corollary heading.
Public-safe introductory links, provenance and final contribution wording
replace internal workflow text. No equation, hypothesis, proof step or
parameter cost is changed by extraction. Existing D/E visual corrections
are inherited unchanged from the reviewed source and earlier public notes.

| Actual whole-public-extraction lens | Record in formal-pvnp research/p-equals-np/ | Scientific verdict |
|---|---|---|
| Independent mathematics, `dimension_public_math` | 2026-09-12-bamboo-dimension-public-proof-review.md | PASS entire proof and indexed implication; no construction or repair |
| Source/scope/readiness, `output_scope_review` | 2026-09-12-bamboo-dimension-public-nonclaims-review.md | GO exact source, claims, contribution description and scientific readiness |

The mathematical reviewer read the whole actual note, independently checked
the complete source-body comparison, conditional PSD, exact size transfer,
integer window and indexed consequence. Its final private receipt SHA256 is
`5ee03a228c240339504eb0b0731c7fda9fb62a4384db2d604a2bdf52dc338255`.
The receipt's local repository locator was replaced by its repository name
before source integration; no proof, verdict or substantive review text
changed. This editorial hygiene is separate from mathematical verification.

The source/scope reviewer read the complete candidate, both significance
assessments and the actual mathematical PASS, and checked all six preserved
Git blobs, historical REVIEW/SOURCES bytes, CFF schema, links and claim
boundaries. Final integration of this receipt table and release text is
checked in that private scope record before the candidate commit. No
mathematical or theorem-scope repair was requested by either extraction
reviewer. These informal AI scientific verdicts do not constitute human
peer review, Lean verification, novelty certification or an owner publication
decision. The exact candidate and release still require the owner's gate;
this record alone authorizes no push, tag, release or live About change.

NOTE.md, FULL-NOTE.md, COROLLARY.md, SIZE-NOTE.md, OUTPUT-NOTE.md and
LICENSE retain their exact v4 Git blobs. The complete historical REVIEW
bytes follow unchanged, including its earlier template/UTF-8 correction
and reviewer disclosures. Historical scope statements apply to their
versions; the new dimension theorem has its own exact assumptions above.
No additional novel method, optimality, all-length/tree amplification,
computational pseudorandomness, compressed-certificate, general SAT,
circuit-lower-bound or P-versus-NP claim is made.

# Contribution, provenance, and review disclosure

## Version 4.0.0: arbitrary-output extension and indexed corollary

Version 4.0.0, 12 September 2026. [OUTPUT-NOTE.md](OUTPUT-NOTE.md)
contains the complete fixed-parameter arbitrary-A proof and the separate
G_q corollary. Its source is formal-pvnp commit
**4b748b22aa87587f761ddd2d99f342f427a9b0c9**. The main source proof is
research/p-equals-np/2026-09-12-bamboo-output-uniformity.md, SHA256
`CADA42936367F0F238BEE5EEEAB873BB9535EE463C1C8F5EA85D5A566170A7D9`.
The corollary is derived in the source review, with both mathematical
reviews independently checking its exact map, encoding and costs.

The extension author supplied the explicit arbitrary-output fiber,
normalization and size proof. The source reviewer supplied the separate
generator derivation and source/model verification. Initial and fresh
mathematical reviewers supplied actual-file verification without author
construction or repair. The independent scope reviewer supplied claim
and readiness checks; one excess terminal blank line in that review
was removed before source integration, without textual changes.

| Source review role | Record in formal-pvnp research/p-equals-np/ | Verdict |
|---|---|---|
| Source/model and complexity | 2026-09-12-bamboo-output-source-review.md | GO |
| Initial independent mathematical proof | 2026-09-12-bamboo-output-proof-review.md | PASS theorem and exact implication |
| Fresh independent adversarial mathematics | 2026-09-12-bamboo-output-fresh-review.md | PASS theorem and exact implication |
| Nonclaims/scientific readiness | 2026-09-12-bamboo-output-nonclaims-review.md | Internal GO; public extraction preparation required |

Their final working-file SHA256 pins are respectively
`F95B9530A6ADBC50430003E8331691BD302F9347A17F3A052152B19936CE60F2`,
`9534EDF20A3922DE61997A1E053E9707DFBD1B472F579C72CF86364C64EB65F2`,
`9E1AE507443B72D008D91FE86EEBCE858DDEA9E112E0963DECE84B83AF14BFC5`,
and `7AD4490421005C8169E450BACF4F1B514A923395D4A0BEC30763CABB95DD66E7`.
Git normalizes text line endings; the commit pins the exact repository
blobs. These source verdicts do not substitute for review of this extraction.

The extracted proof has SHA256 `8b37a7b333bcf2bd0cd4552364486dc3b5fa3e930601fb8168a890c19db28be2`, 22963 bytes,
Git blob `069565e25d8d991476f80bdfb6385972a62571d4`. Its separate actual-file extraction reviews returned the following
scientific verdicts on 12 September 2026:

| Actual public extraction lens | Record in formal-pvnp research/p-equals-np/ | Verdict |
|---|---|---|
| Independent mathematics, `output_fresh_proof` | 2026-09-12-bamboo-output-public-proof-review.md | PASS complete proof and separately stated G_q corollary; no construction or repair |
| Source/nonclaims/readiness, `output_scope_review` | 2026-09-12-bamboo-output-public-scope-review.md | GO exact source, scope, contribution description and scientific readiness |

The mathematical reviewer read the entire OUTPUT-NOTE, complete linked
FULL-NOTE and SIZE-NOTE, and accompanying metadata. Its private review
SHA256 is `98A2379BF3A7A02EA619FBE1D8A00F9227E5FEF1705D28E2A32FF74FE8F769EE`.
The source/scope reviewer inspected the complete candidate, preserved
Git blobs, CFF schema, source contracts, attribution and claim boundaries,
then read the actual mathematical PASS. Neither requested a mathematical
or theorem-scope repair. The scope reviewer did identify a UTF-8 encoding
regression in the historical v2.1 REVIEW paragraph. The extraction author
restored the entire historical suffix exactly from the v3 Git blob;
this metadata-only correction did not change OUTPUT-NOTE or its hash.

These verdicts are distinct from the underlying source reviews and do
not assert publication or authorize it. The integrated review metadata
receives a separate actual-file recheck before the owner's exact-candidate
decision. All mathematics and reviews are informal AI work, not human
peer review, Lean verification or novelty certification. The work uses
established tools and restriction machinery; its source-relative increment
is output uniformity at fixed m=q^2, with no improved exponent or iteration.

NOTE.md, FULL-NOTE.md, COROLLARY.md, SIZE-NOTE.md and LICENSE remain
exact Git blobs from v3.0.0 commit
`613ceb80a6211097cd8e353c47ad79ba3069ecb5`. Their earlier scope statements
are historical. The D/E corrections in the unchanged size note are the
source transcription corrections disclosed below, not new templates.
No arbitrary-m theorem, other encoding, circuit-compressed certificate
hardness, computational pseudorandomness, inversion hardness, all-length
padding, amplification, nearly quadratic/exponential stretch, general SAT
runtime, circuit lower bound or P-versus-NP result is claimed.

## Historical v3.0.0 and earlier record

The following sections retain prior attribution and review history.
Their identity-only or no-generator scope concerns those versions.

## Version 3.0.0: explicit SoS size consequence

Version 3.0.0, 12 September 2026. [SIZE-NOTE.md](SIZE-NOTE.md) proves that for even `q>=1024`, input width `N=8q+4`, `m=q^2`, and `D=floor(q/(32 log_2 q))`, every specified explicit real SoS certificate for the unaugmented simple bamboo encoding has `S >= (8/7)^((2D-1)/2) = exp(Omega(N/log N))`. The size convention counts original axiom-multiplier and square-root monomials, before squares or complement substitutions are expanded. It is not an `exp(Omega(N))` result and does not cover circuit-compressed roots.

Underlying derivation repository: formal-pvnp. Exact source commit: **ea7a89576712fc21ae0127d688f703dfa05b1af1**. Main source record: research/p-equals-np/2026-09-12-bamboo-size-mechanism.md. The new step derives bounded-row-space square positivity from the earlier complete-row conditional estimates, then uses the primary source's existing Section 6.8 restriction and 6.9 survival bound with explicit root/multiplier counting. Residual width is q, not N, and m=q^2 is retained.

The underlying corrected mathematical snapshot has SHA256 `BD3DD17A493D9F1F481FBBD3946882F3AFC0904935CF07F5F4F8B80F6C318258`. Its initial independent proof review and fresh independent adversarial proof review both returned PASS; the source/model and complexity review returned GO; the independent nonclaims/significance review returned GO-WITH-NOTES. The source commit pins the final integrated record and review files. Records in formal-pvnp research/p-equals-np/ are 2026-09-12-bamboo-size-proof-review.md, 2026-09-12-bamboo-size-fresh-review.md, 2026-09-12-bamboo-size-source-review.md, and 2026-09-12-bamboo-size-nonclaims-review.md.

The author supplied the row-space derivation and size implication. The source reviewer supplied methodological guidance and corrected two initial template transcriptions using the rendered primary PDF: D's first row is `[1 * 1 0 0 * * *]`, and E's first row is `[1 0 0 1 * * * *]`. Both independent proof reviewers checked the corrected snapshot; neither supplied construction or mathematical repair. The fresh adversarial review also checked the rendered templates. These contributions are distinct from the earlier full-positivity theorem's authorship described below.

The public extraction received separate actual-file mathematical and source/nonclaims/readiness reviews on 12 September 2026. Both inspected SIZE-NOTE.md (13,590 bytes; SHA256 `6d22e0f1d72fb5fc2dc5446ca56da4c820ea5e24bb33809c8bb2335917c93667`; Git blob `4f7f0750b2e805d65a1789ec3cc4fc43af6f521c`) and the relevant accompanying metadata. The mathematical reviewer reread the complete linked FULL-NOTE.md and independently checked the newly explicit original clause table and public equation references. The source/nonclaims reviewer inspected the complete extraction, preserved blobs, attribution and metadata and then read the actual mathematical PASS. Neither requested a mathematical, source or scope repair to this public extraction.

| Actual extraction role | Record in formal-pvnp research/p-equals-np/ | Scientific verdict |
|---|---|---|
| Independent mathematical proof, `bamboo_size_fresh` | 2026-09-12-bamboo-size-public-proof-review.md | PASS for the complete extraction, exact size convention, row-space bridge, restriction and local annihilation; verification only. |
| Source/nonclaims/readiness, `bamboo_size_nonclaims` | 2026-09-12-bamboo-size-public-nonclaims-review.md | GO for exact source applicability, attribution, scope and scientific readiness. |

These extraction verdicts concern the actual public artifact and are distinct from the underlying source reviews. The mathematical artifact is unchanged by this review-status integration. The final integrated metadata receives a separate recheck before the exact-candidate publication decision. Scientific review metadata does not assert that publication has occurred. No novelty, priority, human peer-review, or Lean-verification certification is asserted.

The following earlier artifact Git blobs are preserved exactly from v2.1.0 commit `8d22bf56cbe3f81278b436ca10840cbed0d23d63`:

| Artifact | Git blob |
|---|---|
| NOTE.md | d66725171fe42f78541382d7b31902230e90a9bf |
| FULL-NOTE.md | 6a5f09aadfd0732a6a7824b22e1aec3c350bdc45 |
| COROLLARY.md | 5a515f8a0301bc6de46edd72438c37e03a1084dc |
| LICENSE | f5e23913507cd1b6fd26f7cf8a6487b37484d8f6 |

Their no-size-claim statements describe their historical version scope. Version 3 adds only the separately stated encoding-specific size theorem. No other-family transfer, general proof-system or arbitrary SAT-runtime lower bound, circuit lower bound, sharp positivity threshold, or P-versus-NP conclusion is claimed.

## Historical v2.1.0 and earlier record

The remainder preserves earlier attribution and review history. Its no-size-claim statements concern those versions, not the separately added v3.0.0 theorem.

## Version 2.1.0: exact SoS degree corollary

Version 2.1.0, 12 September 2026. [COROLLARY.md](COROLLARY.md) excludes raw real SoS certificate degree at most 2D+1 for the exact Boolean clause encoding BT•Rank′_n^m(I_m), for even n>=1024, m=n^2 and D=floor(n/(32 log_2 n)); minimum degree is therefore at least 2D+2. It records two explicit degree-preserving simple-bamboo transfers. The corollary is the standard positive-functional implication of the existing full-square theorem after complete axiom and degree accounting. It is not a new lower-bound mechanism.

Underlying corollary repository: formal-pvnp. Exact source commit: **918e90fd9117b6689c068bac0148e8556149f454**. Main source record: research/p-equals-np/2026-09-12-positivity-complexity-consequence.md. At that pin the source corollary has completed separate proof (PASS), source/complexity (GO), and non-claims (PASS) reviews: 2026-09-12-positivity-consequence-proof-review.md, 2026-09-12-positivity-consequence-source-review.md, and 2026-09-12-positivity-consequence-nonclaims-review.md in the same research/p-equals-np/ directory. The source/complexity reviewer authored the earlier PSD theorem and is not its independent mathematical certifier. The corollary author supplied the exact degree argument and encoding transfers; the independent proof reviewer supplied verification without repair. Source reviewers supplied the primary-source comparison and interpretation limits. Novelty and priority remain unknown.

This public extraction received separate actual-file mathematical and source/non-claims/readiness reviews on 12 September 2026. Both inspected COROLLARY.md (11,313 bytes; SHA256 794F762688E398669F3788ECE92FFF29C52F87FC6A711F571EFE2C9DA6E28F3A; Git blob ce7bb0842fee7035626f9d2c7792929fcfffbe91) and its surrounding version metadata. No mathematical repair or source/scope correction was required. These extraction verdicts are distinct from the underlying source reviews and do not constitute human peer review, Lean verification, or novelty certification.

| Extraction role | Record in formal-pvnp research/p-equals-np/ | Final scientific disposition |
|---|---|---|
| Independent mathematical proof | 2026-09-12-degree-addendum-public-proof-review.md | PASS for the exact standalone corollary, raw-degree accounting, boundary axioms and both transfers; verification only. |
| Source/non-claims/readiness | 2026-09-12-degree-addendum-public-nonclaims-review.md | GO for source applicability, bounded claims, attribution, and scientific publication readiness. |

The table records scientific review of the candidate. The corollary proof bytes are unchanged by this review-status integration. Version metadata and scientific readiness alone do not assert that publication has occurred.

The positivity proof FULL-NOTE.md is preserved byte-for-byte from v2.0.0 commit 95701cf018a81894a2d20b95121c2a724a17992c (Windows checkout SHA256 876B27AE9F9A8911E6568ED86BF0EFA394F988CB02BE056210B302C9B098A50F). NOTE.md remains unchanged from v1.0.0 (Windows checkout SHA256 9BCEAAFB47B6C79B5B87B78B9C0E88108DE8CF3A000EA293FD73707F89E8D28B). Their historical no-SoS-degree statements report the scope of those versions; the new corollary is stated separately in version 2.1.0.

The current work is informal mathematics with AI-agent review, not human peer review or Lean verification. No SoS size lower bound, general SAT algorithm or runtime lower bound, general proof-system lower bound, circuit lower bound, or P-versus-NP conclusion is claimed. No sharp positivity threshold or novelty certification is asserted.

## Historical v2.0.0 provenance and review

The remainder of this file preserves the v2.0.0 attribution and review record. Its statements about scope and limits refer to that version, not the added v2.1.0 corollary.


## Version and review status

Version 2.0.0, 12 September 2026. Underlying derivation repository: formal-pvnp. Source commit: **90868e5d032db6dba4cdf61d8a3fe07bfacdbfd7**. Main source record: research/p-equals-np/2026-09-12-shared-row-conditioning.md. The public note preserves source equations (7)--(30), renumbered (1)--(24), with an explicit standalone source contract. Final independent actual-artifact mathematical review returned PASS after rereading the entire restored note and version metadata. The separate final source/non-claims/readiness review returned GO after its own whole-note and metadata check. Neither required a mathematical repair or source/scope change. The underlying proof's review does not automatically certify this extraction, its source contract, or its metadata.

The full theorem is: for even n>=1024, m=n^2 and D=floor(n/(32 log_2 n)), the unchanged specified bamboo-tree source satisfies R(p^2)>=0 for every actual ordinary-degree-at-most-D X/Y/U polynomial. The complete proof appears in [FULL-NOTE.md](FULL-NOTE.md).

## AI contributions and underlying review

AI agents authored the source-conditioned construction, conditional Fourier estimates with affine and full-rank exclusions, same-side rank estimate, and mixed-block conditional-covariance reduction. The author and source reviewer independently proposed the same hierarchical local-complement and context-counting argument before reading one another's proposal. Both contributions are credited. The source reviewer therefore is not presented as an independent mathematical verifier of that bridge.

A separate proof reviewer checked the complete argument without supplying a construction or mathematical repair. A fresh independent adversarial reviewer subsequently checked it and returned PASS without a repair. The source/model reviewer returned GO for the exact source laws, row-support bounds and claim scope. These underlying AI-agent reviews found no defect; they are not human peer review, formal verification, novelty certification, or automatic certification of every later edit. The source pin above includes the four completed source reviews listed below. The completed separate extraction-review status is recorded above and pinned below.


## Frozen underlying review records

All four records below are included at source commit 90868e5d032db6dba4cdf61d8a3fe07bfacdbfd7 in the repository-relative directory research/p-equals-np/. This is an exact provenance pin; it is not a claim that the development commit has been publicly released.

| Role | Record | Final decision and scope |
|---|---|---|
| Independent mathematical proof | 2026-09-12-shared-row-conditioning-proof-review.md | PASS for the complete saved argument; no construction or repair supplied. |
| Source/model | 2026-09-12-shared-row-conditioning-source-review.md | GO for exact source/model applicability and scope; independent co-contributor to the hierarchical bridge. |
| Fresh independent adversarial mathematics | 2026-09-12-shared-row-conditioning-fresh-review.md | PASS after reading the primary source and actual argument without relying on the other review reports; no repair supplied. |
| Independent non-claims | 2026-09-12-shared-row-conditioning-nonclaims-review.md | PASS for exact theorem, contribution disclosure, and bounded publication significance. |

The source record's initial conditional-reference comparison was superseded by its direct conditional-mixing and hierarchical-complement proof. This public note extracts the completed direct proof; it does not assert that the unused comparison inequality was proved.

## Exact v2 extraction reviews

Both reviewers inspected the complete extraction snapshot of FULL-NOTE.md, 18,176 bytes, SHA256 44AE45216BFD880EC1135383C93D121667A580E2B10CEC95186678AA3A237F1C, and its metadata on 12 September 2026. That historical review snapshot preceded a metadata-only change to timeless version wording; the mathematical proof text is unchanged. Their records are in formal-pvnp, repository-relative research/p-equals-np/:

| Independent role | Record | Final disposition |
|---|---|---|
| Mathematical extraction and fresh adversarial review | 2026-09-12-full-positivity-public-candidate-proof-review.md | PASS for the complete standalone proof and version metadata; no construction or repair supplied. |
| Source/non-claims/readiness | 2026-09-12-full-positivity-public-candidate-nonclaims-review.md | GO for exact source scope, attribution, metadata and bounded publication readiness; no source/scope fix required. |

The mathematical proof text in the review snapshot above is unchanged by the final version-wording update. These are informal AI-agent reviews of the actual extraction, not human peer review, Lean verification, novelty certification or evidence that publication has occurred.
## Limits

The work is an informal written mathematical argument. It has no Lean verification, computational experiment or benchmark. Evaluation and local decompositions may be expensive; no efficient algorithm is established. Novelty and priority are unknown. No SoS degree or size lower bound, general SAT solver, P-versus-NP conclusion, or all-proof-systems statement is claimed.

The complete-row functions used inside the proof can have high ordinary degree. Their pairings use genuine union-context source laws and are explicitly shown to preserve the value of the original actual polynomial square. They are not silently reclassified as low-degree X/Y polynomials.

## Preserved v1 result

[NOTE.md](NOTE.md) is unchanged from v1.0.0 and retains its X-only lower window and upper-window witness. The v1 note received distinct AI-agent mathematical and source/claims review on 12 September 2026, including review of its extraction. Its contribution history included a constructive reviewer for the witness followed by a distinct verification-only proof reviewer. Those historical verdicts concern v1 and do not substitute for v2 artifact review. The published v1 history remains available.
