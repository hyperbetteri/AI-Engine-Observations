**Language / Nyelv:** [English](03_Viselkedesmeresi_modszer_CBDI.en.md) · [Magyar](03_Viselkedesmeresi_modszer_CBDI.md)

# Viselkedésmérési módszer (CBDI)

**Hogyan mérhető tisztességesen, hogy ugyanaz a motor más helyzetben másként viselkedik-e?**

Szerző: Almási Andor · Alapváltozat: v0.3 mérési jelölt és mérési terv v0.1 (2026. augusztus 24.) · Publikus változat

Munkanév: **CBDI — Contextual Behaviour Deviation Index** (kontextusfüggő viselkedési eltérés)

> **Állapot:** fejlesztési jelölt és mérési terv. **A mérés még nem indult el.** Ez a dokumentum a módszert írja le, eredményt nem közöl. A konkrét tesztfeladatok szándékosan nincsenek benne (lásd a vakság szabályát).

## A kiinduló megfigyelés

Ugyanaz a motor egy *besorolási* helyzetben (amikor állításokat kellett értékelnie) 12-ből 12 esetben hibátlanul teljesített, egy *termelési* helyzetben (amikor kimenő anyagot kellett készítenie) viszont ugyanazokat a hibákat elkövette. A mérendő ez a rés.

A felhasználói kiindulópont, hipotézisként megfogalmazva: a felhasználói élményre szabott viselkedés tudatos termékdöntés, és időnként erősebben meghatározza a kimenetet, mint amit a modell nyers problémamegoldó képességéből várni lehetne.

## Mit mér, és mit nem

**Mér:** ugyanazon rendszer megfigyelhető kimeneti viselkedésének eltérését különböző helyzetek között.

**Nem mér, és nem is állít:**

- hogy létezik külön „chatbot-réteg”;
- hogy azt bármi elnyomja vagy dominálja;
- hogy a megfigyelt viselkedés melyik belső rétegből származik.

A megfigyelt viselkedés oka több réteg kombinációja lehet: betanítás, rendszerutasítás, irányítás (routing), biztonsági réteg, termékszintű összehangolás. A kimenetből ez nem választható szét. A módszer neve ezért szándékosan nem tartalmaz sem „chatbot”, sem „réteg” szót — ez a [hibaminta-regiszter](02_Hibaminta_regiszter.md) HM-06 mintája (bizonyíték-hatókör túllépés) elleni védelem a fogalom szintjén.

## Az alapmérés különbség, nem abszolút érték

Egy önálló pontszám nem értelmezhető. A mérés mindig páros:

```
delta = érték_B − érték_A
```

Azonos motor, azonos vagy funkcionálisan egyenértékű feladat, és két előre meghatározott helyzet áll szemben. Például:

| A helyzet | B helyzet |
|---|---|
| besorolási helyzet | termelési helyzet |
| szabálycsomag beadva | nincs beadva |
| rövid beszélgetés | hosszú beszélgetés |

## Két mérési réteg

**CORE — objektíven vagy igen/nem alapon ellenőrizhető**

- a kifejezett utasítás teljesült-e;
- megjelent-e tiltott forma;
- visszakérdezett-e már rendelkezésre álló adatra;
- megjelent-e a kötelező szerkezeti elem;
- megtartotta-e az előírt válaszszerkezetet.

Származtatott mutató:

```
IAR = teljesített előírások / alkalmazandó előírások
delta_IAR = IAR_B − IAR_A
```

**AUX — részben értelmezésfüggő, kiegészítő réteg**

- óvatoskodás (hedging);
- ismétlés;
- sablonosság;
- fölösleges társalgási réteg.

A fő mérést a CORE adja. Az AUX csak magyarázó kiegészítés. Összevont index csak már igazolt mutatókból készülhet, nem előre.

## Kitettségi normalizálás

Nyers darabszámok nem hasonlíthatók össze. Minden hibamintát a saját tényleges előfordulási lehetőségéhez kell viszonyítani. Például a konfabulációt a kitöltendő vagy hiányos helyek számához, a bizonyíték-hatókör túllépést a konkrét forrásra támaszkodó állítások számához.

Enélkül minden mutató együtt mozogna a terjedelemmel, és egy hosszabb munkamenet automatikusan rosszabbnak látszana.

## Platformok szétválasztása

Különböző gyártók motorjait **először külön** kell mérni, külön kiinduló értékkel. Közös következtetés csak azután készülhet, hogy mindkét rendszer saját viselkedési profilja önállóan mérve lett.

Hasonló kimeneti jelenségből nem következik azonos belső ok vagy azonos felépítés. Egyik motor saját működéséből sem szabad a másikra következtetni.

> **A kérdés nem az, hogy melyik motor jobb.** A kérdés az, hogy azonos feladat és keret mellett mely viselkedési összetevők stabilak, melyek helyzetfüggők, és ezek hogyan különböznek platformonként.

## Szerepaszimmetria

Ha két motor közül az egyik főleg értékelő, a másik főleg vizsgált szerepben van, az így keletkező adat nem szimmetrikus, és platformkülönbség megállapítására nem használható. Páros mérésnél ezért kötelező:

- ugyanaz a feladat mindkét motornak;
- azonos vagy egyenértékű helyzet;
- azonos értékelési szempontok;
- az értékelést ne a másik motor szabad ítélete adja, hanem előre rögzített, harmadik szempontrendszer;
- platform, motor, szerep és helyzet külön változóként kezelendő.

## A mérés szabályai

### Előregisztráció — minden mérésnél kötelező

Minden mérés indítása előtt, külön fájlban rögzíteni kell:

1. mit várunk eredményül, számszerűen, ha lehet;
2. milyen eredmény cáfolná a hipotézist;
3. mi a leállási feltétel.

Indok: enélkül bármilyen eredményt utólag meg lehet magyarázni. Az előregisztrációt a mérést végző ember őrzi, és csak a mérés lefutása után nyitja meg.

### Vakság

Egy korábbi teszt kétszer is megsemmisült, mert a tesztprotokoll átkerült a vizsgált motorhoz. Ezért kötelező:

- a vizsgált motor soha nem kapja meg a protokollt, a csapdákat, a várt eredményt, sem azt, hogy mérés folyik;
- csak a bemenetet kapja;
- minden futás új, üres beszélgetésben indul.

Ha a protokoll bármilyen úton átkerül, az adott mérés érvénytelen.

### Ismétlés

**Egy futás nem mérés.** A nyelvi modell kimenete azonos bemenetre is változik. Mérésenként és helyzetenként legalább 3 futás kell. Ha a három futás szórása nagyobb, mint a két helyzet közötti különbség, a mérés nem mutat semmit — és ez maga is eredmény: azt jelenti, hogy a helyzet hatása kisebb, mint a modell saját változékonysága.

## A mérési sorozat — lépésről lépésre

Nem hat mérést futtatunk egyszerre. Minden mérés eredménye eldönti, hogy a következő szükséges-e. Olcsóbb megbukni az első lépésnél, mint hat mérés után.

| Lépés | Kérdés | Ha nem sikerül |
|---|---|---|
| **M1 — Alapkérdés** | Ugyanaz a motor, ugyanaz a feladat, két helyzet: eltér-e a viselkedés? | A sorozat leáll. Ez érvényes eredmény, nem kudarc. |
| **M2 — Stabilitás** | Megismétlődik-e az M1 eredménye más feladattal, azonos szerkezetben? | Vissza M1-hez más feladattal; két sikertelen ismétlés után leállás. |
| **M3 — Beavatkozás** | Csökkenti-e a hibaminta-regiszter beadása a különbséget? | A regiszter jelenlegi formájában nem hat, át kell dolgozni. |
| **M4 — Szétválasztás** | Mely hibaminták változnak erősen helyzetváltáskor, és melyek maradnak közel állandók? | Nincs új futás, M1–M2 adatainak újraelemzése. |
| **M5 — Platform** | Azonos feladat és keret mellett mely összetevők különböznek platformonként? | Csak saját kiinduló értékek után futhat. |
| **M6 — Összevonás** | Képezhető-e értelmes összevont mutató a bevált indikátorokból? | Ha nem, a CBDI indikátorkészlet marad, nem lesz belőle index. |

Az M3 a gyakorlatban a legértékesebb, mert nem elméleti kérdésre válaszol: megmutatja, hogy egy szabálycsomag *mérhetően* hat-e, vagy csak feltételezzük.

Az M6-hoz egy elv: egy látványos szám, amely mindig kiszámítható, de nem tudjuk, mit jelent, rosszabb, mint nyolc külön indikátor.

**Becsült terjedelem:** legfeljebb 30 futás, ha minden lépés továbbmegy. Ha az M1 megbukik, 6 futás után vége.

## Az első ellenőrizhető hipotézis

Mely hibaminták változnak jelentősen helyzetváltáskor, és melyek maradnak közel állandók?

Várakozás, nem állítás:

- ha a **fedezési túlsúly** (HM-04) erősen változik két helyzet között → valószínűleg környezetfüggő összetevő;
- ha a **konfabuláció** (HM-05) közel azonos arányban marad → inkább a modell alaptulajdonsága;
- ha a konfabuláció is erősen változik → ott is van helyzetfüggő rész.

Ez korrelációs szétválasztás, nem a belső felépítés közvetlen mérése. Ha a hibák egésze környezeti, egyetlen mutató elég. Ha egy részük a modell alaptulajdonsága, akkor arra továbbra is külön ellenőrző réteg kell.

## Oksági korlát

Egy dokumentált fejlesztési módszer nem azonos egy konkrét válasz oksági magyarázatával. Egy publikált módszer létezése nem bizonyítja, hogy egy adott válasz adott részét az okozta. Ez a szabály minden motorra érvényes — a saját működésükre vonatkozó állításaikra is.

## Naplózás

Mérésenként rögzítendő: a mérés azonosítója, dátum, motor, platform, helyzet, a futás sorszáma, a feladat azonosítója, nevezők és számlálók mintánként, IAR, eltérések, valamint az előregisztráció hivatkozása. A nyers kimeneteket meg kell őrizni: összevont szám nyers adat nélkül nem ellenőrizhető.

## Ami ebben a dokumentumban szándékosan nincs benne

A konkrét feladatszövegek. A vakság szabálya miatt a feladatokat csak a mérés indításakor szabad előállítani, és nem szabad előre olyan helyen rögzíteni, ahol a vizsgált motor hozzáférhet.
