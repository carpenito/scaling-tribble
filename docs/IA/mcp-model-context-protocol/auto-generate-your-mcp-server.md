---
title: Genera Automaticamente il Tuo Server MCP
excerpt: >-
  Con ReadMe, ogni progetto include automaticamente un server MCP completamente
  configurato. Basta abilitare MCP per connettere la documentazione API agli
  strumenti AI.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
Con ReadMe, ogni progetto include automaticamente un server MCP completamente configurato. Basta abilitare MCP per connettere la documentazione API agli strumenti AI.

## Come Generare il Proprio Server MCP

In Modalità Modifica, nell'angolo in alto a destra, clicca su **:sparkles:AI** per aprire il pannello laterale. Seleziona **MCP** e attiva il toggle Server MCP per attivare il tuo server MCP. Il tuo URL MCP sarà: `https://your-project.readme.com/mcp`. Puoi condividere il tuo URL MCP con i tuoi sviluppatori, e potranno connettere i loro assistenti AI e strumenti direttamente alla tua API. Gli endpoint che non vuoi rendere accessibili nel tuo server MCP possono essere disabilitati sotto Route MCP Abilitate.

L'AI dovrebbe ora avere accesso ai dati del tuo account ReadMe e alla documentazione tramite il server MCP.

<Image align="center" border={false} width="35% " src="https://files.readme.io/f4981199e6757d7c7a64ff259c4c592ab97b8b91f91255804a6a5a8d696fbd9b-mcp_advanced.png" />

### Strumenti Personalizzati

<br />

## Testare la Configurazione MCP

Una volta configurato, puoi testare la connessione del tuo server MCP:

1. Apri il tuo editor AI (Cursor, VS Code, ecc.)
2. Inizia una nuova chat con l'assistente AI
3. Fai domande sulla tua API e documentazione. Prova queste domande:
   * "Come faccio a [caso d'uso comune]?"
   * "Mostrami un esempio di [funzionalità API]"
   * "Crea una [tipo di integrazione] usando [la tua API]"

## Come Generare Istruzioni di Accesso Per i Tuoi Utenti

Una volta attivato il tuo server MCP, puoi generare automaticamente le istruzioni di accesso per i tuoi utenti finali cliccando il pulsante "Genera Template MCP". Questo crea un nuovo documento non pubblicato chiamato "MCP" nelle tue Guide che mostra come connettersi al tuo server MCP in strumenti come Cursor e Claude Desktop. Puoi trovare il documento in fondo alle tue Guide o Riferimenti API in una nuova categoria chiamata "MCP SERVER."