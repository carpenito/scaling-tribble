---
title: Linter
excerpt: >-
  Il Linter automatizza la validazione dei contenuti controllando la
  documentazione rispetto alla guida di stile aziendale e agli standard di
  scrittura consolidati.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
Il Linter automatizza la validazione dei contenuti controllando la documentazione rispetto alla guida di stile della tua azienda e agli standard di scrittura consolidati. Semplifica il processo di revisione manuale che gli scrittori tipicamente eseguono con strumenti esterni.

Puoi configurare regole personalizzate per applicare la formattazione del codice, la scelta delle parole e l'adesione allo stile interno e alle migliori pratiche. Che la tua documentazione includa HTML personalizzato o esempi di codice estesi, il Linter garantisce coerenza in tutti i tuoi documenti.

<PlanTable currentPlan="Startup" />

## Configurazione

Puoi aggiungere prompt al Linter che sono categorizzati come guida di stile, errori o avvertenze.

<Image border={false} src="https://files.readme.io/6844539c6c370fbc5fe87fa2bab007e50aa4fb52673fa629d247d0836534c971-image.png" />

**Guida di Stile**: Scrivi su cosa rende eccezionale la documentazione e il Linter valuterà i tuoi contenuti. Esempio:

> Mantienilo breve:
>
> Il testo breve è sempre migliore. I paragrafi brevi sono più facili da leggere. Cerca di mantenere le intestazioni su una riga. Le intestazioni su due righe occupano il doppio dello spazio verticale. Usa parole brevi nelle intestazioni; se un cliente usa caratteri più grandi per migliorare l'accessibilità, le parole lunghe potrebbero andare a capo.

<br />

> Chiarezza:
>
> Testo chiaro e conciso per una facile scansione e leggibilità. Vai al punto così gli utenti possono trovare facilmente quello che cercano. Non usare parole eccessive.

<br />

> Tono naturale e umano:
>
> Usa parole di tutti i giorni che sono facili da capire. Meno formale ma più professionale della conversazione quotidiana. Occasionalmente usa un tono divertente per momenti di celebrazione ma mai per testi informativi. Sii caloroso e di supporto agli utenti che leggono la documentazione.

<br />

**Errori**: Regole che possono essere verificate oggettivamente. Esempio:

> Scrivi ReadMe correttamente:
>
> Sbagliato: Readme
>
> Giusto: ReadMe

<br />

> Racchiudi gli elementi di codice in backtick (`):
>
> Sbagliato: Esegui npm install –g my–package
>
> Giusto: Esegui `npm install –g my–package`

<br />

> Segnala il testo segnaposto come TODO, FIXME, o Lorem ipsum
>
> Esempio: TODO: Aggiungi descrizione e immagine a questa funzionalità

<br />

**Avvertenze**: Per evidenziare problemi che potrebbero essere soggettivi. Esempio:

> Linguaggio Evasivo:
>
> Evita di usare un linguaggio incerto o eccessivamente cauto. Compromette la fiducia e rende le tue istruzioni meno dirette. Opta per un linguaggio chiaro e sicuro.
>
> Sbagliato: Potresti voler considerare di installare l'ultima versione.
>
> Giusto: Puoi installare l'ultima versione per accedere alle nuove funzionalità.

<br />

> Scrittura debole:
>
> Evita la scrittura debole come 'Puoi' o 'C'è'. Queste frasi nascondono l'azione, rendono la scrittura meno diretta e spesso aggiungono parole inutili. La documentazione efficace è chiara e orientata all'azione.
>
> Sbagliato: Puoi configurare l'API modificando il file delle impostazioni.
>
> Giusto: Configura l'API modificando il file delle impostazioni.

<br />

> Forma attiva:
>
> Evita di usare la forma passiva. La forma attiva è più chiara, più breve e dice al lettore esattamente chi sta facendo cosa.
>
> Sbagliato: Il token viene generato quando l'utente effettua l'accesso.
>
> Giusto: Il sistema genera un token quando l'utente effettua l'accesso.

<br />

## Esecuzione del Linter

Una volta configurato, l'esecuzione del Linter controlla la tua pagina rispetto ai tuoi prompt. I problemi possono essere risolti automaticamente utilizzando l'Agent.

<Image align="center" border={false} width="350px" src="https://files.readme.io/02345a8505f8f89eaa3d97019252e3cfc3c9e16fdaed63ac7ed7b6df97b765f5-linter.png" />

<br />

## FAQ

<Accordion title="Dove dovrei inviare feedback o domande?" icon="fa-messages-question">
  Invia feedback o domande via email a [beta@readme.io](mailto:beta@readme.io)
</Accordion>

<Accordion title="Quale modello usa il Linter?" icon="fa-wand-sparkles">
  Al momento utilizziamo Gemini 2.5 Flash—anche se potrebbe cambiare mentre ci adattiamo per bilanciare qualità e velocità. In futuro gli utenti avranno l'opzione di selezionare i modelli di loro scelta.
</Accordion>