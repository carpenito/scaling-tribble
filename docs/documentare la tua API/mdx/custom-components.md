---
title: Componenti Personalizzati
excerpt: >-
  Crea e gestisci componenti MDX personalizzati dalle impostazioni. Costruisci
  componenti riutilizzabili per la tua documentazione con anteprima in tempo
  reale.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
Crea e gestisci componenti MDX personalizzati dalla pagina **Componenti Personalizzati** in **Impostazioni**. Mentre costruisci, scriverai codice JSX e vedrai un'anteprima in tempo reale del tuo componente. Una volta salvato, puoi accedere ai tuoi componenti dal menu `<` e riutilizzarli in tutta la tua documentazione.

### Vantaggi Principali

* Trasforma i pattern comuni in componenti riutilizzabili per garantire coerenza, semplificare la manutenzione e creare un'interfaccia unificata in tutta la documentazione.
* Personalizza i contenuti in base al pubblico, caso d'uso o livello di accesso _senza_ duplicare le pagine.
* Adatta i componenti al tuo prodotto e fai risaltare la tua documentazione.
* Aggiungi interattività alla tua documentazione con componenti che fanno di più che mostrare solo contenuti.

## Marketplace

Sfoglia il Marketplace per esplorare componenti open-source sviluppati dalla community. Ogni componente è revisionato da ReadMe per qualità e conformità. Seleziona semplicemente un componente, apporta le modifiche necessarie, o usalo così com'è—poi salvalo per iniziare a integrarlo nella tua documentazione.

<Image align="center" border={false} src="https://files.readme.io/4878ee5ee5a98ad931898ff6a4638d3f79ea3f57c90296bcc65b0623d58c5219-Screenshot_2025-09-04_at_4.29.16_PM.png" />

<Callout icon="💡" theme="default">
  **Ti senti creativo?** Contribuisci con il tuo! Apri una pull request nel [repository GitHub](https://github.com/readmeio/marketplace). Una volta unita, vedi il tuo componente live nel Marketplace e aiuta a far crescere la libreria per tutti.
</Callout>

***

## Crea il Tuo Primo Componente

Analizziamo come creare un componente personalizzato semplice ma utile. Costruiremo un componente "Nota" che fa risaltare informazioni importanti nella tua documentazione.

```jsx
export const ExampleComponent = props => {
  return (
    <div className="flex items-center h-full w-full">
      <div className="bg-gray-800 rounded-md p-6 m-4">
        {props.children}
      </div>
    </div>
  );
};

<ExampleComponent>
  Ecco un esempio di componente molto semplice piuttosto che uno stato vuoto. Questo dovrebbe aiutarti a capire cosa sta succedendo più velocemente e vedere cosa è possibile con i componenti personalizzati!
</ExampleComponent>
```

### Comprendere il Codice

<Image align="center" border={false} src="https://files.readme.io/e6e6aa810d1cd0f55f001261284d475c244902bd3bd14b46e98a6b15ac2680e4-CleanShot_2025-02-24_at_12.57.54.gif" />

**Riga 1:** `export const ExampleComponent = props => {`

* Qui stiamo definendo un nuovo componente chiamato `ExampleComponent`
* La parola chiave `export` è richiesta per definire qualsiasi variabile o componente in MDX
* Possiamo accedere alle `props` di React per renderizzare qualsiasi attributo o contenuto aggiunto al tag del componente

**Righe 2-8:** La struttura del componente

* `return (...)` definisce cosa renderizzerà il componente quando viene utilizzato
* Il `<div>` esterno usa [classi Tailwind](https://tailwindcss.com/docs/styling-with-utility-classes) per centrare il contenuto (`flex items-center`) e occupare tutta la larghezza e altezza (`h-full w-full`)
* Il `<div>` interno crea una scatola grigio scuro (`bg-gray-800`) con angoli arrotondati (`rounded-md`) e spaziatura (`p-6 m-4`)
* `{props.children}` è l'ingrediente magico — renderizza qualsiasi contenuto che inserisci tra i tag del tuo componente

<Callout icon="💁" theme="default">
  ### Una Nota Rapida su Tailwind CSS

  Non preoccuparti se queste classi sembrano poco familiari! Puoi consultare la [documentazione ufficiale di Tailwind CSS](https://tailwindcss.com/docs/styling-with-utility-classes) per una guida completa su come stilizzare con le classi di utilità
</Callout>

**Righe 10-14:** Per renderizzare il componente predefinito nell'anteprima e nella tua documentazione

* Richiediamo che i componenti siano aggiunti DOPO tutte le esportazioni per renderizzare il componente nell'anteprima e utilizzarlo nell'editor
* La sintassi MDX richiede di creare una nuova riga prima del componente di anteprima o si verificherà un errore
* `<ExampleComponent>` apre il componente
* Il testo tra i tag diventa la prop `children`
* `</ExampleComponent>` chiude il componente

Questo semplice esempio crea un contenitore stilizzato riutilizzabile che puoi usare in tutta la tua documentazione. Basta avvolgere qualsiasi contenuto con i tag `<ExampleComponent>`, e apparirà in una bella scatola grigio scuro con spaziatura appropriata e angoli arrotondati!

### Guarda la ricetta qui sotto per attraversare il codice!

<Recipe slug="create-a-custom-component" title="Crea un Componente Personalizzato" />

Cosa rende questo potente? Ora puoi usare questo componente ovunque nella tua documentazione dove devi evidenziare contenuti in modo coerente. Hai bisogno di cambiare come appare il contenuto evidenziato in tutta la tua documentazione? Basta aggiornare il componente una volta, e i cambiamenti si applicano ovunque lo hai utilizzato!