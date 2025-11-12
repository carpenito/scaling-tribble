---
title: Guida introduttiva a TranslationsQA_Nov2025
excerpt: >-
  Questa pagina ti aiuterà a muovere i primi passi con
  Kirb_TranslationsQA_Nov2025. Sarai operativo in un batter d'occhio!
hidden: false
---
# Benvenuto in ReadMe

Benvenuto nel tuo nuovo hub per sviluppatori: basato sull'intelligenza artificiale, supportato da Git e progettato per aiutare i tuoi documenti a evolversi insieme al tuo prodotto.

Quella che stai guardando è una pagina iniziale che abbiamo incluso per aiutarti a iniziare. Sentiti libero di considerarla come il tuo primo documento: clicca su Modifica in alto per personalizzarla o eliminala per ricominciare da capo.

***

## ✍️ Scrivi documenti con componenti e guide

Inizia creando <Anchor label="**Guide**" target="_blank" href="https://docs.readme.com/main/docs/creating-and-managing-guides">**Guide**</Anchor> - il manuale di istruzioni della tua API, dove puoi guidare gli utenti attraverso concetti chiave, tutorial o best practice.

Con l'editor MDX di ReadMe, puoi combinare Markdown e componenti JSX personalizzati come `<Carta>`, `<scheda>`, and `<Fisarmonica>` per contenuti più ricchi e una struttura migliore.

Puoi anche [Crea i tuoi **componenti** personalizzati**](/docs/getting-started#/settings/custom-components/start) da riutilizzare nei tuoi documenti.

<Cards columns={3}>
  <Card title="Esplora il marketplace dei componenti" href="https://github.com/readmeio/marketplace/tree/main/components" icon="fa-store" target="_blank">
    Inserisci e personalizza i componenti.
  </Card>

  <Card title="MDX (Markdown + JSX)" href="https://docs.readme.com/main/docs/mdx" icon="fa-code">
   Scopri di più su MDX per creare componenti interattivi.
  </Card>

  <Card title="Componenti MDX personalizzati" href="https://docs.readme.com/main/docs/building-custom-mdx-components" icon="fa-wrench">
    Crea i tuoi componenti personalizzati da riutilizzare ovunque.
  </Card>
</Cards>

Cerchi un punto di accesso brandizzato? Abilita un **<Anchor label="Pagina di destinazione" target="_blank" href="https://docs.readme.com/main/docs/landing-page">Pagina di destinazione</Anchor>** per dare il benvenuto ai tuoi sviluppatori e indirizzarli ai documenti chiave.

***

## 🤖 Aggiungi l'IA al tuo Dev Hub

L'intelligenza artificiale è integrata in ReadMe per aiutare te e i tuoi utenti a muovervi più velocemente. Apri il pannello facendo scorrere il cursore su **:sparkles:AI** nella barra di navigazione superiore.

* **Agente AI**  
  Il nostro agente AI integrato è il tuo assistente per redigere documenti, tradurre pagine e applicare guide di stile.

* **Server MCP**  
  Genera un server **MCP** per convertire la tua documentazione API in una risorsa strutturata che gli assistenti AI possono comprendere e con cui possono interagire a livello di programmazione.

* **Ricerca basata sull'intelligenza artificiale**  
  Abilita la ricerca AI per aiutare gli sviluppatori a porre domande sul tuo prodotto e ricevere immediatamente una risposta.

* **Apri in altri servizi di intelligenza artificiale**  
  Consenti ai tuoi sviluppatori di aprire i tuoi documenti in strumenti come ChatGPT, Claude o altri LLM, utilizzando il contesto della tua API e `llms.txt` configurazione.

***

## 🌿 Modifica, anteprima e pubblicazione nei rami

<Anchor label="Rami" target="_blank" href="https://docs.readme.com/main/docs/branches">Rami</Anchor> introduci flussi di lavoro in stile Git nel tuo processo di documentazione. Usali per:

* Modifica bozze su più pagine senza pubblicarle immediatamente
* Controlla e visualizza in anteprima gli aggiornamenti prima che vengano pubblicati
* Condividi le modifiche con i colleghi per ricevere feedback
* Ripeti le operazioni in modo sicuro senza interrompere la produzione dei documenti

Puoi creare un ramo direttamente dal menu Versioni e rami, salvare le modifiche in un nuovo ramo o sincronizzare con GitHub e riflettere automaticamente i rami su entrambe le piattaforme.

Una volta pronto, unisci il ramo alla versione live. I piani Enterprise consentono di controllare chi ha accesso all'unione e prima dell'unione viene sempre eseguito un controllo dei conflitti.

***

## 🔁 Sincronizza con Git

Che tu scriva documenti nell'editor di ReadMe o nel tuo ambiente di sviluppo locale, ReadMe si adatta al tuo flusso di lavoro:

* **[Sincronizzazione bidirezionale con GitHub](https://docs.readme.com/main/docs/bi-directional-sync)**  
  Collega un repository GitHub al tuo progetto e lavora nei rami. Le modifiche in Git o ReadMe rimarranno sincronizzate: perfetto per i flussi di lavoro di staging e revisione del codice.

* **Sincronizza i tuoi file OpenAPI**  
  Utilizzo [`rdme`](https://docs.readme.com/docs/rdme#upload) oppure l'API ReadMe per inviare le specifiche OpenAPI e mantenere aggiornato automaticamente il riferimento API.

***

## 👀 Comprendere i propri sviluppatori

Vuoi sapere come gli sviluppatori utilizzano effettivamente la tua API e la tua documentazione?

* **<Anchor label="I miei sviluppatori" target="_blank" href="https://docs.readme.com/main/docs/developer-dashboard">I miei sviluppatori</Anchor>** ti offre visibilità in tempo reale su chi sta visitando i tuoi documenti, quali endpoint stanno utilizzando e dove si bloccano.
* Segmenta l'utilizzo in base agli utenti chiave o ai gruppi per monitorare il coinvolgimento e individuare i problemi prima che si trasformino in richieste di assistenza.
* Per configurare My Developers, dovrai prima autenticare gli utenti che hanno effettuato l'accesso con il <Anchor label="Webhook personalizzato per documenti" target="_blank" href="https://docs.readme.com/main/docs/personalized-docs-webhook">Webhook personalizzato per documenti</Anchor>, quindi integrare il [SDK Metrics](https://docs.readme.com/main/docs/sending-api-logs) per inviare i log API a ReadMe.

***

## 🚀 Prossimi passi

* Inizia a scrivere: crea la tua prima Guida o sincronizza il tuo file OAS.
* [Connetti GitHub per la sincronizzazione bidirezionale](/docs/getting-started#/settings/git-connection/github).
* Configura il tuo <Anchor label="Server MCP" target="_blank" href="https://docs.readme.com/main/docs/mcp-servers">Server MCP</Anchor>.
* Visita **I miei sviluppatori** nella barra di navigazione in alto per iniziare a comprendere il tuo pubblico.

***

<Callout icon="💼" theme="default">
  Need support for multiple products, advanced permissions, or deeper customization?  
  Our enterprise features are built for teams managing business-critical APIs at scale. [Let's talk.](mailto:growth@readme.io)
</Callout>

## 💬 Need Help?

Our team is here to support you. If you get stuck, [email us](mailto:support@readme.io) or open the Intercom widget on any page to chat with someone from our team. We've also got a <Anchor label="Slack community" target="_blank" href="https://readme.com/slack">Slack community</Anchor> if you want to say hi to the team and connect with other ReadMe users!
