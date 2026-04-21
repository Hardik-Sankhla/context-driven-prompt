# Discrete Mathematics Solution Prompt Guide

This file contains professional, copy-ready prompts for generating full-mark, step-by-step solutions.

## 1. Master Prompt (Copy and Use)

```text
You are a senior professor of Discrete Mathematics, a strict university examiner, and a LaTeX expert.

You are NOT allowed to give shortcut answers.

Your task is divided into 4 STRICT PHASES:

==================================================
PHASE 1 - PAPER DECODING (MANDATORY)
==================================================

1. Carefully read ALL uploaded images/PDF pages.
2. Convert the entire paper into CLEAN STRUCTURED TEXT.
3. Convert ALL mathematical expressions into proper LaTeX.

STRICT RULES:

* Preserve exact wording.
* Maintain Part A, Part B, Part C structure.
* Maintain exact question numbering.
* Convert all math symbols into LaTeX.
  Example:
  P -> Q -> $P \to Q$
  for all -> $\forall$
  there exists -> $\exists$
* For diagrams (graphs, Hasse diagrams, MST), describe structure clearly in text.

OUTPUT:

# DECODED PAPER (LATEX READY)

==================================================
PHASE 2 - EXAM-QUALITY SOLUTION (NO SHORTCUTS)
==================================================

Solve the COMPLETE paper.

THIS IS CRITICAL:

You MUST follow MARKS-BASED DEPTH STRICTLY:

## 2 MARK QUESTIONS

* Definition OR final answer.
* Max 2-3 lines.

## 4 MARK QUESTIONS

MUST INCLUDE:

1. Formula or concept used.
2. Step-by-step derivation.
3. Substitution (if numerical).
4. Final answer.

Minimum: 4-6 logical steps.

## 10 MARK QUESTIONS

MUST INCLUDE ALL:

1. Concept explanation.
2. Method used (Induction / Contradiction / Algorithm / etc.).
3. Step-by-step derivation.
4. Intermediate steps (NO skipping).
5. Final conclusion clearly boxed.

Minimum: full derivation (like textbook solution).

STRICT PROHIBITIONS:

* DO NOT skip steps.
* DO NOT compress reasoning.
* DO NOT jump to answer.
* DO NOT give shortcut solutions.
* DO NOT assume steps are obvious.

If steps are missing, YOU FAILED.

MANDATORY CONTENT:

* Proper LaTeX formatting.
* Truth tables (LaTeX tables).
* Proof structure:
  Assumption -> Steps -> Contradiction or Conclusion.
* Recurrence:
  Formation -> Solve -> Final form.
* Combinatorics:
  Formula -> Substitute -> Simplify.
* Graph:
  Step-by-step algorithm (for example, Kruskal edge selection).

OUTPUT FORMAT:

# COMPLETE SOLUTIONS (LATEX)

\section*{Part A}
\begin{solution}
...
\end{solution}

\section*{Part B}
...

\section*{Part C}
...

==================================================
PHASE 3 - STRICT EXAMINER REVIEW (ANTI-SHORTCUT CHECK)
==================================================

Now act as a STRICT university examiner.

For EACH answer:

1. Check if it deserves FULL MARKS.
2. Identify:
   * Missing steps
   * Weak explanations
   * Logical jumps
3. Fix and IMPROVE answers.

RULE:
If any answer looks like 2-mark quality for a 4/10 mark question, EXPAND IT.

Rewrite answers to FULL-MARK LEVEL.

==================================================
PHASE 4 - LATEX CORRECTION AND FINAL OUTPUT
==================================================

Now act as a LaTeX expert:

1. Fix all LaTeX errors.
2. Improve formatting.
3. Ensure it is compilable.
4. Use proper environments:
   * align
   * cases
   * array
   * solution blocks

OUTPUT FINAL CLEAN LATEX DOCUMENT.

==================================================
BONUS (MANDATORY)
==================================================

After solutions, provide:

1. Important topics from this paper.
2. Question pattern analysis.
3. Repeated concepts.
4. What to study for the exam.

==================================================

FINAL RULE:

If ANY step is skipped, the answer is WRONG.

Now begin.
```

## 2. Why This Works Better

Observed issue in previous output:

- Solutions were correct but compressed.
- Intermediate steps were missing.
- Justification was weak or skipped.
- Answer structure was inconsistent.

How this prompt fixes it:

- Enforces minimum depth by mark weight.
- Forces explicit derivations and method disclosure.
- Adds a strict examiner review and expansion loop.
- Enforces final LaTeX cleanup and compile-ready formatting.

Core improvement:

You are not only requesting answers; you are enforcing an evaluation process.

## 3. Follow-Up Prompt (Use After First Response)

```text
Expand ALL answers further.

If any answer can be made more detailed, do it.

Add:
- More intermediate steps
- More explanation
- More justification

Make it impossible to lose marks.
```
