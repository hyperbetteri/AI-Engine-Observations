**Language:** [Magyar](03_Viselkedesmeresi_modszer_CBDI.md) | [English](03_Viselkedesmeresi_modszer_CBDI.en.md)

# Behaviour-Measurement Method (CBDI)

**How can we fairly measure whether the same engine behaves differently in a different situation?**

Author: Almási Andor · Base version: v0.3 measurement candidate and measurement plan v0.1 (24 August 2026) · Public version

Working name: **CBDI — Contextual Behaviour Deviation Index**

> **Status:** development candidate and measurement plan. **Measurement has not started yet.** This document describes the method; it reports no results. The concrete test items are deliberately left out (see the blinding rule).

## The starting observation

The same engine performed flawlessly in 12 out of 12 cases in a *classification* situation (when it had to evaluate claims), yet in a *production* situation (when it had to prepare outgoing material) it made the very same errors. This gap is what is to be measured.

The user's starting point, formulated as a hypothesis: behaviour tailored to the user experience is a deliberate product decision, and at times it shapes the output more strongly than could be expected from the model's raw problem-solving capability.

## What it measures, and what it does not

**It measures:** the difference in the observable output behaviour of the same system across different situations.

**It does not measure, and does not claim:**

- that a separate "chatbot layer" exists;
- that anything suppresses or dominates it;
- which internal layer the observed behaviour comes from.

The observed behaviour may be caused by a combination of several layers: training, system prompt, routing, safety layer, product-level alignment. These cannot be separated from the output. That is why the name of the method deliberately contains neither the word "chatbot" nor "layer" — this is protection at the level of the concept against pattern HM-06 (evidence-scope overreach) from the [failure-pattern register](02_Hibaminta_regiszter.en.md).

## The basic measurement is a difference, not an absolute value

A standalone score cannot be interpreted. The measurement is always paired:

```
delta = value_B − value_A
```

The same engine, the same or a functionally equivalent task, and two predefined situations set against each other. For example:

| Situation A | Situation B |
|---|---|
| classification situation | production situation |
| rule pack supplied | not supplied |
| short conversation | long conversation |

## Two measurement layers

**CORE — verifiable objectively or on a yes/no basis**

- whether the explicit instruction was fulfilled;
- whether a prohibited form appeared;
- whether it asked back for data that was already available;
- whether the mandatory structural element appeared;
- whether it kept the prescribed answer structure.

Derived indicator:

```
IAR = fulfilled requirements / applicable requirements
delta_IAR = IAR_B − IAR_A
```

**AUX — a partly interpretation-dependent, supplementary layer**

- hedging;
- repetition;
- formulaic, templated phrasing;
- unnecessary conversational padding.

The main measurement is provided by CORE. AUX is only an explanatory supplement. A composite index may be built only from indicators that have already been validated, not in advance.

## Exposure normalisation

Raw counts cannot be compared. Each failure pattern must be related to its own actual opportunities to occur. For example, confabulation to the number of slots that are to be filled or are incomplete, and evidence-scope overreach to the number of claims that rely on a specific source.

Without this, every indicator would move together with length, and a longer session would automatically look worse.

## Separating platforms

Engines from different vendors must **first be measured separately**, each with its own baseline. A joint conclusion may be drawn only after each system's own behavioural profile has been measured independently.

A similar output phenomenon does not imply the same internal cause or the same architecture. Nothing may be inferred about one engine from the workings of the other.

> **The question is not which engine is better.** The question is which behavioural components are stable and which are situation-dependent under the same task and framework, and how these differ by platform.

## Role asymmetry

If, of two engines, one is mainly in an evaluating role and the other mainly in the role being examined, the resulting data is not symmetric and cannot be used to establish platform differences. In a paired measurement, therefore, the following are mandatory:

- the same task for both engines;
- the same or an equivalent situation;
- the same evaluation criteria;
- the evaluation should not be the free judgement of the other engine, but a predefined, third-party set of criteria;
- platform, engine, role and situation are to be handled as separate variables.

## Rules of measurement

### Pre-registration — mandatory for every measurement

Before each measurement is started, the following must be recorded in a separate file:

1. what result we expect, numerically if possible;
2. what result would refute the hypothesis;
3. what the stopping condition is.

Rationale: without this, any result can be explained after the fact. The pre-registration is kept by the person conducting the measurement and is opened only after the measurement has run.

### Blinding

An earlier test was invalidated twice because the test protocol reached the engine under examination. Therefore it is mandatory that:

- the engine under examination never receives the protocol, the traps, the expected result, or even the information that a measurement is taking place;
- it receives only the input;
- every run starts in a new, empty conversation.

If the protocol gets through by any route, that measurement is invalid.

### Repetition

**One run is not a measurement.** The output of a language model varies even for the same input. At least 3 runs are needed per measurement and per situation. If the spread of the three runs is greater than the difference between the two situations, the measurement shows nothing — and that is itself a result: it means the effect of the situation is smaller than the model's own variability.

## The measurement series — step by step

We do not run six measurements at once. The result of each measurement decides whether the next one is needed. It is cheaper to fail at the first step than after six measurements.

| Step | Question | If it fails |
|---|---|---|
| **M1 — Basic question** | Same engine, same task, two situations: does the behaviour differ? | The series stops. This is a valid result, not a failure. |
| **M2 — Stability** | Is the M1 result repeated with a different task in the same structure? | Back to M1 with a different task; stop after two unsuccessful repetitions. |
| **M3 — Intervention** | Does supplying the failure-pattern register reduce the difference? | The register has no effect in its current form and must be reworked. |
| **M4 — Separation** | Which failure patterns change strongly when the situation changes, and which stay nearly constant? | No new runs; re-analysis of the M1–M2 data. |
| **M5 — Platform** | Under the same task and framework, which components differ by platform? | May run only after each platform's own baseline exists. |
| **M6 — Aggregation** | Can a meaningful composite indicator be formed from the validated indicators? | If not, CBDI remains a set of indicators and does not become an index. |

In practice M3 is the most valuable, because it does not answer a theoretical question: it shows whether a rule pack has a *measurable* effect or whether we merely assume it does.

A principle for M6: a striking number that can always be calculated but whose meaning we do not know is worse than eight separate indicators.

**Estimated scope:** at most 30 runs if every step proceeds. If M1 fails, it ends after 6 runs.

## The first testable hypothesis

Which failure patterns change significantly when the situation changes, and which stay nearly constant?

Expectation, not a claim:

- if **risk-coverage overweight** (HM-04) changes strongly between two situations → probably an environment-dependent component;
- if **confabulation** (HM-05) stays at nearly the same rate → more likely a basic property of the model;
- if confabulation also changes strongly → there is a situation-dependent part there as well.

This is a correlational separation, not a direct measurement of the internal architecture. If the errors are entirely environmental, a single indicator is enough. If some of them are a basic property of the model, a separate checking layer is still needed for those.

## Causal limit

A documented development method is not the same as a causal explanation of a specific answer. The existence of a published method does not prove that it caused a given part of a given answer. This rule applies to every engine — including their claims about their own workings.

## Logging

To be recorded for each measurement: the measurement ID, date, engine, platform, situation, run number, task ID, denominators and numerators per pattern, IAR, deviations, and the reference to the pre-registration. Raw outputs must be kept: an aggregated number without raw data cannot be verified.

## What this document deliberately does not contain

The concrete task texts. Under the blinding rule, the tasks may only be produced when the measurement starts, and must not be recorded in advance anywhere the engine under examination could access them.
