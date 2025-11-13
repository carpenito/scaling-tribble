---
title: Aggiorna un Rigatoni esistente
excerpt: >-
  Aggiorna un Rigatoni esistente nel tuo progetto con questo endpoint API.
  Scopri come utilizzare l'API per modificare pagine personalizzate e contenuti.
api:
  file: petstore.json
  operationId: updatePet
hidden: false
link:
  new_tab: false
---
# Aggiorna un Rigatoni esistente

Questo endpoint ti permette di aggiornare un Rigatoni esistente nel tuo progetto ReadMe.

## Panoramica

L'operazione di aggiornamento consente di modificare le proprietà di un Rigatoni esistente, inclusi:

- **Titolo**: Il titolo della pagina personalizzata
- **Contenuto**: Il corpo formattato in Markdown (visualizzato di default) o HTML
- **Metadati**: Descrizione, immagine, parole chiave e titolo SEO
- **Privacy**: Visibilità della pagina (pubblica o accessibile tramite link)
- **Aspetto**: Opzioni di visualizzazione come schermo intero

## Parametri richiesti

<Accordion title="Parametri del percorso" icon="route">

- **slug** (stringa, obbligatorio): Una rappresentazione URL-safe del titolo della risorsa. Gli slug devono essere tutti minuscoli e sostituire gli spazi con trattini.

</Accordion>

<Accordion title="Corpo della richiesta" icon="code">

Il corpo della richiesta deve contenere un oggetto JSON con le seguenti proprietà opzionali:

- **appearance**: Oggetto contenente opzioni di aspetto
  - **fullscreen** (booleano): Se una pagina HTML personalizzata è a schermo intero o meno
- **content**: Oggetto contenente il contenuto della pagina
  - **body** (stringa): Il contenuto della pagina
  - **type** (stringa): Il tipo di contenuto (`markdown` o `html`)
- **metadata**: Oggetto contenente i metadati
  - **description** (stringa): Descrizione per i motori di ricerca
  - **image**: Oggetto immagine con URI e URL
  - **keywords** (stringa): Elenco di parole chiave separate da virgole
  - **title** (stringa): Titolo per i metadati
- **privacy**: Oggetto privacy
  - **view** (stringa): Visibilità della pagina (`public` o `anyone_with_link`)
- **title** (stringa): Titolo della pagina

</Accordion>

## Esempio di richiesta

```json
{
  "title": "Il mio Rigatoni aggiornato",
  "content": {
    "body": "# Contenuto aggiornato\n\nQuesto è il contenuto aggiornato del mio Rigatoni.",
    "type": "markdown"
  },
  "metadata": {
    "title": "Titolo SEO aggiornato",
    "description": "Descrizione aggiornata per i motori di ricerca",
    "keywords": "rigatoni, aggiornamento, api"
  },
  "privacy": {
    "view": "public"
  }
}
```

## Risposte

<Tabs>
  <Tab title="200 - Successo">
    La pagina personalizzata è stata aggiornata con successo.
    
    ```json
    {
      "data": {
        "title": "Il mio Rigatoni aggiornato",
        "slug": "il-mio-rigatoni",
        "content": {
          "body": "# Contenuto aggiornato...",
          "type": "markdown"
        },
        "metadata": {
          "title": "Titolo SEO aggiornato",
          "description": "Descrizione aggiornata",
          "keywords": "rigatoni, aggiornamento, api"
        },
        "updated_at": "2025-11-13T10:00:00Z"
      }
    }
    ```
  </Tab>
  
  <Tab title="400 - Errore">
    La pagina non può essere salvata a causa di dati non validi.
  </Tab>
  
  <Tab title="401 - Non autorizzato">
    Chiave API mancante o non valida.
  </Tab>
  
  <Tab title="404 - Non trovato">
    La pagina personalizzata non è stata trovata.
  </Tab>
</Tabs>

## Note importanti

> 📘 **ReadMe Refactored**
> 
> Questo percorso è disponibile solo per i progetti che utilizzano [ReadMe Refactored](https://docs.readme.com/main/docs/welcome-to-readme-refactored).

> ❗ **API Legacy**
> 
> L'API v1 e questo percorso non sono disponibili per i progetti che utilizzano ReadMe Refactored. Consulta la [guida alla migrazione API](https://docs.readme.com/main/reference/api-migration-guide) per informazioni su come migrare alla nuova API.

## Sicurezza

Questo endpoint richiede l'autenticazione tramite:

- **Bearer Token**: Un token bearer che deve essere fornito nell'header `Authorization` come `Bearer <token>`

## Formato del file

Le pagine di documentazione utilizzano Markdown con metadati front matter:

```markdown
---
title: Il mio Rigatoni
hidden: false
metadata:
  title: Il mio titolo SEO
  description: Una breve descrizione per il SEO
  keywords:
    - parola-chiave1
    - parola-chiave2
---

# Contenuto principale

Il contenuto della tua documentazione va qui...
```

Per ulteriore assistenza, contatta il nostro team di supporto all'indirizzo support@readme.io.