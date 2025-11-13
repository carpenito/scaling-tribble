---
title: Temi
excerpt: >-
  Personalizza l'aspetto della tua documentazione con le opzioni di tema
  disponibili in ReadMe, inclusi layout, branding e stili di intestazione.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
Tutti i piani hanno accesso alla personalizzazione nelle impostazioni **Tema**. Apri **Impostazioni** in alto a sinistra dell'interfaccia di amministrazione, quindi seleziona **Tema** nella barra laterale.

* Layout
* Branding (Logo, Favicon e Colori)
* Stile intestazione

<PlanTable currentPlan="Free" />

<Callout icon="💁‍♂️" theme="default">
  **Nota:** Opzioni di personalizzazione aggiuntive e servizi sono disponibili nei piani Business ed Enterprise.
</Callout>

***

## Layout

<Image align="center" border={false} width="400px" src="https://files.readme.io/3d30b1d7f55cd7e37def92bb05c5c4799bc0e1294169209626ff9a24181733cc-Launch_Week-20250628-1026262x.webp" />

Puoi scegliere tra 3 opzioni di layout: Classic, Compact e Modern. C'è anche un'opzione per estendere il layout per schermi più grandi. Potrai visualizzare l'anteprima del layout prima di salvare.

<Callout icon="🚧" theme="warn">
  Un'opzione solo barra laterale arriverà presto!
</Callout>

***

## Branding

### Logo

È disponibile un'opzione per caricare un logo bianco quando è necessaria un'alternativa per certi temi e impostazioni del colore dell'intestazione.

**Formato**

* SVG è preferito per la migliore qualità.
* Se il tuo logo è troppo complesso per un SVG, WEBP è una buona alternativa—usa 2x della dimensione desiderata del tuo logo per la chiarezza nei display ad alta risoluzione.
* I GIF non sono supportati.

**Dimensioni**

* 24px di altezza per default. Nei temi Classic e Modern puoi selezionare un logo di altezza più grande a 40px.

**Personalizzazione Avanzata**

* I clienti con accesso al CSS Personalizzato possono usare le nostre classi globali e variabili css per modificare ulteriormente la visualizzazione del loro logo:

```css
.rm-Logo-img {
  --Header-logo-height: TUA_ALTEZZA_PERSONALIZZATA
}
```

***

## Intestazione

<Image align="center" border={false} width="400px" src="https://files.readme.io/9c14d52d69809626037d9cb483cd2fb0619734f6ccc3c3428fd6380936a44b43-Launch_Week-20250628-1043112x.webp" />

Puoi scegliere tra 4 opzioni di layout: Linea, Colore Solido, Gradiente e Sovrapposizione.

<Callout icon="💁‍♂️" theme="default">
  L'opzione intestazione Linea ora è predefinita con una visualizzazione a schede per i link. Gli utenti con la precedente visualizzazione a pulsanti possono cambiare. Una volta cambiato, non potrai tornare indietro.
</Callout>

**Personalizzazione Avanzata**

* I clienti con accesso al CSS Personalizzato possono usare le nostre classi globali e variabili css per modificare ulteriormente la loro intestazione:

```css
.rm-Header {
  --Header-background: TUO_VALORE_PERSONALIZZATO /* predefinito al tuo colore del brand */
  --Header-border-color: TUO_VALORE_PERSONALIZZATO /* predefinito: rgba(0, 0, 0, 0.1) */
  --Header-button-padding: TUO_VALORE_PERSONALIZZATO /* predefinito: 10px */

  /* Solo tema Linea */
  --Header-tab-underline: TUO_VALORE_PERSONALIZZATO /* predefinito al tuo colore del brand */
}
```