---
title: API's bouwen vanaf nul met de API Designer
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overzicht

Geen OpenAPI-specificatie? Geen probleem! Met ReadMe's API Designer kun je je API-referentie rechtstreeks in het platform bouwen via een intuïtieve visuele interface – geen YAML of JSON vereist.

In deze handleiding lopen we door het aanmaken van een Social Media API met endpoints voor het weergeven en aanmaken van berichten. Je zult zien hoe eenvoudig het is om je API te documenteren, zelfs als je vanaf een blanco pagina begint.

## Je API-definitie aanmaken

Laten we beginnen met het opzetten van de basisstructuur voor je API:

1. Navigeer naar **API Reference** in je ReadMe-project
2. Klik op de knop **+ Add**
3. Selecteer **Start Building** onder "Build an API definition from scratch"

<Image align="center" border={false} src="https://files.readme.io/f9e241f98e3e8ad91e999561f4e3b4dfe260a8e6a18662e23da840887977b6c7-CleanShot_2025-03-11_at_11.18.13.gif" />

4. Voer de details van je API-definitie in:
   * **API Title**: Voer een beschrijvende naam in (bijv. "Social Media API")
   * **Target Host URL**: De basis-URL van je API (bijv. "[http://api.example.com](http://api.example.com)")
   * **Authentication Type**: Selecteer je authenticatiemethode (None, API Key, Basic of Bearer)

<Image align="center" border={false} src="https://files.readme.io/7a81519f9faf96f4af361d26c405792fe78488558a9c8e972d084d102dda098e-CleanShot_2025-03-11_at_11.21.07.gif" />

5. Klik op **Save** om je API-definitie aan te maken

Je nieuwe API-definitie verschijnt in het linker navigatiepaneel, klaar om endpoints aan toe te voegen.

## Je eerste endpoint aanmaken (Sociale mediaposts weergeven)

Laten we een endpoint aanmaken om een lijst van sociale mediaposts op te halen:

1. In de linker navigatie zie je een standaard endpoint met het label `/new-endpoint`
2. Hernoem dit om je API-structuur beter weer te geven – laten we het "Posts" noemen
3. Je ziet deze categorie nu in je linker navigatie

<Image align="center" border={false} src="https://files.readme.io/fc908c66586d12aa0327f1bc17d60a045a23e550e82161ae4818a37eb91b3931-CleanShot_2025-03-11_at_11.29.12.gif" />

4. Maak je GET-endpoint aan voor het weergeven van berichten:
   * Klik op het endpoint om het te bewerken
   * Verander de titel naar "List Social Media Posts"
   * Selecteer de methode **GET** uit het dropdownmenu
   * Stel het pad in op `/posts`
   * Voeg een beschrijving toe die uitlegt wat het endpoint doet (bijv. "Geeft een gepagineerde lijst van sociale mediaposts terug")

<Image align="center" border={false} src="https://files.readme.io/72e65717ef6534caa7b0d2a187deb7125b1466bc72a95a8fdcd7459267ae8b35-CleanShot_2025-03-11_at_11.31.27.gif" />

### Queryparameters toevoegen

De meeste lijstendpoints ondersteunen paginering of filtering. Laten we enkele queryparameters toevoegen:

1. Zoek de sectie **Query Parameters** en klik op de knop **+**
2. Voeg parameters toe voor paginering:
   * Voeg een parameter `page` toe van het type `integer`
   * Voeg een parameter `limit` toe van het type `integer`
   * Voeg eventuele andere filterparameters toe (bijv. `category` als een `string`)
3. Voor elke parameter:
   * Voeg een beschrijving toe
   * Geef aan of deze verplicht is
   * Geef een standaardwaarde op indien van toepassing

<Image align="center" border={false} src="https://files.readme.io/c596d7f09014adbfb1166f81b10936c0427f6b0e4a4c1cc9f2983a51c55aaa55-CleanShot_2025-03-11_at_11.35.30.gif" />

<br />

## Je tweede endpoint aanmaken (Een sociale mediabericht aanmaken)

Laten we nu een endpoint toevoegen voor het aanmaken van nieuwe berichten:

1. Klik in de linker navigatie op de knop **+ New Category** als je een nieuwe categorie nodig hebt, of gebruik je bestaande categorie "Posts"
2. Klik op het +-pictogram om een nieuw endpoint toe te voegen
3. Stel je POST-endpoint in:
   * Titel: "Create New Post"
   * Methode: Selecteer **POST** uit het dropdown
   * Pad: `/posts`
   * Beschrijving: "Stelt geauthenticeerde gebruikers in staat nieuwe berichten aan te maken"

<Image align="center" border={false} src="https://files.readme.io/fa7c7a03010f8fdbc0bee4ff32db7a11e34f723f3640ed6e3f311234e93dd2bd-CleanShot_2025-03-11_at_11.52.25.gif" />

### Parameters voor de request body toevoegen

Voor een POST-endpoint moet je de request body definiëren:

1. Zoek de sectie **Request Body** en klik om deze uit te vouwen
2. Stel het inhoudstype in op `object`
3. Voeg de verplichte velden toe:
   * Voeg een veld `content` toe van het type `string` en markeer het als verplicht
   * Voeg eventuele aanvullende velden toe die je API accepteert (bijv. `image_url`, `tags`)
4. Voor elk veld:
   * Voeg een duidelijke beschrijving toe
   * Geef aan of het verplicht is
   * Geef eventuele beperkingen op (min/max lengte, patroon, enz.)

<Image align="center" border={false} src="https://files.readme.io/2a114a0bb8cfab72df455ea87638aa51d75a1ea3b931987fc18d1450f94cb08d-CleanShot_2025-03-11_at_11.57.21.gif" />

### Codevoorbeelden voor requests toevoegen

Een van de krachtige functies van ReadMe is het automatisch genereren van codevoorbeelden:

1. Zoek de sectie **Request Code** aan de rechterkant
2. ReadMe genereert automatisch codevoorbeelden in meerdere talen
3. Je kunt ook op "Write your own static samples" klikken om aangepaste voorbeelden toe te voegen

<Image align="center" border={false} src="https://files.readme.io/646ce4e3467087d3d7b8396632e29af646bf02be9113054d0c63e69c14561a6c-CleanShot_2025-03-11_at_12.03.35.gif" />

<br />

## Je API-documentatie testen

Na het aanmaken van je endpoints:

1. Sla je wijzigingen op
2. Schakel naar de modus "View" om te zien hoe je documentatie eruitziet voor ontwikkelaars
3. Test de interactieve functies om te controleren of je voorbeelden correct werken

## Tips voor geweldige API-documentatie

* **Wees grondig met beschrijvingen**: Leg duidelijk uit wat elk endpoint doet en waarom
* **Geef realistische voorbeelden**: Gebruik voorbeelddata die lijkt op gebruik in de echte wereld
* **Documenteer foutstatussen**: Voeg voorbeelden toe van foutreacties en hoe je daarmee omgaat
* **Gebruik consistente naamgeving**: Handhaaf een consistente stijl voor alle endpoints en parameters
* **Voeg "What's Next" toe**: Gebruik de sectie "What's Next" om gebruikers te begeleiden naar gerelateerde endpoints die ze mogelijk nodig hebben

Door deze handleiding te volgen, heb je vanaf nul een goed gedocumenteerde API-referentie aangemaakt met ReadMe's API Designer. Je ontwikkelaars beschikken nu over interactieve, duidelijke documentatie die hen helpt snel en eenvoudig te integreren met je API.

Onthoud dat je altijd terug kunt keren naar de API Designer om endpoints toe te voegen, parameters bij te werken of je documentatie te verbeteren naarmate je API zich ontwikkelt.

<br />

## Momenteel niet-ondersteunde OpenAPI-functies in de API Designer

We ondersteunen momenteel niet alle OpenAPI-functies in onze API Designer. Als je een van deze functies in een endpoint gebruikt, kun je ze niet bewerken in onze UI. Deze endpoints worden echter nog steeds correct weergegeven in de documentatie en kunnen nog steeds worden bijgewerkt door het OpenAPI-bestand rechtstreeks te bewerken.

<br />

| Niet-ondersteunde OpenAPI-functie | Uitleg                                                                                                                                                                                                          | OpenAPI-documentatie                                                                                                                       |
| --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Additional Properties             | Het sleutelwoord additionalProperties wordt binnen een schema gebruikt om te definiëren of eigenschappen die niet expliciet in het schema zijn gedefinieerd, zijn toegestaan in objecten, en zo ja, welke typen ze moeten hebben. | [Dictionaries, HashMaps and Associative Arrays](https://swagger.io/docs/specification/v3_0/data-models/dictionaries/)                      |
| Callbacks/Webhooks                | OpenAPI heeft een functie om endpoints te definiëren die een API-aanroep doen zodra een gebeurtenis is voltooid.                                                                                                | [Callbacks](https://swagger.io/docs/specification/v3_0/callbacks/)                                                                         |
| References                        | Elk endpoint dat een object definieert met behulp van een $ref.                                                                                                                                                 | [Using Ref](https://swagger.io/docs/specification/v3_0/using-ref/)                                                                         |
| Common Parameters                 | Endpoints waarbij parameters worden gedefinieerd op padniveau in plaats van op methodeniveau, zodat de parameters worden gedeeld tussen alle methoden voor die URL.                                             | [Describing Parameters](https://swagger.io/docs/specification/v3_0/describing-parameters/#common-parameters)                               |
| Links                             | Links zijn een OpenAPI-functie die beschrijft hoe de reacties van één endpoint kunnen worden gebruikt als invoer voor andere bewerkingen.                                                                       | [Links](https://swagger.io/docs/specification/v3_0/links/)                                                                                 |
| Polymorphism                      | Polymorfisme stelt je in staat een schema te definiëren dat meerdere typen of modellen kan vertegenwoordigen.                                                                                                   | [Inheritance and Polymorphism](https://swagger.io/docs/specification/v3_0/data-models/inheritance-and-polymorphism/?sbsearch=Polymorphism) |
| Server Variables                  | Variabelen kunnen worden gedefinieerd in het basispad en kunnen een vooraf ingestelde lijst met waarden hebben waaruit de gebruiker kan kiezen.                                                                  | [API Server and Base Path](https://swagger.io/docs/specification/v3_0/api-host-and-base-path/?sbsearch=server%20variables)                 |
| Style                             | Het sleutelwoord Style maakt configuratie mogelijk voor hoe meerdere waarden aan een parameter moeten worden doorgegeven.                                                                                       | [Parameter Serialization](https://swagger.io/docs/specification/v3_0/serialization/?sbsearch=Styles)                                       |
| XML                               | Endpoints die XML-gegevens accepteren of beantwoorden.                                                                                                                                                          | [Representing XML](https://swagger.io/docs/specification/v3_0/data-models/representing-xml/?sbsearch=xml)                                  |