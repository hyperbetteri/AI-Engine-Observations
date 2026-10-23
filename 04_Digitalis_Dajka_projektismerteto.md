**Language / Nyelv:** [English](04_Digitalis_Dajka_projektismerteto.en.md) · [Magyar](04_Digitalis_Dajka_projektismerteto.md)

# Digitális Dajka / Digitális Cumi / Digitális Babysitter

**Publikus projektismertető**

Szerző: Almási Andor · Változat: v1 (2026. augusztus 7.) · Ember–AI együttműködésben készült

> Ez a dokumentum kizárólag publikus projektismertető. Nem tartalmazza a részletes belső implementációs terveket, validációs rendszereket, küszöbértékeket vagy más reprodukálható fejlesztési know-how-t.

## 1. Mi a Digitális Dajka ötlete?

A Digitális Dajka egy olyan AI-alapú fejlesztési koncepció, amely a gyermek által már használt telefon vagy tablet szerepét alakítja át. A cél nem az, hogy a gyermek még több passzív képernyőidőt kapjon, hanem hogy ugyanaz az eszköz aktív tanulási, kommunikációs, kreatív és biztonsági csatornává váljon.

A rendszer alapgondolata, hogy az AI ne egyszerűen kérdésekre válaszoló chatbot legyen, hanem a gyermekkel hosszabb távon együttműködő, következetes digitális segítő. Figyeli a gyermek reakcióit, érdeklődését, terhelhetőségét és fejlődési mintázatait, majd ezekhez igazítja a kommunikációt és a feladatokat.

## 2. Miért „Digitális Cumi” és miért „Digitális Dajka”?

A „Digitális Cumi” elnevezés arra a kiinduló problémára utal, hogy a telefon és a tablet sok családban már kisgyermekkorban figyelemlekötő eszközzé válik. A projekt ezt a meglévő helyzetet nem pusztán tiltani akarja, hanem értelmesebb működéssé alakítani.

A „Digitális Dajka” és „Digitális Babysitter” elnevezés már a továbbfejlesztett szerepet jelöli: egy olyan digitális segítőt, amely tanul, kommunikál, játékosan fejleszt, és a későbbi rendszerverziókban a fizikai környezetből érkező jeleket is képes lehet értelmezni.

## 3. A rendszer központi eleme: dinamikus gyermekmodell

A rendszer nem egyetlen merev címkével vagy pontszámmal írja le a gyermeket. Több különböző működési területet figyelhet: például beszédértést, szókincset, figyelmet, memóriát, problémamegoldást, térbeli gondolkodást, kreativitást, motivációt, frusztrációtűrést és érzelmi reakciókat.

A gyermekmodell folyamatosan frissül. A rendszer a gyermeket elsősorban saját korábbi állapotához hasonlítja, és azt vizsgálja, hogy egy adott feladat, kommunikációs mód vagy nehézségi szint milyen reakciót váltott ki.

**Fontos:** ez a modell nem orvosi diagnózis és nem statikus minősítés, hanem a személyre szabott kommunikációt és tanulási támogatást szolgáló, folyamatosan módosítható működési hipotézis.

## 4. Játékos, természetes tanulás

A gyermek felmérése és fejlesztése nem klasszikus vizsgáztatásra épül. A rendszer játékos beszélgetésekből, feladatokból, történetekből, képekből, választásokból és hétköznapi interakciókból gyűjt visszajelzést.

A cél az, hogy a tanulás élményszerű maradjon. A rendszer képes lehet például a feladat nehézségét, a magyarázat stílusát, a beszéd tempóját vagy a témát a gyermek aktuális érdeklődéséhez és terhelhetőségéhez igazítani.

## 5. Stabil AI-karakter

A gyermek egy következetes, felismerhető digitális karakterrel találkozik, nem minden alkalommal más személyiséggel. A stabil vizuális és hangbeli jelenlét kiszámíthatóbb kapcsolatot teremt.

A digitális karakter nem a szülő vagy más családtag helyettesítője. Feladata az ismétlődő kérdések megválaszolása, játékos tanítás, történetmesélés, gyakorlás, egyszerű rutinok támogatása és a gyermekkel folytatott következetes párbeszéd.

## 6. A szülő szerepe

A projekt alapelve, hogy a szülő vagy gyám marad az elsődleges emberi döntéshozó. Az AI megfigyelhet, elemezhet, javaslatokat tehet, visszamérhet és az előre meghatározott működési keretek között reagálhat, de nem a család felett álló hatóság.

A rendszer családi profilt is használhat: például nyelv, napirend, szokások, nevelési célok, érdeklődési körök és képernyőhasználati szabályok alapján. Ezek az információk a személyre szabást szolgálják.

## 7. Multimodális érzékelés

A későbbi fejlesztési rétegekben a rendszer nemcsak a leírt szöveget értelmezheti. A telefon vagy tablet kamerája, mikrofonja, érintési adatai és mozgásérzékelői együtt segíthetnek a helyzet jobb megértésében.

A hang például két külön csatornán dolgozható fel: az egyik a beszéd tartalmát alakítja szöveggé, a másik a hangzás jellemzőit — például tempót, hangerőt, szüneteket vagy bizonytalanságot — használhatja kiegészítő állapotjelként.

Egyetlen jelből a rendszer nem tekinthet biztosnak egy érzelmi vagy fizikai állapotot; a cél több jel együttes, bizonytalanságot is kezelő értelmezése.

## 8. A következő nagy lépcső: térbeli Digitális Dajka

A projekt következő architekturális szintje a szenzorfúzió és a dinamikus 3D környezeti világmodell. Ebben a telefon vagy tablet már nem az egyetlen megfigyelési pont, hanem egy nagyobb érzékelőrendszer része.

A rendszer később összekapcsolhat fix helyiségérzékelőket, kamerákat, mikrofonokat, távolság- vagy térérzékelőket, illetve egy gyermekhez kapcsolódó kis viselhető szenzormodult.

A cél az, hogy a rendszer ne csak azt tudja, mit mond vagy érint meg a gyermek, hanem azt is képes legyen becsülni, hol van, merre mozog, milyen tárgyak vagy személyek vannak körülötte, és hogyan változik a környezet.

## 9. Dinamikus 3D világmodell és kockázatbecslés

A fejlesztési koncepcióban a különböző érzékelések közös idő- és térbeli modellbe kerülnek. A rendszer külön kezeli a megfigyelést, a több szenzorból létrehozott helyzethipotézist és az ezekből folyamatosan frissített környezeti világmodellt.

Ez lehetővé teheti statikus és mozgó objektumok, emberek, állatok, ajtók, lépcsők vagy más releváns környezeti elemek követését. A rendszer rövid távú mozgási előrejelzést és dinamikus kockázatbecslést is készíthet.

A hangsúly itt sem egyetlen szenzor „tévedhetetlenségén” van, hanem több részleges mérés egyesítésén és annak kifejezett kezelésén, hogy a rendszer mennyire biztos az adott becslésben.

## 10. Mit nem akar a projekt?

- Nem cél a szülő, nagyszülő, testvér vagy valódi emberi kapcsolat lecserélése.
- Nem cél a gyermek folyamatos passzív képernyőn tartása.
- Nem cél egyetlen merev intelligencia- vagy személyiségpontszám létrehozása.
- Nem cél, hogy az AI orvosi vagy pszichológiai diagnózist állítson fel.
- Nem cél az, hogy a rendszer egyetlen kamera vagy szenzor jeléből biztos következtetéseket tegyen.

## 11. Mitől különleges az elképzelés?

A projekt nem egyetlen alkalmazást vagy egyetlen oktatási funkciót ír le. Egy olyan összekapcsolt rendszerarchitektúrát céloz, amelyben a hosszú távú gyermekmodell, az adaptív kommunikáció, a családi beállítások, a multimodális érzékelés, a későbbi térbeli világmodell és a fokozatos AI-reakció ugyanannak a rendszernek a részei.

Az alapgondolat röviden: a gyermek által már használt digitális eszközből olyan intelligens, személyre szabható fejlődési felületet létrehozni, amely a képernyőt nem önmagáért használja, hanem a tanulást, kíváncsiságot, kommunikációt, kreativitást, biztonságot és a családi együttműködést támogatja.

## 12. Jelenlegi fejlesztési állapot

A koncepció rendszermagja és a szenzorfúziós/3D környezeti architektúra első szerkezeti alapváza elkészült, és külön ellenőrzési körökön ment át. A részletes 3D világmodell, a viselhető szenzormodul, a fix térérzékelő hálózat, a valós idejű veszély- és állapotbecslés, az AI-beavatkozási logika és az intelligens otthon integráció további fejlesztési munka tárgya.

## 13. Adatvédelem és gyermekbiztonság

A rendszer gyermekekről gyűjtene adatot, köztük kamera-, hang-, érintési és mozgásadatot, valamint ezekből levont állapotbecslést. Ezért az adatvédelem nem kiegészítő funkció, hanem a tervezés kiinduló feltétele. A koncepció az alábbi elveket rögzíti. Ezek követelmények, nem már megvalósított funkciók.

- **Jogi keret:** az uniós általános adatvédelmi rendelet (GDPR), a gyermekek adataira vonatkozó szigorúbb szabályok és az uniós MI-rendelet (AI Act) követelményei. Bármilyen megvalósítás előtt adatvédelmi hatásvizsgálat szükséges.
- **Szülői hozzájárulás és kontroll:** adatgyűjtés csak a szülő vagy gyám kifejezett, bármikor visszavonható hozzájárulásával. A szülő látja, mit tárol a rendszer, és törölheti.
- **Adattakarékosság:** csak a működéshez szükséges adat keletkezik; a nyers kép- és hangfelvétel lehetőség szerint nem tárolódik.
- **Helyi feldolgozás elsőbbsége:** amit lehet, az eszközön vagy a család saját hálózatán belül kell feldolgozni. Felhőbe csak szükséges, titkosított és minimalizált adat kerülhet.
- **Nincs másodlagos felhasználás:** a gyermek adatai nem használhatók reklámra vagy más célú profilalkotásra, és nem adhatók tovább.
- **Az állapotbecslés korlátai:** az érzelmi vagy fizikai állapot becslése bizonytalan, nem minősítés és nem diagnózis, emberi felülvizsgálat nélkül nem alapozhat meg döntést.
- **Megőrzés és törlés:** meghatározott megőrzési idő; a gyermekmodell és a hozzá tartozó adatok teljes egészében törölhetők.

---

## Egymondatos összefoglaló

A Digitális Dajka / Digitális Cumi / Digitális Babysitter célja, hogy a gyermek által már használt telefonból vagy tabletből passzív figyelemlekötő eszköz helyett személyre szabott, adaptív tanulási, kommunikációs és később térbeli biztonsági támogató rendszer váljon, a családi kapcsolatok helyettesítése nélkül.
