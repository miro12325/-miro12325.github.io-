---
layout: zadania
title: Zadanie 2.
cvicenie: Štvrtok 17:40
cviciaci: doc. Ing. Marián Šimko, PhD.
autor: Miroslav Borecký
fakulta: Fakulta Informatiky a Informačných technológií
datum: "29.04.2019"
nazov: XML prezentácia
---
## Opis typu dokumentu
Opis typu dokumentu som navrhol v RELAX NG ktorý je možné nájsť v súbore RelaxNG.rng.

## Ukážková XML preznetácia
Ukážková XML prezentácia sa nachádza v súbore Prezentacia.xml
A obsahuje tieto Elementy Presentation-root element.

Slide - zakladný element do ktorého sa vkladá obsah slajdov prezentácie môžu byť try druhy podľa atribútu typ a to Opening-úvodný kde je len title a subtitle,
Navigation -  kde sa vygenruje stručný obsah s možnosťou priameho presunu na jednotlivé slajdy, Content -  obsahový slajd kde už sa priamo dávajú elemnty title a content

title - Názov buď prezentácie alebo slajdu

subtitle - podnázov na hlavný slajd

content - obsahový element do ktorého sa dávajú  texts, image, table, list, link, literature

texts - slúži na textový obsah slajdu umožňuje zvýrazňovať časti textu pomocou elementov strong a italic

table - slúži na vytváranie tabuliek je zložené atribútu caption čo je názov tabuľky a z elementov tablehead čo sú vlastne názvy stĺpcov v tabuľke a tableitem čo je vlastne obsah pre riadky v tabuľke

obidva obsahujú element item v ktorom majú uložené hodnoty pre jednotlivé bunky tabuľky

list - slúži na vytváranie zoznamov obsahuje atribút enum ktorého hodnoty sú true alebo false a udáva či bude zoznam číselný alebo odrážkový, zoznam obshuje listitem ktorý buď 

obshuje text alebo pod zoznam(list)

image -  slúžie na zobrazovanie obrázkov má atribúty source - kde sa má obrázok nachádzať, height,width - veľkosť obrázka a caption - popis k obrázku.

link - slúži na vytváranie hypertextových odkazov na webové stránky a podobne má atribúty url - cieľová url adresa a samotný obsah určuje čo sa bude zobrazať v prezentácií 

literature - slúži na vkladanie použitej literatúry - nedokončené z dôvodu nedostatku času ale už som to nechcel vymazávať

##Parametrizácia
Súbor s parametra sa volá parameters.xsl ktorý umožňuje nastavovať druh fontu "font" hlavnú farbu "titleColor" secundárnu farbu "backgroundColor" farbu textu "FontColor"
farbu titulných textov "TitleFontColor" veľkosť textu "FontSize" a veľkosť titulných textov "TitleFontSize".
Tento súbore je následne importnutý v XSL súboroch.

##XSLT pre XHTML
Súbor obsahujúci transformáciu do XHTML sa volá template.xsl a súbor s použitým css sa volá Style.css

##XSLT pre PDF
Súbor obsahujúci transformáciu do PDF(fo) sa volá template-fo.xsl.


