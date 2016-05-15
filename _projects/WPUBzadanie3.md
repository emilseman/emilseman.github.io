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

```xml
<s>
```
vložiť slajd prezentácie s možnými atribútmi background-color a layout. Background-color je potrebné uviesť v HTML kóde, je možné ho uviesť aj na koreňový element 

```xml
<presentation>
```
V slajde je možné zadefinovať nadpis 

```xml
<tit>
```
podnadpis 

```xml
<sub>
```
a obsah slajdu 

```xml
<content>
```

Slajd môže obsahovať text v tagu 

```xml
<text>
```
odrážkový zoznam v tagu _list_ s odrázkami _item_ 

```xml
<list>
  <item>Ahoj</item>
```
. Taktiež je možné vložiť obrázok v tagu _i_ s atribútom _src_ obsahujúcim cestu k obrázku.

Pre zobrazenie obsahu vo viacerých stĺpcoch je možné využiť tag _r_ s vloženými stĺpacmi _col_. Stĺpcov môže byť od 1 do 4 a ich počet je potrebné určiť v atribúte 

```xml
<r size="3">
<col>
  <text>Ahoj</text>
</col>
<col>
  <text>Ahoj2</text>
</col>
<col>
  <i src="ahoj.jpg"/>
</col>
</r>
```
