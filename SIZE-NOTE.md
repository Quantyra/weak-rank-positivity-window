# An explicit SoS size lower bound for simple bamboo weak rank

Version 3.0.0, 12 September 2026. Provenance and informal AI-review
disclosures are in [REVIEW.md](REVIEW.md). This note gives a new
bounded-row-space consequence of the complete-row conditional estimates
in [FULL-NOTE.md](FULL-NOTE.md), then combines it with the primary
source's random restriction. Its exact bound is
`exp(Omega(N/log N))`; an `exp(Omega(N))` bound is not established.

## Exact theorem

Let q>=1024 be even, N=8q+4, m=q^2, A=I_m, and

    D=floor(q/(32 log_2 q)), B=2D, a=sqrt(7/8).

Let F be the real clause-falsification encoding of the **unrestricted simple
bamboo** CNF BT-bullet-Rank_N^m(I_m), with every Boolean equation v^2-v=0.
Optional literal twins have equations v+bar(v)-1=0 and their Boolean
equations. This is source Definition 6.1, not the Section 5 encoding with
additional product variables and not the perfect-matching encoding.

To specify the clause encoding explicitly, for each i,j in [m] and k in
[N], x=x_(i,k), y=y_(k,j), and b=u_(i,j,k) are Boolean variables. The
output falsification polynomial is 1-u_(i,j,N) if A_ij=1 and u_(i,j,N)
if A_ij=0. At k=1 the three base polynomials are

    (1-b)xy, (1-x)b, (1-y)b.

For k>=2 put a=u_(i,j,k-1). The six summation polynomials are

    (1-x)a(1-b), (1-x)(1-a)b,
    (1-y)a(1-b), (1-y)(1-a)b,
    xyab, xy(1-a)(1-b).

Every displayed polynomial is set equal to zero. On Boolean points these
encode b=a+xy modulo 2, rather than the real equation b-a-xy=0. The
base equations encode b=xy. Add all Boolean equations and, if the chosen
presentation uses twins, their complement equations. This fully specifies
the original axiom family; the random substitution below introduces the
separately described residual boundary prefixes.

For an explicit polynomial identity

    sum_i f_i g_i + sum_j h_j^2 = -1,

where f_i are these nonzero axioms, define its size exactly as source
Definition 4.3:

    S=sum_i ||f_i|| ||g_i|| + sum_j ||h_j||,

where ||p|| counts nonzero monomials in the ordinary polynomial ring of the
chosen variable/twin presentation, before Boolean reduction. Repeated
occurrences in different polynomials count separately. Coefficient bit
length is not charged. There is no degree limit and the h_j are explicitly
represented polynomials, not arithmetic circuits or implicit Gram factors.

**Theorem:** every such certificate has

    S >= a^(-(B-1)) = (8/7)^((2D-1)/2)
      = exp(Omega(N/log N)).                              (1)

The family is contradictory: any satisfying assignment yields XY=I_m over
F_2, impossible since m>N. Its clause/variable count is polynomial in N
(O(m^2 N)=O(N^5)); thus (1) is superpolynomial in its explicit input length.
This is an analytic consequence of the full-source estimates below and the
published random substitution. It is not obtained from the published
ordinary-degree theorem alone, or a generic size-degree tradeoff.

## Sources and the precise missing bridge

The primary source is [Garlik--Gryaznov--Ren--Tzameret, ECCC TR26-133](https://eccc.weizmann.ac.il/report/2026/133/),
Definitions 4.3, 6.1, 6.5--6.8 and Lemmas 6.7, 6.9--6.10, Theorem 6.11.
The analytic PSD source is [FULL-NOTE.md](FULL-NOTE.md), equations (1)--(24).
The previous exact degree interpretation is [COROLLARY.md](COROLLARY.md).
The v2 full-positivity theorem bounds ordinary root degree. Section 6.8 shrinks
the number of typed rows a term mentions, **not** its ordinary degree:
a surviving term can mention many coordinates in one row. Thus simply
inserting the ordinary-degree theorem in the SA proof is invalid. The
additional bridge proved next is a stronger bounded-row-space PSD statement.
It uses the actual full-positivity proof estimates, not a claim that this stronger
statement was already the published theorem.

## New row-space PSD lemma

Use the residual source with width q, m=q^2 and output I_m. The law rho_T
for each typed row set |T|<=q-2 is exactly the uniform augmented full-rank
X/Y law, with odd free vectors, prescribed dot outputs, all-ones boundary
row/column, and actual prefix U evaluation from Definitions 6.5--6.6.
Typed X_i and Y_j are distinct even if i=j; boundary m+1 costs no label.
Source Lemma 6.7 gives complete-row marginal consistency. Define R on the
span of Boolean monomials with at most q-2 labels using these local laws.

**Lemma.** R(p^2)>=0 whenever each monomial of the Boolean-reduced p has
at most B=2D typed labels, with no bound on its ordinary degree and no
bound on the total labels appearing across the sum p.

Here and below R(p^2) means Boolean reduction first. Pair monomial unions
have at most 2B=4D<=q-2 labels, so this value is defined. The proof can even
pair arbitrary complete-row functions, but only its polynomial consequence
is needed.

For every A of size at most B let L_A=L2(rho_A), and J_A be the orthogonal
complement of the span of all proper-subset function spaces in L_A. Each
local function decomposes as a sum of h_T in J_T for T subset A: orthogonally
project onto J_A and induct on the proper subsets. The spaces are finite
dimensional; existence suffices. Combining components gives p=sum_A h_A.
Every identity is a local almost-sure identity, and consistency lifts it to
each pair union. Consequently

    R(p^2)=sum_(A,C) E_(rho_(A union C))[h_A h_C].          (2)

No globally satisfying law is posited. The potentially high ordinary
degree of h_A causes no problem: all evaluations in (2) are in actual
complete-row spaces on <=2B labels.

FULL-NOTE.md (1)--(15) proves, uniformly in every supported separator realization,
maximal correlation at most

    epsilon=2^(-q/2+4D+5)

between disjoint mixed added blocks when total separator/block support is
at most 4D. Those estimates apply to **all complete-row L2 functions**, with
all rank exclusions and prescribed outputs retained. They have no
ordinary-degree hypothesis. For incomparable A,C the J components have
conditional mean zero on A intersect C. Conditional correlation and
Cauchy--Schwarz yield an off-diagonal bound epsilon ||h_A|| ||h_C||.
Nested distinct supports instead have pairing exactly zero by J
orthogonality. Diagonal pairings are ||h_A||^2.

There are at most L=sum_(r<=B) binom(2q^2,r) supports. Hence

    R(p^2)>=[1-(L-1)epsilon]sum_A ||h_A||^2
           >=(1/2)sum_A ||h_A||^2>=0.                    (3)

The numerical bounds are exactly FULL-NOTE.md (23):
log_2 L<=1+6D log_2 q<=1+3q/16, 4D<=q/8, and
L epsilon<=2^(-3q/16+6)<1/2. This proves the additional lemma explicitly.
It is the all-support bound, not positivity in one fixed context. In
particular arbitrary cancellation, arbitrary coefficients and arbitrary
numbers of monomials in each square root are covered.

## Exact restriction distribution and residual encoding

Apply source Definition 6.8 to N=8q+4. Independently for every original
X_i choose s_i uniform in [4] and alpha_i uniform in {0,1}, and for every
Y_j choose r_j uniform in [4] and beta_j uniform in {0,1}. All choices
are mutually independent. The source's two four-by-eight templates are

    D = [1 * 1 0 0 * * *; 0 1 * 1 * * * 0;
         * * 0 * 1 0 1 *; * 0 * * * 1 0 1],
    E = [1 0 0 1 * * * *; 0 * 1 * 1 * 0 *;
         * 1 * 0 * 0 * 1; * * * * 0 1 1 0].

Original X endpoints (1,2,N-1,N) become (alpha_i,1,alpha_i,1),
and Y endpoints become (1,beta_j,1,beta_j). Split the N-4 interior
columns into eight consecutive blocks of q. In block b at offset ell,
X becomes D_(s_i,b) if constant and x-tilde_(i,ell) for a star;
Y uses E similarly. The output matrix A and m are unchanged.

For each i,j,b set gamma_b to A_ij for the star/star case, 1 for
star/1 or 1/star, and 0 otherwise. Put
p_b=alpha_i+beta_j+sum_(c<b) gamma_c modulo 2.
Interior U_(i,j,k) becomes the actual residual prefix literal with
parity offset p_b: u-tilde_(i,j,ell) in star/star,
u-tilde_(i,m+1,ell) in star/1, or u-tilde_(m+1,j,ell) in 1/star,
complemented exactly when p_b=1. In 1/1 it becomes the constant
p_b+(ell mod 2); if either entry is 0 it becomes p_b. Endpoints become
alpha_i, alpha_i+beta_j, A_ij+beta_j, A_ij respectively, modulo 2.
Literal twins always map to the complementary image.

This is exactly the published substitution; every image is a literal or
constant. There is no parity-polynomial substitution and no new encoding.
It is a real polynomial-ring homomorphism when a complement is written
1-v, and is Boolean-valued on Boolean assignments. It cannot add a typed
label to any variable; boundary-prefix images can drop one label.

The residual system is source BT-bullet-Rank-prime_q^m(I_m), including
both boundary parity strips. Choosing **original m=q^2** is essential:
the source preserves m, and starting instead with m=N^2 would not meet
the exact available PSD theorem at residual q.

## Shrinkage event and every size cost

For each monomial occurrence t in each g_i or h_j, remove the factors
whose column index lies in {1,2,N-1,N}, and let r(t) be the number of typed
rows of this remaining interior subterm. Repeated powers do not change
its row set and may be reduced for purposes of the survival event.
If twins occur they are literals in the same sense as source Lemma 6.9.
That lemma gives

    Pr[t under rho is not identically zero] <= a^r(t).    (4)

An image that becomes zero only upon Boolean reduction can equally be
discarded; the bound on failure remains valid. Endpoint factors all become
constants, so each image monomial/literal product has residual row support
at most r(t). Complement expansion and Boolean reduction cannot add rows.

The number T of g/h monomial occurrences is at most S because every
nonzero f_i has ||f_i||>=1. Include Boolean and optional twin-equation
multipliers too; this only makes the union bound more conservative.
If S<a^(-(B-1)), (4) and a union bound imply

    Pr[some t with r(t)>=B-1 survives] <=T a^(B-1)<1.

Choose a substitution outside this event. Every surviving g/h monomial
image then has at most B-2 residual typed rows. This bound does not count
monomials in expanded h_j^2: the roots themselves were counted before
squaring. The polynomial homomorphism preserves h_j^2 as rho(h_j)^2,
and (3) applies to the arbitrary sum rho(h_j).

For completeness, affine complement expansion of an individual degree-e
monomial may produce as many as 2^e ordinary monomials before cancellations.
No upper bound on e or on the size of the restricted certificate is
assumed or needed: the probability space counts original monomials only,
and the positivity lemma depends on rows, not the expanded count. The
source uses 6m independent random bits (two type bits and one parity bit
per typed X/Y label); constructing an explicit full substitution has size
O(m^2 N). Local L2 spaces can have 2^(q|A|) states, and their decomposition
is not an efficient algorithm. The result is a lower bound on explicit
certificate monomial size, not a polynomial-time procedure or a lower
bound for circuit-compressed roots.

## Axiom annihilation and final contradiction

Do not import the SA proof conversion as an equality-ideal simulation.
Use the substituted identity itself in the residual Boolean quotient.
Every source clause involves at most the original typed labels X_i,Y_j.
Its substituted polynomial is zero on the residual local law for those
labels: Lemma 6.10's semantic case check gives this fact. Explicitly,
outputs and bases at the initial positions become satisfied constants;
the four endpoint transitions use constants or residual output equations;
within each block the parity transition is a residual summation/base gate
(possibly on a boundary strip), or a satisfied constant transition.
At a block boundary the preceding residual output and new residual base
give the transition. The templates' odd star/star count and even
star/1,1/star counts, together with even q, give the prescribed overall
output. Complements only change the parity offset. These checks use the
original clause semantics on Boolean points; they do not substitute the
incorrect real equation b-a-xy=0 for a parity gate.

Fix one surviving multiplier monomial t. Its image uses <=B-2 labels;
the union with the whole substituted clause's <=2 labels has size <=B.
On that genuine residual local law the clause image is identically zero,
so its product with rho(t) has expectation zero. Consistency gives
R(rho(f_i)rho(t))=0 after expanding/reducing, even if rho(t) contains
many ordinary monomials. Sum over multiplier monomials and clauses.
Boolean axiom images vanish identically in the Boolean quotient, and
twin equations do too. Thus every axiom summand has R value zero.

Each root image has monomials of row support <=B-2, hence (3) gives
R(rho(h_j)^2)>=0. All square monomials use at most 2B-4<=q-2 rows;
all clause products above use <=B<=q-2. Applying R to the substituted
Boolean identity is therefore legitimate and yields

    0+sum_j R(rho(h_j)^2)=-1,

contradicting R(1)=1. This proves (1).

## Comparison and limits

Source Theorem 6.11 already proves exponential SA size by this same
restriction and its linear row-degree lower bound. The new claimed step
here is the row-space **square** positivity bridge and its use for explicit
SoS roots, yielding the weaker exponent Omega(N/log N). Source Theorem
5.18 already proves exponential SoS size for a different perfect-matching
rank encoding. No first-rank-SoS or exhaustive novelty claim is made.
Neither the original ordinary-degree statement alone nor SA term
positivity implies this theorem. This note makes no Frege, arbitrary
proof-system, SAT solver, NP/coNP, or P-versus-NP conclusion.
