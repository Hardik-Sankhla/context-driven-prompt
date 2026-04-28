# Prompt Library — Overview

This file documents the prompt collection under `prompts/education/` and explains conventions, usage, and enforcement rules for the available master prompts.

## Prompts included

- [prompts/education/microprocessor/mp-generate-solutions-prompt.md](prompts/education/microprocessor/mp-generate-solutions-prompt.md) — Microprocessor Solution Prompt Guide (8085 & 8051). Enforces: exam-structured LaTeX solutions, mandatory diagrams/waveforms for hardware/timing/interfacing questions, CO/unit mapping, 4-phase workflow (decoding → solve → examiner review → LaTeX cleanup).

- [prompts/education/discrete-mathematics/dm-generate-solutions-prompt.md](prompts/education/discrete-mathematics/dm-generate-solutions-prompt.md) — Discrete Mathematics Solution Prompt Guide. Enforces: LaTeX math, mandatory diagrams (Hasse, graphs, trees, Venn), marks-based depth rules, 4-phase workflow and strict examiner review.

- [prompts/education/theory-of-computation/toc-master-prompt.md](prompts/education/theory-of-computation/toc-master-prompt.md) — Theory of Computation FINAL MASTER PROMPT. Enforces: full LaTeX output, formal models (tuples/grammars/TM definitions), mandatory TikZ/ASCII diagrams for automata, CO/unit mapping, marks-based answer structure, 4-phase workflow and LaTeX validation.

## Common conventions and rules (applies to all master prompts)

- All final output must be a clean, compilable LaTeX document.
- Every answer must include unit and course-outcome tags (e.g., `[Unit 2 | CO2]`).
- Diagrams are mandatory where the topic requires structure (automata, timing waveforms, Hasse diagrams, graphs, interfacing blocks, etc.). Text-only answers are not acceptable for such questions.
- Marks-driven depth: 2-mark → short definition; 4-mark → concept + steps (+ diagram if applicable); 10-mark → full theory, derivation/proof, diagrams, and final boxed conclusion.
- Four-phase workflow required for every paper: 1) Paper decoding (preserve wording/numbering and produce LaTeX-ready text), 2) Exam-quality solutions (full steps + diagrams), 3) Examiner review (audit and expand weak answers), 4) LaTeX & technical correction (compile-ready formatting).
- Strict prohibitions: do not skip steps, do not compress proofs, do not omit formal definitions or diagrams. If required items are missing the answer is considered WRONG and must be rewritten.

## Recommended authoring workflow for using these prompts

1. Use the prompt to decode the uploaded paper to a LaTeX-ready question list.
2. Produce solutions following the marks-based template and include diagrams (TikZ preferred) or ASCII blocks inside LaTeX verbatim environments.
3. Run the examiner-review pass: validate marks-depth, diagrams present and correct, and add any missing intermediate steps.
4. Run LaTeX cleanup: ensure environments (`align`, `array`, `tabular`, `verbatim`/`lstlisting`) are used appropriately and output compiles.
5. Provide a short postamble: important topics, pattern analysis, repeated concepts, and study strategy.

## Adding new prompts

- Place new domain prompts at `prompts/<domain>/<topic>/<name>.md`.
- Follow the same 4-phase structure and clearly document the course context, unit map, and CO mapping in the prompt header.
- Include example ASCII or LaTeX diagram styles as a template within the prompt.

## Notes

- This overview does not modify any master prompt text — it only documents their purpose and usage. Each master prompt file itself remains authoritative for exact enforcement text.

---

If you want, I can:
- add this overview to the top-level `prompts/README.md`, or
- generate a one-page printable PDF of this overview, or
- run a quick LaTeX compile check on a sample converted paper.

Which would you like next?