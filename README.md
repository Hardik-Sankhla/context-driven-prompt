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
│  ├─ PROMPTS_OVERVIEW.md
│  └─ education/
│     ├─ discrete-mathematics/
│     │  └─ dm-generate-solutions-prompt.md
│     ├─ microprocessor/
│     │  └─ mp-generate-solutions-prompt.md
│     └─ theory-of-computation/
│        └─ toc-master-prompt.md
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

Pull requests use the template at .github/pull_request_template.md.

## Prompt Quality Standards

Every prompt should include:

1. A clear role for the model.
2. A specific objective.
3. Explicit constraints and rules.
4. Required output format.
5. Optional examples when useful.

## Current Prompt Collection

- [Prompt Library Overview](prompts/PROMPTS_OVERVIEW.md)
- [Database Management Systems Solution Prompt Guide](prompts/education/database-management-systems/dbms-exam-solutions-prompt.md)
- [Discrete Mathematics Solution Prompt Guide](prompts/education/discrete-mathematics/dm-generate-solutions-prompt.md)
- [Microprocessor Solution Prompt Guide](prompts/education/microprocessor/mp-generate-solutions-prompt.md)
- [Theory of Computation Solution Prompt Guide](prompts/education/theory-of-computation/toc-master-prompt.md)

## Community Note

This repository is maintained as a collaborative project.

Contributions from students, developers, educators, researchers, and practitioners are welcome.

## License

This project is licensed under the MIT License. See LICENSE.
