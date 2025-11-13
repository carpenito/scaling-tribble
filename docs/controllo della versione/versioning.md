---
title: Versionamento
excerpt: >-
  Mantenere più versioni della tua documentazione è fondamentale per molti
  prodotti tecnici diversi. Questa pagina entra nei dettagli di come funziona il
  versionamento in ReadMe.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
Mantenere più versioni della tua documentazione è fondamentale per molti prodotti tecnici diversi. Questa pagina entra nei dettagli di come funziona il versionamento in ReadMe, così come diversi casi d'uso.

<Callout icon="🚧" theme="warn">
  **Sezioni Interessate:** Solo le sezioni Guide, Ricette e Riferimenti sono versionate. I contenuti per Landing Page, Discussioni e Changelog persisteranno attraverso le versioni.
</Callout>

## Creare una Nuova Versione

Per creare una nuova versione, apri il menu Versioni e Rami selezionando il **nome della versione** (es. v3.0) nella navigazione amministrativa. Quindi clicca sul pulsante **+ Nuova Versione** nell'angolo in alto a destra. Scegli da quale versione fare il fork e nomina la tua nuova versione. Questo creerà una copia di questa versione, non sarai in grado di riportare le modifiche alla versione da cui è stato fatto il fork.

<Image align="center" border={false} src="https://files.readme.io/c543cc3ff266bd3b210d720cfb7c5e09d7750c78dcb5ccfd60f669eae003ca39-versions.png" />

### Semver(-ish)

Il nostro versionamento è basato su [Semver](http://semver.org/), ma è molto più flessibile di Semver in termini di input accettabili. Questo significa che le tue versioni possono essere semplici come `v1.0`, ma anche complesse come `v1.0-ciao-questa-è-una-versione`.

***

## Opzioni della Versione

<Image align="center" border={false} width="500px" src="https://files.readme.io/159f0425970c8c5849bc6b6e7b684f51fdab23a656f6488139337adaa75e9d60-version_options.png" />

### Predefinita

Questa è la versione a cui il tuo dominio punterà. Gli utenti possono cambiare a una versione diversa cliccando il selettore dropdown delle versioni.

<Callout icon="🙅‍♂️" theme="default">
  Non è possibile unire due versioni. Se vuoi apportare modifiche a entrambe, dovrai farlo manualmente!
</Callout>

### Pubblica

Selezionando questo renderai questa versione disponibile nel selettore dropdown delle versioni e a chiunque possa visualizzare i tuoi documenti. Se non selezionato, questa versione sarà contrassegnata come **Nascosta** e sarà visibile solo agli amministratori del progetto.

### Beta

Indicare che una versione è una beta aggiungerà un badge accanto alla versione nel selettore dropdown delle versioni. Non crea un callout sulla pagina o altri cambiamenti visibili.

### Deprecata

Seleziona questo per contrassegnare le versioni più vecchie. Oltre a vedere un badge "deprecata" accanto alla versione nel selettore dropdown delle versioni, gli utenti vedranno anche un grande banner rosso sopra i documenti quando visitano questa versione deprecata. Ecco come appare:

<Image align="center" border={true} width="smart" src="https://files.readme.io/RhO7iWuhSMGsBrHSrFMt_Screen%20Shot%202015-12-16%20at%2012.17.04%20PM.png" className="border" />

***

## Visualizzazione del Dropdown delle Versioni

<Image align="center" border={false} caption="Vista amministratore: Nascosta e Deprecata non sono visibili agli utenti finali" src="https://files.readme.io/5f0ac4bab3338c5e1cceee0368a02363bb6c2eca6f40324725d6d43593e564ab-version_drop.png" />

Di default, mostriamo il suddetto selettore dropdown delle versioni nella barra di sottonavigazione. Puoi alternare per mostrare o nascondere questo in **Impostazioni > Intestazione e Piè di pagina > Sottonavigazione**.

<Image align="center" border={false} src="https://files.readme.io/1a975ae96b399662d42cee67ca226a8fd49bfb9188da95ccfd00a2125f0347d7-version_picker.png" />

***

## Contenuto Riutilizzabile

Qualsiasi [Contenuto Riutilizzabile](doc:reusable-content) creato all'interno di una Versione può essere utilizzato solo all'interno della documentazione di quella Versione; non è possibile definire blocchi di Contenuto Riutilizzabile che possono essere utilizzati attraverso le Versioni all'interno di un singolo progetto.

Se viene creata una nuova Versione quando viene fatta il fork da una Versione esistente, la nuova Versione eredita tutti i blocchi di Contenuto Riutilizzabile definiti nella Versione esistente. Tuttavia, i blocchi di Contenuto Riutilizzabile nella nuova Versione sono completamente indipendenti dalla vecchia Versione.

> 📘 Contenuto Riutilizzabile Globale
>
> I progetti con un piano Enterprise hanno la capacità di definire **Contenuto Riutilizzabile Globale** che _può_ essere utilizzato attraverso Progetti e Versioni. Vedi i nostri [documenti Contenuto Riutilizzabile per Gruppi Enterprise](https://docs.readme.com/ent/docs/reusable-content-enterprise) per maggiori informazioni!

***

## Casi d'Uso

Ci sono molti scenari diversi in cui il versionamento dei documenti potrebbe essere utile — alcuni sono più ovvi di altri. Il caso d'uso più ovvio è quando la versione della tua documentazione deve corrispondere al versionamento che potrebbe aver luogo con la tua API o altro prodotto tecnico, e hai bisogno di mantenere copie dei tuoi documenti per ogni rispettiva versione.

Un altro caso d'uso è per ristrutturazioni di contenuto più grandi o migrazioni, specialmente quando questi cambiamenti sono più complessi del semplice aggiornamento di alcune pagine (nel qual caso raccomanderemmo [Modifiche Suggerite](doc:suggested-edits). Puoi fare il fork di una nuova versione dei tuoi documenti, fare una ristrutturazione importante (es. riorganizzare le categorie delle pagine, combinare pagine, eliminare contenuto obsoleto, ecc.), e avere ancora i tuoi vecchi documenti come cambiamenti pubblici. E quando sei pronto a fare il cambio, è semplice come rinominare le versioni e attivare alcune impostazioni della versione!

***

## FAQ

<Accordion title="Quante versioni posso creare?" icon="fa-tags">
  Gli utenti del piano gratuito possono creare fino a 3 versioni. Aggiorna al piano Startup o superiore per sbloccare versioni illimitate.
</Accordion>