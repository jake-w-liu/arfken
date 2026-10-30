# Audit progress

Line-by-line audit of every exercise solution in `sections/` for
(1) mathematical correctness and (2) pedagogical completeness: a student
must be able to follow each solution step by step, with no missing
intermediate steps. The work is split into the parts listed below, and each
part is committed and pushed to `main` as soon as it is finished, so the
audit can be resumed from this file at any time.

## How to resume

1. `git pull origin main`, then take the next `pending` part(s) from the
   table below. Work on at most one part per chapter file at a time.
2. Audit every exercise of the part with the checklist below, editing only
   that exercise range of `sections/chNN.tex`.
3. Compile the chapter on its own (the preamble of `main.tex`, the
   chapter's `\section` line, and `\input{sections/chNN.tex}`); it must
   give no errors and no overfull boxes.
4. Mark the part `done` in the table, add its corrections to the log at the
   end of this file, commit `sections/chNN.tex` together with this file,
   and push to `main`.
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

Progress: 0 of 54 parts done. `main.pdf` last rebuilt: before the audit.

| Part | Exercises | Status |
|---|---|---|
| ch01-p1 | 1.1.1–1.2.16 | pending |
| ch01-p2 | 1.3.1–1.7.11 | pending |
| ch01-p3 | 1.8.1–1.11.9 | pending |
| ch02-p1 | 2.1.1–2.2.34 | pending |
| ch02-p2 | 2.2.35–2.2.51 | pending |
| ch03-p1 | 3.2.1–3.5.13 | pending |
| ch03-p2 | 3.6.1–3.10.2 | pending |
| ch03-p3 | 3.10.3–3.10.37 | pending |
| ch04-p1 | 4.1.1–4.3.12 | pending |
| ch04-p2 | 4.4.1–4.7.3 | pending |
| ch05-p1 | 5.1.1–5.3.4 | pending |
| ch05-p2 | 5.4.1–5.7.3 | pending |
| ch06-p1 | 6.2.1–6.5.11 | pending |
| ch06-p2 | 6.5.12–6.5.21 | pending |
| ch07-p1 | 7.2.1–7.5.10 | pending |
| ch07-p2 | 7.5.11–7.8.4 | pending |
| ch08-p1 | 8.2.1–8.4.1 | pending |
| ch09-p1 | 9.2.1–9.7.4 | pending |
| ch10-p1 | 10.1.1–10.2.7 | pending |
| ch11-p1 | 11.2.1–11.6.11 | pending |
| ch11-p2 | 11.7.1–11.8.22 | pending |
| ch11-p3 | 11.8.23–11.10.7 | pending |
| ch12-p1 | 12.1.1–12.5.10 | pending |
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
