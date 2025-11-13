---
title: Rami
excerpt: >-
  Scopri come utilizzare i rami in ReadMe per modificare, rivedere e collaborare
  sui contenuti prima di pubblicarli dal vivo.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
Con i rami, puoi continuare a modificare come hai sempre fatto! I rami sono un flusso di lavoro opzionale che offre flessibilità nel processo di scrittura. Gli scrittori utilizzano i rami per:

* Apportare modifiche e rivederle in un ambiente di anteprima prima che siano pubblicate.
* Inviare le modifiche ai compagni di squadra per la revisione.
* Apportare modifiche su più pagine.

<PlanTable currentPlan="Business" />

<Callout icon="💼" theme="default">
  **Nota:** Le opzioni di revisione aggiuntive sono disponibili solo sui piani Enterprise.
</Callout>

***

## Creazione di un Ramo

Ci sono tre modi per creare un ramo:

1. Naviga nel menu delle versioni e dei rami. Una volta lì, puoi creare nuovi rami da una versione.
2. Mentre modifichi una versione, invece di salvare puoi salvare in un nuovo ramo.
3. Se stai [sincronizzando con GitHub](https://docs.readme.com/main/docs/bi-directional-sync), i rami creati in GitHub appariranno in ReadMe. E i rami creati nell'interfaccia ReadMe appariranno automaticamente in GitHub!

Una volta creato il tuo ramo, puoi iniziare a scrivere! Le modifiche non saranno pubblicate fino a quando non unirai il tuo ramo in una versione pubblica.

<Image align="center" border={false} src="https://files.readme.io/65abcb59c51a4be0b668815cf0046ee818e93228057a6bff5ddbe4d3a4b9b97e-Getting_Started_with_Owlberts_Journeys-20250512-1502362x.webp" />

Non ci sono limiti di tempo o scadenze sui rami. Qualsiasi amministratore del tuo team può visualizzare, modificare, unire ed eliminare qualsiasi ramo.

***

## Revisione delle Modifiche

<Image align="center" alt="Scheda di revisione che mostra le differenze tra due pagine riga per riga" border={false} src="https://files.readme.io/95ab92ffd9eec49ad16b279f1e4a66de1f54cc95eb121f43c381258fb1d7915e-Review-20251104-1847122x.webp" />

Quando modifichi un ramo, puoi accedere alla scheda Revisione per confrontare le modifiche apportate nel tuo ramo.

<Callout icon="☝️" theme="default">
  Quando riordini i file, sono rappresentati come modifiche al file `_order` nella tua documentazione. Ogni elemento nel file `_order` rappresenta una pagina nella tua documentazione e corrisponde allo slug di ogni pagina
</Callout>

I clienti con la funzione di Revisione possono anche contrassegnare i rami come pronti per la revisione, il che aggiunge un badge nel menu delle versioni e dei rami, e avvia il [AI Linter](https://docs.readme.com/main/docs/linter). Gli utenti possono bypassare i requisiti di unione spuntando la casella "Unisci senza requisiti soddisfatti" per abilitare il pulsante **Unisci**.

***

## Unione delle Modifiche

Una volta che sei pronto per rendere pubbliche le modifiche, puoi unire dal menu del ramo:

<Image align="center" border={false} width="300px" src="https://files.readme.io/0c4c2909e376be33b974e008b8b9b9f14860b13c3eff12b5be8a377395fd68e4-Getting_Started_with_Owlberts_Journeys-20250528-1418472x.png" />

Durante l'unione, verrà eseguito un controllo per assicurarsi che non ci siano conflitti di unione. Se ci sono conflitti che devono essere risolti, raccomandiamo di [risolvere i conflitti da GitHub](https://docs.readme.com/main/docs/branches#/handling-conflicts). Se il tuo progetto non si sincronizza con GitHub, puoi ignorare il conflitto e unire forzatamente le loro modifiche—con preferenza per le modifiche nel ramo.

Una volta uniti, i tuoi rami non vengono eliminati così puoi rivedere le modifiche prima di eliminarli.

<Callout icon="💁‍♂️" theme="default">
  Gli utenti GitHub possono anche unire un ramo in una versione—incluso tramite Pull Request.
</Callout>

### Limitare l'Unione agli Amministratori

I clienti Enterprise possono limitare l'accesso all'unione per progetto a [Solo Amministratori o Amministratori ed Editor](https://docs.readme.com/ent/docs/user-roles/). Le impostazioni si trovano nella pagina del progetto del Dashboard Enterprise. Apri **Impostazioni** > **Nome Enterprise** (in fondo) > **Progetti**

***

## Sincronizzazione con GitHub

Non è necessario sincronizzare con GitHub per utilizzare i rami.

Quando crei rami da GitHub, il loro nome deve essere formattato per includere la loro versione: `{versione}_{ramo}`. Esempi:

```
v2.0_riscrivi-guida-iniziale
v2.0_aggiungi-nuova-funzione
v2.0_correggi-errore-tipografico
```

### Accesso e Permessi

I permessi di ReadMe e GitHub sono indipendenti. Gli utenti con accesso ai rami del tuo progetto GitHub avranno accesso a qualsiasi modifica del contenuto. Affinché gli utenti possano visualizzare le modifiche del contenuto apportate nei rami tramite GitHub, avranno bisogno di un account ReadMe con accesso al ramo del tuo progetto.

### Gestione dei Conflitti

Quando si unisce da GitHub, l'utente può risolvere i conflitti tramite l'editor di GitHub o lo strumento di unione di sua scelta localmente prima di effettuare il push.

Quando si unisce da ReadMe, le modifiche che vedi durante l'anteprima corrisponderanno sempre a ciò che viene pubblicato durante l'unione. Le modifiche in conflitto da GitHub non appariranno.

***

## FAQ

<Accordion title="Chi può visualizzare un ramo?" icon="fa-help-circle">
  Solo i compagni di squadra con accesso al tuo progetto possono visualizzare i tuoi rami—inclusi i ruoli di Editor e Visualizzatore del team.
</Accordion>