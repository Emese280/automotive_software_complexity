# automotive_software_complexity
Developer oriented research on software complexity in automotive embedded systems.

## Miért lehet több millió sor egy autóipari szoftverben?

Egy modern autóban rengeteg különböző elektronikus vezérlőegység (ECU)
és szoftveres funkció található. Ezek kezelik többek között a motort,
fékrendszert, világítást, kommunikációt, diagnosztikát és biztonsági
funkciókat.

## A nagy kódbázis kialakulásának főbb okai:

- sok különböző funkció és ECU
- különböző autó- és hardverváltozatok
- kommunikációs és diagnosztikai rétegek
- biztonsági és megbízhatósági követelmények
- generált kód és konfigurációk
- régi, továbbhasznált (legacy) kód
- korábbi projektekből származó komponensek és workaroundok

Ezért a több millió sor nem feltétlenül jelent rossz vagy felesleges
kódot. A kódbázis jelentős része infrastruktúrát, konfigurációt,
hardvertámogatást és különböző változatokat kezel.

## Miért C?

A C különösen elterjedt az embedded és automotive rendszerekben, mert
közvetlenebb kapcsolatot biztosít a hardverrel, kevés erőforrást igényel,
és jól használható kis teljesítményű mikrovezérlőkön is.

Emellett a C-nek hosszú ideje kialakult fordító-, debugger- és
eszköztámogatása van az embedded világban, és az autóiparban olyan
szabványok és fejlesztési gyakorlatok is kialakultak köré, mint például
a MISRA C.

## Összegzés

A több millió soros automotive codebase általában nem egyetlen okból
alakul ki. A sok funkció, változat, hardverközeli kód, generált kód,
biztonsági követelmény és évek alatt felhalmozódott legacy együtt
eredményezi a nagy kódbázist.



# Autóipari fejlesztés vs. alkalmazásfejlesztés

Az autóipari szoftverfejlesztés több szempontból eltér egy átlagos
alkalmazás, például egy weboldal vagy mobilalkalmazás fejlesztésétől.

## Legfontosabb különbségek

### 1. Biztonság

Egy alkalmazás hibája gyakran kellemetlenséget vagy adatvesztést okoz.
Egy autóipari szoftver hibája viszont akár közvetlenül veszélyeztetheti
az utasok biztonságát.

Ezért fontos szerepet kapnak a safety követelmények és szabványok,
például az ISO 26262.

### 2. Hardverközeli működés

Az automotive software gyakran közvetlenül mikrovezérlőkkel,
szenzorokkal és különböző elektronikus egységekkel kommunikál.

Ezért sokkal nagyobb szerepe van a drivereknek, memóriakezelésnek,
kommunikációs protokolloknak és a hardver korlátainak.

### 3. Valós idejű működés

Bizonyos funkcióknak meghatározott időn belül kell végrehajtódniuk.

Például egy vezérlési feladatnál nem elég, hogy a program "végül"
helyesen működik, hanem annak megfelelő időzítéssel is meg kell történnie.

### 4. Hosszú életciklus

Egy mobilalkalmazást viszonylag könnyen lehet frissíteni vagy lecserélni.
Egy autóipari software viszont akár sok éven keresztül támogatandó lehet.

Ez miatt a régi kód, kompatibilitási megoldások és legacy komponensek
hosszú ideig a rendszer részét képezhetik.

### 5. Tesztelés és validáció

Az automotive software-t nem lehet egyszerűen csak kiadni és figyelni,
hogy a felhasználók találnak-e hibákat.

A működést különböző szinteken kell tesztelni és validálni, gyakran
hardware-rel együtt is.

### 6. Megbízhatóság

Egy autóipari rendszernek szélsőséges körülmények között is működnie kell,
például hőmérséklet-, feszültség- vagy kommunikációs problémák esetén.

## Összegzés

Az autóipari fejlesztés egyik legnagyobb különbsége, hogy a software
közvetlenül fizikai rendszereket irányít, miközben szigorú biztonsági,
megbízhatósági és időzítési követelményeknek kell megfelelnie.

Ezért az automotive software fejlesztése általában nagyobb hangsúlyt
fektet a validációra, tesztelésre, dokumentációra, szabványokra és a
hardverrel való együttműködésre, mint egy tipikus alkalmazásfejlesztés.
