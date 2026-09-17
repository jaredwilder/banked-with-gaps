# Historical claims with missing proofs

This repository preserves mathematical statements whose original source cards did not contain enough proof material to support the status attached to them.

One major gap has since been repaired; one group of claims remains unresolved.

## Conference-switching theorem — repaired

The historical conference-matrix card asserted a construction-class impossibility theorem for order `N=4m+2`. The missing contradiction has since been completed.

Let `C` be the switched conference matrix, `r_i=\sum_j C_{ij}`, and `s_i=r_i-1`. The two book-avoidance inequalities imply, for every distinct pair,

\[
C_{ij}(s_i+s_j)\le0.
\]

But `r=C\mathbf1` and `C^2=(N-1)I`, so

\[
Cs=(N-2)\mathbf1-s.
\]

For each `i`,

\[
\sum_j C_{ij}(s_i+s_j)
=s_i r_i+(Cs)_i
=s_i^2+N-2>0,
\]

contradicting the pairwise nonpositivity.

The completed theorem now lives in the Ramsey records; the original incomplete card is retained here only as source history.

## Entire-function claims — unresolved

[`cards/entire-functions.jsonl`](cards/entire-functions.jsonl) contains 17 statements about

\[
\beta(f)=\liminf_r \frac{\mu(r,f)}{M(r,f)}
\]

for transcendental entire functions.

The cards include assertions about:

- Newton-envelope breakpoints;
- normalized switch profiles;
- a two-active-coefficient `\pi/2` bound;
- a claimed interval for a theta-family minimizer;
- recurrences between consecutive switch profiles.

The historical cards label these statements as proved, but they contain no proof bodies. Until proofs are reconstructed or supplied independently, these 17 statements should be treated as open verification tasks rather than established theorems.

## Files

- [`cards/conference-elimination.jsonl`](cards/conference-elimination.jsonl) — the original incomplete conference card.
- [`cards/entire-functions.jsonl`](cards/entire-functions.jsonl) — the 17 entire-function statements awaiting proof reconstruction.

This repository is deliberately small: completed mathematics belongs in its subject repository; only unresolved source gaps remain here.

Author: Jared Wilder. License: Apache-2.0.
