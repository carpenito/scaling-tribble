---
title: Creazione di API da Zero con l'API Designer
excerpt: >-
  Scopri come creare documentazione API completa utilizzando l'API Designer di
  ReadMe, anche senza specifiche OpenAPI esistenti.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
# Panoramica

Nessuna specifica OpenAPI? Nessun problema! L'API Designer di ReadMe ti permette di costruire la tua documentazione API direttamente nella piattaforma con un'interfaccia visuale intuitiva – senza bisogno di YAML o JSON.

In questa guida, creeremo una Social Media API con endpoint per elencare e creare post. Vedrai quanto è facile documentare la tua API anche se stai partendo da zero.

## Creazione della Definizione API

Iniziamo configurando la struttura base per la tua API:

1. Naviga su **API Reference** nel tuo progetto ReadMe
2. Clicca il pulsante **+ Add**
3. Seleziona **Start Building** sotto "Build an API definition from scratch"

<Image align="center" border={false} src="https://files.readme.io/f9e241f98e3e8ad91e999561f4e3b4dfe260a8e6a18662e23da840887977b6c7-CleanShot_2025-03-11_at_11.18.13.gif" />

4. Inserisci i dettagli della definizione API:
   * **API Title**: Inserisci un nome descrittivo (es. "Social Media API")
   * **Target Host URL**: L'URL base della tua API (es. "[http://api.example.com](http://api.example.com)")
   * **Authentication Type**: Seleziona il tuo metodo di autenticazione (None, API Key, Basic, o Bearer)

<Image align="center" border={false} src="https://files.readme.io/7a81519f9faf96f4af361d26c405792fe78488558a9c8e972d084d102dda098e-CleanShot_2025-03-11_at_11.21.07.gif" />

5. Clicca **Save** per creare la definizione API

La tua nuova definizione API apparirà nel pannello di navigazione a sinistra, pronta per aggiungere endpoint.

## Creazione del Primo Endpoint (Elenco Post Social Media)

Creiamo un endpoint per recuperare un elenco di post social media:

1. Nella navigazione a sinistra, vedrai un endpoint predefinito etichettato `/new-endpoint`
2. Rinominalo per riflettere meglio la struttura della tua API - chiamiamolo "Posts"
3. Ora vedrai questa categoria nella tua navigazione a sinistra

<Image align="center" border={false} src="https://files.readme.io/fc908c66586d12aa0327f1bc17d60a045a23e550e82161ae4818a37eb91b3931-CleanShot_2025-03-11_at_11.29.12.gif" />

4. Crea il tuo endpoint GET per elencare i post:
   * Clicca sull'endpoint per modificarlo
   * Cambia il titolo in "List Social Media Posts"
   * Seleziona il metodo **GET** dal menu a discesa
   * Imposta il percorso su `/posts`
   * Aggiungi una descrizione che spiega cosa fa l'endpoint (es. "Restituisce un elenco paginato di post social media")

<Image align="center" border={false} src="https://files.readme.io/72e65717ef6534caa7b0d2a187deb7125b1466bc72a95a8fdcd7459267ae8b35-CleanShot_2025-03-11_at_11.31.27.gif" />

### Aggiunta di Parametri Query

La maggior parte degli endpoint di elenco supporta paginazione o filtri. Aggiungiamo alcuni parametri query:

1. Individua la sezione **Query Parameters** e clicca il pulsante **+**
2. Aggiungi parametri per la paginazione:
   * Aggiungi un parametro `page` di tipo `integer`
   * Aggiungi un parametro `limit` di tipo `integer`
   * Aggiungi altri parametri di filtro (es. `category` come `string`)
3. Per ogni parametro:
   * Aggiungi una descrizione
   * Imposta se è obbligatorio
   * Fornisci un valore predefinito se applicabile

<Image align="center" border={false} src="https://files.readme.io/c596d7f09014adbfb1166f81b10936c0427f6b0e4a4c1cc9f2983a51c55aaa55-CleanShot_2025-03-11_at_11.35.30.gif" />

<br />

## Creazione del Secondo Endpoint (Creazione Post Social Media)

Ora aggiungiamo un endpoint per creare nuovi post:

1. Nella navigazione a sinistra, clicca il pulsante **+ New Category** se hai bisogno di una nuova categoria, o usa la categoria "Posts" esistente
2. Clicca l'icona + per aggiungere un nuovo endpoint
3. Configura il tuo endpoint POST:
   * Titolo: "Create New Post"
   * Metodo: Seleziona **POST** dal menu a discesa
   * Percorso: `/posts`
   * Descrizione: "Consente agli utenti autenticati di creare nuovi post"

<Image align="center" border={false} src="https://files.readme.io/fa7c7a03010f8fdbc0bee4ff32db7a11e34f723f3640ed6e3f311234e93dd2bd-CleanShot_2025-03-11_at_11.52.25.gif" />

### Aggiunta di Parametri Request Body

Per un endpoint POST, dovrai definire il corpo della richiesta:

1. Individua la sezione **Request Body** e clicca per espanderla
2. Imposta il tipo di contenuto su `object`
3. Aggiungi i campi richiesti:
   * Aggiungi un campo `content` di tipo `string` e marcalo come obbligatorio
   * Aggiungi eventuali campi aggiuntivi accettati dalla tua API (es. `image_url`, `tags`)
4. Per ogni campo:
   * Aggiungi una descrizione chiara
   * Marca se è obbligatorio
   * Fornisci eventuali vincoli (lunghezza min/max, pattern, ecc.)

<Image align="center" border={false} src="https://files.readme.io/2a114a0bb8cfab72df455ea87638aa51d75a1ea3b931987fc18d1450f94cb08d-CleanShot_2025-03-11_at_11.57.21.gif" />

### Aggiunta di Esempi di Codice Request

Una delle funzionalità potenti di ReadMe è la generazione automatica di esempi di codice:

1. Trova la sezione **Request Code** a destra
2. ReadMe genera automaticamente esempi di codice in più linguaggi
3. Puoi anche cliccare "Write your own static samples" per aggiungere esempi personalizzati

<Image align="center" border={false} src="https://files.readme.io/646ce4e3467087d3d7b8396632e29af646bf02be9113054d0c63e69c14561a6c-CleanShot_2025-03-11_at_12.03.35.gif" />

<br />

## Test della Documentazione API

Dopo aver creato i tuoi endpoint:

1. Salva le modifiche
2. Passa alla modalità "View" per vedere come appare la tua documentazione agli sviluppatori
3. Testa le funzionalità interattive per assicurarti che i tuoi esempi funzionino correttamente

## Consigli per Ottima Documentazione API

* **Sii completo con le descrizioni**: Spiega chiaramente cosa fa ogni endpoint e perché
* **Fornisci esempi realistici**: Usa dati di esempio che sembrano un utilizzo nel mondo reale
* **Documenta gli stati di errore**: Includi esempi di risposte di errore e come gestirle
* **Usa nomenclatura coerente**: Mantieni uno stile coerente tra tutti gli endpoint e parametri
* **Aggiungi "What's Next"**: Usa la sezione "What's Next" per guidare gli utenti verso endpoint correlati di cui potrebbero aver bisogno

Seguendo questa guida, hai creato una documentazione API ben strutturata da zero utilizzando l'API Designer di ReadMe. I tuoi sviluppatori ora hanno documentazione interattiva e chiara che li aiuta a integrarsi rapidamente e facilmente con la tua API.

Ricorda, puoi sempre tornare all'API Designer per aggiungere endpoint, aggiornare parametri o migliorare la tua documentazione man mano che la tua API evolve.

<br />

## Funzionalità OpenAPI Attualmente Non Supportate nell'API Designer

Attualmente non supportiamo tutte le funzionalità OpenAPI nel nostro API Designer. Se usi una di queste funzionalità in un endpoint non potrai modificarle nella nostra UI. Tuttavia, questi endpoint verranno comunque renderizzati correttamente nella documentazione e possono ancora essere aggiornati modificando direttamente il file OpenAPI.

<br />

| Funzionalità OpenAPI Non Supportata | Spiegazione                                                                                                                                                                              | Documentazione OpenAPI                                                                                                                     |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Additional Properties                | La keyword additionalProperties viene utilizzata all'interno di uno schema per definire se le proprietà non esplicitamente definite nello schema sono consentite negli oggetti, e se sì, quali dovrebbero essere i loro tipi. | [Dictionaries, HashMaps and Associative Arrays](https://swagger.io/docs/specification/v3_0/data-models/dictionaries/)                      |
| Callbacks/Webhooks                  | OpenAPI ha una funzionalità per definire endpoint che faranno una chiamata API una volta completato un evento.                                                                          | [Callbacks](https://swagger.io/docs/specification/v3_0/callbacks/)                                                                         |
| References                          | Qualsiasi endpoint che definisce un oggetto utilizzando un $ref.                                                                                                                        | [Using Ref](https://swagger.io/docs/specification/v3_0/using-ref/)                                                                         |
| Common Parameters                    | Endpoint dove i parametri sono definiti a livello di percorso invece che di metodo, quindi i parametri sono condivisi tra tutti i metodi per quell'URL.                                | [Describing Parameters](https://swagger.io/docs/specification/v3_0/describing-parameters/#common-parameters)                               |
| Links                                | I Links sono una funzionalità OpenAPI che descrive come le risposte di un endpoint possono essere utilizzate come input per altre operazioni.                                          | [Links](https://swagger.io/docs/specification/v3_0/links/)                                                                                 |
| Polymorphism                         | Il polimorfismo ti permette di definire uno schema che può rappresentare più tipi o modelli.                                                                                            | [Inheritance and Polymorphism](https://swagger.io/docs/specification/v3_0/data-models/inheritance-and-polymorphism/?sbsearch=Polymorphism) |
| Server Variables                     | Le variabili possono essere definite nel percorso base che possono avere una lista preimpostata di valori tra cui l'utente può scegliere.                                               | [API Server and Base Path](https://swagger.io/docs/specification/v3_0/api-host-and-base-path/?sbsearch=server%20variables)                 |
| Style                                | La keyword Style consente la configurazione su come più valori dovrebbero essere passati a un parametro.                                                                                | [Parameter Serialization](https://swagger.io/docs/specification/v3_0/serialization/?sbsearch=Styles)                                       |
| XML                                  | Endpoint che accettano o rispondono con dati XML.                                                                                                                                       | [Representing XML](https://swagger.io/docs/specification/v3_0/data-models/representing-xml/?sbsearch=xml)                                  |