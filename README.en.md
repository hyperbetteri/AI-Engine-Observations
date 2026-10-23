**Language:** [Magyar](README.md) | [English](README.en.md)

# AI Engine Observations

**Almási Andor** — long-term, day-to-day work with large language models ("engines"): how they behave, where and how they fail, and how this can be observed and measured fairly.

## What is this repository about?

This collection is neither code nor a prompt pack. It contains observations, failure patterns and measurement principles that grew out of several years of hands-on work with multiple engines (OpenAI, Anthropic, Google and offline models).

It centres on three questions:

1. **What should an AI system remember, and what should it not?** — memory hygiene in long-term collaboration.
2. **What recurring failure patterns do the engines show?** — documented cases, each with a check question.
3. **How can the behaviour of engines be measured fairly?** — pre-registration, blinding, repetition.

## Contents

| # | Document | In brief |
|---|---|---|
| 01 | [AI memory hygiene and multi-engine control](01_AI_memoriahigienia_es_tobbmotoros_kontroll.en.md) | Memory is an operating compass, not a knowledge base. A layered model for long-term human–AI work. |
| 02 | [Failure-pattern register](02_Hibaminta_regiszter.en.md) | Six documented failure patterns (e.g. downgrading without searching, drift without evidence, confabulation), each with a check question. |
| 03 | [Behaviour-measurement method (CBDI)](03_Viselkedesmeresi_modszer_CBDI.en.md) | How to measure whether the same engine behaves differently in different situations — and what counts as a real result. |
| 04 | [Digital Nanny – project overview](04_Digitalis_Dajka_projektismerteto.en.md) | Concept: turning a child's phone from a passive attention-holder into an adaptive learning and safety companion. |

## What is not included — on purpose

The documents present the principles, the problem statement and the results. They do **not** contain executable internal prompts, boot packages, source code, thresholds, concrete test items, personal data or project-sensitive details. The reason is not secrecy but risk management: detailed operational material can be misunderstood or wrongly reused without its context.

## Related

- Portfolio and validation evidence: [AI-Workflow-Validation-Portfolio](https://github.com/hyperbetteri/AI-Workflow-Validation-Portfolio)
- Engineering case studies: [Engineering-Case-Studies](https://github.com/hyperbetteri/Engineering-Case-Studies)
- Legal AI framework (overview): [LEGAL-RQV-Overview](https://github.com/hyperbetteri/LEGAL-RQV-Overview)
- Lunar recycling concept studies: [Lunar-Recycling-and-Terminator-Lab](https://github.com/hyperbetteri/Lunar-Recycling-and-Terminator-Lab)

---

© 2026 Almási Andor. All rights reserved. Quotation with attribution is welcome.
