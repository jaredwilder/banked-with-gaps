# banked-with-gaps

**Historical claim bank for results whose original cards lacked enough proof evidence. One of the two principal gaps has now been repaired; the other remains an explicit unproved statement bank.**

Author: Jared Wilder. First public timestamp: 2026-09-11.

This repository is an audit/provenance object. Its purpose is to preserve what the original cards actually contained, including missing proof bodies, while linking outward when a claim is later repaired or promoted elsewhere.

## 1. Conference-switching elimination — RESOLVED

The historical card in `cards/conference-elimination.jsonl` stated a construction-class impossibility theorem for symmetric conference matrices of order `N=4m+2`, but its proof stopped after deriving the exact common-neighbour formulas.

During the September 11 public topology audit, the missing contradiction was completed.

The canonical theorem and full proof now live at:

`jaredwilder/combinatorial-records/ramsey/conference-switching-book-elimination.md`

### Completed argument

Let `r_i=sum_j C_ij` and put `s_i=r_i-1`.

The two book-avoidance inequalities imply:

- if `C_ij=-1`, then `s_i+s_j>=0`;
- if `C_ij=+1`, then `s_i+s_j<=0`.

Thus for every distinct pair,

`C_ij(s_i+s_j)<=0`.

But `r=C1` and `C^2=(N-1)I`, so

`Cs=(N-2)1-s`.

Therefore, for every `i`,

`sum_j C_ij(s_i+s_j)`

`= s_i r_i + (Cs)_i`

`= s_i^2 + N - 2 > 0`,

contradicting the pairwise nonpositivity.

Hence the conference-switching construction class really is eliminated. The historical card remains here unchanged as provenance; the gap status is closed by the canonical proof, not by silently editing the card.

## 2. Seventeen entire-function cards — UNRESOLVED

`cards/entire-functions.jsonl` contains seventeen statements concerning

`beta(f)=liminf_r mu(r,f)/M(r,f)`

for transcendental entire functions. Their historical status labels say `PROVED-HERE`, but the cards contain **no proof bodies**.

The statements include:

- a reduction to Newton-envelope breakpoints;
- a switch-profile formula;
- a two-active-coefficient bound `||F||_infinity >= pi/2` and hence `mu/M <= 2/pi`;
- confinement `3/2 < K < 8` for a theta-family minimizer;
- a recursion between consecutive normalized switch profiles.

Those statements are specific enough to investigate, but the old `PROVED-HERE` label is not evidence. They should not be cited as established until reconstructed proofs or independent proofs are supplied.

The unrelated appearance of a `pi/2` lower bound in another engineering-style optimization card is heuristic cross-context evidence only; it does not prove any of these entire-function statements.

## Why retain this repository

A missing proof is useful information when it is visible. The correct lifecycle is:

1. preserve the historical card;
2. state the gap precisely;
3. repair or independently prove the mathematics if possible;
4. route the completed result to its mathematical subject home;
5. leave this repository as the provenance record.

The conference-switching theorem has now completed that lifecycle. The seventeen entire-function cards have not.

## License

Apache-2.0.
