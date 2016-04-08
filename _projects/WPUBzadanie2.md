---
layout: projects
name: "Webové publikovanie - zadanie 2"
language: "DocBook, XML, XSLT"
categories: school thirdyear
tags: [docbook]
---

Zadanie je bakalárska práca vypracovaná vo formáte docBook a prekonvertovaná pomocou procesora do FO a z neho do PDF.  
Text sa člení na kapitoly (chapter) a na jednotlivé podkapitoly (section), ktoré môžu byť aj vnorené (napr. 1.2.1. O UPnP protokole).  
Na zvýraznenie textu sa používa  

```xml
<emphasis role="bold">
```
Pre poznámky pod čiarou používam  

```xml
<footnote>
    <para>
        <citetitle>(Molisch, 2011)</citetitle>
    </para>
</footnote>
```
Pre vloženie obrázkov vrátane poznámky pod čiarou bolo použité:

```xml
<figure id="obr.pripady">
      <title>Prípady použitia systému
        <footnote>
          <para>
            <citetitle>Vlastný graf</citetitle></para>
        </footnote>
      </title>
      <mediaobject>
        <imageobject>
          <imagedata fileref="ob2.png"/>
        </imageobject>
        <textobject>
          <phrase>Vlastný graf</phrase>
        </textobject>
      </mediaobject>
</figure>
```

Pre vygenerovanie zoznamu obrázkov a tabuliek bolo pridané do parametru  

```xml
<xsl:param name="generate.toc">
```
v súbor thesis.xsl prvky: figure, table. 

Taktiež pred odsekmi bolo nastavené odriadkovanie na 1,5 riadka  

```xml
<xsl:attribute name="space-before.optimum">1.5em</xsl:attribute>
```
a bol upravený template s názvom chapappendix.title, aby nezobrazoval napr. **kapitola 1** pred prvou kapitolou, ale aby zobrazil **1. Analýza**.

Ku koncu dokumentu je vytvorená bibliografia a v texte sa na diela z nej cituje, napr. 

```xml
<xref linkend="lit.sysmocom"/>
```
cituje na webstránku sysmocomu, v sekcii **BTS Stanice**.
