# Output-uniform positivity and explicit SoS size for simple bamboo

**Version 4.1.0, 12 September 2026.** [DIMENSION-NOTE.md](DIMENSION-NOTE.md)
is a dimension-budget addendum to the existing argument. For even q>=1024,
N=8q+4 and integer 8q+4<m<=2^(q/32-1), it sets
D=floor(q/(32 log_2(2m)))>=1 and proves, for every fixed Boolean output A,
explicit real SoS refutation size at least (8/7)^(D-1/2) for the exact
unrestricted simple-bamboo encoding. The source restriction keeps m and A
and reduces input width N to residual width q. The proof checks complete-row
square positivity and the full ambient support count.

The measure is S=sum_i ||f_i||||g_i||+sum_j ||h_j|| for the identity
sum_i f_i g_i+sum_j h_j^2=-1. It counts ordinary polynomial monomials before
Boolean reduction, roots before squaring, with no degree limit or
coefficient-bit charge. It is not arithmetic-circuit or implicit-root size.
The general window can have constant D; a sufficient condition for a bound
superpolynomial in actual formula length is q/(log m)^2 tending to infinity.

A separately checked indexed family uses integers r>=32,
q=2r^3, m=2^r and N=16r^3+4. The same map G_r(X,Y)=XY over F_2 has

    s_r=2^(r+1)(16r^3+4), t_r=2^(2r),
    t_r=Theta(s_r^2/(log s_r)^6),
    S >= (8/7)^(r^2/64)=exp(Omega((log s_r)^2)).

The output-to-seed ratio is Theta(s_r/(log s_r)^6), distinct from output
length. Its CNF has 2mN+m^2N variables and (6N-2)m^2 clauses before
Boolean/twin additions, width at most four, and O(4^r r^4) explicit bits.
Evaluation and construction are polynomial in actual seed/formula lengths,
not the short index r. Prefix variables are witnesses, not seed bits.

Range is exactly rank_F2(A)<=N. In-range outputs are satisfiable and their
refutation bound is vacuous. Rank testing and preimage recovery remain
polynomial-time. The indexed nonrange bound is superpolynomial in seed,
output and formula lengths, and asserts no computational pseudorandomness.

[OUTPUT-NOTE.md](OUTPUT-NOTE.md) preserves v4's stronger m=q^2 theorem,
with D=floor(q/(32 log_2 q)), output Theta(s^(4/3)) and hardness
exp(Omega(s^(1/3)/log s)). Version 4.1 trades a larger indexed output for
a weaker seed-normalized hardness scale, using the same mechanism.
[SIZE-NOTE.md](SIZE-NOTE.md), [FULL-NOTE.md](FULL-NOTE.md),
[COROLLARY.md](COROLLARY.md), [NOTE.md](NOTE.md) and [LICENSE](LICENSE)
also retain their exact previous Git blobs and historical scopes.

This is a modest re-budgeting extension. Near-quadratic rank-map geometry
and the primary source's stronger different-system/different-encoding
results are credited in [SOURCES.md](SOURCES.md). Novelty and priority are
unknown. Review is informal AI analysis, not human peer review or Lean
verification. No new general method, optimal window, unbounded-m bound,
all-length padding, iteration, function generator, compressed-proof bound,
general SAT runtime, circuit lower bound or P-versus-NP conclusion is claimed.

[REVIEW.md](REVIEW.md) records provenance and actual review status.
Maintained by Quantyra Research under [Apache 2.0](LICENSE).
Citation metadata is in [CITATION.cff](CITATION.cff).
