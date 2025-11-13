---
title: MCP (Protocollo di Contesto del Modello)
excerpt: >-
  Il Protocollo di Contesto del Modello (MCP) è una standardizzazione di come
  gli assistenti AI interagiscono con le API, e ReadMe sta portando questa
  capacità al tuo hub per sviluppatori.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
[Il Protocollo di Contesto del Modello (MCP)](https://modelcontextprotocol.io/introduction) è una standardizzazione di come gli assistenti AI interagiscono con le API, e ReadMe sta portando questa capacità al tuo hub per sviluppatori. Con i server MCP, puoi convertire la documentazione della tua API in una risorsa strutturata che gli assistenti AI possono comprendere e con cui possono interagire programmaticamente.

## Caratteristiche Principali

* **Strumentazione Personalizzata**: Definisci combinazioni personalizzate di flussi di lavoro e endpoint. <Badge label="Nuovo" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **Route Abilitate**: Disabilita gli endpoint che non vuoi siano accessibili nel tuo server MCP <Badge label="Nuovo" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **Integrazione OpenAPI**: Genera un server MCP dalla tua specifica OpenAPI esistente.
* **Gli assistenti AI possono connettersi al tuo server MCP per**:
  * Leggere e comprendere la tua specifica OpenAPI.
  * Eseguire chiamate API.
  * Cercare nella documentazione con [Ask AI](/docs/ask-ai).
* **Strumenti MCP**:
  * **Strumenti OpenAPI**:
    * `execute-request` - Effettua chiamate API direttamente dalla tua specifica
    * `get-endpoint` - Ottieni informazioni dettagliate sull'endpoint su richiesta
    * `get-request-body` - Accedi ai parametri di richiesta strutturati
    * `get-response-schema` - Comprendi cosa restituisce la tua API
    * `list-endpoints` - Naviga tutti gli endpoint API disponibili
    * `list-security-schemes` - Accedi ai requisiti di autenticazione
    * `search-schema` - Trova esattamente quello che ti serve nella tua specifica API
    * `get-code-snippet` - Esempi di snippet di codice nel tuo linguaggio preferito per interagire con il tuo endpoint.
  * **Strumenti di Documentazione**:
    * `search` - Cerca nell'intera base di conoscenza per informazioni rilevanti
    * `fetch` - Restituisci una pagina di guide

<Callout icon="📘" theme="info">
  Gli Strumenti di Documentazione richiedono l'aggiornamento del tuo piano attuale con il <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor>.

  Per i clienti Enterprise, contatta il tuo CSM.

  Per i clienti Startup e Business, aggiorna il tuo piano con l'AI Booster Pack dalla pagina **Gestisci Piano** nelle Impostazioni.
</Callout>

## Come Funziona

Creiamo un server MCP dedicato che si connette alla tua specifica OpenAPI e alla funzionalità [Ask AI](/docs/ask-ai). Questo crea un ponte tra la documentazione della tua API e gli assistenti AI, rendendo la tua API istantaneamente più accessibile e comprensibile agli strumenti AI.

## Funzionalità Extra

* **Branch** Per impostazione predefinita, il server MCP è connesso all'ultima versione stabile. Per scegliere un branch diverso, aggiungi `?branch=<nome>` all'URL MCP. NOTA: Quando sei su un branch, `search-documentation` non sarà disponibile.
* **Progetti Privati** Per accedere a progetti protetti, dovrai configurare il tuo client MCP per inviare un header `x-readme-auth`
  * Protetto da password: `x-readme-auth` dovrebbe essere la password del sito
  * Solo membri del team e Login personalizzato: `x-readme-auth` dovrebbe essere una chiave API nella forma `bearer <api_key>`

## Iniziare con MCP

Scegli come vorresti iniziare a lavorare con MCP:

1. <Anchor label="Auto-Genera il Tuo Server MCP" target="_blank" href="doc:generate-your-own-mcp-server">Auto-Genera il Tuo Server MCP</Anchor>: Ogni progetto ReadMe include automaticamente un server MCP completamente configurato. Abilita semplicemente MCP per connettere la documentazione della tua API agli strumenti AI.
2. <Anchor label="Usa il Server MCP di ReadMe" target="_blank" href="doc:readmes-mcp-server">Usa il Server MCP di ReadMe</Anchor>: Con il server MCP di ReadMe, puoi fare tutto quello che normalmente faresti in ReadMe, come aggiungere e modificare pagine, direttamente attraverso la nostra API.