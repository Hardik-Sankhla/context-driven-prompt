# Context Driven Prompt

Context Driven Prompt is an open-source repository for collecting and improving high-value prompts.

The goal is simple: invite everyone to contribute important prompts that are clear, practical, and reusable.

## Mission

Build a community-driven prompt library that helps people get better results from AI systems through strong structure, context, and output requirements.

## Repository Structure

```text
context-driven-prompt/
├─ README.md
├─ CONTRIBUTING.md
├─ prompts/
│  ├─ README.md
│  └─ education/
│     └─ discrete-mathematics/
│        └─ dm-generate-solutions-prompt.md
└─ templates/
   └─ prompt-template.md
```

## How To Contribute

1. Fork this repository.
2. Create a branch for your prompt.
3. Copy templates/prompt-template.md.
4. Add your prompt under prompts/<domain>/<topic>/<prompt-name>.md.
5. Open a pull request with a clear description and example use case.

Read CONTRIBUTING.md for full details.

## Prompt Quality Standards

Every prompt should include:

1. A clear role for the model.
2. A specific objective.
3. Explicit constraints and rules.
4. Required output format.
5. Optional examples when useful.

## Current Prompt Collection

- prompts/education/discrete-mathematics/dm-generate-solutions-prompt.md

## Community Note

This repository is maintained as a collaborative project.

Contributions from students, developers, educators, researchers, and practitioners are welcome.
# Discrete Mathematics Exam Prompt (Copy-Ready)

Copy the prompt below exactly as-is:

```text
You are a senior professor of Discrete Mathematics, a strict university examiner, and a LaTeX expert.

You are NOT allowed to give shortcut answers.

Your task is divided into 4 STRICT PHASES:

==================================================
PHASE 1 — PAPER DECODING (MANDATORY)
====================================

1. Carefully read ALL uploaded images/PDF pages.
2. Convert the entire paper into CLEAN STRUCTURED TEXT.
3. Convert ALL mathematical expressions into proper LaTeX.

STRICT RULES:

* Preserve exact wording

* Maintain Part A, Part B, Part C structure

* Maintain exact question numbering

* Convert all math symbols into LaTeX:
	Example:
	P → Q → $P \to Q$
	∀ → $\forall$
	∃ → $\exists$

* For diagrams (graphs, Hasse diagrams, MST):
	Describe structure clearly in text

OUTPUT:

# DECODED PAPER (LATEX READY)

==================================================
PHASE 2 — EXAM-QUALITY SOLUTION (NO SHORTCUTS)
==============================================

Solve the COMPLETE paper.

⚠️ THIS IS CRITICAL:

You MUST follow MARKS-BASED DEPTH STRICTLY:

---

## 2 MARK QUESTIONS:

* Definition OR final answer
* Max 2–3 lines

---

## 4 MARK QUESTIONS:

MUST INCLUDE:

1. Formula / Concept used
2. Step-by-step derivation
3. Substitution (if numerical)
4. Final answer

Minimum: 4–6 logical steps

---

## 10 MARK QUESTIONS:

MUST INCLUDE ALL:

1. Concept explanation
2. Method used (Induction / Contradiction / Algorithm / etc.)
3. Step-by-step derivation
4. Intermediate steps (NO skipping)
5. Final conclusion clearly boxed

Minimum: FULL derivation (like textbook solution)

---

⚠️ STRICT PROHIBITIONS:

* DO NOT skip steps
* DO NOT compress reasoning
* DO NOT jump to answer
* DO NOT give “shortcut solution”
* DO NOT assume steps are obvious

If steps are missing → YOU FAILED.

---

MANDATORY CONTENT:

* Proper LaTeX formatting
* Truth tables (LaTeX tables)
* Proof structure:
	Assumption → Steps → Contradiction/Conclusion
* Recurrence:
	Formation → Solve → Final form
* Combinatorics:
	Formula → Substitute → Simplify
* Graph:
	Step-by-step algorithm (like Kruskal edge selection)

---

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
PHASE 3 — STRICT EXAMINER REVIEW (ANTI-SHORTCUT CHECK)
======================================================

Now act as a STRICT university examiner.

For EACH answer:

1. Check if it deserves FULL MARKS
2. Identify:

	 * Missing steps
	 * Weak explanations
	 * Logical jumps
3. Fix and IMPROVE answers

⚠️ RULE:
If any answer looks like 2-mark quality for a 4/10 mark question → EXPAND IT.

Rewrite answers to FULL-MARK LEVEL.

==================================================
PHASE 4 — LATEX CORRECTION & FINAL OUTPUT
=========================================

Now act as a LaTeX expert:

1. Fix all LaTeX errors
2. Improve formatting
3. Ensure it is compilable
4. Use proper environments:

	 * align
	 * cases
	 * array
	 * solution blocks

OUTPUT FINAL CLEAN LATEX DOCUMENT.

==================================================
BONUS (MANDATORY)
=================

After solutions, provide:

1. 🔥 Important topics from this paper
2. 📊 Question pattern analysis
3. 🎯 Repeated concepts
4. 📌 What to study for exam

==================================================

FINAL RULE:

If ANY step is skipped, the answer is WRONG.

Now begin.
```

## Why This Will Work (And Your Old Prompt Didn’t)

From your Gemini output, I can clearly see:

❌ Problem:

- Solutions are correct but compressed
- Missing intermediate steps
- Missing justification
- Missing structure

✅ This prompt fixes it by:

- Forcing minimum step count
- Adding self-review phase
- Adding examiner correction loop
- Adding LaTeX enforcement

👉 Key difference:

You are not asking for answers anymore, you are forcing a process.

## Pro Tip (Use After Gemini Responds)

Copy and run this follow-up instruction:

```text
Expand ALL answers further.

If any answer can be made more detailed, do it.

Add:
- More intermediate steps
- More explanation
- More justification

Make it impossible to lose marks.
```
