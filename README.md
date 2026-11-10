# Relationeel model en database-gebruik voor bouwhistorie data

De module 'Relationeel model en database-gebruik voor bouwhistorie' data is ontwikkeld voor erfgoedvrijwilligers en professionals die systematisch gegevens verzamelen over bouwhistorische objecten. 
De module laat je de meerwaarde zien van het gebruik van een relationeel model en laat je proeven aan de kracht van database-gebruik. 

## Voor wie is deze module?

We raden aan deze module te volgen na de module [Dataorganisatie in spreadsheets voor bouwhistorie](https://digitaal-erfgoed-trainingen.github.io/Dataorganisatie_spreadsheets_bouwhistorie/), 
maar de module kan ook op zichzelf gevolgd worden als de cursist bekend is met dataorganisatie in spreadsheets.

De module is echt bedoeld als **inzicht geven in** het relationele model en gebruik van databases,
**specifiek niet het aanleren van vaardigheden om met databases om te gaan**.
In het laatste hoofdstuk geven we de volgende stappen aan om die vaardigheden echt te leren.
Het idee van deze aanpak is dat het nuttig is wanneer je data verzameld in een spreadsheet om alvast een beeld te hebben 
van hoe de data uiteindelijk terecht kan komen in een database.

De casuïstiek is weliswaar glas voor bouwhistorie, maar de lessen zijn ook bruikbaar voor andere (sub) domeinen.

## Deze module geven?
Dit lesmateriaal is openbaar en kan vrij en gratis gebruikt worden. Ben je van plan de module te gebruiken? 
We helpen je graag bij de voorbereiding en krijgen ook graag feedback op de module. 
Laat ons weten als je de module gaat geven door te mailen naar [m.dekleijn@cultureelerfgoed.nl](mailto:m.dekleijn@cultureelerfgoed.nl). 

## Bijdragen
Als je wilt bijdragen aan deze module, neem dan contact op met Maurice de Kleijn ([m.dekleijn@cultureelerfgoed.nl](mailto:m.dekleijn@cultureelerfgoed.nl)).

## Lokaal draaien
Om deze module lokaal te bouwen, volg je de [installatie-instructies voor de Workbench](https://carpentries.github.io/sandpaper-docs/#overview). 
Kort gezegd: 
- Zorg er voor dat R, Git en Pandoc zijn geïnstalleerd. 
- Open vervolgens R en run de volgende commands in de console om de benodigde 
infrastructuurpakketten te installeren of bij te werken:
```R
install.packages(c("sandpaper", "varnish", "pegboard"),
  repos = c("https://carpentries.r-universe.dev/", getOption("repos")))
```

Om te renderen, run:
```R
sandpaper::serve()
```
Bekijk ook de [Carpentries Workbench](https://carpentries.github.io/workbench/#usage) instructies.

## Beheerders
Maurice de Kleijn ([m.dekleijn@cultureelerfgoed.nl](mailto:m.dekleijn@cultureelerfgoed.nl))
Sven van der Burg
Olivier Wieringa