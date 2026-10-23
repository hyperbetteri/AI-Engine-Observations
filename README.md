**Nyelv:** [Magyar](README.md) | [English](README.en.md)

# AI-motor megfigyelések / AI Engine Observations

**Almási Andor** — hosszú távú, napi szintű munka nagy nyelvi modellekkel („motorokkal”): hogyan viselkednek, hol és hogyan hibáznak, és hogyan lehet ezt tisztességesen megfigyelni és mérni.

> **English summary below.**

## Miről szól ez a repó?

Ez a gyűjtemény nem kód és nem promptcsomag. Megfigyeléseket, hibamintákat és mérési elveket tartalmaz, amelyek több év, több motorral (OpenAI, Anthropic, Google és offline modellek) végzett gyakorlati munkából születtek.

A középpontban három kérdés áll:

1. **Mit jegyezzen meg egy AI-rendszer, és mit ne?** — memóriahigiénia hosszú távú együttműködésben.
2. **Milyen visszatérő hibamintákat mutatnak a motorok?** — dokumentált esetek, ellenőrző kérdésekkel.
3. **Hogyan lehet a motorok viselkedését tisztességesen mérni?** — előregisztráció, vakság, ismétlés.

## Tartalom

| # | Dokumentum | Röviden |
|---|---|---|
| 01 | [AI-memóriahigiénia és többmotoros kontroll](01_AI_memoriahigienia_es_tobbmotoros_kontroll.md) | A memória működési iránytű, nem tudástár. Rétegzett modell hosszú távú ember–AI munkához. |
| 02 | [Hibaminta-regiszter](02_Hibaminta_regiszter.md) | Hat dokumentált hibaminta (pl. keresés nélküli lefokozás, bizonyíték nélküli elmozdulás, konfabuláció), mindegyikhez ellenőrző kérdéssel. |
| 03 | [Viselkedésmérési módszer (CBDI)](03_Viselkedesmeresi_modszer_CBDI.md) | Hogyan mérhető, hogy ugyanaz a motor más-más helyzetben másként viselkedik-e — és mi számít valódi eredménynek. |
| 04 | [Digitális Dajka – projektismertető](04_Digitalis_Dajka_projektismerteto.md) | Koncepció: a gyermek telefonjából passzív figyelemlekötő helyett adaptív tanulási és biztonsági segítő. |

## Mi nincs benne — szándékosan

A dokumentumok az elveket, a problémafelvetést és az eredményeket mutatják be. **Nem** tartalmaznak végrehajtható belső promptokat, indítócsomagokat, forráskódot, küszöbértékeket, konkrét tesztfeladatokat, személyes adatokat vagy projektérzékeny részleteket. Ennek oka nem titkolózás, hanem kockázatkezelés: a részletes operatív anyag kontextus nélkül félreérthető vagy hibásan újrahasznosítható.

## Kapcsolódó

- Portfólió és validációs bizonyítékok: [AI-Workflow-Validation-Portfolio](https://github.com/hyperbetteri/AI-Workflow-Validation-Portfolio)
- Mérnöki esettanulmányok: [Engineering-Case-Studies](https://github.com/hyperbetteri/Engineering-Case-Studies)

---

## English summary

This repository collects observations from several years of intensive, day-to-day work with large language models ("engines") from multiple vendors and offline models. It is not code and not a prompt pack. It documents:

- **AI memory hygiene** — why long-term AI memory should be a short operating compass, not a knowledge base, and how a layered model (core, deep-work starter, master file, archive, quarantine, control engine) keeps long collaborations stable.
- **A failure-pattern register** — six documented LLM failure patterns (e.g. downgrading a claim without searching, drifting toward the user's position without new evidence, confabulation, overstepping the scope of a cited source), each with a self-check question.
- **A behaviour-measurement method (CBDI, working name)** — paired, pre-registered, blinded, repeated measurements to test whether the same engine behaves differently across contexts.
- **Digital Nanny** — a public concept description of an adaptive, family-controlled learning and safety companion for children.

The documents are in Hungarian. They deliberately omit internal prompts, boot packages, source code, thresholds, concrete test items and personal or project-sensitive data.

---

© 2026 Almási Andor. Minden jog fenntartva. Forrásmegjelöléssel szabadon idézhető. / All rights reserved. Quotation with attribution is welcome.
