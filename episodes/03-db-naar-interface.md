---
title: "Demo: van database naar interface"
teaching: 5 # teaching time in minutes
exercises: 10 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions 

- Hoe verhoudt een gebruikersinterface zich met de data?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Beschrijven hoe een databasestructuur zich vertaald naar een gebruikersinterface

::::::::::::::::::::::::::::::::::::::::::::::::

We hebben tot nu toe gezien hoe je je data kunt structureren volgens een relationeel model en 
wat de voordelen zijn van een database. 
Het is tijd om nu te zien hoe dit er dan voor de eindgebruiker uit kan komen te zien en hoe dit zich verhoudt tot de onderliggende data structuur.

In dit hoofdstuk bekijken we deze gebruikersinterface
https://digitaal-erfgoed-trainingen.github.io/Relational_database_demo/. 
De interface is (met behulp van AI) gebouwd voor educatieve doeleinden, 
gebaseerd op de `historisch glas in gebouwen` dataset van het vorige hoofdstuk.

::: challenge
Bekijk https://digitaal-erfgoed-trainingen.github.io/Relational_database_demo/.

1. Hoeveel glasobjecten zijn er in de kleur amber?
2. Hoe zie je de relatie tussen gebouwen en glasobjecten terug in deze interface?
3. Bekijk [de pagina over Jachthuis Sint Hubertus](https://digitaal-erfgoed-trainingen.github.io/Relational_database_demo/#/gebouw/9)
Beschrijf in je eigen woorden hoe er in de database wordt gezocht om het overzicht van gekoppelde glasobjecten te verkrijgen.


:::: solution
1. 2 glasobjecten (je kunt in de glasobjecten view filteren op `KLEUR`).
2. In de gebouwen view zie je hoeveel glasobjecten er in een gebouw zitten. Bij de view van een enkel gebouw zie je alle glasobjecten die eronder vallen. 
Bij de view van een enkel glasobject zie je alle glasobjecten die in hetzelfde gebouw zitten.
3. Op basis van het `gebouwid` `9` wordt in de `glasobjecten` tabel alle rijen gezocht met `9` als waarde voor `gebouwid`.
::::
:::

Hopelijk zie je in dat een gebruikersinterface nauw samenhangt met de database structuur daaronder.

::: callout
## Opschalen
Deze interface werkt met een relatief kleine dataset met maar 2 tabellen. In theorie zou je hiervoor ook een spreadsheet als databestand kunnen gebruiken.
Maar stel je voor dat we een vergelijkbare interface voor alle noemenswaardige glasobjecten in alle 63142 monumenten in het rijksmonumentenregister zouden willen bouwen.
Dan heb je echt een database nodig om de data nog snel doorzoekbaar te houden.
:::

::::::::::::::::::::::::::::::::::::: keypoints 

- In een gebruikersinterface vind je dezelfde logica als in een database structuur

::::::::::::::::::::::::::::::::::::::::::::::::
