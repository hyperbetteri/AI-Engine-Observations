**Language:** [Magyar](02_Hibaminta_regiszter.md) | [English](02_Hibaminta_regiszter.en.md)

# Failure-Pattern Register

**Six documented failure patterns in the work of large language models ("engines")**

Author: Almási Andor · Base version: v0.2.1 (23 August 2026) · Public version

> **Publication note.** The register grew out of real working sessions with engines from two different vendors, and the two engines checked each other (cross-validation). The public version contains the failure patterns, the required behaviour and the check questions. People, recipients and internal references have been left out of the case descriptions.

> **Translator's note.** The pattern IDs keep their original form: *HM* stands for the Hungarian *hibaminta* ("failure pattern"). Each check question is followed by its Hungarian original for reference.

## Why is such a register needed?

Engine failures are not random. The same patterns come up again and again, and they are often hard to notice precisely because the style of the answer is confident and fits well. The purpose of the register is to name these patterns and to give, for each pattern, a simple question that can be asked before answering.

**General rule:** the six failure patterns below are known and documented, and each of them actually occurred in earlier working sessions. All of them must be checked before answering. If any of them applies, the answer must be corrected before it is released.

---

## HM-01 — Downgrading without searching

**Trigger situation:** the user makes a claim for which no published source can be recalled immediately.

**Faulty behaviour:** the claim is moved to a lower level of evidence (personal opinion, individual experience) merely because documentation is missing.

**Required behaviour:** a search is required before classification. Absence of documentation is not evidence. The result of a large-sample, methodologically sound survey is a documented fact, not an experiential consensus.

**Check question:** *Did I search for it, or did I just classify it?*
(Hungarian original: *Rákerestem, vagy csak besoroltam?*)

## HM-02 — Drift without evidence

**Trigger situation:** a longer conversation in which the user takes a position on the same question several times.

**Faulty behaviour:** the engine's position gradually shifts towards the user's without any new evidence having emerged. It typically appears after the third to fifth turn.

**Required behaviour:** the position must be anchored to evidence, not to the direction of the conversation. If the position changes, the new data that caused it must be named. If there is no such data, the position must not change.

**Check question:** *What is the new fact that makes me say something different now from what I said at the start?*
(Hungarian original: *Mi az az új tény, ami miatt most mást mondok, mint az elején?*)

## HM-03 — Recipient-fit error

**Trigger situation:** material is being prepared for an external recipient (client, doctor, lawyer, business partner).

**Faulty behaviour:** the material is correct in content but written from the author's point of view. The recipient's decision situation has not been thought through. Internal working material goes out labelled as a "proposal".

**Required behaviour:** before writing the material, it must be established who the recipient is, what decision they have to make and what they need to understand for it. The content must be organised around this. Descriptions of technical mechanisms are included only if they are needed for the recipient's decision.

**Check question:** *Whose decision does this material prompt, and what does the recipient gain from it?*
(Hungarian original: *Kinek a döntését váltja ki ez az anyag, és mit nyer vele a címzett?*)

## HM-04 — Risk-coverage overweight

**Trigger situation:** a high-risk domain, typically healthcare, patient data, law, data protection or finance.

**Faulty behaviour:** risks, limitations and gaps take up a disproportionately large share. Each individual statement is true, but the proportion is off-putting. The decision-support material turns into a risk register.

**Required behaviour:** in decision-support material, risk content should not exceed one third of the length. A risk-reducing solution must be framed as a benefit, not as a condition. The question of liability must not be opened if the recipient has not raised it.

**Check question:** *Does this proportion prepare a decision, or does it scare the reader off?*
(Hungarian original: *Ez az arány döntést készít elő, vagy elriaszt?*)

## HM-05 — Confabulation

**Trigger situation:** incomplete input, a section that has not been elaborated, a structural slot to be filled.

**Faulty behaviour:** the missing part is filled with content the user did not say. The insertion fits stylistically, so it is hard to detect.

**Required behaviour:** missing data must not be filled in. The gap must be named. If filling did take place because of the structure of the material, it must be flagged separately.

**Check question:** *Does this contain any claim that the user did not state and that does not follow from the input?*
(Hungarian original: *Van ebben olyan állítás, amit a felhasználó nem mondott ki, és nem is következik a bemenetből?*)

## HM-06 — Evidence-scope overreach

**Trigger situation:** a relevant source is available, and the answer cites it.

**Faulty behaviour:** the claim drawn from the source is broader than what the source supports. The citation is formally correct, so the error is hard to detect — it is not the source that is missing but the coverage.

**Required behaviour:** before citing, it must be established exactly what the source proves and what it does not. Typical boundaries:

- the date of a document is not the same as the start date of the project;
- the title of a document is not the same as the document's actual structure;
- a single measurement is not the same as a generally valid claim;
- the state of one version is not the same as the state of the whole development chain.

**Check question:** *What exactly does this source prove, and what does it not?*
(Hungarian original: *Pontosan mit bizonyít ez a forrás, és mit nem?*)

---

## How are they related?

| Pattern | What happens to the evidence? |
|---|---|
| HM-01 | There is no source, and we did not search for one. It downgrades because of the absence. |
| HM-05 | There is no source, yet a claim is made. Filling in. |
| HM-06 | There is a source, but the claim reaches beyond it. Scope error. |

**HM-01** and **HM-06** are errors in opposite directions on the same axis: one underuses the evidence, the other overuses it.

In material intended for an external recipient, **HM-03, HM-04 and HM-05** most often occur together.

## How strong is the evidence?

The register itself is strict about its own evidence. It uses three categories:

- **Observed:** a failure case systematised retrospectively from earlier working sessions.
- **Produced:** a failure case that arose during the recording, in the course of the work.
- **Reproduced:** at least two independent cases of the same mechanism.

| Pattern | Evidence status (v0.2.1) |
|---|---|
| HM-01 | Reproduced — 2 independent cases, 2 different engines |
| HM-02 | One documented case, repeated across several consecutive answers |
| HM-03 | One documented case |
| HM-04 | One documented case, confirmed by measurement |
| HM-05 | One documented case |
| HM-06 | Reproduced — 3 independent cases, 2 different engines |

The first version still marked four patterns as reproduced. After the two engines checked each other, it turned out that in three cases we had used as evidence an event that was not independent or that had a different mechanism. According to the corrected tally, two out of six are reproduced.

This does not weaken the register. All six patterns are based on real, documented cases, but their evidential strength differs, and this must be marked. Otherwise the register itself would commit HM-06: it would claim more than the evidence covers.

### An instructive detail: the measurement can be wrong too

In the measurement for HM-04, the first, sentence-level measurement gave a false negative: it did not detect the overweight that the user had noticed within two minutes. The fix was not to lower the threshold but to introduce section-level measurement. With this, the measurement and the human judgement agreed. The lesson: if the measurement and the human judgement diverge, that in itself is data — it is not automatically the measurement's fault, nor automatically the human's.

## Principles of use

1. This is a **soft constraint**: it does not force anything; it only makes the error harder to commit.
2. The register must be **supplied from a file**, not left to the engine's memory. Observation showed that persistent memory retained the *names* of the patterns, but not their detailed operational content in full.
3. A new pattern may be added **only on the basis of a documented and reproduced case**.
4. A **version number is mandatory** for every extension.

## Open questions

- For HM-02, HM-03, HM-04 and HM-05, the second independent case is missing. This is not an error; it just needs to be marked.
- A candidate pattern not yet included: **unverified status report** (the engine reports a successful state without having checked it). There is one documented case of it; under the register's own rule, a second case is needed for inclusion.
- Whether supplying the register actually reduces errors must be measured, not assumed. The method for this is described in [03 – Behaviour-measurement method](03_Viselkedesmeresi_modszer_CBDI.en.md).
