# Positivity and explicit SoS size for bamboo-tree weak rank

**Version 3.0.0, 12 September 2026.** Exact provenance and informal AI-review status are in [REVIEW.md](REVIEW.md).

[SIZE-NOTE.md](SIZE-NOTE.md) proves an explicit SoS certificate-size lower bound for the unaugmented simple bamboo encoding `BT-bullet-Rank_N^m(I_m)`. For even `q>=1024`, input width `N=8q+4`, `m=q^2`, and `D=floor(q/(32 log_2 q))`, every certificate has `S >= (8/7)^((2D-1)/2) = exp(Omega(N/log N))`. Here `S=sum_i ||f_i||||g_i||+sum_j ||h_j||` counts explicit axiom-multiplier and square-root monomials as in source Definition 4.3. It imposes no root-degree limit, but does not address circuit-compressed roots. The bound is superpolynomial in this family's explicit input length; it is not an `exp(Omega(N))` bound.

The proof first establishes positivity for arbitrary sums whose individual monomials mention at most `2D` typed rows, with no ordinary-degree bound. The primary source's Section 6 random substitution then maps input width `N` to residual width `q`, retaining `m=q^2`. It eliminates high-row-support multiplier and root monomials; residual local laws annihilate the substituted clauses. The new row-space step is proved explicitly and is not inferred from ordinary-degree positivity alone.

[FULL-NOTE.md](FULL-NOTE.md) retains the v2 full-variable theorem: for even `n>=1024`, `m=n^2`, and `D=floor(n/(32 log_2 n))`, the specified restricted functional satisfies `R(p^2)>=0` for every actual ordinary-degree-at-most-D X/Y/U polynomial. [COROLLARY.md](COROLLARY.md) retains v2.1's exact degree consequence and two encoding transfers. [NOTE.md](NOTE.md) retains v1's X-only result and upper-window witness. Those three notes and [LICENSE](LICENSE) are unchanged Git blobs from v2.1.0. Their historical no-size-claim statements describe the scope of those earlier versions; the size theorem is stated separately in v3.0.0. [SOURCES.md](SOURCES.md) identifies the credited inputs and comparisons.

Novelty and priority are unknown. This is informal mathematics with AI-agent review, not human peer review or Lean verification. No transfer to other rank encodings, general proof-system lower bound, arbitrary SAT algorithm or runtime lower bound, circuit lower bound, sharp positivity threshold, or P-versus-NP conclusion is claimed.

Maintained by Quantyra Research. Licensed under [Apache 2.0](LICENSE). Citation metadata is in [CITATION.cff](CITATION.cff).
