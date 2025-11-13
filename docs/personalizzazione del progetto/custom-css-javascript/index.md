---
title: CSS e JavaScript Personalizzati
excerpt: >-
  Scopri come aggiungere CSS e JavaScript personalizzati per personalizzare
  ulteriormente l'aspetto del tuo sito di documentazione.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
In questa sezione puoi aggiungere CSS e Javascript per personalizzare ulteriormente l'aspetto del tuo sito di documentazione.

<Image align="center" border={true} src="https://files.readme.io/ca07f17-CleanShot_2022-09-25_at_09.57.452x.png" className="border" />

> 🚧 Selettori
>
> Usa selettori con prefisso `.rm-`. I selettori con hash cambiano costantemente e **non dovrebbero** essere usati come selettori (es. `Header-bottom2eLKOFXMEmh5`).

## Foglio di Stile Personalizzato

<Callout icon="📘" theme="info">
  Dovresti limitare le tue modifiche a piccoli aggiustamenti. Inoltre, i fogli di stile non hanno versioni; tutte le versioni usano lo stesso foglio di stile.
</Callout>

## Javascript Personalizzato

Il tuo Javascript verrà incluso in fondo alla pagina.

<details>
  <summary><b>Variabili Globali</b></summary>

  ReadMe espone certe variabili globali per aiutarti a personalizzare l'esperienza utente del tuo hub:

  * **`RM_ReferenceSidebarScrollTopOffset`**\
    Offset in pixel per la logica di scorrimento-verso-elemento-attivo della sidebar nelle sezioni di <Glossary>Reference</Glossary> continue.
</details>

## Tag di Inclusione Personalizzati

**HTML Header**

Qualsiasi html qui verrà incluso nel tag head, che è utile per cose come meta tag e caricamento di CSS o JS esterni.

**HTML Footer**  
​  
Questo andrà proprio prima del tag `</body>`. Utile per cose come analisi e tracciamento.

## Attivazione/Disattivazione di Javascript e CSS Personalizzati

Aggiungi i parametri di query `?disableCustomCss=true&disableCustomJs=true` alla fine di qualsiasi URL.