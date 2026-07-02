---
title: Handleidingen aanmaken en beheren
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overzicht

Laten we ingaan op de details van het organiseren van je documentatie in ReadMe. Van het aanmaken van nieuwe handleidingen tot het beheren van content in de loop van de tijd: deze gids laat je zien hoe je een goed gestructureerde kennisbank opbouwt en onderhoudt die ontwikkelaars helpt precies te vinden wat ze nodig hebben, wanneer ze het nodig hebben.

### Waarom handleidingen belangrijk zijn

Handleidingen vormen de ruggengraat van je ontwikkelaarsdocumentatie. Terwijl je API-referentie ontwikkelaars vertelt wat er mogelijk is, laten handleidingen zien hoe ze succesvol kunnen zijn. Goede handleidingen:

* Begeleiden ontwikkelaars van beginner tot expert
* Bieden context die API-referenties niet kunnen vastleggen
* Beantwoorden het "waarom" naast het "hoe"
* Lossen echte problemen op waar ontwikkelaars tegenaan lopen

## Je eerste handleiding aanmaken

### Categorieën aanmaken 📂

Categorieën helpen je documentatie te organiseren in logische secties, vergelijkbaar met hoofdstukken in het verhaal van je API. Elke categorie zorgt voor een natuurlijke overgang in de verhaallijn van je documentatie, waardoor het voor ontwikkelaars gemakkelijker wordt om de draad te volgen.

1. Navigeer naar je documentatiehub en schakel over naar de **Bewerkmodus**.
2. Klik op de knop **+ NIEUWE CATEGORIE** in de zijbalknavigatie.
3. Voer een naam in voor je categorie (bijv. "Aan de slag" of "Geavanceerde onderwerpen")
4. Klik op **Enter** om op te slaan.

> 📘 Gebruikerservaring
>
> Denk aan de reis van je ontwikkelaar bij het benoemen van categorieën. Wat zou het meest logisch zijn voor iemand die je API voor het eerst verkent? Overweeg categorieën te organiseren op vaardigheidsniveau (beginner tot gevorderd) of op gebruiksscenario.

### Een handleidingpagina aanmaken 📝

Nu je categorieën zijn ingesteld, gaan we pagina's toevoegen:

1. Beweeg in de **Bewerk**modus over een categorie en klik op de **+** knop
2. Vul de essentiële details in:
   * **Titel**: Maak deze duidelijk en beschrijvend
   * **Slug**: Dit wordt het URL-pad (automatisch gegenereerd, maar je kunt het aanpassen)
   * **Verborgen**: Zet dit aan als je aan de handleiding wilt werken voordat je deze openbaar maakt
3. Klik op **Opslaan** om je nieuwe handleiding aan te maken

### De editor-UI gebruiken ✏️

<Image align="left" border={false} width="50% " src="https://files.readme.io/53c229bb50f36b2a6398894e5de72e9909397911c2deba6c77e629733e714a99-Editing_UI_-_view_to_edit_toggle.gif" />

<br />

<br />

<br />

<br />

<br />

<br />

Met de bewerkings-UI van ReadMe maak en bewerk je content rechtstreeks op je hub. Dit betekent dat wat je ziet precies is wat je ontwikkelaars zullen zien.

1. Na het aanmaken van je pagina ben je automatisch in de editor
2. Gebruik de opmaakwerkbalk voor eenvoudige tekstopmaak
3. Typ `/` om het opdrachtmenu te openen voor het invoegen van:
   * Codeblokken
   * Callouts
   * Afbeeldingen
   * En meer!
4. Schakel tussen de modi **Bewerken** en **Bekijken** om precies te zien hoe je content er voor ontwikkelaars uitziet

<Image align="center" border={false} src="https://files.readme.io/a106664539184b9eebb366fd2c51ed5ba10ca5c1224c0ce52a209dd8c08ac143-CleanShot_2024-11-08_at_20.24.59.gif" />

> 📘 Volledige controle over je Markdown
>
> Met de Raw-modus van ReadMe kun je nieuwe content toevoegen en bestaande content rechtstreeks in Markdown bewerken. Open gewoon het menu met drie puntjes naast de zichtbaarheidsinstellingen en kies **Raw-modus**.

## Effectieve handleidingen structureren

### De anatomie van een goede handleiding

Succesvolle handleidingen volgen een consistente structuur die ontwikkelaars helpt informatie snel te begrijpen en toe te passen:

1. **Duidelijke inleiding**: Welk probleem lost deze handleiding op?
2. **Vereisten**: Wat moeten ontwikkelaars weten of hebben voordat ze beginnen?
3. **Stapsgewijze instructies**: Verdeel complexe processen in beheersbare stappen
4. **Codevoorbeelden**: Laat zien, vertel niet alleen
5. **Probleemoplossing**: Behandel veelvoorkomende problemen en hun oplossingen
6. **Volgende stappen**: Waar moeten ontwikkelaars naartoe na het voltooien van deze handleiding?

### Schrijven voor ontwikkelaars

Onthoud bij het schrijven van handleidingen dat ontwikkelaars problemen snel willen oplossen:

* **Wees beknopt**: Kom ter zake en vermijd onnodige uitleg
* **Gebruik ruimschoots codevoorbeelden**: Ontwikkelaars begrijpen code vaak sneller dan tekst
* **Markeer belangrijke informatie**: Gebruik callouts voor waarschuwingen, tips en belangrijke opmerkingen
* **Breek tekst op**: Gebruik koppen, lijsten en korte alinea's om de leesbaarheid te verbeteren
* **Gebruik praktijkvoorbeelden**: Toon code die echte problemen oplost

> 📘 Blijf realistisch
>
> Gebruik authentieke codevoorbeelden die realistische implementaties demonstreren. Als je authenticatie laat zien, gebruik dan een volledig voorbeeld met foutafhandeling. Als je gegevensophaling demonstreert, laat dan zien hoe je die gegevens op een praktische manier verwerkt en gebruikt. Praktijkvoorbeelden helpen ontwikkelaars de kloof tussen documentatie en implementatie te overbruggen.

```javascript
// Good example - with meaningful comments and clear variable names
const apiKey = 'your_api_key_here';

// Initialize the client with your API key
const client = new ReadMeAPI(apiKey);

// Fetch user data and handle potential errors
try {
  const userData = await client.getUser(userId);
  console.log(`Found user: ${userData.name}`);
} catch (error) {
  console.error(`Error fetching user: ${error.message}`);
}
```

## Handleidingen verbeteren met MDX

ReadMe ondersteunt nu MDX (Markdown + JSX), waarmee je interactieve documentatie kunt maken met herbruikbare componenten.

### Basis MDX-componenten

Hier is een voorbeeld van onze ingebouwde MDX-tabcomponenten die je kunt gebruiken om je handleidingen te verbeteren:

<Tabs>
  <Tab title="Node.js">
    ```javascript
    const client = new ReadMeAPI(apiKey);
    ```
  </Tab>

  <Tab title="Python">
    ```python
    client = ReadMeAPI(api_key)
    ```
  </Tab>

  <Tab title="Ruby">
    ```ruby
    client = ReadMeAPI.new(api_key)
    ```
  </Tab>
</Tabs>

### Herbruikbare content aanmaken

Voor content die je in meerdere handleidingen gebruikt, [maak herbruikbare contentblokken aan](doc:reusable-content)

1. Navigeer naar **Contentinstellingen** in de bewerkings-UI
2. Selecteer **Herbruikbare content**
3. Maak blokken aan voor veelgebruikte elementen zoals:
   * API-authenticatiestappen
   * Instructies voor het instellen van de omgeving
   * Standaard codepatronen
4. Voeg ze in elke handleiding in met de opdracht `/`

## Je documentatie organiseren

### Een documentatiestrategie opstellen

Overweeg voordat je aan individuele handleidingen begint je algehele documentatiestructuur:

1. **Breng de ontwikkelaarsreis in kaart**: Welk pad volgen ontwikkelaars van eerste aanmelding tot geavanceerd gebruik?
2. **Identificeer kennishiaten**: Waar lopen ontwikkelaars typisch vast?
3. **Maak progressieve leerpaden**: Hoe kan elke handleiding voortbouwen op eerder opgedane kennis?

### Te overwegen handleidingtypen

Verschillende handleidingen dienen verschillende doelen:

* **Aan de slag**: Nieuwe ontwikkelaars inwerken
* **Tutorials**: Stapsgewijze instructies voor specifieke taken
* **Conceptuele handleidingen**: Complexe ideeën of architectuur uitleggen
* **Instructiehandleidingen**: Gerichte instructies voor specifieke functies
* **Probleemoplossing**: Oplossingen voor veelvoorkomende problemen

## Handleidingen in de loop van de tijd onderhouden

### Content actueel houden

Documentatie vereist regelmatig onderhoud:

1. Plan regelmatige reviewcycli (per kwartaal werkt goed)
2. Werk handleidingen en je changelog bij wanneer functies veranderen
3. Let op gebruikersfeedback die op verwarring wijst
4. Monitor analyses om te zien welke handleidingen verbetering nodig hebben

### Overwegingen bij versiebeheer

Als je API meerdere versies heeft:

1. Gebruik de versiefunctie van ReadMe om afzonderlijke documentatiesets bij te houden
2. Markeer versiespecifieke informatie duidelijk
3. Overweeg callouts te gebruiken om verschillen tussen versies te benadrukken

## Samenwerken met Git-integratie

Met de [bidirectionele Git-synchronisatie](doc:bi-directional-sync) van ReadMe kun je nu samenwerken aan documentatie met vertrouwde Git-workflows:

1. Verbind je ReadMe-project met GitHub/GitLab
2. Bewerk documentatiebestanden rechtstreeks in je repository
3. Wijzigingen worden automatisch gesynchroniseerd met je ReadMe-project
4. Gebruik pull requests en reviews voor documentatiewijzigingen

## Succes meten

### Analyses gebruiken

ReadMe biedt inzicht in hoe ontwikkelaars je documentatie gebruiken:

1. Monitor paginaweergaven om populaire handleidingen te identificeren
2. Volg zoekopdrachten om ontbrekende informatie te vinden
3. Gebruik deze gegevens om verbeteringen aan de documentatie te prioriteren

### Feedback verzamelen

Maak feedbacklussen om continu te verbeteren:

1. Schakel discussies in handleidingen in
2. Bekijk regelmatig vragen en opmerkingen
3. Werk handleidingen bij op basis van veelgestelde vragen

## Volgende stappen

Nu je weet hoe je handleidingen in ReadMe aanmaakt en beheert, probeer dan:

* Je eerste categorie en handleiding aanmaken
* Experimenteren met MDX-componenten
* Een reviewproces voor documentatie opzetten
* Je documentatie verbinden met GitHub voor gezamenlijk bewerken

Meer hulp nodig? Bekijk onze andere bronnen:

* [MDX-documentatie](doc:mdx)
* [Bidirectionele synchronisatie instellen](doc:bi-directional-sync)