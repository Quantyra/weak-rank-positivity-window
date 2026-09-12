# Output-uniform positivity and explicit SoS size for simple bamboo

**Version 4.0.0, 12 September 2026.** [OUTPUT-NOTE.md](OUTPUT-NOTE.md)
extends the identity-output result to every Boolean matrix A, at even
q>=1024, residual width q, input width N=8q+4, m=q^2 and
D=floor(q/(32 log_2 q)). It proves square positivity for arbitrary sums
whose individual monomials use at most 2D typed rows, without an ordinary
degree bound. The source's A-preserving restriction then gives explicit
SoS certificate size at least (8/7)^((2D-1)/2)=exp(Omega(N/log N)).

The measure is S=sum_i ||f_i||||g_i||+sum_j ||h_j|| for the real identity
sum_i f_i g_i+sum_j h_j^2=-1. It counts original explicit multiplier and
root monomials, before squaring or Boolean reduction, with no degree
limit or coefficient-bit charge. It is not arithmetic-circuit size.
The exact simple-bamboo clause encoding and proof are stated in the note.

A separate corollary specifies G_q(X,Y)=XY over F_2 with seed length
s_q=16q^3+8q^2 and output length t_q=q^4=Theta(s_q^(4/3)). Every nonrange
output has the same explicit SoS lower bound under the stated inversion
encoding. Prefix variables are encoding witnesses, not seed bits.
Range is exactly rank(A)<=N: in-range outputs are satisfiable and their
refutation-size statement is vacuous. Rank testing and preimage recovery
are polynomial-time; this encoding-specific proof-complexity generator
does not assert computational pseudorandomness or inversion hardness.

[SIZE-NOTE.md](SIZE-NOTE.md) preserves v3's identity-output size theorem.
[FULL-NOTE.md](FULL-NOTE.md), [COROLLARY.md](COROLLARY.md), and
[NOTE.md](NOTE.md) preserve the earlier full-variable ordinary-degree,
certificate-degree, and X-only results. These four notes and
[LICENSE](LICENSE) are unchanged Git blobs from v3.0.0. Historical
no-size or identity-only statements retain their earlier-version scope;
the arbitrary-output theorem is stated separately in v4.

The increment is output uniformity, not a better exponent, newly invented
restriction or general SoS method. Novelty and priority are unknown.
This is informal mathematics with AI-agent review, not human peer review
or Lean verification. No arbitrary-m, other-encoding, all-length padding,
iteration, amplification, nearly quadratic/exponential stretch, general
SAT runtime, circuit lower-bound or P-versus-NP conclusion is claimed.

[SOURCES.md](SOURCES.md) gives attribution and comparisons;
[REVIEW.md](REVIEW.md) gives exact provenance and review status.
Maintained by Quantyra Research under [Apache 2.0](LICENSE).
Citation metadata is in [CITATION.cff](CITATION.cff).
