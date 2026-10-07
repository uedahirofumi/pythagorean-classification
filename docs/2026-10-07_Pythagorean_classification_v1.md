# 2026-10-07 — Pythagorean Classification Project, Canonical Record v1

## 1. Problem

Study functions F:N→C such that

1. F(mn)=F(m)F(n) for all positive integers m,n;
2. F(1)=1;
3. for every primitive Pythagorean triple a^2+b^2=c^2,
   F(a)+F(b)=F(c).

The project arose from the separate physics question of whether a quadratic weight can be forced by additive, multiplicative, and Pythagorean-type consistency. The number theory below stands independently of that motivation.

## 2. Main theorem — proved

If F(2) and F(3) are not simultaneously zero, then F is exactly one of 13 possibilities:

- the square function F(n)=n^2;
- 12 Dirichlet-character solutions.

Hence the nondegenerate branch is completely classified.

## 3. The 12 non-square solutions

| Modulus | Character type | Number | Prime where it vanishes |
|---:|---|---:|---:|
| 2 | principal character | 1 | 2 |
| 8 | Kronecker (2/·) | 1 | 2 |
| 3 | principal character | 1 | 3 |
| 9 | cubic characters | 2 | 3 |
| 5 | Legendre character | 1 | 5 |
| 25 | order-10 characters | 4 | 5 |
| 13 | order-6 characters | 2 | 13 |

Total: 12.

Each was verified exactly by exhaustive residue-class checking and proved to satisfy the Pythagorean functional equation globally.

Controls that fail:
- chi_{-4};
- principal character mod 5;
- quartic characters mod 5.

## 4. Finite base classification

The equations from primitive Pythagorean triples with c<=85 were solved over C using a division-free Gröbner-basis computation.

Result:
- 13 nondegenerate pairs (F(2),F(3));
- one degenerate branch F(2)=F(3)=0.

The 13 nondegenerate branches are exactly the square function plus the 12 characters above.

The earlier approximate real branch near F(2)≈1.185 is eliminated by the full finite system; in particular the relation from (36,77,85) removes it.

## 5. Global uniqueness / propagation

The positive-real induction was re-examined. The propagation argument only needs division by F(1) and F(7).

For all 13 nondegenerate branches, F(7) != 0.

Therefore each admissible pair (F(2),F(3)) propagates uniquely to all n. No additional nondegenerate branches can appear at larger integers.

## 6. Rigidity corollary

Every one of the 12 character exceptions vanishes at one of the primes 2,3,5,13.

Therefore

F(2)F(3)F(5)F(13) != 0

implies

F(n)=n^2  for all n.

The earlier positive-real theorem is a special case.

## 7. Degenerate branch — unresolved globally

Assume F(2)=F(3)=0.

Then F(5)=F(7)=0 is also forced.

A trivial solution exists:
- F(1)=1;
- F(n)=0 for n>1.

It is not yet proved that this is the only degenerate solution.

If a nontrivial degenerate solution exists and p0 is the smallest prime with F(p0) != 0, necessary conditions include:

- p0 ≡ 3 (mod 4);
- (p0^2+1)/2 is prime;
- with
  alpha=((p0+1)+(p0-1)i)/2,
  Re(alpha^(2k)) is not divisible by any prime below p0 for the relevant positive integers k.

A search found no such p0<10^6.

There were 3543 preliminary candidates; all were eliminated using primes <=31.

This is finite computational evidence, not a global proof.

## 8. Historical dead end

An earlier route used the standard triple

(p, (p^2-1)/2, (p^2+1)/2)

for p≡3 mod4 and generated upward dependencies such as (11,60,61). A ν2-descent idea did not fully prove well-foundedness because downward moves could reset the measure.

That route is no longer part of the proof.

The successful induction instead chooses a small auxiliary odd d so that a constructed Pythagorean triple has a controlled composite hypotenuse; this removes the dependency-graph problem.

## 9. Physics interpretation — safe statement only

The intended physical bridge is:

additivity of distinguishable alternatives
+ multiplicativity of serial/independent composition
+ reversible Pythagorean mixing
+ nonnegative/nonvanishing physical weight
=> quadratic rigidity.

Safe claim:

Under explicit composition and nonvanishing assumptions, exponent 2 is rigid.

Unsafe current claim:

“The Born rule has been derived from first principles.”

Still to audit:
1. whether the weight is assumed to depend only on component magnitude;
2. whether rational/Pythagorean rotations are physically realizable reversible transformations;
3. whether additive probability structure is being assumed rather than derived;
4. whether multiplicative composition imports too much;
5. why physical refinement should exclude zero weights.

## 10. Information-geometric connection

Candidate larger chain:

distinguishability
→ information geometry
→ orthogonality / reversible mixing
→ Pythagorean rigidity
→ quadratic weight.

The theorem may fill the earlier “why quadratic?” gap.

It does not yet explain:
- why quantum amplitudes are complex;
- why a single outcome occurs in one measurement.

## 11. Publication status

The nondegenerate complex-valued classification is already a coherent theorem suitable for a number-theory paper.

Possible title:

Completely Multiplicative Functions Additive on Primitive Pythagorean Triples

Suggested structure:
1. definitions and main theorem;
2. finite Gröbner-basis classification;
3. exact identification of the 12 characters;
4. propagation/uniqueness;
5. nonvanishing corollary;
6. degenerate branch and computational obstruction;
7. open problems.

Before a novelty claim, perform a final MathSciNet/zbMATH literature audit.

## 12. Canonical status at 2026-10-07

PROVED:
- nondegenerate complex-valued classification;
- exactly 13 nondegenerate branches;
- 12 character exceptions;
- global uniqueness/propagation;
- F(2)F(3)F(5)F(13)!=0 => F(n)=n^2.

COMPUTATIONALLY VERIFIED ONLY:
- no nontrivial degenerate minimal prime p0<10^6.

OPEN:
- complete degenerate-branch classification;
- physical audit of the Born-rule bridge;
- origin of complex amplitudes;
- single-outcome measurement problem.

Canonical conclusion:

The nondegenerate complex-valued classification is complete.
Only the fully degenerate zero branch remains globally unresolved.
