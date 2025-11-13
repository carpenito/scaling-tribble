---
title: Creazione e Gestione delle Guide
excerpt: >-
  Impara come creare, organizzare e mantenere guide di documentazione efficaci
  in ReadMe. Dalla creazione di categorie alla strutturazione di contenuti per
  sviluppatori.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
# Panoramica

Immergiamoci negli aspetti pratici dell'organizzazione della tua documentazione in ReadMe. Dalla creazione di nuove guide alla gestione dei contenuti nel tempo, questa guida ti mostrerà come costruire e mantenere una knowledge base ben strutturata che aiuta gli sviluppatori a trovare esattamente ciò di cui hanno bisogno, quando ne hanno bisogno.

### Perché le Guide Sono Importanti

Le guide sono la spina dorsale della tua documentazione per sviluppatori. Mentre il riferimento API dice agli sviluppatori cosa è possibile fare, le guide mostrano loro come avere successo. Ottime guide:

* Guidano gli sviluppatori da principianti a esperti
* Forniscono un contesto che i riferimenti API non possono catturare
* Rispondono al "perché" oltre al "come"
* Risolvono problemi del mondo reale che gli sviluppatori incontrano

## Creazione della Tua Prima Guida

### Creazione di Categorie 📂

Le categorie ti aiutano a organizzare la tua documentazione in sezioni logiche, funzionando come capitoli nella storia della tua API. Ogni categoria crea una pausa naturale nella narrativa della tua documentazione, rendendo più facile per gli sviluppatori seguire il percorso.

1. Naviga al tuo hub di documentazione e attiva la **Modalità Modifica**.
2. Fai clic sul pulsante **+ NUOVA CATEGORIA** nella navigazione laterale.
3. Inserisci un nome per la tua categoria (es. "Primi Passi" o "Argomenti Avanzati")
4. Fai clic su **Invio** per salvare.

> 📘 Esperienza Utente
>
> Pensa al percorso del tuo sviluppatore quando nomini le categorie. Cosa avrebbe più senso per qualcuno che esplora la tua API per la prima volta? Considera di organizzare le categorie per livello di competenza (principiante ad avanzato) o per caso d'uso.

### Creazione di una Pagina Guida 📝

Ora che hai impostato le tue categorie, aggiungiamo alcune pagine:

1. In modalità **Modifica**, passa il mouse sopra una categoria e fai clic sul pulsante **+**
2. Compila i dettagli essenziali:
   * **Titolo**: Rendilo chiaro e descrittivo
   * **Slug**: Questo sarà il percorso URL (generato automaticamente, ma puoi personalizzarlo)
   * **Nascosto**: Attiva questo se vuoi lavorare sulla guida prima di renderla pubblica
3. Fai clic su **Salva** per creare la tua nuova guida

### Utilizzo dell'Interfaccia Editor ✏️

<Image align="center" border={false} src="https://files.readme.io/53c229bb50f36b2a6398894e5de72e9909397911c2deba6c77e629733e714a99-Editing_UI_-_view_to_edit_toggle.gif" />

Con l'interfaccia di editing di ReadMe, creerai e modificherai il contenuto direttamente sul tuo hub. Questo significa che quello che vedi è esattamente quello che vedranno i tuoi sviluppatori.

1. Dopo aver creato la tua pagina, sarai nell'editor automaticamente
2. Usa la barra degli strumenti di formattazione per lo stile del testo di base
3. Digita `/` per accedere al menu comandi per inserire:
   * Blocchi di codice
   * Callout
   * Immagini
   * E altro ancora!
4. Alterna tra le modalità **Modifica** e **Visualizza** per vedere esattamente come apparirà il tuo contenuto agli sviluppatori

<Image align="center" border={false} src="https://files.readme.io/a106664539184b9eebb366fd2c51ed5ba10ca5c1224c0ce52a209dd8c08ac143-CleanShot_2024-11-08_at_20.24.59.gif" />

> 📘 Controllo completo del tuo Markdown
>
> La Modalità Raw di ReadMe ti permette di aggiungere nuovo contenuto e modificare contenuto esistente direttamente in Markdown. Apri semplicemente il menu a tre punti accanto alle impostazioni di visibilità e scegli **Modalità Raw**.

## Strutturazione di Guide Efficaci

### L'Anatomia di una Grande Guida

Le guide di successo seguono una struttura coerente che aiuta gli sviluppatori a comprendere e applicare rapidamente le informazioni:

1. **Introduzione Chiara**: Quale problema risolve questa guida?
2. **Prerequisiti**: Cosa dovrebbero sapere o avere gli sviluppatori prima di iniziare?
3. **Istruzioni Passo-Passo**: Suddividi i processi complessi in passaggi gestibili
4. **Esempi di Codice**: Mostra, non limitarti a dire
5. **Risoluzione Problemi**: Affronta problemi comuni e le loro soluzioni
6. **Prossimi Passi**: Dove dovrebbero andare gli sviluppatori dopo aver completato questa guida?

### Scrivere per Sviluppatori

Quando scrivi guide, ricorda che gli sviluppatori vogliono risolvere i problemi rapidamente:

* **Sii conciso**: Vai al punto ed evita spiegazioni non necessarie
* **Usa abbondantemente esempi di codice**: Gli sviluppatori spesso capiscono il codice più velocemente della prosa
* **Evidenzia informazioni importanti**: Usa callout per avvertimenti, suggerimenti e note importanti
* **Suddividi il testo**: Usa intestazioni, elenchi e paragrafi brevi per migliorare la leggibilità
* **Usa esempi del mondo reale**: Mostra codice che risolve problemi effettivi

> 📘 Mantienilo Reale
>
> Usa esempi di codice autentici che dimostrano implementazioni realistiche. Se stai mostrando l'autenticazione, usa un esempio completo con gestione degli errori. Se stai dimostrando il recupero dati, mostra come elaborare e utilizzare quei dati in modo pratico. Gli esempi del mondo reale aiutano gli sviluppatori a colmare il divario tra documentazione e implementazione.

```javascript
// Buon esempio - con commenti significativi e nomi di variabili chiari
const apiKey = 'your_api_key_here';

// Inizializza il client con la tua chiave API
const client = new ReadMeAPI(apiKey);

// Recupera i dati utente e gestisci potenziali errori
try {
  const userData = await client.getUser(userId);
  console.log(`Utente trovato: ${userData.name}`);
} catch (error) {
  console.error(`Errore nel recupero utente: ${error.message}`);
}
```

## Potenziamento delle Guide con MDX

ReadMe ora supporta MDX (Markdown + JSX), dandoti il potere di creare documentazione interattiva con componenti riutilizzabili.

### Componenti MDX di Base

Ecco un esempio dei nostri componenti tab MDX integrati che puoi usare per potenziare le tue guide:

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

### Creazione di Contenuti Riutilizzabili

Per contenuti che userai in più guide, [crea blocchi di contenuti riutilizzabili](doc:reusable-content)

1. Naviga a **Impostazioni Contenuto** nell'interfaccia di editing
2. Seleziona **Contenuto Riutilizzabile**
3. Crea blocchi per elementi comuni come:
   * Passaggi di autenticazione API
   * Istruzioni di configurazione ambiente
   * Modelli di codice standard
4. Inseriscili in qualsiasi guida con il comando `/`

## Organizzazione della Tua Documentazione

### Creazione di una Strategia di Documentazione

Prima di immergerti nelle singole guide, considera la struttura complessiva della tua documentazione:

1. **Mappa il percorso dello sviluppatore**: Quale percorso seguono gli sviluppatori dalla prima registrazione all'uso avanzato?
2. **Identifica le lacune di conoscenza**: Dove si bloccano tipicamente gli sviluppatori?
3. **Crea percorsi di apprendimento progressivi**: Come può ogni guida basarsi sulla conoscenza precedente?

### Tipi di Guide da Considerare

Diverse guide servono scopi diversi:

* **Primi Passi**: Onboarding di nuovi sviluppatori
* **Tutorial**: Istruzioni passo-passo per compiti specifici
* **Guide Concettuali**: Spiegazione di idee o architetture complesse
* **Guide Come Fare**: Istruzioni mirate per funzionalità specifiche
* **Risoluzione Problemi**: Soluzioni a problemi comuni

## Mantenimento delle Guide nel Tempo

### Mantenere il Contenuto Fresco

La documentazione richiede manutenzione regolare:

1. Programma cicli di revisione regolari (trimestrale funziona bene)
2. Aggiorna le guide e il changelog quando le funzionalità cambiano
3. Osserva i feedback degli utenti che indicano confusione
4. Monitora le analisi per vedere quali guide necessitano miglioramenti

### Considerazioni sul Versioning

Se la tua API ha più versioni:

1. Usa la funzionalità di versioning di ReadMe per mantenere set di documentazione separati
2. Marca chiaramente le informazioni specifiche della versione
3. Considera l'uso di callout per evidenziare differenze tra versioni

## Collaborazione con Integrazione Git

Con la [sincronizzazione Git bidirezionale](doc:bi-directional-sync) di ReadMe, ora puoi collaborare sulla documentazione usando flussi di lavoro Git familiari:

1. Connetti il tuo progetto ReadMe a GitHub/GitLab
2. Modifica i file di documentazione direttamente nel tuo repository
3. I cambiamenti si sincronizzano automaticamente al tuo progetto ReadMe
4. Usa pull request e revisioni per le modifiche alla documentazione

## Misurazione del Successo

### Utilizzo delle Analisi

ReadMe fornisce insights su come gli sviluppatori usano la tua documentazione:

1. Monitora le visualizzazioni di pagina per identificare le guide popolari
2. Traccia le query di ricerca per trovare informazioni mancanti
3. Usa questi dati per dare priorità ai miglioramenti della documentazione

### Raccolta di Feedback

Crea cicli di feedback per migliorare continuamente:

1. Abilita discussioni sulle guide
2. Rivedi regolarmente domande e commenti
3. Aggiorna le guide basandoti su domande comuni

## Prossimi Passi

Ora che sai come creare e gestire guide in ReadMe, prova:

* Creare la tua prima categoria e guida
* Sperimentare con i componenti MDX
* Impostare un processo di revisione della documentazione
* Collegare la tua documentazione a GitHub per editing collaborativo

Hai bisogno di più aiuto? Consulta le nostre altre risorse:

* [Documentazione MDX](doc:mdx)
* [Configurazione Sincronizzazione Bidirezionale](doc:bi-directional-sync)