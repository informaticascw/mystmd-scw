+++
title = "SQL Webshop Opdracht"
weight = 3
+++

Hier vind je informatie over de SQL Webshop opdracht. Deze wordt gegeven aan havo-5 en vwo-5.

<!--more-->
2do in startcode:
- bestandsnaam voor plaatje toevoegen
- SELECT * in initiele sql
- iets met api/products/dummy
- filters verbergen in html als leeg antwoord uit api
- in hoeverre is id-veld nodig bij andere tabellen : ik denk van wel, die zou je ...

## 0. Voor de docent

### 0.1. Voorkennis en leerdoelen

Veronderstelde voorkennis voor leerlingen
- database: sql (SELECT, JOIN met 3 tabellen, WHERE, CREATE)
- api: python (variabelen, selectie, iteratie, functies, lijsten)
- website: html en css (kunnen werken met enkele html5 tags en css properties, denk aan h1-3, p, ul/li, a href, img src, div id/class, content/padding/border/margin, color/background-color)

Handige voorkennis, maar niet noodzakelijk
- database: normaliseren van een database
- api: kennis van json en basale kennis van REST api's
- website: javascript, al dan niet in combinatie met het Document Object Model

Leerdoel voor leerlingen
- Opdoen van praktisch inzicht in de werking van hedendaagse webbased systemen die gebruikt worden voor het opvragen van gestructureerde informatie. We beperken we ons tot de context van een webshop.

Leerdoelen in meer detail
- Informatie opvragen met sql uit een database met meerdere tabellen (veronderstelde voorkennis)
- Opzetten van een database met meerdere tabellen in sql
- Bepalen van de cardinaliteit van relaties tussen tabellen (1:n en n:m) in sql
- Begrijpen hoe REST-api's werken aan de hand van begrippen zoals endpoint, CRUD en json
- Uitbreiden van gegeven REST-api's in python met de fastAPI library
- Statische webpagina's in html en css aanpassen en uitbreiden (veronderstelde voorkennis)
- Begrijpen wat DOM manipulatie met de javascript is
- Aanpassen van gegeven javascript programma's die DOM manipulatie doen

### 0.2. Lesplanner

Hoofdstuk|Aantal lessen|Basis of optioneel
--|--|--
1 Inleiding | 1 | basis
2 Aanpassen | 2 | basis
3 1:n | 2 | basis
4 n:m | 2 | basis
5 Filters | 2 | optioneel
6 Front end | 2 | optioneel
7 Uitbreidingen | 2 tot 8 | optioneel
Totaal | 7 tot 19 |

Opmerkingen:
- We gaan uit van een lesduur van 45 tot 60 minuten per les.
- Hoofdstuk 1, 2, 3 en 4 bouwen op. 
- Hoofdstukken 5 en 6 staan los van elkaar maar bouwen door op hoofdstuk 1, 2, 3 en 4.
- Hoofdstuk 7 kan worden gedaan als 5 en 6 zijn overgeslagen, maar niet alle voorgestelde extra's zullen voor alle leerlingen haalbaar zijn.

### 0.3. Startcode en uitwerking

Startcode volgt

Uitwerking volgt

Een concept (work in progress) van de code staat op 
[https://github.com/informaticascw/h5v5-sql-webshop-template](https://github.com/informaticascw/h5v5-sql-webshop-template)

### 0.4. Beoordelingsmodel

volgt

### 0.5. Ontwikkelomgeving inrichten

Minimale variant voor docenten die niet eerder gewerkt hebben met GitHub.
- Laat leerlingen 1 account per groepje maken
- Laat leerlingen startcode kopieren (use template in GitHub)
- Verzamel de linkjes naar de repositories, zodat je kunt meekijken en nakijken
- Uitleg onder de ontwikkelomgeving staat in de leerlinghandleiding Codespaces (zie bijlage)
- Het kost tijd om de ontwikkelomgeving (GitHub + Codespaces + VSCode en voor docenten ook nog GitHub Classroom) te leren kennen. Een goed begin is het zelf maken van de opdracht.

Varianten voor docenten die ervaring hebben met GitHub.
- Zie minimale variant en voeg daaraan één of meerdere van onderstaande punten toe.
- Groepjes van meerdere personen met elke persoon een eigen account (voordeel: beter voor samenwerken in groepjes, complicatie: toegangsrechten tot repositories per repository instellen en merge conflicten oplossen)
- Inrichten van eigen github organisaties (voordeel: toegang tot repositories voor docenten eenvoudiger)
- Inschrijven via GitHub Classroom (voordeel: toegangsrechten automatisch ingesteld, eenvoudiger voor leerlingen om startcode te krijgen)

Aanbevolen variant voor docenten die ervaring hebben met GitHub Classroom.
- Opdracht met startcode aanmaken in Github Classroom.
- Inschrijflink verspreiden onder leerlingen.

Een uitgebreide handleiding, toegespitst op docenten die hun leerlingen deze opdracht willen laten maken, is (nog) niet beschikbaar. Er is veel informatie te vinden op internet, maar het vergt tijd om bekend te raken met de ontwikkelomgeving.

## 1. Inleiding

### 1.1. Webshop

Je mag zelf kiezen welke producten je in je webshop aanbiedt. Denk aan kleding, sieraden, clubshirts, telefoons, auto's, eten of iets anders dat jij leuk vindt. Zorg ervoor dat het netjes blijft, vraag het aan je docent als je twijfelt.

Je webshop bevat een plaatje en informatie over wat je verkoopt. Bezoekers kunnen filteren welke producten ze willen zien. Bestellen doen ze door je een mailtje te sturen.

Bezoekers kunnen niet inloggen op je webshop en er zit geen betaalmogelijkheid in de webshop. Dat maakt de webshop een stuk eenvoudiger. Bezoekers die willen bestellen sturen een mailte (of appje). De webshop houdt geen winkelmand, geen oude bestellingen en geen voorraad bij.

Je webshop maak je in een ontwikkelomgeving. Zodra je de ontwikkelomgeving afsluit, is je webshop niet meer bereikbaar. Als je wilt dat je webshop altijd bereikbaar is, dan moet je je code neerzetten op een server die altijd bereikbaar is. Dat noemen ze hosten. Je kunt een oude server gebruiken die je thuis hebt, of er eentje bij een bedrijf huren. Je webshop heeft een server met het Unix-besturingssysteem nodig. Als je dit wilt doen dan heb je handigheid met Unix nodig. Het hosten van je webshop is geen onderdeel van deze opdracht. 

### 1.2. Startcode

Je docent geeft aan hoe je aan de startcode voor deze opdracht komt.

### 1.3. Werkwijze

Je werkt op de volgende manier aan de opdrachten.

- Je gebruikt de startcode die je van de docent krijgt en je volgt de opdrachten.
- Je werkt regelmatig, minimaal één keer per les sla je werk op, dat doe je door een commit in github te zetten.
- Als je in een groepje werkt, dan programmeert iedereen even veel. De opdrachten in hoofdstuk 1 tot en met 6 maak je samen, de uitbreidingen in hoofdstuk 7 mag je verdelen.
- Je werkt op je eigen account. Als je samen aan dezelfde opdracht werkt dan gebruik je het account van degene die typt, na elke opdracht wissel je wie typt en wiens account gebruik wordt.
- Als je bronnen gebruikt, dan zet je een verwijzing naar de bron als commentaar in je code. Verwijzingen zijn linken chats op chat-gpt, tutorials op youtube of webpagina's. In elk geval moet duidelijk zijn welke stukken code je helemaal zelf hebt bedacht en waar je hulp hebt gehad. 

### 1.4. Ontwikkelomgeving
Een handleiding voor de ontwikkelomgeving die we gebruiken om deze webshop te maken staat in de bijlage.

## 2. Producten aanpassen

### Verander de naam van producten (database)
Gegevens aanpassen

### Verander de plaatjes van producten (database)
Bestand aanpassen

### Voeg een product toe (database)
Voeg regel toe aan de tabel products

### Voeg een prijs toe (database)
Maak een extra veld `price`

### Voeg een beschrijving toe (database)
Maak een extra veld `description`

## 3. Soort aan product toevoegen
1:n relaties toevoegen

### maak tabel met soorten (database)
create table
insert

### maak veld dat product aan soort koppelt (database)
voeg verwijzende sleutel toe
laat de naam eindigen op _id, dan kan onze website er goed mee omgaan

### beschrijf cardinaliteit (database)
voeg constraint toe

### koppel producten aan soort (database)
vul verwijzingen in

### api (uitleg)
api verbindt de database met de website

back end: api en database
front end: website

webserver voor static files, bij ons in de api, bij grotere projecten vaak op aparte servers. Database draait ook vaak op één of meerdere aparte servers.

### voeg soort toe aan query (api)
api aanpassing: query met join

### niet benodigde velden verwijderen (niet nodig, verwijderen) / namen van velden aanpassen (api)
speciale velden: name, price, description uit de tabel products worden herkend in de html en op speciale wijze getoond
het veld id de tabel products en velden die eindigen op _id worden herkend in de html en niet getoond, deze zijn wel handig om erin te houden

de website gebruikt de naam van de velden, meestal zijn die Engelstalig. Het is handig om die in de api aan te passen
AS gebruiken

## 4. Kleuren aan product toevoegen
In ons voorbeeld bestaat een product uit één of meer kleuren en een kleur wordt gebruikt in één of meerdere producten. Dat betekent dat er een n:m (spreek uit als "en op em") relatie tussen producten en kleuren. Andere voorbeelden van een n:m relatie zijn materialen of ingrediënten.

### Maak tabel met kleuren (database)
create table
insert

### Maak tabel die producten en kleuren koppelt (database)

### Beschrijf cardinaliteit (database)
voeg constraint toe

### Geef aan welke producten en kleuren bij elkaar horen (database)
vul verwijzingen in

### Json (uitleg)
api geeft resultaten in de vorm van json
- key value pairs
- dict
- list
voorbeeld

### Maak query voor kleuren per product (api)
api aanpassing: query met join
juiste velden selecteren

### Voeg kleurinformatie toe aan producten (api)

## 5. Filters maken

### 5.1 REST API (uitleg)

#### REST

API (Engels, spreek uit ee-pie-aai) staat voor Application Programming Interace. Een API is een stuk software dat computerprogramma op een gestandaardiseerde manier met elkaar verbindt. Een API tussen computerprogramma's die via het internet met elkaar zijn verbonden heet een webservice. Een webservice wordt aangeboden door een server en gebruikt door één of meerdere clients. Moderne webservices zijn RESTful (Engels, spreek uit als rest-foel). REST staat voor REpresentational State Transfer, maar meestal wordt alleen de afkorting gebruikt. REST is geen protocol maar een set ontwerp-richtlijnen.

Hier volgen enkele ontwerp-richtlijnen van REST.

-  _Platform-onafhankelijk_

    REST werkt via standaardprotocollen zoals HTTP en maakt gebruik van eenvoudige dataformaten zoals JSON. Daardoor kunnen verschillende systemen zoals Windows, Linux, iOS en Android probleemloos met elkaar communiceren.

-  _Client-Server scheiding_

    De client (zoals een app of website) en de server (waar de gegevens staan) werken onafhankelijk van elkaar. De client weet alleen wat hij nodig heeft, niet hoe de server dat regelt. Dit maakt onderhoud en ontwikkeling eenvoudiger: de client-zijde (frontend) en server-zijde (backend) kunnen apart worden aangepast.

-  _Statusloos_

    Elke aanvraag (request) van de client bevat alle informatie die de server nodig heeft. De server bewaart geen gegevens over vorige aanvragen. Daardoor zijn REST API’s gemakkelijk uit te breiden en te beheren.

Clients en servers met REST API's communiceren met HTTP. Dit is hetzelfde protocol dat webbrowsers gebruiken om een webpagina van een server op te vragen. De client verstuurt een HTTP-request naar de server. De server antwoordt met een HTTP-response.

#### HTTP-request

Een request is een bericht van de client (bijvoorbeeld een browser of app) naar de server (API). Hiermee vraag je iets op, voeg je iets toe, of verander/verwijder je iets.

Een request bestaat uit:

- Method (actie die je uitvoert – gebaseerd op CRUD):
  - GET – Gegevens opvragen (Read)
  - POST – Nieuwe gegevens aanmaken (Create)
  - PUT – Gegevens volledig bijwerken (Update)
  - DELETE – Gegevens verwijderen (Delete)
- Endpoint: De link naar de resource, zoals /gebruikers/42.
- Headers: bijvoorbeeld
 - Content-Type: Geeft aan in welk formaat je data stuurt (bijv. application/json)
 - Authorization: Bevat een token of API-key voor toegang tot beveiligde data
- Body (optioneel): De gegevens die je meestuurt, bijvoorbeeld een JSON-object bij POST of PUT.

#### HTTP-response

Een response is het antwoord van de server op het verzoek van de client.

Een response bevat:

- Statuscode (resultaat van de aanvraag), bijvoorbeeld:
  - 200 OK – Alles is goed verlopen
  - 401 Unauthorized – Geen toegang (bijv. geen of fout token)
  - 404 Not Found – Gevraagde resource bestaat niet
  - 500 Internal Server Error – Fout aan serverzijde
- Headers: Extra info over het antwoord, zoals het dataformaat
- Body: De gegevens die teruggestuurd worden (bijv. een lijst, een bevestiging of een foutmelding)

#### Structuur van endpoints

Er zijn geen harde regels voor de structuur van endpoints. Er zijn wel tips die helpen bij het maken van een goede structuur. 

Hier zijn enkele tips voor de structuur van endpoints.

- _Gebruik hiërarchie voor subresources_

    Geef aan dat iets *onderdeel* is van iets anders:

    ✅ /gebruikers/42/boeken → alle boeken van gebruiker 42  

    ✅ /klassen/5v/leerlingen → alle leerlingen in klas 5v

- _Gebruik queryparameters voor filters, sorteren of paginering_

    Bijv. als je iets zoekt of sorteert:

    ✅ /boeken?jaar=2024  

    ✅ /gebruikers?rol=docent&sort=naam  

- _Gebruik zelfstandige naamwoorden in meervoud, geen werkwoorden_

    Endpoints gaan over **resources** (zoals gebruikers, boeken, producten). Gebruik dus meervoud:

    ✅ /gebruikers

    ❌ /gebruiker

    De HTTP-methodes (`GET`, `POST`, enz.) geven al aan *wat* je doet. Dus geen `getGebruiker`, `deleteUser`, enzovoort:

    ✅ /gebruikers

    ❌ /getGebruiker

- _Gebruik koppelstreepjes tussen woorden, geen hoofdletters_

    Koppeltekens zijn beter leesbaar in linken:

    ✅ /middelbare-scholen

    ❌ /middelbare_scholen

    Gebruik kleine letters:

    ✅ /middelbare-scholen

    ❌ /Middelbare-Scholen

- _Houd het consistent_

    Gebruik een duidelijke en eenduidige structuur door je hele API. Als je bijvoorbeeld `/producten` gebruikt, noem het dan niet ergens anders `/artikelen`.

### Maak filters voor soort

### Maak filters voor kleur

### 5.4 Extra gegevens in een request (uitleg)

Bij het gebruiken van een REST API kun je informatie op verschillende manieren meegeven in een request. Hier zijn de drie meest gebruikte manieren:

-  Informatie in het endpoint zelf (path parameters)

    - Je stopt informatie direct in de link, als onderdeel van het pad.
    - Dit gebruik je voor het opvragen van een specifiek item.
    - Bijvoorbeeld:
        - `/leerlingen/42` → vraag leerling met ID 42 op
        - `/boeken/9783` → vraag boek met ISBN 9783 op
    - Het getal of woord in de link wordt herkend als een parameter.


- Informatie achter het endpoint met `?` (query parameters)

    - Je zet parameters achter een vraagteken in de link.
    - Dit wordt gebruikt om informatie mee te geven voor filteren, zoeken, sorteren of pagineren.
    - Bijvoorbeeld:
        - `/leerlingen?klas=5V`
        - `/producten?categorie=boeken&sort=prijs`
    - Meerdere parameters worden gescheiden met een `&`, meerdere waarden voor dezelfde parameter worden gescheiden door een `,`.

- Informatie in de body (bij POST en PUT)

    - Stuur de gegevens mee in de body van de request, meestal in JSON-formaat.
    - Dit gebruik je als je gegevens aanmaakt of bijwerkt.
    - Dit zie bijvoorbeeld bij:
        - `POST /leerlingen` → nieuwe leerling toevoegen
        - `PUT /gebruikers/42` → gebruiker met ID 42 aanpassen
    - De data staat niet in de link, maar wordt meegestuurd in de inhoud van het verzoek.

### Zorg dat filters werken (copy code)

## 6. front end aanpassingen

### Pas kleuren aan (css)

### Maak aparte bestelpagina (html)

### 6.3 DOM (uitleg)

#### Wat is de DOM?

De DOM (Document Object Model) is een boomstructuur die je browser maakt van een HTML-pagina.  
Elke tag in de HTML (zoals `<h1>`, `<div>`, `<p>`) wordt een object in die boom. 
JavaScript kan via de DOM elementen zoeken, toevoegen, of aanpassen.

JavaScript is een programmeertaal die elke browser begrijpt. Veel webpagina's bevatten JavaScript-code. Je kunt JavaScript-code vinden tussen de tag `<script>` in een `.html`-bestand of in een bestand met een naam die eindigt op `.js`.

#### Objecten zoeken

Met JavaScript kun je bestaande elementen op verschillenden manieren in de DOM zoeken, bijvoorbeeld:

```javascript
element = document.getElementById("mijn-lijst");
anotherElement = document.querySelector(".knop");
```

#### Objecten toevoegen

Je kunt nieuwe elementen maken en aan de DOM toevoegen:

```javascript
parent = document.getElementById("mijn-lijst");
let newChild = document.createElement("li");
newChild.textContent = "Hallo!";
parent.appendChild(newChild);
```

Hier maak je een nieuw list-item en voeg je die toe aan het einde van de lijst.

#### Objecten wijzigen

Je kunt een DOM-element aanpassen door het in een variabele te stoppen en vervolgens de eigenschappen van het object te veranderen.

Voorbeeld:

```javascript
let knop = document.querySelector(".knop");
knop.textContent = "Klik hier!";
```

Dit verandert de echte knop op de pagina, want `knop` wijst naar het originele object. Niet de hele knop met alles erin is gekopieerd, maar alleen het geheugenadres dat wijst naar de knop is gekopieerd. De variabele `knop` noem je een variabele by reference.

### Maak aparte pagina per product (javascript)

## 7. Uitbreidingen
- 1 pagina per product toevoegen (nieuw entrypoint :id, nieuwe static webpagina, aangepast javascript, linkje op oude webpagina)
- 1 bestelpagina (nieuwe static webpagina)
- meer tabellen en producten
- wie dit kocht kocht ook dat / dit product past bij deze producten 
- sorteren
- meerdere plaatjes per product
- verschillende eigenschappen per soort (1:1)
- varianten, zoals maten
- prijs range filter 
- ...

## 8. Bijlage: Leerlinghandleiding Codespaces

Zie
[https://stanislas.informatica.nu/help/codespaces/](https://stanislas.informatica.nu/help/codespaces/)