**Language / Nyelv:** [English](README.md) · [Magyar](README.hu.md)

# AI-motor megfigyelések / AI Engine Observations

**Almási Andor** — hosszú távú, napi szintű munka nagy nyelvi modellekkel („motorokkal”): hogyan viselkednek, hol és hogyan hibáznak, és hogyan lehet ezt tisztességesen megfigyelni és mérni.

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
- Jogi AI-keretrendszer (bemutató): [LEGAL-RQV-Overview](https://github.com/hyperbetteri/LEGAL-RQV-Overview)
- Holdi újrahasznosítási koncepciótanulmányok: [Lunar-Recycling-and-Terminator-Lab](https://github.com/hyperbetteri/Lunar-Recycling-and-Terminator-Lab)

---

© 2026 Almási Andor. Minden jog fenntartva. Forrásmegjelöléssel szabadon idézhető. / All rights reserved. Quotation with attribution is welcome.
