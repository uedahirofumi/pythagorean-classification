# 2026-10-07 — Pythagorean Classification Project, Canonical Record v1

## 1. Problem

Study functions

\[
F:\mathbb N\to\mathbb C
\]

such that

1. \(F(mn)=F(m)F(n)\) for all positive integers \(m,n\);
2. \(F(1)=1\);
3. for every primitive Pythagorean triple
   \[
   a^2+b^2=c^2,
   \qquad \gcd(a,b,c)=1,
   \]
   one has
   \[
   F(a)+F(b)=F(c).
   \]

The goal is to classify all such completely multiplicative functions.

## 2. Main theorem — proved

If \(F(2)\) and \(F(3)\) are not simultaneously zero, then \(F\) is exactly one of 13 possibilities:

- the square function
  \[
  F(n)=n^2;
  \]
- 12 Dirichlet-character solutions.

Hence the nondegenerate branch is completely classified.

## 3. The 12 non-square solutions

| Modulus | Character type | Number | Prime where it vanishes |
|---:|---|---:|---:|
| 2 | principal character | 1 | 2 |
| 8 | Kronecker \((2/\cdot)\) | 1 | 2 |
| 3 | principal character | 1 | 3 |
| 9 | cubic characters | 2 | 3 |
| 5 | Legendre character | 1 | 5 |
| 25 | order-10 characters | 4 | 5 |
| 13 | order-6 characters | 2 | 13 |

Total: 12.

Each of these 12 candidates was checked exactly by exhaustive residue-class analysis and proved to satisfy

\[
F(a)+F(b)=F(c)
\]

for every primitive Pythagorean triple.

The following comparison candidates fail:

- \(\chi_{-4}\);
- the principal character modulo \(5\);
- quartic characters modulo \(5\).

## 4. Finite base classification

The equations arising from primitive Pythagorean triples with

\[
c\le 85
\]

were solved over \(\mathbb C\) using a division-free Gröbner-basis computation.

The solution set consists of:

- 13 nondegenerate pairs \((F(2),F(3))\);
- one degenerate branch
  \[
  F(2)=F(3)=0.
  \]

The 13 nondegenerate branches are exactly the square function plus the 12 Dirichlet characters listed above.

A previously observed approximate real branch near

\[
F(2)\approx1.185
\]

does not survive the full system. In particular, the equation arising from

\[
(36,77,85)
\]

eliminates it.

## 5. Global uniqueness / propagation

The induction used to propagate the finite base to all positive integers only requires division by \(F(1)\) and \(F(7)\).

For all 13 nondegenerate branches,

\[
F(7)\neq0.
\]

Therefore every admissible pair \((F(2),F(3))\) determines the function uniquely on all of \(\mathbb N\). No additional nondegenerate branches can appear beyond the finite base.

## 6. Rigidity corollary

Every one of the 12 Dirichlet-character exceptions vanishes at at least one of the primes

\[
2,3,5,13.
\]

Therefore:

### Corollary

If

\[
F(2)F(3)F(5)F(13)\neq0,
\]

then

\[
\boxed{F(n)=n^2\quad\text{for every }n\in\mathbb N.}
\]

The positive-real case is a special case of this corollary.

## 7. Degenerate branch — unresolved globally

Assume

\[
F(2)=F(3)=0.
\]

Then the Pythagorean relations also force

\[
F(5)=F(7)=0.
\]

A trivial solution exists:

\[
F(1)=1,
\qquad
F(n)=0\quad(n>1).
\]

It is not yet proved that this is the only solution in the degenerate branch.

Suppose a nontrivial degenerate solution exists, and let \(p_0\) be the smallest prime satisfying

\[
F(p_0)\neq0.
\]

Necessary conditions derived so far include:

- \(p_0\equiv3\pmod4\);
- \((p_0^2+1)/2\) is prime;
- with
  \[
  \alpha=\frac{(p_0+1)+(p_0-1)i}{2},
  \]
  the values \(\operatorname{Re}(\alpha^{2k})\) avoid divisibility by primes below \(p_0\) for the relevant positive integers \(k\).

A computational search found no such \(p_0<10^6\).

There were 3543 preliminary candidates, and every one was eliminated using primes at most \(31\).

This is finite computational evidence, not a global proof.

## 8. Earlier proof route and its replacement

An earlier route used the standard triple

\[
\left(p,\frac{p^2-1}{2},\frac{p^2+1}{2}\right)
\]

for primes \(p\equiv3\pmod4\). This can generate upward dependencies such as

\[
(11,60,61),
\]

leading to a dependency-graph / well-foundedness problem.

A \(\nu_2\)-descent idea did not completely exclude infinite zig-zag chains and is not part of the final proof.

The successful induction instead chooses a small auxiliary odd parameter so that the constructed Pythagorean triple has a controlled composite hypotenuse. This removes the dependency-graph problem.

## 9. Publication structure

The nondegenerate complex-valued classification is a self-contained number-theoretic result.

A neutral title is:

**Completely Multiplicative Functions Additive on Primitive Pythagorean Triples**

A natural paper structure is:

1. definitions and main classification theorem;
2. finite Gröbner-basis classification;
3. exact identification of the 12 Dirichlet characters;
4. propagation / uniqueness theorem;
5. nonvanishing corollary;
6. degenerate branch and computational obstruction;
7. open problems.

Before making a novelty claim, a final MathSciNet/zbMATH literature audit is required.

## 10. Canonical status at 2026-10-07

### PROVED

- exact finite nondegenerate base classification over \(\mathbb C\);
- exactly 13 nondegenerate branches;
- exactly 12 non-square Dirichlet-character branches;
- exact global verification of those 12 characters;
- global propagation / uniqueness in the nondegenerate case;
- full nondegenerate classification theorem;
- the corollary
  \[
  F(2)F(3)F(5)F(13)\neq0
  \Longrightarrow
  F(n)=n^2.
  \]

### COMPUTATIONALLY VERIFIED, NOT A GLOBAL PROOF

- no nontrivial degenerate minimal prime \(p_0<10^6\);
- 3543 preliminary candidates all eliminated by primes \(\le31\).

### OPEN

- complete classification of the branch
  \[
  F(2)=F(3)=0;
  \]
- proof that the trivial zero-after-1 function is the only degenerate solution;
- final literature audit for novelty and overlap.

## 11. Canonical conclusion

\[
\boxed{\text{The nondegenerate complex-valued classification is complete.}}
\]

\[
\boxed{F(2)F(3)F(5)F(13)\neq0\Longrightarrow F(n)=n^2.}
\]

\[
\boxed{\text{Only the fully degenerate branch remains globally unresolved.}}
\]
