---
title: Agente
excerpt: >-
  L'Agente è un potente assistente per la documentazione che ti aiuta a creare,
  modificare e migliorare i contenuti su Guide, Riferimenti API e Pagine
  Personalizzate con capacità avanzate di ricerca e analisi.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
L'Agente è un potente assistente per la documentazione che ti aiuta a creare, modificare e migliorare i contenuti su Guide, Riferimenti API e Pagine Personalizzate con capacità avanzate di ricerca e analisi.

## Cosa Può Fare

L'Agente fornisce un'assistenza completa per la documentazione:

* **Creazione e Modifica di Contenuti**: Scrive, riscrive, traduce e corregge la grammatica con formattazione markdown appropriata
* **Ricerca e Analisi**: Cerca sul web, analizza URL e recupera informazioni dalla tua documentazione
* **Componenti Intelligenti**: Suggerisce e implementa i componenti MDX integrati di ReadMe
* **Flussi di Lavoro Multi-step**: Combina ricerca, analisi e creazione di contenuti in un'unica richiesta
* **Correzione Errori del Linter**: Risolve errori di sintassi e avvisi secondo la tua guida di stile configurata

## Utilizzo

L'Agente eccelle in attività di documentazione complesse e multi-step. Puoi fare richieste come:

* "Ricerca le ultime tendenze di design API e crea una guida"
* "Analizza questo URL e aggiungi i punti chiave alla nostra documentazione"
* "Trova informazioni di autenticazione dai nostri documenti ed espandi questa sezione"

Ogni sessione di chat mantiene il contesto completo della tua pagina corrente e dei file delle specifiche OpenAPI. Tutte le conversazioni sono private al tuo account. Usa il nostro modello selezionato automaticamente o scegli il tuo modello dall'elenco preconfigurato.

<Image align="center" border={false} src="https://files.readme.io/f678000604c17fb27accb05314a554ec94cf776d81f91701f4ed479db7e6b551-agent_mini.png" />

### Chiedi Informazioni su ReadMe

Fai domande all'Agente relative a ReadMe per navigare rapidamente nella nostra piattaforma mentre lavori sulla tua documentazione. Attinge dalla nostra base di conoscenze per rispondere alle tue domande e guidarti attraverso funzionalità, strumenti e best practice.

## Configurazione

Aiuta l'Agente a lavorare meglio per te:

* Se alcuni modelli non sono compatibili con la tua documentazione, disabilitali nelle impostazioni AI Chat (<i class="fa-regular fa-solid fa-gear" color="var(--gray80" />).
* Per migliorare le risposte dell'Agente, indicizza la tua base di codice per fornire contesto aggiuntivo o aggiungi contenuti personalizzati.

<Image align="center" border={false} width="350px" src="https://files.readme.io/5525b67a2ebb59fdfefbdc82f8c8b88f86f6cf3ba9b03c6c5b927d5acb8a499d-agent_settings_2.png" />

<br />

## FAQ

<Accordion title="Quale LLM alimenta l'agente?" icon="fa-robot">
  L'Agente è alimentato da modelli linguistici avanzati inclusi Google Gemini Pro 2.5, Claude e modelli OpenAI, fornendo capacità avanzate di ragionamento e ricerca.
</Accordion>

<Accordion title="I miei dati vengono condivisi con l'LLM?" icon="fa-shield-alt">
  Solo quando usi la funzione Agente. Se non la usi, nessun dato viene condiviso. Quando attivata, la pagina corrente che stai visualizzando e la documentazione rilevante vengono incluse nel prompt inviato al modello linguistico per generare una risposta.
</Accordion>

<Accordion title="Può accedere a siti web esterni?" icon="fa-globe">
  Sì! L'Agente può cercare sul web e analizzare URL per migliorare la tua documentazione.
</Accordion>

<Accordion title="Come accede ai miei documenti esistenti?" icon="fa-search">
  Può cercare attraverso la documentazione del tuo progetto e le fonti di conoscenza per trovare e incorporare informazioni rilevanti.
</Accordion>