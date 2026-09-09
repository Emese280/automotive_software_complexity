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
