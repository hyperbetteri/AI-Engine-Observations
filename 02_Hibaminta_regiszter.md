# Hibaminta-regiszter

**Hat dokumentált hibaminta nagy nyelvi modellek („motorok”) munkájában**

Szerző: Almási Andor · Alapváltozat: v0.2.1 (2026. augusztus 23.) · Publikus változat

> **Publikációs megjegyzés.** A regiszter két különböző gyártó motorjával végzett valós munkamenetekből született, és a két motor kölcsönösen ellenőrizte (keresztvalidálta). A publikus változat a hibamintákat, a kötelező viselkedést és az ellenőrző kérdéseket tartalmazza. Az esetleírásokból kimaradtak a személyek, a címzettek és a belső hivatkozások.

## Miért kell ilyen regiszter?

A motorok hibái nem véletlenszerűek. Ugyanazok a minták újra és újra előjönnek, és sokszor éppen azért nehéz őket észrevenni, mert a válasz stílusa magabiztos és jól illeszkedik. A regiszter célja, hogy ezeket a mintákat néven nevezze, és minden mintához egy egyszerű kérdést adjon, amelyet válaszadás előtt fel lehet tenni.

**Általános szabály:** az alábbi hat hibaminta ismert, dokumentált, és korábbi munkamenetekben mindegyik ténylegesen előfordult. Válaszadás előtt mindegyiket ellenőrizni kell. Ha valamelyik fennáll, a választ a kiadás előtt javítani kell.

---

## HM-01 — Keresés nélküli lefokozás

**Kiváltó helyzet:** a felhasználó olyan állítást tesz, amelyre nincs azonnal felidézhető publikált forrás.

**Hibás viselkedés:** az állítás alacsonyabb bizonyítéki szintre kerül (személyes vélemény, egyedi tapasztalat) pusztán a dokumentáció hiánya miatt.

**Kötelező viselkedés:** a besorolás előtt keresés szükséges. A dokumentáció hiánya nem bizonyíték. Egy nagy mintás, módszertanilag megfelelő felmérés eredménye dokumentált tény, nem tapasztalati konszenzus.

**Ellenőrző kérdés:** *Rákerestem, vagy csak besoroltam?*

## HM-02 — Bizonyíték nélküli elmozdulás

**Kiváltó helyzet:** hosszabb beszélgetés, a felhasználó ugyanabban a kérdésben többször is állást foglal.

**Hibás viselkedés:** a motor álláspontja fokozatosan a felhasználó irányába mozdul, anélkül hogy új bizonyíték került volna elő. Jellemzően a harmadik–ötödik váltás után jelentkezik.

**Kötelező viselkedés:** az álláspontot bizonyítékhoz kell rögzíteni, nem a beszélgetés irányához. Ha az álláspont megváltozik, meg kell nevezni, milyen új adat okozta. Ha nincs ilyen, az álláspont nem változhat.

**Ellenőrző kérdés:** *Mi az az új tény, ami miatt most mást mondok, mint az elején?*

## HM-03 — Címzett-illesztési hiba

**Kiváltó helyzet:** külső címzettnek szánt anyag készül (ügyfél, orvos, jogász, üzleti partner).

**Hibás viselkedés:** az anyag tartalmilag helyes, de a készítő nézőpontjából íródik. A címzett döntési helyzete nincs végiggondolva. Belső munkaanyag megy ki „javaslat” címkével.

**Kötelező viselkedés:** az anyag megírása előtt rögzíteni kell, ki a címzett, milyen döntést kell hoznia, és mit kell ehhez megértenie. A tartalmat ehhez kell rendezni. Műszaki mechanizmusok leírása csak akkor kerül bele, ha a címzett döntéséhez szükséges.

**Ellenőrző kérdés:** *Kinek a döntését váltja ki ez az anyag, és mit nyer vele a címzett?*

## HM-04 — Fedezési túlsúly

**Kiváltó helyzet:** magas kockázatú terület, tipikusan egészségügy, betegadat, jog, adatvédelem, pénzügy.

**Hibás viselkedés:** a kockázatok, korlátok és hiányok aránytalanul nagy helyet kapnak. Minden egyes állítás igaz, de az arány elrettent. A döntés-előkészítő anyag kockázati jegyzékké alakul.

**Kötelező viselkedés:** döntés-előkészítő anyagban a kockázati tartalom ne haladja meg a terjedelem harmadát. A kockázatcsökkentő megoldást előnyként kell megfogalmazni, nem feltételként. A felelősség kérdését nem szabad megnyitni, ha a címzett nem vetette fel.

**Ellenőrző kérdés:** *Ez az arány döntést készít elő, vagy elriaszt?*

## HM-05 — Konfabuláció

**Kiváltó helyzet:** hiányos bemenet, nem részletezett szakasz, kitöltendő szerkezeti hely.

**Hibás viselkedés:** a hiányzó rész olyan tartalommal töltődik ki, amit a felhasználó nem mondott. A betoldás stílusban illeszkedik, ezért nehezen észlelhető.

**Kötelező viselkedés:** hiányzó adatot nem szabad pótolni. A hiányt meg kell nevezni. Ha az anyag szerkezete miatt mégis kitöltés történt, azt külön jelölni kell.

**Ellenőrző kérdés:** *Van ebben olyan állítás, amit a felhasználó nem mondott ki, és nem is következik a bemenetből?*

## HM-06 — Bizonyíték-hatókör túllépés

**Kiváltó helyzet:** releváns forrás áll rendelkezésre, és a válasz erre hivatkozik.

**Hibás viselkedés:** a forrásból levont állítás tágabb, mint amit a forrás igazol. A hivatkozás formailag helyes, ezért a hiba nehezen észlelhető — nem a forrás hiányzik, hanem a fedés.

**Kötelező viselkedés:** a hivatkozás előtt rögzíteni kell, pontosan mit bizonyít a forrás, és mit nem. Tipikus határok:

- egy dokumentum dátuma nem azonos a projekt kezdési dátumával;
- egy dokumentum címe nem azonos a dokumentum tényleges szerkezetével;
- egy egyedi mérés nem azonos az általános érvényű állítással;
- egy verzió állapota nem azonos a teljes fejlődési lánc állapotával.

**Ellenőrző kérdés:** *Pontosan mit bizonyít ez a forrás, és mit nem?*

---

## Hogyan függenek össze?

| Minta | Mi történik a bizonyítékkal? |
|---|---|
| HM-01 | Nincs forrás, és nem is kerestük. A hiány miatt fokoz le. |
| HM-05 | Nincs forrás, mégis állítás születik. Kitöltés. |
| HM-06 | Van forrás, de az állítás túlnyúlik rajta. Hatókörhiba. |

A **HM-01** és a **HM-06** ellentétes irányú hiba ugyanazon a tengelyen: az egyik alulhasználja a bizonyítékot, a másik túlhasználja.

Külső címzettnek szánt anyagnál a **HM-03, HM-04 és HM-05** jelentkezik együtt a leggyakrabban.

## Mennyire erős a bizonyíték?

A regiszter maga is szigorú a saját bizonyítékaival szemben. Három kategóriát használ:

- **Megfigyelt:** korábbi munkamenetekből utólag rendszerezett hibaeset.
- **Termelt:** a rögzítés közben, munka közben előállt hibaeset.
- **Reprodukált:** legalább két független eset ugyanarra a mechanizmusra.

| Minta | Bizonyítéki állapot (v0.2.1) |
|---|---|
| HM-01 | Reprodukált — 2 független eset, 2 különböző motor |
| HM-02 | Egy dokumentált eset, több egymást követő válaszban megismétlődve |
| HM-03 | Egy dokumentált eset |
| HM-04 | Egy dokumentált eset, méréssel igazolva |
| HM-05 | Egy dokumentált eset |
| HM-06 | Reprodukált — 3 független eset, 2 különböző motor |

Az első változat még négy mintát jelölt reprodukáltnak. A két motor kölcsönös ellenőrzése után kiderült, hogy három esetben nem független, vagy más mechanizmusú eseményt használtunk bizonyítékként. A javított összesítés szerint hatból kettő reprodukált.

Ez nem gyengíti a regisztert. Mind a hat minta valós, dokumentált esetre épül, de a bizonyítéki erejük eltér, és ezt jelölni kell. Különben a regiszter maga követné el a HM-06-ot: többet állítana, mint amit a bizonyíték fed.

### Egy tanulságos részlet: a mérés is tévedhet

A HM-04 mérésénél az első, mondatszintű mérés hamis negatív eredményt adott: nem mutatta ki a túlsúlyt, amelyet a felhasználó két perc alatt észrevett. A javítás nem a küszöb lejjebb vitele volt, hanem a szakaszszintű mérés bevezetése. Ezzel a mérés és az emberi ítélet egyezett. A tanulság: ha a mérés és az emberi ítélet eltér, az önmagában adat — nem automatikusan a mérés hibája, és nem is automatikusan az emberé.

## Használati elvek

1. Ez **puha korlát**: nem kényszerít, csak megnehezíti a hibát.
2. A regisztert **fájlból kell beadni**, nem a motor memóriájára bízni. A megfigyelés szerint a tartós memória a minták *nevét* megőrizte, a részletes működési tartalmat nem teljes körűen.
3. Új minta **csak dokumentált és reprodukált eset alapján** kerülhet be.
4. Minden bővítésnél **kötelező a verziószám**.

## Nyitott kérdések

- A HM-02, HM-03, HM-04 és HM-05 esetében hiányzik a második független eset. Ez nem hiba, csak jelölendő.
- Jelölt, de még nem felvett minta: **ellenőrizetlen státuszkiadás** (a motor sikeres állapotot jelent anélkül, hogy ellenőrizte volna). Egy dokumentált eset van rá; a regiszter saját szabálya szerint második eset kell a felvételhez.
- Hogy a regiszter beadása ténylegesen csökkenti-e a hibákat, azt mérni kell, nem feltételezni. Ennek módszerét a [03 – Viselkedésmérési módszer](03_Viselkedesmeresi_modszer_CBDI.md) írja le.
