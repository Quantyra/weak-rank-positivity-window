# Full-variable positivity for the bamboo-tree weak-rank functional

**Prepared v2.0.0, 12 September 2026; not yet published.** Underlying derivation: formal-pvnp commit **90868e5d032db6dba4cdf61d8a3fe07bfacdbfd7**. Exact source provenance and informal AI-review status are in [REVIEW.md](REVIEW.md). This preparation does not claim that a release, tag, or DOI has been published.

## Theorem and scope

For every even integer n>=1024, put m=n^2 and D=floor(n/(32 log_2 n)). Let R be the restricted bamboo-tree weak-rank functional specified below, with prescribed matrix A=I_m. Then

    R(p^2)>=0

for every Boolean-reduced real polynomial p of ordinary degree at most D in the actual X, Y, and prefix auxiliary U variables. Write V_D for this space. The square is reduced in the Boolean quotient before applying R. Thus D grows on the n/log n scale; it is the degree of p, not of p^2. The proof controls arbitrary sums over many row contexts.

This statement concerns this particular published functional. It is not a SoS degree or size lower-bound claim, a general SAT algorithm, or a P-versus-NP claim. Novelty and priority are unknown. The proof is informal mathematics reviewed by AI agents, not human peer review or Lean verification. See [REVIEW.md](REVIEW.md).

The [v1 X-only note](NOTE.md), including its upper-window negative-square witness, is retained unchanged as a prior result. This note adds a full-variable lower positivity window; it does not claim a sharp threshold.

## Exact imported source contract

Use Garlik, Gryaznov, Ren, and Tzameret, *The Weak Rank Principle: Lower Bounds and Applications*, [ECCC TR26-133](https://eccc.weizmann.ac.il/report/2026/133/) and [arXiv:2608.08760v1](https://arxiv.org/abs/2608.08760v1), Section 6.1, Definitions 6.5--6.6, equation (36), Lemma 6.7, and R in the proof of Lemma 6.4. The ECCC text locates these on printed pages 69--71; arXiv v1 uses different pagination. Consistency and nonemptiness are credited source imports. The conditional estimates and assembly below are proved rather than imported as source conclusions.

All vector algebra is over F_2. Let e=(1,...,1) in F_2^n. Typed labels comprise m X rows and m Y columns; an X label and Y label remain distinct even if their numeric indices coincide. For typed context S=(I,J), |I|+|J|<=n-2, the local law rho_S is uniform on pairs of vectors

    (x_i in F_2^n : i in I), (y_j in F_2^n : j in J)

such that e with the selected X rows is linearly independent, e with the selected Y columns is linearly independent, and

    e dot x_i=1, e dot y_j=1, x_i dot y_j=A_ij.

Equivalently the two matrices augmented by the fixed boundary e both have full rank and their product is the source's restricted augmented prescribed matrix. Since n is even, e dot e=0, as required for its boundary entry. All normalizations use this same rank-restricted law.

The actual coordinate variables evaluate as x_(i,t) and y_(t,j). An interior auxiliary u_(i,j,k) evaluates as sum_(t<=k) x_(i,t)y_(t,j) modulo two. Boundary auxiliaries use e as the relevant endpoint. In particular u_(i,j,n)=A_ij. These U variables retain ordinary degree one; eliminating them into X/Y would change the degree model. Complementary variables, when present, are their Boolean complements.

The source proves that these laws are nonempty and that their marginals under deletion of typed rows agree. Define R on a multilinear monomial by its expectation in any source context containing its row support; extend linearly, monomial by monomial, to row-degree at most n-2. Every variable touches at most two typed rows. Hence 4D<=n-2 suffices for every actual degree-D square, even if the complete polynomial mentions many more rows.

Pairings of arbitrary complete-row functions below are defined through their union law. The proof checks that they preserve R on each original polynomial square. No globally satisfying distribution on all m labels is assumed.

## Norm convention

Every L2 norm uses the indicated uniform probability law on a finite source or affine fiber. A kernel acts as (Kg)(x)=E_y[K(x,y)g(y)], so matrix singular values include probability normalization. Maximal correlation is the conditional-expectation operator norm between centered L2 spaces of the actual marginals. Only supported separator assignments are conditioned on; zero-dimensional centered spaces contribute norm zero.
## Conditional opposite-side operators

We first bound conditional coupling between pure opposite-side blocks, then handle mixed blocks by conditional covariance and prove positivity by local hierarchical complements.

Fix supported separator data with r X rows and s Y columns. Let

    U=span(e, separator X rows),  V=span(e, separator Y columns),
    u=r+1, v=s+1, t=rank of the dot pairing U x V,
    h=n-u-v+t >= n-r-s-2.                                (1)

For one added X row the unrestricted affine fiber is X0=x0+V^perp, whose equations prescribe dot products with every separator Y column and with e. For one added Y column it is Y0=y0+U^perp. The rank-admissible sets are X*=X0\U and Y*=Y0\V. All these sets come from the source, not independent odd-row substitutions.

The bilinear character operator K(x,y)=(-1)^(x dot y) between the uniform L2 spaces of X0 and Y0 has exact norm

    ||K||=2^(-h/2).                                      (2)

To check it, the bilinear pairing between V^perp and U^perp has left radical U intersect V^perp, of dimension u-t. Its rank is therefore (n-v)-(u-t)=h. Affine translations only multiply rows and columns of the character matrix by signs. Equivalently KK* has zero entries unless x-x' lies in that radical; each surviving radical coset gives a rank-one signed block. With uniform probability normalization its nonzero eigenvalue is 2^(u-t)/2^(n-v)=2^(-h), proving (2).

The removed fraction |X0 intersect U|/|X0| is either zero or 2^(-h); the Y fraction is likewise either zero or 2^(-h). Restricting the operator to the remaining sets, with their own uniform probability normalizations, costs at most 1/(1-2^(-h)). Thus

    ||K restricted to X* x Y*|| <= alpha,
    alpha=2^(-h/2)/(1-2^(-h)).                           (3)

The prescribed new dot output c has indicator (1+(-1)^c K)/2. Both conditional source marginals are uniform on X*,Y*. This also follows directly without assuming constant deletion counts: for x outside U, precisely half of Y0 has x dot y=c. For each excluded y in Y0 intersect V, x dot y is fixed by the defining equations of X0, independent of x. Hence its deletion subtracts the same number for every admissible x. The other side is symmetric. These are the source's uniform extension counts.

The normalized coupling density with respect to the uniform product on X* x Y* is (1+sigma K)/Z, where sigma=(-1)^c and Z=1+sigma E K. For mean-zero f,g the constant term vanishes. Since |E K|<=alpha, for h>=3,

    |E_source[f g]| <= beta_h ||f||_2 ||g||_2,
    beta_h=alpha/(1-alpha)
          =2^(-h/2)/(1-2^(-h)-2^(-h/2)).                (4)

All norms are those of the actual conditional singleton marginals. Total support |S|+2<=n-2 is required. The bound is uniform in supported separator values and affine right-hand sides; it includes all same-side rank exclusions. For h large it is exponentially small. It treats arbitrary fixed mixed separator frames. It does not assert that (4) is the exact centered singular value.

### Pure multirow extension without a quadratic channel-count loss

Now add a>=1 X rows as one block and b>=1 Y columns as the other, keeping the same arbitrary supported separator. Require |S|+a+b<=n-2. Each X row has its own prescribed affine coset of V^perp; each Y column has its own coset of U^perp. First use the product of these affine cosets. Retain exactly the tuples which extend U, respectively V, to full rank.

For X, conditional on the preceding independent draws, the probability that the i-th added row (i=0,...,a-1) lies in the span of U and its predecessors is at most 2^(i-h): that span has dimension at most u+i, and its dot pairing with V has rank at least t. Its intersection with the required affine coset therefore has at most 2^(u+i-t) points, while the coset has 2^(n-v) points. A union bound gives failure probability at most

    delta_X=(2^a-1)2^(-h),
    delta_Y=(2^b-1)2^(-h).                              (5)

This is a bound under the unrestricted affine tuple law, not an assertion of independence after rank conditioning.

Fourier-expand the complete a-by-b prescribed new output matrix. For channel C in F2^(a x b), let K_C(X,Y)=(-1)^(sum_ij C_ij x_i dot y_j). If C has rank k, its bilinear pairing on the affine product directions has rank kh: in bases it is the tensor product of C and the residual pairing of rank h. Thus

    ||K_C||=2^(-hk/2).                                  (6)

Affine shifts again only give separate sign multipliers. There are at most 2^(k(a+b)) matrices C of rank k, since each has a factorization through a k-dimensional space. Hence, putting tau=2^(a+b-h/2), when tau<1 the sum of the operator norms of all nonzero Fourier channels is bounded by

    sum_(k>=1) tau^k = tau/(1-tau).                     (7)

This rank count avoids the crude 2^(ab) channel loss. Rank-shell enumeration and finite-field Fourier analysis are standard: the independent source reviewer checked the bilinear-forms scheme discussion in [arXiv:1709.09011, Section 7](https://arxiv.org/abs/1709.09011). That precedent does not by itself identify the present conditional rank-excluded source fiber, and no novelty claim is made for the counting method or resulting estimate. After restricting to the independently rank-admissible X and Y tuple sets, (5) bounds the normalization cost. If delta_X,delta_Y<1, put

    gamma = tau / ((1-tau) sqrt((1-delta_X)(1-delta_Y))). (8)

The full prescribed-output indicator, multiplied by 2^(ab), equals 1+E, where E is the signed sum of nonzero character kernels. The restricted operator norm of E is at most gamma. The actual conditional source marginals are the uniform rank-admissible affine tuple laws, by source consistency (or iteration of its uniform extension count). Its normalized density relative to their product is (1+E)/Z, with |Z-1|<=gamma. Therefore, if gamma<1,

    ||T_(pure X block,pure Y block | s)||
            <= gamma/(1-gamma).                        (9)

Here the operator is centered using the actual conditional marginals. This proof retains output and rank constraints and is uniform in all supported separator data. It uses no positive global distribution on all m labels.

For |S|+a+b<=4D, (1) gives

    tau <= 2^(-n/2+4D+1),
    delta_X,delta_Y <= 2^(-n+4D+2).                      (10)

Thus (9) is exponentially small uniformly for these pure opposite-side blocks when D is proportional to n/log n and n is sufficiently large. This is uniform in the growing-degree window; the mixed-block reduction below is still needed.

### Why a separate mixed-block reduction is needed

For the full conditional estimate, each added block can itself contain both X rows and Y columns and internal prefix observables. The present Fourier argument puts all newly added X rows on one operator side and all newly added Y columns on the other. It does not yield the same bound for that different grouping. Conditioning each mixed block on its own internal cross outputs by a naive density-restriction argument can cost a factor exponential in D^2; the rank count in (7) has not been shown to remove that cost. Same-side cross-block rank exclusions must also be handled in the mixed grouping. The conditional-covariance reduction (13)--(14) below avoids this naive density penalty.

After resolving mixed grouping, local complements will control arbitrary label sums directly.

## Full mixed-block estimate

For two pure same-side added blocks of sizes a,b and supported separator S, sample each block independently from its own rank-admissible affine tuple law in (1). Their joint source law additionally requires their combined extension to have full rank. Write F for the indicator of failure and e for its product-law probability. For each fixed admissible first block, the sequential estimate in (5), starting from a span of dimension u+a whose pairing with V has rank at least t, gives

    e <= e_ab := 2^a(2^b-1)2^(-h)/(1-d_b),
    d_b=(2^b-1)2^(-h).                                  (11)

The denominator conditions the second block on its own admissibility. The same argument applies to Y blocks. Source consistency implies that the combined-rank conditioning preserves both uniform admissible marginals. Therefore F has constant row and column averages e. The weighted Schur bound gives ||F||<=e. The source density is (1-F)/(1-e), and centered maximal correlation satisfies

    rho_same <= e/(1-e) <= e_ab/(1-e_ab), e_ab<1.         (12)

Here rho denotes maximal correlation. No independence of retained joint frames is asserted.

For every finite joint law, total covariance and conditional-variance Cauchy--Schwarz give

    rho(A ; (B,C)) <= rho(A;B)
                      + sup_(supported b) rho(A;C|B=b).  (13)

For centered f(A),g(B,C), the covariance of their means given B is at most the first term times ||f|| ||g||. The expected conditional covariance is at most the second term times the square root of the expected two conditional variances, and hence times ||f|| ||g||. Center each conditional function in its own supported fiber.

Split mixed blocks A=(A_X,A_Y), B=(B_X,B_Y). Apply (13), its symmetric version, and then (13) in each term:

    rho(A;B|s) <= rho(A_X;B_X|s)
       + sup_bx rho(A_X;B_Y|s,bx)
       + sup_ax rho(A_Y;B_X|s,ax)
       + sup_ax,bx rho(A_Y;B_Y|s,ax,bx).                 (14)

Each term uses a pure same-side or opposite-side source law with an enlarged supported separator and unchanged total support. Empty blocks contribute zero. Thus (9) and (12) apply, without conditioning a raw density on all internal outputs.

Put t0=2^(-n/2+4D+1), d0=2^(-n+4D+2). Suppose t0,d0<=1/16 and d0<=t0. Equations (8)--(10) give gamma<=2t0 and rho_opposite<=4t0. Equations (11)--(12) give e_ab<=2d0 and rho_same<=4d0. Hence for every disjoint typed S,A,B of total size<=4D and every supported s,

    rho(A;B|s) <= epsilon_D :=16t0=2^(-n/2+4D+5).        (15)

This proves the full mixed-block conditional estimate in the stated window, with all output and rank restrictions. Every law used is a genuine source law on at most 4D rows.

## Hierarchical local complements and full source PSD

The local-complement argument requires only the consistent local laws and the uniform conditional estimate. Attribution and review limitations are in [REVIEW.md](REVIEW.md).

For each typed A with |A|<=2D, let L_A=L2(rho_A) on complete-row functions, and define

    J_A = orthogonal complement in L_A of the span of
          all functions on proper subsets of A.         (16)

J_empty consists of constants. Marginal consistency makes all lifts isometries. Every f in L_A is a sum of h_T in J_T over T subset A: project onto J_A, write the residual as a sum of proper-subset functions, and induct on |A|. All spaces are finite-dimensional, so their sums are closed. No product-law orthogonality or efficient decomposition is assumed.

Apply this to each actual monomial M of degree<=D in its row support A_M, whose size is at most 2D. Combine equal-support components across p:

    p = sum_(A: |A|<=2D) h_A, h_A in J_A.                (17)

These are local almost-sure evaluation identities. The components can have high ordinary degree; they are not asserted to belong to V_D. Define their pairings by

    [f,g]=E_(rho_(A union B))[f g], f on A, g on B.       (18)

The union has size<=4D, so this is available. Versions off source support do not matter. Every local identity in the decomposition remains valid on any such larger union by marginal consistency. Expanding the original p monomial by monomial and replacing within each pair union therefore proves exactly

    R(p^2)=sum_(A,B)[h_A,h_B].                           (19)

No globally satisfying measure or low ordinary degree for h_A is used.

If A is properly contained in B, the pairing is zero by (16). For incomparable A,B, put S=A intersect B. Both components have conditional mean zero given S, by (16), under their marginals and hence the union law. Apply (15) to the disjoint differences given S and average by Cauchy--Schwarz. Thus for every distinct A,B,

    |[h_A,h_B]|<=epsilon_D ||h_A||_(rho_A)||h_B||_(rho_B),
    [h_A,h_A]=||h_A||_(rho_A)^2.                         (20)

The empty-context case follows from orthogonality to constants. Let L=sum_(j<=2D) binom(2m,j). Since sum_(A!=B) a_A a_B <=(L-1)sum_A a_A^2,

    R(p^2)>=[1-(L-1)epsilon_D]sum_A ||h_A||_(rho_A)^2.   (21)

This accounts for arbitrary label sums. It is a bound on the unchanged source form, not a positive sandwich GHG or a replacement moment functional.

Take even n>=1024, m=n^2, and

    D=floor(n/(32 log_2 n)).                             (22)

Then D>=1, 4D<=n-2, and 4D<=n/8. Thus t0,d0<=1/16 and d0<=t0. Moreover

    L<=2(2n^2)^(2D),
    log_2 L<=1+6D log_2 n<=1+3n/16,
    L epsilon_D<=2^(-3n/16+6)<1/2.                       (23)

The last inequality uses (15) and 4D<=n/8. Consequently for every actual p in V_D,

    R(p^2)>=(1/2)sum_A ||h_A||_(rho_A)^2>=0.             (24)


## Conclusion and limits

The final inequality proves the stated theorem for the unchanged source functional. Its normalization, Boolean identities, and available source gate/output identities have not been replaced by those of a comparison functional.

The proof uses finite Fourier analysis, rank counting, conditional covariance, finite-dimensional orthogonal decomposition and diagonal dominance. It supplies no efficient evaluation procedure: there are sum_(j<=2D) binom(2m,j) contexts and complete-row spaces can be exponentially large. No experiment or computational benchmark is part of the proof.

[REVIEW.md](REVIEW.md) records exact provenance, contributions and informal review limitations; [SOURCES.md](SOURCES.md) records primary comparisons. Version 2.0.0 is prepared locally and not yet published.
