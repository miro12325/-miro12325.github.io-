---
layout: zadania
title: Zadanie 2.
cvicenie: Štvrtok 17:40
cviciaci: doc. Ing. Marián Šimko, PhD.
autor: Miroslav Borecký
fakulta: Fakulta Informatiky a Informačných technológií
datum: "27.03.2019"
nazov: Transformácia vybraného dokumentu do formátu DocBook
---
## Použité elementy

Štandardné členenie textu na kapitoli,podkapitoli a podpodkapitoli som zabezpečil použitím <chapter>, <section> a <simplesect>. Príloh a a zoznamy a obsah boli automaticky generované Docbookom skrze šablonu.   
Na zvýrazňovanie slov som použil <emphasis> konkrétne <emphasis role="bold">  a na vytvorenie odrážok som použil <itemizedlist>, <listitem>.   
Odkaz na vlastný text som použil iba raz a to pomocou <anchor id="ARV1" />, <link linkend="ARV1">[ARV1]</link>. v časti Rozšírena realita v Chapter2.xml.   
Poznámky pod čiarov som realizoval za pomoci <footnote> v časti Rozšírena realita v Chapter2.xml.   
Zoznam použitej literatúry je možné nájsť v Bib.xml kde som použil <bibliography>,<biblioentry> na ktoré som následne v texte odkazoval za pomoci <citation>.   
Obrázky som vkladal do textu za použitia elementu <figure> na ktoré som následne odkazoval v texte <link linkend="figure1">[figure1]</link>. Zoznam obrázkov použitých v texte sa automaticky generuje po menšej uprave v šablóne : 
<xsl:param name="generate.toc">
book      title,toc,figure
</xsl:param>   
Na vytvorenie registra pojmov(index) som použil <index/>(možné nájsť v Bib.xml) a <indexterm>(možné nájsť v Chapter2.xml ) v ktorom som použil jednotlivé úrovne zaradenia.

## Poznámka

V šablone som odstránil z prvej strany neexistujúci obrazáok. 
A niektoré elementy a časti boli umelo vsunuté oproti originálu pre potreby tohto zadania.
Zadanie je rozdelené do piatich osobytných xml súborov podľa obsahu ktoré sú spojené v hlavnom xml súbore Z2.xml a to cez <!ENTITY CH1 SYSTEM "Uvod.xml">, <!ENTITY CH2 SYSTEM "Chapter2.xml">, <!ENTITY CH3 SYSTEM "Chapter3.xml">, <!ENTITY Bib SYSTEM "Bib.xml"> ktoré sú neskôr volané v texte 
&CH1; , &CH2; , &CH3; , &Bib;

