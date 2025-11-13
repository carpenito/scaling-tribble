---
title: Creare una Ricetta
excerpt: >-
  Guida completa per creare ricette interattive di codice in ReadMe. Impara come
  trasformare esempi di codice in esperienze di apprendimento coinvolgenti per
  sviluppatori con annotazioni dettagliate e personalizzazioni visive.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
# Panoramica

Pronto a trasformare i tuoi esempi di codice in esperienze di apprendimento user-friendly per sviluppatori? Questa guida ti accompagna nella creazione della tua prima Ricetta dall'inizio alla fine. Imparerai come suddividere codice complesso in passaggi digeribili, aggiungere annotazioni utili e personalizzare l'esperienza visiva per adattarla al tuo brand.

<br />

<Image align="center" border={false} src="https://files.readme.io/05e72a5519ad6e9421775f6688bbee366623e93528abf9df93dd5ae1973b81dd-Screenshot_2025-05-22_at_2.16.36_PM.png" />

<br />

## Prima di Iniziare

* Prepara il tuo esempio di codice (oppure identifica quale endpoint API vuoi usare come punto di partenza)
* Assicurati che la sezione Ricette sia accessibile nel tuo progetto ReadMe
* Considera quali linguaggi di programmazione usano maggiormente i tuoi sviluppatori
* Rifletti sugli obiettivi di apprendimento chiave per questo particolare tutorial di codice

## Creazione di una Ricetta

<Image border={false} src="https://files.readme.io/4482047-Screen_Shot_2020-12-01_at_3.42.35_PM.png" />

### 1. Accedere all'Editor di Ricette

Naviga al tuo progetto ReadMe e clicca **Modifica** per entrare nell'interfaccia di editing. Dal menu di navigazione principale, seleziona **Ricette** per accedere all'area di gestione delle Ricette. Clicca il pulsante **Crea Nuova Ricetta** per avviare il costruttore di Ricette.

<Image align="center" border={false} src="https://files.readme.io/139f1a2224d1add344a0071284be7614929b7cac5be5babf7cb0860b16b9f81e-Screenshot_2025-05-22_at_12.47.08_PM.png" />

### 2. Configurare il Tuo Esempio di Codice

1. Nel pannello in alto a destra, seleziona il tuo linguaggio di programmazione dal menu a discesa.
2. Aggiungi il tuo esempio di codice e assicurati che sia formattato correttamente con l'evidenziazione della sintassi. Questa sarà la base su cui faranno riferimento le tue annotazioni passo-passo.

<Image align="center" border={false} src="https://files.readme.io/91f78f372bffaf5521f48ba6972275b5d3fa1b74cf4b4f917a5d7284a6d51c11-Screenshot_2025-05-22_at_2.09.51_PM.png" />

**Nota:** Ogni Ricetta può supportare più linguaggi di programmazione, quindi puoi aggiungere versioni di linguaggi aggiuntivi dopo aver configurato il primo.

### 3. Costruire le Tue Annotazioni Passo-Passo

Nella barra laterale sinistra, crea i tuoi passaggi evidenziati che guideranno gli sviluppatori attraverso il tuo codice. Per ogni passaggio:

* Scrivi un titolo chiaro e descrittivo che spieghi cosa realizza questa parte del codice
* Aggiungi spiegazioni dettagliate che aiutino gli sviluppatori a comprendere il "perché" dietro ogni sezione
* Specifica i numeri delle righe che dovrebbero essere evidenziate per questo passaggio
* Usa un linguaggio colloquiale che renda i concetti complessi accessibili

Ogni passaggio dovrebbe focalizzarsi su un concetto o azione specifica all'interno del tuo esempio di codice, costruendo comprensione progressivamente.

<Image border={false} src="https://files.readme.io/cece453-Screen_Shot_2020-12-01_at_3.49.54_PM.png" />

### **4. Aggiungere Esempi di Risposta**

Nel pannello in basso a destra, includi la risposta API prevista quando il tuo codice viene eseguito con successo. Questo mostra agli sviluppatori esattamente come appare il successo e li aiuta a verificare la loro implementazione.

Se il tuo codice non genera una risposta (o se mostrarla non è rilevante), puoi lasciare vuota questa sezione: si nasconderà automaticamente dalla Ricetta finale.

**Nota:** Anche le variabili dati utente funzionano nelle Ricette! Se hai configurato documenti personalizzati, puoi includere contenuto dinamico nelle tue risposte.

> 👍 Le variabili dati utente funzionano nelle Ricette!
>
> Se hai [variabili](doc:personalized-docs) nella tua documentazione, per esempio passate tramite il Webhook Documenti Personalizzati, funzioneranno anche nelle Ricette!

### 5. Personalizzare l'Aspetto Visivo

Passa alla scheda **Aspetto** per rendere la tua Ricetta unica:

* **Seleziona un'emoji**: Clicca l'icona emoji per scegliere dal menu a discesa
* **Imposta il colore di sfondo**: Usa il selettore colore per scegliere uno sfondo che si abbini al tuo brand (supporta valori RGB, HSL o HEX)
* **Scrivi una descrizione**: Aggiungi una descrizione dettagliata che apparirà sulla carta Ricetta più grande nella tua sezione Ricette

Il colore del pulsante _Apri Ricetta_ eredita automaticamente dalle impostazioni del colore dei link del tuo progetto.

<Image border={false} src="https://files.readme.io/ea6500f-Screen_Shot_2020-10-19_at_12.41.19_PM.png" />

### **6. Scegliere le Posizioni di Embedding**

Decidi dove dovrebbe apparire la tua Ricetta attraverso la tua documentazione:

* **Embedding Reference API**: Seleziona endpoint specifici dove questa Ricetta fornisce contesto rilevante
* **Sezione Ricette**: La tua Ricetta apparirà automaticamente nell'area principale delle Ricette una volta pubblicata
* **Embedding Guide**: Puoi incorporare manualmente la Ricetta nelle pagine guida successivamente usando il widget Ricetta

Seleziona le caselle accanto agli endpoint rilevanti per rendere la tua Ricetta accessibile esattamente dove gli sviluppatori ne hanno più bisogno.

La Ricetta apparirà come una carta cliccabile come mostrato nell'area anteprima del passaggio Aspetto.

<Image border={false} src="https://files.readme.io/20cf1e2-Screen_Shot_2020-12-03_at_5.14.16_PM.png" />

<br />

<Image border={false} src="https://files.readme.io/e4619b5-Screen_Shot_2020-12-01_at_2.59.43_PM.png" />

<br />

<Callout icon="🚧" theme="warn">
  Gli embed non appariranno nella sezione Reference [finché la sezione Ricette non sarà abilitata](#enable-recipes-section).
</Callout>

<br />

### 7. Impostare lo Stato di Pubblicazione

Scegli il livello di visibilità della tua Ricetta:

* **Non pubblicata**: Visibile solo agli amministratori del progetto (predefinito per nuove Ricette)
* **Pubblicata**: Visibile a tutti gli utenti nella tua raccolta di Ricette
* **In evidenza**: Messa in mostra in modo prominente in cima alla tua sezione Ricette (solo una Ricetta può essere in evidenza alla volta)

Inizia con "Pubblicata" per rendere la tua Ricetta disponibile agli sviluppatori, oppure mantienila "Non pubblicata" mentre stai ancora perfezionando il contenuto.

|                     |                                                                                                                                                                     |
| :------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **In evidenza**     | Questa è la Ricetta messa in mostra in cima alla sezione Ricette. Una Ricetta deve essere in evidenza se la tua pagina Ricette è pubblica, e deve essere pubblicata. |
| **Pubblicata**      | Visibile agli utenti nella griglia di carte sotto la Ricetta in evidenza                                                                                           |
| **Non pubblicata**  | Non può essere vista dai clienti. Le nuove Ricette sono non pubblicate per impostazione predefinita.                                                               |

<Image border={false} src="https://files.readme.io/445d0c8-Screen_Shot_2020-12-16_at_3.54.22_PM.png" />

<br />

## FAQ & Risoluzione Problemi

**Posso rimuovere l'icona Ricetta nella barra di navigazione?**

Questa sezione è visibile solo agli amministratori del progetto. I tuoi clienti non vedranno questa sezione a meno che tu non la [abiliti](#enabling-your-recipes-page) per renderla visibile a loro.

Mentre trasferiamo più capacità di editing al frontend del tuo hub documenti, continueremo a rendere più chiaro cosa vedono gli amministratori del progetto rispetto a cosa vedono i tuoi clienti.

**Come cambio il colore del pulsante blu "Apri Ricetta"?**

Il colore di questo pulsante è ereditato dal Colore Link che hai impostato nell'[Editor Tema](/main/docs/design-themes) nelle impostazioni del tuo progetto. Per cambiarlo, dovrai cambiare il Colore Link per l'intero hub ReadMe.

**Posso rinominare la sezione Ricette come le altre sezioni?**

Non ancora, ma ci stiamo lavorando!

**L'evidenziazione del mio codice non funziona correttamente?** Ricontrolla che i numeri delle tue righe siano accurati e che tu abbia selezionato il linguaggio di programmazione corretto. Ricorda che i numeri delle righe iniziano da 1, non da 0.

**Il widget Ricetta non appare nelle mie guide?** Assicurati che la sezione Ricette sia abilitata nelle impostazioni di navigazione del tuo sito. Il widget non sarà disponibile finché le Ricette non sono attivate per il tuo progetto.

**La mia Ricetta incorporata non si mostra nelle pagine Reference API?** Le Ricette incorporate appaiono solo una volta che la sezione Ricette è pubblicamente abilitata. Controlla le impostazioni di navigazione del tuo sito e assicurati che almeno una Ricetta sia pubblicata.

**La sezione risposta è scomparsa?** Se cancelli completamente il contenuto della risposta predefinita, il pannello risposta si nasconderà automaticamente. Aggiungi contenuto per renderlo di nuovo visibile.