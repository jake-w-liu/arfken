# Audit progress

Line-by-line audit of every exercise solution in `sections/` for
(1) mathematical correctness and (2) pedagogical completeness: a student
must be able to follow each solution step by step, with no missing
intermediate steps. The work is split into the parts listed below, and each
part is committed and pushed to `main` as soon as it is finished, so the
audit can be resumed from this file at any time.

## How to resume

Each part passes through three stages, recorded in its Status column:
`pending` → `audited` (audit committed) → `done` (independently verified,
confirmed findings applied, committed). The pre-audit text of every chapter
is commit `d04e67a`; diff a part against it to see what the audit changed.

1. `git pull origin main`, then take the next part that is not `done`.
   Work on at most one part per chapter file at a time.
2. **Audit** a `pending` part: check every exercise against the checklist
   below, editing only that exercise range of `sections/chNN.tex`; commit
   it as `audited` with a log entry.
3. **Verify** an `audited` part with three independent, read-only reviews:
   (a) every changed line of the audit diff, trying to refute each
   correction; (b) an independent re-solution of every exercise; (c) a
   student's line-by-line reading for missing steps. Apply the confirmed
   findings and commit the part as `done`, adding a verification note to
   its log entry.
4. Before each commit, compile the chapter on its own (the preamble of
   `main.tex`, the chapter's `\section` line, and
   `\input{sections/chNN.tex}`): no errors and no overfull boxes.
5. Rebuild `main.pdf` (`latexmk -pdf main.tex`) after every few completed
   chapters and at the end, and commit it.

A part is an inclusive range of exercise numbers; a subsection heading
belongs to the part that contains the first exercise after it.

## Checklist (applied to every exercise)

Reader: a student who has read the corresponding section of Arfken, Weber
& Harris (7th ed.) and works through the solution line by line.

1. **Statement.** Typos, garbled or missing mathematics, missing parts, and
   agreement with the solution and with any quoted answer (ANS.). Keep the
   textbook's wording; a change of meaning is marked with `\erratum{...}`
   and explained in the solution.
2. **Correctness.** Re-derive every step and result independently (SymPy,
   mpmath, NumPy for algebra, integrals, series, matrices, special
   functions, and numerical values). Fix wrong signs, factors, limits,
   indices, conditions, and conclusions. Every part (a), (b), ... is
   answered.
3. **No missing steps.** Each displayed line follows from the previous one
   by a step the reader can check mentally or with a line or two of scratch
   work. Where the text says "a short calculation gives", "clearly",
   "similarly", "one finds", "integrating by parts twice", etc., and the
   step is not immediate, show it: the substitution and new limits, the
   partial fractions, the integration by parts with its boundary terms, the
   residues, the recurrence or index shift, the matrix product, the limit.
   Name the theorem, identity, or equation used. Keep the existing style;
   do not pad trivial steps or rewrite clear, correct solutions.
4. **Reproducible numerics.** The repository has no helper scripts, so
   phrases such as "the supplementary script ... gives" are replaced by a
   description of the computation the reader can carry out (what is summed
   or integrated, the cutoff, the method), and every quoted number is
   re-verified.
5. **No production remarks.** Remarks about how this document was produced
   ("the transcription", "the supplied transcription", "has now been
   restored") are removed; a genuine discrepancy with the printed textbook
   is restated as such.
6. **Errata.** `\erratum{...}` (dark red) marks published errata and the
   corrections or qualifications established in the solutions, including
   new ones found in this audit, each with a one-sentence justification.
7. **LaTeX.** Only the packages and macros of `main.tex` (`\solution`,
   `\erratum`, `\PVint`); keep the exercise block structure
   (`\Needspace`, `\par\bigskip`, `\noindent\textbf{N.M.K}`, `\solution`).

## Parts

Progress: 0 of 54 parts done (audited and verified); 7 audited and awaiting verification.

`main.pdf` last rebuilt: before the audit.

| Part | Exercises | Status |
|---|---|---|
| ch01-p1 | 1.1.1–1.2.16 | audited |
| ch01-p2 | 1.3.1–1.7.11 | pending |
| ch01-p3 | 1.8.1–1.11.9 | pending |
| ch02-p1 | 2.1.1–2.2.34 | audited |
| ch02-p2 | 2.2.35–2.2.51 | pending |
| ch03-p1 | 3.2.1–3.5.13 | audited |
| ch03-p2 | 3.6.1–3.10.2 | pending |
| ch03-p3 | 3.10.3–3.10.37 | pending |
| ch04-p1 | 4.1.1–4.3.12 | audited |
| ch04-p2 | 4.4.1–4.7.3 | pending |
| ch05-p1 | 5.1.1–5.3.4 | audited |
| ch05-p2 | 5.4.1–5.7.3 | pending |
| ch06-p1 | 6.2.1–6.5.11 | audited |
| ch06-p2 | 6.5.12–6.5.21 | pending |
| ch07-p1 | 7.2.1–7.5.10 | pending |
| ch07-p2 | 7.5.11–7.8.4 | pending |
| ch08-p1 | 8.2.1–8.4.1 | pending |
| ch09-p1 | 9.2.1–9.7.4 | pending |
| ch10-p1 | 10.1.1–10.2.7 | pending |
| ch11-p1 | 11.2.1–11.6.11 | pending |
| ch11-p2 | 11.7.1–11.8.22 | pending |
| ch11-p3 | 11.8.23–11.10.7 | pending |
| ch12-p1 | 12.1.1–12.5.10 | audited |
| ch12-p2 | 12.6.1–12.8.8 | pending |
| ch13-p1 | 13.1.1–13.2.14 | pending |
| ch13-p2 | 13.2.15–13.4.8 | pending |
| ch13-p3 | 13.5.1–13.6.16 | pending |
| ch14-p1 | 14.1.1–14.1.28 | pending |
| ch14-p2 | 14.1.29–14.3.10 | pending |
| ch14-p3 | 14.4.1–14.5.16 | pending |
| ch14-p4 | 14.6.1–14.7.17 | pending |
| ch15-p1 | 15.1.1–15.2.19 | pending |
| ch15-p2 | 15.2.20–15.4.18 | pending |
| ch15-p3 | 15.4.19–15.6.4 | pending |
| ch16-p1 | 16.1.1–16.3.7 | pending |
| ch16-p2 | 16.3.8–16.4.6 | pending |
| ch17-p1 | 17.1.1–17.4.6 | pending |
| ch17-p2 | 17.5.1–17.9.2 | pending |
| ch18-p1 | 18.1.1–18.3.10 | pending |
| ch18-p2 | 18.4.1–18.4.28 | pending |
| ch18-p3 | 18.5.1–18.6.15 | pending |
| ch18-p4 | 18.6.16–18.8.6 | pending |
| ch19-p1 | 19.1.1–19.2.14 | pending |
| ch19-p2 | 19.2.15–19.3.3 | pending |
| ch20-p1 | 20.2.1–20.3.6 | pending |
| ch20-p2 | 20.4.1–20.7.8 | pending |
| ch20-p3 | 20.8.1–20.8.24 | pending |
| ch20-p4 | 20.9.1–20.10.13 | pending |
| ch21-p1 | 21.1.1–21.2.17 | pending |
| ch21-p2 | 21.3.1–21.4.8 | pending |
| ch22-p1 | 22.1.1–22.1.15 | pending |
| ch22-p2 | 22.2.1–22.4.11 | pending |
| ch23-p1 | 23.1.1–23.5.5 | pending |
| ch23-p2 | 23.6.1–23.7.4 | pending |

## Log of corrections

Each finished part adds an entry: the exercises whose mathematics was
corrected (and how), and a summary of the steps added and other cleanups.

- Setup: 15.2.22/15.2.23 were run together on one source line; separated.
- **ch01-p1** (1.1.1–1.2.16) — audit: no wrong results; a typo in 1.1.11(a) corrected ($[(\ln x)^2-1]/2$ → $[(\ln M)^2-1]/2$). Steps added in 31 of 32 exercises (e.g. the shifted $\alpha$-sums and error bound in 1.1.14, the assembly of 1.1.16(b), Gauss' test parameters in 1.2.5–1.2.7, the Lagrange remainder in 1.2.8). Script references in 1.1.3, 1.1.12, 1.1.16 replaced by the computations themselves; "the manual" → "the Instructor's Manual"; a reason added to the 1.2.7 erratum.
- **ch02-p1** (2.1.1–2.2.34) — audit: no mathematical errors found. Steps added in 22 exercises (e.g. the general elimination step and pivots of the Hilbert matrix in 2.1.5, an integer back substitution in 2.1.7, the $L_\pm$ algebra in 2.2.13, a derivation replacing a guess in 2.2.25, both orthogonal families in 2.2.29). The script reference in 2.1.5 replaced by a closed-form product; `\,10^{-n}` → `\times10^{-n}`; cross-references added; "the manual" → "the Instructor's Manual".
- **ch03-p1** (3.2.1–3.5.13) — audit: no wrong results; a misleading side remark in 3.2.6 (altitude described as adjacent side times the sine of the opposite angle) replaced by $h=A\sin\beta=B\sin\alpha$. Steps added in 31 exercises (e.g. every matrix–vector product in 3.3.4–3.3.5, the Euler-angle construction in 3.4.2, the passive-rotation argument in 3.4.5, the commutator in 3.5.12); part labels added; notation $\hat{\mathbf z}$ → $\hat{\mathbf e}_z$ in the 3.2.12 statement.
- **ch04-p1** (4.1.1–4.3.12) — audit: no mathematical errors found. Steps added in 23 exercises (e.g. the expansion of $B_{kilm}$ in 4.1.5, the polarization argument and a complex boost in 4.1.9, Jacobi's formula in 4.3.11). Cleanups: a comma in the 4.1.2 statement; the translation vector renamed $s^i$ in 4.1.7 (it clashed with a dummy index); a summed-index clash in 4.3.4.
- **ch05-p1** (5.1.1–5.3.4) — audit: no mathematical errors found. Steps added in all 24 exercises (e.g. both integrations by parts in 5.1.8, the Leibniz-rule norm in 5.2.1, the re-expansion of lower-degree terms in 5.3.4). The condition number in 5.1.3 is now computed from the eigenvalues instead of citing a deleted script; "the source" → "the textbook" in two notes.
- **ch06-p1** (6.2.1–6.5.11) — audit: no mathematical errors found. Steps added in 26 of 35 exercises (e.g. the first-row cofactor expansions and factorizations of the characteristic polynomials in 6.2.3–6.2.15 and the principal-axes substitution in 6.2.15, both determinant facts in 6.4.6, the simultaneous change of basis, $2\times2$ products and direct-product anticommutators in 6.5.7, the pairing of zero singular values in 6.5.11). Cleanups: "the original wording" in 6.5.10 restated as the textbook's condition $\lambda_i^*\ne\lambda_j$; a symbol clash in 6.5.7 ($a,d$ reused in $z=a+ib$, $w=c+id$) removed; cross-references to 6.2.7, 6.4.1, 6.5.6, 6.5.8 added.
- **ch12-p1** (12.1.1–12.5.10) — audit: no mathematical errors found. Steps added in all 29 exercises (e.g. the arc bounds, residue and negative-axis substitution in 12.4.3(b), Euler–Maclaurin on $[n,M]$ with the $1/n$ shift in 12.3.2, the derivation of the corrected intermediate identities in the 12.1.4 erratum, the cotangent series from the Bernoulli generating function in 12.2.3). Cleanups: the vague double-precision description in 12.3.2 replaced by the explicit computation ($H_{1000}$, $\ln1000$, rounding budget of the $4.5\times10^{-16}$ discrepancy), all numbers re-verified; "it is restored above" (12.3.2) restated as a textbook erratum; "the source's" → "the textbook's" (12.1.4); undefined $R^{\rm bound}$ notation in 12.4.6–12.4.7 replaced by the explicit bounds $2^{-24}\zeta(25)$ and $\frac{32}{15}4^{-14}\zeta(14)$.
