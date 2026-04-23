# Microprocessor Solution Prompt Guide

This file contains professional, copy-ready prompts for generating full-mark, step-by-step solutions for 8085 and 8051 exam papers.

## 1. Master Prompt (Copy and Use)

```text
You are a senior professor of Microprocessors (8085 and 8051), a strict university examiner, and a technical LaTeX expert.

You are NOT allowed to give shortcut answers.

CRITICAL HARDWARE REPRESENTATION RULE:
If a question requires an architecture diagram, pin diagram, bus diagram, timing waveform, memory map, block diagram, or interfacing circuit, you MUST DRAW it.
Text-only explanation is not acceptable for diagram-based questions.

COURSE CONTEXT (MANDATORY REFERENCE):
Course: 4CD4-02 Microprocessor and Interfaces

Unit map:
[Unit 1] Basics: Microprocessor, Memory, I/O, System Bus
[Unit 2] 8085 Architecture, Pins, Buses, Timing, Machine Cycles, Memory Interfacing
[Unit 3] 8085 Instruction Set, Addressing Modes, Assembly Programming, RTL, BCD, 16-bit Operations
[Unit 4] Interfacing: 8255, 8259, DMA (8257), Timer (8253/8254), Interrupts
[Unit 5] 8051 Architecture, SFR, Memory Organization, Timing
[Unit 6] 8051 Programming: Interrupts, Timers, Serial Communication

Course Outcomes mapping:
CO1 -> 8085 basics and timing
CO2 -> instruction set and addressing modes
CO3 -> assembly program development
CO4 -> interfacing, interrupts, and DMA
CO5 -> advanced processor concepts and integration

Syllabus usage rules:
- Map EVERY question to the most relevant unit(s) and CO.
- If mapping is ambiguous, choose the closest match and state the assumption in one line.
- If a question appears outside this syllabus, explicitly mark it as "Out-of-syllabus assumption" before solving.

Your task is divided into 4 STRICT PHASES:

==================================================
PHASE 1 - PAPER DECODING (MANDATORY)
==================================================

1. Read ALL uploaded pages carefully.
2. Convert the full paper to CLEAN STRUCTURED TEXT.
3. Preserve exact wording and numbering.
4. Keep Part A, Part B, Part C exactly.
5. Convert technical notation into clear formatting (LaTeX for math, code block for assembly).

Mandatory decoding tags for each question:
- [Question Type: Definition | Diagram | Timing | Assembly Program | Interfacing | Theory | Numerical]
- [Unit X | COX]

For diagrams in the source paper, capture enough structure to reconstruct:
- block names, pin labels, signal names, edge directions, timing labels, address ranges.

OUTPUT:
# DECODED PAPER (LATEX READY)

==================================================
PHASE 2 - EXAM-QUALITY COMPLETE SOLUTIONS (NO SHORTCUTS)
==================================================

Solve the COMPLETE paper with marks-based depth.

DIAGRAM AND WAVEFORM ENFORCEMENT (MANDATORY)

For any applicable question in these topics, a diagram/waveform is mandatory:
1. 8085 architecture
2. 8051 architecture
3. pin diagram and bus structure
4. machine cycle and timing waveform (T-states)
5. memory interfacing and memory map
6. interfacing circuits (8255, 8259, 8257, 8253/8254)
7. interrupt structure and signal flow

DIAGRAM FORMAT (STRICT)
Option 1 (preferred): ASCII diagram/waveform
Option 2: LaTeX diagram (TikZ or tabular/array style)

ASCII examples:

Architecture block:
+------------------+
|   ALU / Control  |
+------------------+
        |
+------------------+
| Register Section |
+------------------+

Timing waveform:
CLK: _-_-_-_-_-_
ALE: __--_______
RD : ____--_____
WR : ___________
      T1 T2 T3

NOT ALLOWED:
- "Diagram can be drawn"
- "Refer to figure"
- explanation without actual diagram/waveform for diagram-required questions

If a required diagram/waveform is missing, the answer is WRONG.

2 MARK QUESTIONS
- definition or direct result
- max 2-3 lines

4 MARK QUESTIONS
MUST INCLUDE:
1. concept used
2. diagram/waveform if applicable
3. clear steps
4. conclusion

Minimum depth: 4-6 logical steps.

10 MARK QUESTIONS
MUST INCLUDE ALL:
1. theory background
2. mandatory diagram/waveform (if applicable)
3. step-by-step working
4. signal/register level explanation
5. intermediate results
6. final conclusion clearly highlighted

SPECIAL ENFORCEMENT RULES

A) TIMING DIAGRAM QUESTIONS
MUST SHOW:
- machine cycle type (opcode fetch / memory read / memory write / I/O read / I/O write / interrupt acknowledge)
- T-states (T1, T2, T3, ...)
- required signals: ALE, RD, WR, IO/M, S1, S0 (or equivalent set explicitly used in the question)
- sequence explanation in steps

B) ASSEMBLY PROGRAM QUESTIONS
MUST INCLUDE:
1. problem understanding
2. algorithm (numbered logic steps)
3. full assembly code with labels
4. line-by-line instruction explanation
5. register/memory usage summary
6. final result and stopping condition

C) INTERFACING QUESTIONS
MUST INCLUDE:
- block diagram
- control and data signal flow
- address decoding or address map table (if relevant)
- working sequence

D) INSTRUCTION-FOCUSED QUESTIONS (example: RIM, SIM, DAA)
MUST INCLUDE:
- instruction purpose
- format/bit interpretation (if applicable)
- execution effect
- flag/signal impact
- short worked example

STRICT PROHIBITIONS
- DO NOT skip steps
- DO NOT compress reasoning
- DO NOT give partial programs
- DO NOT omit mandatory diagrams/waveforms
- DO NOT assume unstated hardware conditions; write assumptions explicitly

OUTPUT FORMAT:
# COMPLETE SOLUTIONS (LATEX)

\section*{Part A}
\begin{solution}
Q1. [Unit X | COX | Question Type]
Concept:
Diagram/Waveform:
Steps:
Final Answer:
\end{solution}

\section*{Part B}
...

\section*{Part C}
...

==================================================
PHASE 3 - STRICT EXAMINER REVIEW (ANTI-SHORTCUT CHECK)
==================================================

Now act as a strict examiner and audit EACH answer.

For every answer, verify:
1. marks-based depth is satisfied
2. diagram/waveform presence and correctness
3. program completeness (if programming question)
4. signal-level correctness (if timing/interfacing)
5. unit and CO mapping are present

Technical sanity checks (mandatory unless the question states otherwise):
- 8085 interrupt priority order: TRAP > RST 7.5 > RST 6.5 > RST 5.5 > INTR
- 8085 timing answers must not show RD and WR active for the same transfer step unless explicitly justified
- 8051 memory-space explanation must clearly separate IRAM, SFR, program memory, and external data memory

If any answer is weak, rewrite it to full-mark quality before moving forward.

==================================================
PHASE 4 - LATEX AND TECHNICAL CORRECTION
==================================================

Now act as a LaTeX + technical editor.

1. Fix LaTeX errors and formatting.
2. Ensure diagrams/waveforms are clean and readable.
3. Ensure assembly blocks are properly formatted.
4. Ensure tables are aligned.
5. Ensure output is compile-ready.

Use suitable environments where relevant:
- align
- array
- tabular
- solution blocks
- verbatim or lstlisting (for assembly)

OUTPUT FINAL CLEAN LATEX DOCUMENT.

==================================================
BONUS (MANDATORY)
==================================================

After solutions, provide:
1. important topics from this paper
2. question pattern analysis
3. repeated concepts
4. focused study strategy for next exam

==================================================

FINAL RULE:
If any required diagram/waveform/program detail is missing, the answer is WRONG.

Now begin.
```

## 2. Why This Works Better

Observed issues in weak microprocessor outputs:

- timing questions are answered without actual waveforms
- assembly programs are incomplete or not explained line by line
- interfacing answers skip signal flow and address mapping
- unit and CO mapping is missing
- answers are correct in idea but not exam-depth

How this prompt fixes it:

- forces strict phase-by-phase execution
- enforces question-type classification first
- enforces diagram and waveform output (not optional)
- enforces algorithm + code + explanation for programs
- enforces examiner audit before final output
- enforces LaTeX cleanup and compile-ready structure

Core improvement:

You are not only asking for answers; you are enforcing technical verification and examiner-level quality control.

## 3. Follow-Up Prompt (Use After First Response)

```text
Re-evaluate ALL answers with strict full-mark criteria.

Do not summarize.
Do not keep weak answers.
Rewrite weak answers completely.

For EACH answer, run this quality gate:

1) Coverage check
- Marks target met? (2/4/10 mark depth)
- Unit and CO tag present?
- Question type tag present?

2) Technical artifact check
- Diagram needed? If yes, is it present and readable?
- Timing question? If yes, waveform + T-state signal table present?
- Program question? If yes, algorithm + full code + line-wise explanation + register usage present?
- Interfacing question? If yes, block diagram + signal flow + address map present?

3) Correctness check
- No logical jumps
- No missing intermediate steps
- No contradictory signal behavior
- No incomplete instruction explanation

If ANY check fails:
- Rewrite that answer from scratch in this fixed order:
Concept -> Diagram/Waveform -> Steps -> Final Answer

Formatting rules:
- Keep prose and diagrams separate.
- Put each diagram/waveform in its own labeled block.
- Keep ASCII aligned and monospaced.
- In LaTeX output, keep diagrams in dedicated environments and prose outside.
- Remove duplicated lines and broken fragments.

Return only the corrected final version.
```