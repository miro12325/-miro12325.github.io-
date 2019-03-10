---
layout: zadania
title: Zadanie 1.
cvicenie: Štvrtok 17:40
cviciaci: doc. Ing. Marián Šimko, PhD.
autor: Miroslav Borecký
fakulta: Fakulta Informatiky a Informačných technológií
datum: "10.03.2019"
nazov: Osobná webová prezentácia na GitHub pages
---
 V tomto zadaní som mal za úlohu vytoriť webové sídlo o sebe za použitia nástrojov Git, GitHub Pages, Jekyll a Markdown.  

 Stránka sa skladá z piatich hlavných stránok Domov, O mne, Záľuby, Projekty, Webové publikovanie. Stránky Záľuby, Projekty a Webové publikovanie obsahujú zoznam svojich podstránok a odkazov na ne.  
 * Domov je základy úvod na stránku kde je popisaný účel stránky a čo jednotlivé stránky obsahujú.  
 * Stránka O mne obsahuje zakladné informácie o mojej osobe kde študujem čomu sa venujem. Stránka využíva plugin a zároveň aj tag avatar a plugin jemoji.  
 * Stránka Záľuby obsahuje odkazy na podstránky ktorých obsahom sú bližšie priblížene jednotlivé moje záľuby. Stránka využíva collections na to aby cez for cyklus zobrazila všetky zoznam všetkých podstránok záľub.   
 * Stránka Projekty obsahuje zozonam mojich projektov zoradených podľa programovacieho jazyka ktorý som použil každá stránka projektu obsahuje základné informácie o projekte a fotky z daných projektov . Stránka využíva collections na to aby cez for cyklus najprv zozbierala a pomocou filtru append pridala do jedného poľa všetky prvé tagy z jednotliých stránok pomocu filtra .first ktoré následne pomcou filtrov split, uniq a sort zotriedi a zariadi to aby neboli duplikáty v poli tagy. Toto pole je následne použité v ďalšom for cykle na to aby sa zoznam projektov bol zotriedený podľa daných tagov. 
 * Stránka Webové publikovanie obsahuje zoznam jednotlivých zadaní na predmet Webové publikovanie jednotlivé stránky zadaní následne obsahujú zakladné informácie o zadaní a dokumentáciu k danému zadaniu. Stránka využíva collections na to vypísanie zoznamu všetkých podstránok zadaní a odakazov na ne.
 
  Na tvorbu stránok som použil štyri šablony ktoré som vytvoril a to sú  default, hobbies, projects, zadania.  
  * Default obsahuje rozloženie navigácie stránky a základny vzhľad využíva premenú page.title.  
  * Hobbies obsahuje rozloženie obsahu stránok pre záľuby šablona obsahuje tieto pracuje s týmto premennými page.title, page.photo, page.video. Ďalej v šablone bol využitý tag youtube ktorý je zároveň aj pluginom na zobrazenie videa z youtubu.  
  * Projects obsahuje rozloženie obsahu stránok pre projekty šablona využíva premenné page.title, page.fotky, page.typ, page.predmet, page.datum, page.firma, page.tags, page.link, tagy, path ďalej využíva filter join a include image-gallery.html.  
  * Zadania obsahuje rozloženie obsahu stránok pre zadania ktorá vaužíva premenné page.title, page.nazov, page.fakulta,page.cviciaci, page.cvicenie, page.autor, page.datum.  