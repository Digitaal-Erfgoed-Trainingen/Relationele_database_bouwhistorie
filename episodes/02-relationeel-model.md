---
title: "Het relationele model"
teaching: 5 
exercises: 15 
---

:::::::::::::::::::::::::::::::::::::: questions 

- Wat is een relationeel model?
- Wat is de meerwaarde van een relationeel model?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Beperkingen van spreadsheets opsommen
- Uitleggen wat een relationeel model is
- Beperkingen van het relationele model opsommen

::::::::::::::::::::::::::::::::::::::::::::::::
::: instructor
Afhankelijk van het niveau en tempo van de groep en de tijd die je hebt kun je ervoor kiezen om 
een deel van de opdrachten klassikaal te doen. 
We raden dan aan om de eerste opdracht 'Beperkingen van spreadsheets' wel individueel te doen, 
vervolgens kun je de vragen bij 'Beperkingen van het relationele model' en 'Wat zijn voor en nadelen van het relationeel model?'
klassikaal stellen.
:::

Voor dit hoofdstuk heb je hebt de bestanden `historisch-glas-in-gebouwen_plat.xlsx` en `historisch-glas-in-gebouwen_relationeel.xlsx` nodig.
[Volg hier de downloadinstructies](learners/setup.md#glas-in-gebouwen-dataset).

::: challenge
## Beperkingen van spreadsheets
Bekijk het bestand `historisch-glas-in-gebouwen_plat.xlsx`.

1. Je wilt het adres aanpassen van het gebouw Jachthuis Sint Hubertus. Hoeveel rijen moet je aanpassen?

Bekijk nu het bestand `historisch-glas-in-gebouwen_relationeel.xlsx`.

2. Je wilt het adres aanpassen van het gebouw Jachthuis Sint Hubertus. Hoeveel rijen moet je aanpassen?
3. Stel dat je per gebouw tientallen glasobjecten in de dataset hebt. 
En dat je vaak informatie over gebouwen moet aanpassen, naar welk format gaat je voorkeur uit? 

:::: solution
## Oplossing

1. 3 rijen
2. 1 rij
3. Het format in `historisch-glas-in-gebouwen_relationeel.xlsx` is dan beter. Je hoeft dan telkens maar 1 rij aan te passen 
in plaats van tientallen rijen. Dit is een stuk minder foutgevoelig.
::::
:::


## Relationeel model
Bovenstaande opdracht toont aan dat het handig kan zijn om verschillende typen data
in verschillende tabellen te zetten.
Dus een tabel met informatie over glasobjecten en een tabel met informatie over gebouwen.

Als we onze data zo organiseren gebruiken we een *relationeel model*. 
Verschillende typen data staan in verschillende tabellen, en hebben bepaalde **relaties** met elkaar.
In dit geval is een glasobject gekoppeld aan een bepaald gebouw in de `gebouwen` tabel via kolom `gebouwid`.

Dit is precies hoe data in een **relationele database** is georganiseerd. 

::: callout
## Technische termen
We hebben nu stiekem al een aantal concepten in database-land geleerd. 
Dit zijn de technische termen die daarbij horen: 

- **Primary key**: Een *primary key* (primaire sleutel) is een attribuut of combinatie van attributen die 
een unieke verwijzing naar een bepaalde rij is. In het voorbeeld is dit de unieke identificatiecode (UID) in de 2 tabellen:
`gebouwid` in de `gebouwen` tabel en `objectid` in de `glasobjecten` tabel.
- **Foreign key**: De *foreign key* (vreemde sleutel) is een attribuut of combinatie van attributen die een unieke verwijzing
naar een bepaalde rij **in een andere tabel** is. De *foreign key* komt dus overeen met de primary key van die tabel.
In het voorbeeld is dit `gebouwid` in de `glasobjecten` tabel die refereert naar een specifieke rij in de `gebouwen` tabel.
- **One-to-Many relatie**: Één rij in een tabel is gelinkt aan meerdere rijen in een andere tabel. Voorbeeld: 1 gebouw bevat meerdere glasobjecten.
Naast *One-to-Many* relaties bestaan er meerdere *cardinality* (kardinaliteit) types, zoals One-to-One, Many-to-many.
:::

::: challenge
## Beperkingen van het relationele model
Bekijk het bestand `historisch-glas-in-gebouwen_plat.xlsx`.

1. Je wilt alle glasobjecten analyseren die zich in gebouwen in Zuid-Holland bevinden.
Beschrijf de stappen die je moet doorlopen om de juiste data te filteren. (Je hoeft het niet echt te doen)

Bekijk nu het bestand `historisch-glas-in-gebouwen_relationeel-model.xlsx`.

2. Je wilt alle glasobjecten analyseren die zich in gebouwen in Zuid-Holland bevinden.
Beschrijf de stappen die je moet doorlopen om de juiste data te filteren. (Je hoeft het niet echt te doen)

:::: solution
1. Je kunt de `Provincie` kolom filteren op de waarde `Zuid-Holland`.
2. Stap 1: Filter de gebouwen met `Zuid-Holland` als waarde in de kolom `Provincie`. 
Stap 2: Gebruik de `gebouwid` van deze gebouwen om de glasobjecten te filteren.
::::
:::

::: challenge
## Wat zijn voor en nadelen van het relationele model?
1. Wat zijn voordelen van het relationele model?
2. Wat zijn nadelen van het relationele model?

:::: solution
. <!--- Nodig voor juiste rendering --->

### Voordelen van het relationele model
- Je breekt informatie op in logische *units*, hoe meer data hoe belangrijker dit is om het overzicht te behouden.
- Gegevens aanpassen is minder foutgevoelig.
- Bij een grote dataset (>10.000 *records*) wordt het al gauw ondoenbaar om nog in spreadsheet software te werken. 
Met een relationele database werkt het nog steeds supersnel.

### Nadelen van het relationele model
- Als je gewend bent om met spreadsheets te werken kunnen al die verschillende tabellen onoverzichtelijk worden.
- Voor analyse of data extractie moet je gebruik maken van een query om data uit verschillende tabellen te aggregeren.

::::
:::

::: callout
## Discussie
Wat is de 'grens' (in grootte, complexiteit van de data) wanneer het handig wordt een relationeel model en database te gebruiken?
:::


::::::::::::::::::::::::::::::::::::: keypoints 

- In een relationeel model staan verschillende typen data in verschillende tabellen die met elkaar gekoppeld zijn.

::::::::::::::::::::::::::::::::::::::::::::::::

