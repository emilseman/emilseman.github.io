---
layout: projects
name: "Webové publikovanie - zadanie 3"
language: "XML, XSLT"
categories: school thirdyear
tags: [xslt]
---

Zadaním bolo vytvoriť XML štruktúru pre prezentáciu a jej XSLT transformáciu do HTML s CSS šablónou a PDF formátu.

Do pdf formátu sa podarilo vložiť len text z prezentácie, pretože obrázky nefungovali.

V html formáte sa nachádza automaticky vygenerovaná navigácia, s odkazmi na ďalší a predchádzajúci slajd, a taktiež na prvý a posledný. V dropup boxe je možné zvoliť si konkrétny slajd.
Do prezentácie je možné tagom
```
<s>
```
vložiť slajd prezentácie s možnými atribútmi background-color a layout. Background-color je potrebné uviesť v HTML kóde, je možné ho uviesť aj na koreňový element
```
<presentation>
```
V slajde je možné zadefinovať nadpis 
```
<tit>
```
podnadpis
```
<sub>
```
a obsah slajdu 
```
<content>
```

Slajd môže obsahovať text v tagu 
```
<text>
```
odrázkový zoznam v tagu list s odrázkami item 
```
<list>
  <item>Ahoj</item>
```
. Taktiež je možné vložiť obrázok v tagu _i_ s atribútom _src_ obsahujúcim cestu k obrázku.
