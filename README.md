# banked-with-gaps

**Two research seams published because of their defects, not despite them: one whose proof stops
before its own conclusion, and seventeen cards marked `PROVED-HERE` that contain no proof at all.**

Author: Jared Wilder. First public timestamp: 2026-09-11.

Both were found in the atlas bank. Neither should be cited as established. They are here because a
corpus that quietly drops its incomplete work is less trustworthy than one that publishes it
labelled.

---

## 1. Conference-switching elimination at order 398 — the proof stops early

**The claim.** Let `C` be any symmetric conference matrix of order `N = 4m+2 ≥ 6`
(`C = Cᵀ`, `C_ii = 0`, `C_ij ∈ {±1}`, `C² = (N−1)I`). Switch it arbitrarily to `DCD` with `D`
diagonal `±1`. Build `G` by making `ij` an edge exactly when `C_ij = −1`. Then it is **impossible**
that every edge of `G` has at most `m−1` common neighbours while every non-edge has at most `m`
common non-neighbours.

At `N = 398 = 4·99 + 2` this would eliminate **every graph in every switching class of every
symmetric conference matrix of order 398** from the search for a graph avoiding `B₉₉` whose
complement avoids `B₁₀₀`.

**What the card actually proves.** With `r_i = Σ_j C_ij`:

- `r_i` is odd (a sum of `N−1 = 4m+1` terms of `±1`)
- row orthogonality gives `Σ_{k≠i,j} C_ik C_jk = 0`
- an edge `ij` has exactly `(N − 4 − r_i − r_j)/4` common neighbours
- a non-edge `ij` has exactly `(N − 4 + r_i + r_j)/4` common non-neighbours

**The two formulas are exact and switching-covariant. The contradiction step is not written down.**
The card ends at the formulas.

**What I checked.** The elimination holds at the smallest case: for `N = 6` (`m = 1`), across **all
64 diagonal switchings** of a verified conference matrix (`C = Cᵀ` and `C² = 5I` both confirmed), no
switched form satisfies the condition. That is consistent with the claim and is not a proof of it.

The gap looks closable — the edge condition forces `r_i + r_j ≥ 2`, the non-edge condition forces
`r_i + r_j ≤ 2`, and `r_i` odd makes the sum even — but **assembling that into the stated
impossibility for all `N` is exactly the step the card omits, and I have not written it either.**

**Do not cite the order-398 elimination as established.**

## 2. Seventeen cards on entire functions with empty proof fields

A program on `β(f) = liminf_r μ(r,f)/M(r,f)` for transcendental entire `f`, banked as 17 cards with
status **`PROVED-HERE`** and **not one proof body among them**.

The statements themselves are specific and testable:

- a reduction to Newton-envelope breakpoints,
  `β(f) = liminf_j μ(e^{τ_j}, f)/M(e^{τ_j}, f)`
- a switch-profile formula, `β(f) = 1 / limsup_j ‖F_j‖_∞`
- a two-active-coefficient bound, `‖F‖_∞ ≥ π/2` and hence `μ/M ≤ 2/π`
- a compactness confinement `3/2 < K < 8` for any theta-family minimiser
- a recursion between consecutive normalised switch profiles,
  `F_{j+1}(z) = ξ_j z^{−d_{j+1}} F_j(qz)`

**`PROVED-HERE` on a card with an empty proof is a status, not evidence.** These are published as
statements that were asserted, so that anyone who wants to work on them starts from the honest
position rather than from a label.

One incidental cross-check: an unrelated engineering card in the same bank independently reaches the
same `π/2` constant — two mandatory unit-magnitude carriers force a continuous peak of at least
`(π/2)A`, with a hostile optimiser using 39 auxiliary tones reaching 1.6610 against the floor
1.5708. That is suggestive of the bound being real. It is not a proof of the entire-function card.

## Why publish either

Because the alternative is what this estate already did once: bank a claim under a confident label,
let it be mined, let it be ranked, and let someone act on it. A separate audit in this release
[refutes a claimed proof](https://github.com/jaredwilder/erdos-findings-ledger/blob/main/ERDOS-1210-CLAIMED-PROOF-IS-FALSE.md)
that had been rated the strongest result in a 110-problem range and dies at `n = 5`.

A gap that is written down is a task. A gap that is hidden behind a status label is a trap.

## License

Apache-2.0.
