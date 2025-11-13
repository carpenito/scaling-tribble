---
title: Elimina utente
excerpt: Questo può essere fatto solo dall'utente collegato.
api:
  file: petstore.json
  operationId: deleteUser
hidden: false
link:
  new_tab: false
---
Elimina la pagina personalizzata con questo slug.

> ❗ Importante
> 
> L'API v1 e questo endpoint non sono disponibili per i progetti che utilizzano [ReadMe Refactored](https://docs.readme.com/main/docs/welcome-to-readme-refactored). [Consulta la nostra guida alla migrazione delle API](https://docs.readme.com/main/reference/api-migration-guide) per informazioni su come migrare alla nuova API.

## Parametri

| Parametro | Tipo | Descrizione | Obbligatorio |
|-----------|------|-------------|--------------|
| `slug` | string | Una rappresentazione URL-safe del titolo della pagina. Gli slug devono essere tutti in minuscolo e sostituire gli spazi con trattini. Ad esempio, per il titolo "Getting Started", inserire lo slug "getting-started". | Sì |

## Risposte

### 204 - Successo
La pagina personalizzata è stata eliminata con successo.

### 401 - Non autorizzato
Errore di autenticazione. Possibili cause:
- Chiave API mancante (`APIKEY_EMPTY`)
- Chiave API non trovata (`APIKEY_NOTFOUND`)

### 403 - Accesso negato
Accesso non autorizzato. La chiave API fornita non corrisponde (`APIKEY_MISMATCH`).

### 404 - Non trovato
La pagina personalizzata non è stata trovata (`CUSTOMPAGE_NOTFOUND`).

## Sicurezza

Questo endpoint richiede l'autenticazione tramite chiave API utilizzando l'autenticazione HTTP Basic.

## Esempio di utilizzo

```bash
curl -X DELETE \
  https://dash.readme.com/api/v1/custompages/{slug} \
  -H 'Authorization: Basic <your-api-key>'
```

## Supporto aggiuntivo

Se hai bisogno di aiuto, invia un'email a support@readme.io

Per informazioni su come configurare le tue pagine personalizzate e creare un'esperienza più interattiva e personalizzata per i tuoi sviluppatori, consulta la [documentazione sulle pagine di riferimento API](https://docs.readme.com/main/docs/reference-core-pages).