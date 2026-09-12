# A full-variable positivity window for the bamboo-tree weak-rank functional

**Version 2.1.0, 12 September 2026.** Exact provenance and informal AI-review status are in [REVIEW.md](REVIEW.md).

For even n>=1024, m=n^2, and D=floor(n/(32 log_2 n)), the specified restricted simple bamboo-tree functional satisfies R(p^2)>=0 for every actual ordinary-degree-at-most-D X/Y/U polynomial. The proof retains its source rank restrictions, output constraints, and prefix auxiliary variables.

[COROLLARY.md](COROLLARY.md) gives the exact SoS consequence: the Boolean clause encoding BT•Rank′_n^m(I_m) has no real SoS refutation of raw certificate degree at most 2D+1, so every refutation has degree at least 2D+2. It checks all clause families, boundary prefixes, Boolean and optional twin equations, and gives two explicit degree-preserving transfers to simple bamboo encodings. This is a standard consequence of the existing positivity theorem, not a new lower-bound mechanism.

The complete positivity proof in [FULL-NOTE.md](FULL-NOTE.md) is byte-for-byte unchanged from v2.0.0. The [X-only note and upper-window witness](NOTE.md) remain unchanged from v1.0.0. Their historical statements that no SoS degree consequence was claimed describe those versions' scope; version 2.1.0 adds the separately checked encoding-specific corollary. [SOURCES.md](SOURCES.md) identifies the source functional and comparisons.

Novelty and priority are unknown. This is informal mathematics with AI-agent review, not human peer review or Lean verification. No SoS size lower bound, general SAT algorithm or runtime lower bound, sharp positivity threshold, general proof-system lower bound, or P-versus-NP conclusion is claimed.

Maintained by Quantyra Research. Licensed under [Apache 2.0](LICENSE). Citation metadata is in [CITATION.cff](CITATION.cff).
