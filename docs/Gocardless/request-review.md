---
title: Verzoek om beoordeling
deprecated: false
hidden: false
icon: fad fa-rocket-launch
metadata:
  robots: index
---
<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ReadMe Platform — Criteria Breakdown</title>
<style>
  :root {
    --bg: #f9f8f6;
    --bg-card: #ffffff;
    --text-primary: #1a1a18;
    --text-secondary: #5c5c57;
    --text-tertiary: #9c9a92;
    --border: rgba(0,0,0,0.1);
    --border-strong: rgba(0,0,0,0.18);
    --green-bg: #eaf3de;
    --green-text: #3b6d11;
    --amber-bg: #faeeda;
    --amber-text: #854f0b;
    --red-bg: #fcebeb;
    --red-text: #a32d2d;
    --radius-md: 8px;
    --radius-lg: 12px;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --bg: #1c1c1a;
      --bg-card: #252523;
      --text-primary: #e8e6de;
      --text-secondary: #b0ae a6;
      --text-tertiary: #6e6c65;
      --border: rgba(255,255,255,0.08);
      --border-strong: rgba(255,255,255,0.14);
      --green-bg: #173404;
      --green-text: #97c459;
      --amber-bg: #412402;
      --amber-text: #ef9f27;
      --red-bg: #501313;
      --red-text: #f09595;
    }
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: 'DM Sans', 'Helvetica Neue', Arial, sans-serif;
    background: var(--bg);
    color: var(--text-primary);
    padding: 2.5rem 2rem;
    max-width: 960px;
    margin: 0 auto;
    line-height: 1.6;
  }
  header { margin-bottom: 2rem; }
  h1 { font-size: 22px; font-weight: 600; margin-bottom: 4px; }
  .subtitle { font-size: 14px; color: var(--text-secondary); }
  .legend {
    display: flex; gap: 20px; margin-bottom: 1.5rem; flex-wrap: wrap;
    font-size: 12px; color: var(--text-secondary);
  }
  .legend span { display: flex; align-items: center; gap: 6px; }
  .legend-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .section-label {
    font-size: 11px; font-weight: 600; color: var(--text-tertiary);
    text-transform: uppercase; letter-spacing: 0.07em;
    margin: 2rem 0 0.75rem;
  }
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 12px;
  }
  .card {
    background: var(--bg-card);
    border: 0.5px solid var(--border);
    border-radius: var(--radius-lg);
    padding: 1rem 1.25rem;
  }
  .card-header {
    display: flex; align-items: flex-start;
    justify-content: space-between; gap: 10px; margin-bottom: 8px;
  }
  .card-title { font-size: 13px; font-weight: 600; color: var(--text-primary); }
  .badge {
    font-size: 11px; font-weight: 600; padding: 3px 9px;
    border-radius: 20px; white-space: nowrap; flex-shrink: 0;
  }
  .badge-yes  { background: var(--green-bg); color: var(--green-text); }
  .badge-partial { background: var(--amber-bg); color: var(--amber-text); }
  .badge-no   { background: var(--red-bg); color: var(--red-text); }
  .card-body  { font-size: 12px; color: var(--text-secondary); line-height: 1.65; }
  .card-detail {
    font-size: 11px; color: var(--text-tertiary);
    margin-top: 8px; padding-top: 8px;
    border-top: 0.5px solid var(--border);
    font-style: italic;
  }
  footer {
    margin-top: 2.5rem;
    font-size: 11px;
    color: var(--text-tertiary);
    border-top: 0.5px solid var(--border);
    padding-top: 1rem;
  }
</style>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&display=swap" rel="stylesheet">
</head>
<body>

<header>
  <h1>ReadMe — Overzicht platformcriteria</h1>
  <p class="subtitle">Beoordeling van ReadMe aan de hand van vereisten voor documentatieplatforms</p>
</header>

<div class="legend">
  <span><span class="legend-dot" style="background:#3b6d11"></span>Native / sterke match</span>
  <span><span class="legend-dot" style="background:#854f0b"></span>Gedeeltelijk / met configuratie</span>
  <span><span class="legend-dot" style="background:#a32d2d"></span>Ontbrekend / vereist workaround</span>
</div>

<!-- Core platform -->
<div class="section-label">Kern documentatieplatform</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">API-referentie als code</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">OpenAPI-spec als enige bron van waarheid — ReadMe rendert API-referentie rechtstreeks vanuit je spec en werkt automatisch bij bij schemawijzigingen. Upload handmatig, via API of via een CI/CD-pipeline.</div>
    <div class="card-detail">Ondersteunt OAS 3.x. Gebruik de rdme CLI voor spec-synchronisatie in GitHub Actions.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Codevoorbeelden in meerdere talen</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Automatisch gegenereerde codevoorbeelden vanuit de OpenAPI-spec in 10+ talen. Aangepaste voorbeelden kunnen per endpoint worden toegevoegd. Taalkiezer is ingebouwd in de referentie-UI.</div>
    <div class="card-detail">Geen handmatig onderhoud nodig als de bron spec-extensies zijn (x-readme).</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Try-it / live sandbox</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Ingebouwde "Try It!"-API-verkenner op elk endpoint. Ondersteunt pre-authenticatie met gebruikersspecifieke API-sleutels voor integrators via de ReadMe JWT/OAuth-integratie.</div>
    <div class="card-detail">Enterprise: gepersonaliseerde variabelen gevuld vanuit de inlogcontext van de gebruiker.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Changelog als content</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Volwaardige Changelog-sectie met versiebeheer en RSS-abonnement. Changelog-vermeldingen kunnen worden gekoppeld vanuit API-referentiepagina's. Schrijf in markdown of via API.</div>
    <div class="card-detail">Automatisch koppelen vanuit referentie vereist handmatige kruisverwijzingen — niet volledig automatisch.</div>
  </div>
</div>

<!-- Search -->
<div class="section-label">Zoeken &amp; vindbaarheid</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Verbeterd zoeken</span>
      <span class="badge badge-partial">Gedeeltelijk</span>
    </div>
    <div class="card-body">ReadMe heeft ingebouwde volledige tekstzoekfunctie. Semantisch zoeken en het bijhouden van zoekopdrachten zonder resultaten zijn niet native — het bijhouden van hiaten is beschikbaar via het analyserapport Zoekopdrachten, maar wordt niet automatisch gemarkeerd.</div>
    <div class="card-detail">Zoekanalyses tonen wat mensen zochten zonder resultaten. Semantische rangschikking is momenteel niet configureerbaar.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Vindbare informatiestructuur</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Hiërarchische navigatie met categorieën, subcategorieën en aangepaste volgorde. Ondersteunt meerdere documentversies en doelgroepgerichte navigatie. De informatiestructuur wordt beheerd via het dashboard of via de Guides API.</div>
    <div class="card-detail">Gepersonaliseerde navigatie per integratietype vereist aangepaste JS of dynamische contentblokken.</div>
  </div>
</div>

<!-- AI -->
<div class="section-label">AI &amp; moderne tooling</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">AI-native / LLM-leesbaar</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Volledig AI-native stack: LLMs.txt automatisch gegenereerd met één schakelaar (alle abonnementen, nul onderhoud). Twee native MCP-servers — één voor documentauteurs om docs te beheren via AI, één voor API-gebruikers om hun AI-tools live toegang te geven tot je spec en docs. ReadMe-pagina's renderen schone HTML en bieden een openbare sitemap — crawlbaar door LLM's. Native llms.txt wordt ondersteund en genereert automatisch een configuratiebestand in de root van je documentatiesite op basis van je bestaande documentatiestructuur.</div>
    <div class="card-detail">LLMs.txt beschikbaar op alle abonnementen. MCP-servers zijn ingebouwd, geen aangepaste integratie.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Personalisatie</span>
      <span class="badge badge-partial">Gedeeltelijk</span>
    </div>
    <div class="card-body">ReadMe ondersteunt gebruikersvariabelen (bijv. vooraf ingevulde API-sleutels, bedrijfsnaam) via JWT SSO. Vertakking van content op basis van schema/land/integratiemethode is niet native — vereist aangepaste logica of afzonderlijke documentversies.</div>
    <div class="card-detail">Enterprise variabele-injectie is sterk voor authenticatiecontext; voorwaardelijke contentblokken zijn beperkt.</div>
  </div>
</div>

<!-- Performance -->
<div class="section-label">Prestaties &amp; governance</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">SSR / snelle paginalaadtijd</span>
      <span class="badge badge-partial">Gedeeltelijk</span>
    </div>
    <div class="card-body">Het gehoste platform van ReadMe maakt gebruik van SSR. TTFB en Core Web Vitals zijn over het algemeen goed op het standaardthema, maar je hebt geen directe controle over de infrastructuur — sub-100ms TTFB-SLA's zijn niet gegarandeerd of contractueel beschikbaar.</div>
    <div class="card-detail">Aangepast domein + CDN wordt ondersteund. Prestatieoptimalisatie is beperkt ten opzichte van zelfgehoste oplossingen.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Contentgovernance</span>
      <span class="badge badge-partial">Gedeeltelijk</span>
    </div>
    <div class="card-body">Bidirectionele GitHub Sync stelt teams in staat PR's te gebruiken voor documentatiereviews. Controle op verbroken links en linting zijn niet native — je hebt een CI-stap nodig tegen de live site of geëxporteerde content.</div>
    <div class="card-detail">GitHub Sync is beschikbaar op Business/Enterprise-abonnementen. Tooling voor kwaliteitscontrole is een hiaat.</div>
  </div>
</div>

<!-- Analytics -->
<div class="section-label">Analyses &amp; feedback</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Feedbackloops voor ontwikkelaars</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Beoordelingen per pagina (duim omhoog/omlaag) zijn ingebouwd. Developer CSAT wordt weergegeven in het Metrics-dashboard. Opmerkingen kunnen per pagina worden ingeschakeld voor directe feedback.</div>
    <div class="card-detail">Beoordelingen worden samengevat in het analysedashboard — filterbaar op pagina, versie en tijdsbereik.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Contentanalyses</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">ReadMe Metrics houdt paginaweergaven, tijd op pagina, zoekopdrachten en uitstappercentages bij. API-aanroepanalyses zijn ook beschikbaar bij gebruik van de API-logging van ReadMe.</div>
    <div class="card-detail">Volledige analyse van zoekresultaathiaten is beschikbaar. Doorsturen naar externe tools vereist de Metrics API of webhook.</div>
  </div>
</div>

<!-- Workflow -->
<div class="section-label">Workflow &amp; bewerken</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Eenvoudig bij te werken</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">WYSIWYG-editor voor niet-technici, markdown/MDX voor engineers, plus GitHub Sync voor code-first teams. Lage drempel voor beide doelgroepen — geen buildstap vereist voor puur inhoudelijke bewerkingen.</div>
    <div class="card-detail">Engineers kunnen ook de Guides API of CLI gebruiken voor bulkupdates en automatisering.</div>
  </div>
</div>

<footer>Gegenereerd vanuit ReadMe-platformevaluatie · readme_criteria_breakdown</footer>

</body>
</html>
`}</HTMLBlock>

Hier is hoe je het totaalplaatje kunt beoordelen:

Waar ReadMe een sterke match is:

* de kern van wat je vraagt is precies waarvoor ReadMe is gebouwd. OpenAPI-gesynchroniseerde referentie, codevoorbeelden in meerdere talen, Try It-sandbox, changelog, paginabeoordelingen en contentanalyses zijn allemaal eersteklas functies. De combinatie van WYSIWYG + GitHub Sync sluit direct aan op de vereiste "eenvoudig bij te werken voor engineers en niet-engineers".
* AI-native / MCP-indexering — ReadMe levert beide kanten van het MCP-verhaal:
  De auteurgerichte MCP-server stelt je team in staat om documentatie te bevragen, te lezen en bij te werken via AI-tools — handig voor contentworkflows, bulkbewerkingen en AI-ondersteund schrijven rechtstreeks tegen je live docs.
  De gebruikersgerichte MCP-server is de strategisch meest significante voor deze evaluatie — die geeft de AI-tools van je API-gebruikers (Cursor, Claude, Windsurf, etc.) live toegang tot je spec en docs als context terwijl ze coderen. Dat is precies wat het criterium "MCP-geïndexeerd" in de oorspronkelijke vereisten vroeg.
  Dit maakt het AI-native verhaal van ReadMe sterker dan ik aanvankelijk had beoordeeld — en sterker dan wat veel concurrenten bieden. De enige resterende nuance op die kaart is of llms.txt native wordt gegenereerd, maar het MCP-onderdeel is duidelijk gedekt. Het is de moeite waard het artefact bij te werken als je het deelt.

Waar het gedeeltelijk is, en wat je eraan kunt doen:

* Semantisch zoeken — het huidige zoeken is op trefwoorden gebaseerd. Het bijhouden van zoekopdrachten zonder resultaten is beschikbaar in analyses (je kunt zien wat geen resultaten opleverde), maar wordt niet automatisch als actiepunt gepresenteerd. Als semantisch zoeken een harde eis is, is dit het grootste hiaat ten opzichte van alternatieven zoals Mintlify of een aangepaste Algolia-integratie.
* Garantie voor sub-100ms TTFB — de SSR-prestaties van ReadMe zijn over het algemeen solide, maar je zit op hun infrastructuur en kunt geen TTFB-SLA contractueel afdwingen. Als dat een harde eis is, geven zelfgehoste oplossingen (Mintlify, Docusaurus + Vercel) je meer controle.
* Contentgovernance / kwaliteitscontrole — GitHub Sync regelt het PR-reviewgedeelte goed, maar controle op verbroken links en linting moeten worden toegevoegd in CI (bijv. broken-link-checker tegen je staging-URL bij elke PR). ReadMe dwingt dit niet native af.
* Personalisatie op basis van schema/land/integratiemethode — injectie van gebruikersvariabelen (API-sleutels, bedrijfsnaam) is uitstekend. Echte voorwaardelijke contentvertakking op integratietype is niet native en vereist ofwel afzonderlijke versioned documentatiebomen of aangepaste JS-blokken.
* Over de vraag bouwen vs. kopen vs. open source — ReadMe valt duidelijk in de categorie "kopen" met een sterk beheerd-platform verhaal. Als strikte prestatie-SLA's, diepgaande MCP/AI-native functies of uitgebreide voorwaardelijke content harde eisen zijn, is het de moeite waard Mintlify naast elkaar te zetten (sterker AI-native verhaal, meer configuratieflexibiliteit) en Docusaurus + Vercel (volledige controle, meer engineeringinspanning). Ik maak graag een directe vergelijking met een van beide als dat nuttig is.