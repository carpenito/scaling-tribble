---
title: Copie de la demande de révision
deprecated: false
hidden: true
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
<title>ReadMe Platform — Analyse des critères</title>
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
  <h1>ReadMe — Analyse des critères de la plateforme</h1>
  <p class="subtitle">Évaluation de ReadMe par rapport aux exigences de la plateforme de documentation</p>
</header>

<div class="legend">
  <span><span class="legend-dot" style="background:#3b6d11"></span>Natif / bonne adéquation</span>
  <span><span class="legend-dot" style="background:#854f0b"></span>Partiel / avec configuration</span>
  <span><span class="legend-dot" style="background:#a32d2d"></span>Lacune / contournement nécessaire</span>
</div>

<!-- Core platform -->
<div class="section-label">Plateforme de documentation principale</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Référence API en tant que code</span>
      <span class="badge badge-yes">Natif</span>
    </div>
    <div class="card-body">La spécification OpenAPI comme source unique de vérité — ReadMe génère la référence API directement depuis votre spec, avec mise à jour automatique lors des changements de schéma. Importation manuelle, via API ou pipeline CI/CD.</div>
    <div class="card-detail">Prend en charge OAS 3.x. Utilisez le CLI rdme pour la synchronisation des specs dans GitHub Actions.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Exemples de code multi-langages</span>
      <span class="badge badge-yes">Natif</span>
    </div>
    <div class="card-body">Exemples de code générés automatiquement depuis la spécification OpenAPI dans plus de 10 langages. Des exemples personnalisés peuvent être ajoutés par endpoint. Le sélecteur de langage est intégré à l'interface de référence.</div>
    <div class="card-detail">Aucune maintenance manuelle nécessaire si les exemples proviennent des extensions de spec (x-readme).</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Try-it / bac à sable en direct</span>
      <span class="badge badge-yes">Natif</span>
    </div>
    <div class="card-body">Explorateur API « Try It! » intégré sur chaque endpoint. Prend en charge la pré-authentification avec des clés API propres à chaque utilisateur pour les intégrateurs via l'intégration JWT/OAuth de ReadMe.</div>
    <div class="card-detail">Enterprise : variables personnalisées renseignées depuis le contexte de connexion de l'utilisateur.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Changelog en tant que contenu</span>
      <span class="badge badge-yes">Natif</span>
    </div>
    <div class="card-body">Section Changelog de premier ordre avec gestion des versions et abonnement RSS. Possibilité de lier des entrées de changelog depuis les pages de référence API. Rédigez en markdown ou via l'API.</div>
    <div class="card-detail">La liaison automatique depuis la référence nécessite des liens croisés manuels — pas entièrement automatique.</div>
  </div>
</div>

<!-- Search -->
<div class="section-label">Recherche &amp; découvrabilité</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Recherche améliorée</span>
      <span class="badge badge-partial">Partiel</span>
    </div>
    <div class="card-body">ReadMe dispose d'une recherche plein texte intégrée. La recherche sémantique et le suivi des requêtes sans résultat ne sont pas natifs — le suivi des lacunes est disponible via le rapport d'analyse des requêtes de recherche, mais n'est pas signalé automatiquement.</div>
    <div class="card-detail">Les analyses de recherche indiquent ce que les utilisateurs ont cherché sans obtenir de résultats. Le classement sémantique n'est pas configurable actuellement.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Architecture de l'information découvrable</span>
      <span class="badge badge-yes">Natif</span>
    </div>
    <div class="card-body">Navigation hiérarchique avec catégories, sous-catégories et ordre personnalisé. Prend en charge plusieurs versions de documentation et une navigation adaptée au public. L'architecture de l'information est gérée dans le tableau de bord ou via l'API Guides.</div>
    <div class="card-detail">La navigation personnalisée par type d'intégration nécessite du JS personnalisé ou des blocs de contenu dynamiques.</div>
  </div>
</div>

<!-- AI -->
<div class="section-label">IA &amp; outillage moderne</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Natif IA / lisible par les LLM</span>
      <span class="badge badge-yes">Natif</span>
    </div>
    <div class="card-body">Stack IA native complète : LLMs.txt généré automatiquement en un seul clic (tous les plans, zéro maintenance). Deux serveurs MCP natifs — l'un pour les auteurs de documentation afin de gérer les docs via l'IA, l'autre pour les utilisateurs d'API afin de donner à leurs outils IA un accès en direct à votre spec et vos docs. Les pages ReadMe génèrent du HTML propre et exposent un sitemap public — indexable par les LLM. Le llms.txt natif est pris en charge et génère automatiquement un fichier de configuration à la racine de votre site de documentation basé sur votre structure de documentation existante.</div>
    <div class="card-detail">LLMs.txt disponible sur tous les plans. Les serveurs MCP sont intégrés, pas une intégration personnalisée.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Personnalisation</span>
      <span class="badge badge-partial">Partiel</span>
    </div>
    <div class="card-body">ReadMe prend en charge les variables utilisateur (ex. : clés API pré-remplies, nom de l'entreprise) via JWT SSO. Le branchement de contenu basé sur le schéma/pays/méthode d'intégration n'est pas natif — nécessite une logique personnalisée ou des versions de documentation séparées.</div>
    <div class="card-detail">L'injection de variables Enterprise est efficace pour le contexte d'authentification ; les blocs de contenu conditionnel sont limités.</div>
  </div>
</div>

<!-- Performance -->
<div class="section-label">Performance &amp; gouvernance</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">SSR / chargement rapide des pages</span>
      <span class="badge badge-partial">Partiel</span>
    </div>
    <div class="card-body">La plateforme hébergée de ReadMe utilise le SSR. Le TTFB et les Core Web Vitals sont généralement bons avec le thème par défaut, mais vous ne contrôlez pas directement l'infrastructure — les SLA de TTFB inférieurs à 100 ms ne sont pas garantis ni disponibles contractuellement.</div>
    <div class="card-detail">Le domaine personnalisé + CDN est pris en charge. L'optimisation des performances est limitée par rapport à une solution auto-hébergée.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Gouvernance du contenu</span>
      <span class="badge badge-partial">Partiel</span>
    </div>
    <div class="card-body">La synchronisation GitHub bidirectionnelle permet aux équipes d'utiliser les PR pour la révision des docs. La vérification des liens brisés et le linting ne sont pas natifs — vous devrez ajouter une étape CI contre le site en production ou le contenu exporté.</div>
    <div class="card-detail">GitHub Sync est disponible sur les plans Business/Enterprise. Les outils de contrôle qualité constituent une lacune.</div>
  </div>
</div>

<!-- Analytics -->
<div class="section-label">Analyses &amp; retours</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Boucles de retour développeur</span>
      <span class="badge badge-yes">Natif</span>
    </div>
    <div class="card-body">Les évaluations par page (pouce levé/baissé) sont intégrées. Le CSAT développeur est affiché dans le tableau de bord Métriques. Les commentaires peuvent être activés par page pour un retour direct.</div>
    <div class="card-detail">Les évaluations sont agrégées dans le tableau de bord analytique — filtrables par page, version et plage de dates.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Analyses de contenu</span>
      <span class="badge badge-yes">Natif</span>
    </div>
    <div class="card-body">ReadMe Metrics suit les pages vues, le temps passé sur la page, les requêtes de recherche et les taux de sortie. Les analyses des appels API sont également disponibles lors de l'utilisation de la journalisation API de ReadMe.</div>
    <div class="card-detail">L'analyse complète des lacunes de recherche est disponible. L'envoi vers des outils externes nécessite l'API Metrics ou un webhook.</div>
  </div>
</div>

<!-- Workflow -->
<div class="section-label">Flux de travail &amp; édition</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Facile à mettre à jour</span>
      <span class="badge badge-yes">Natif</span>
    </div>
    <div class="card-body">Éditeur WYSIWYG pour les non-ingénieurs, markdown/MDX pour les ingénieurs, plus GitHub Sync pour les équipes orientées code. Faible barrière à l'entrée pour les deux publics — aucune étape de build requise pour les modifications de contenu uniquement.</div>
    <div class="card-detail">Les ingénieurs peuvent également utiliser l'API Guides ou le CLI pour les mises à jour en masse et l'automatisation.</div>
  </div>
</div>

<footer>Généré à partir de l'évaluation de la plateforme ReadMe · readme_criteria_breakdown</footer>

</body>
</html>
`}</HTMLBlock>

Voici comment appréhender l'ensemble du tableau :

Là où ReadMe est une solution bien adaptée :

* le cœur de ce que vous demandez est exactement ce pour quoi ReadMe a été conçu. La référence synchronisée avec OpenAPI, les exemples de code multi-langages, le bac à sable Try It, le changelog, les évaluations par page et les analyses de contenu sont tous des fonctionnalités de premier ordre. La combinaison WYSIWYG + GitHub Sync répond directement à l'exigence « facile à mettre à jour pour les ingénieurs et les non-ingénieurs ».
* IA native / indexation MCP — ReadMe couvre les deux aspects de l'histoire MCP :
  Le serveur MCP côté auteur permet à votre équipe d'interroger, lire et mettre à jour la documentation via des outils IA — utile pour les flux de travail de contenu, les modifications en masse et la rédaction assistée par IA directement sur vos docs en production.
  Le serveur MCP côté utilisateur est le plus stratégiquement significatif pour cette évaluation — il donne aux outils IA de vos utilisateurs d'API (Cursor, Claude, Windsurf, etc.) un accès en direct à votre spec et vos docs comme contexte pendant qu'ils codent. C'est exactement ce que le critère « indexé par MCP » dans les exigences initiales demandait.
  Cela rend en réalité l'histoire IA native de ReadMe plus solide que je ne l'avais initialement évaluée — et plus solide que ce que proposent de nombreux concurrents. La seule nuance restante sur cette carte serait de savoir si llms.txt est généré nativement, mais la partie MCP est clairement couverte. Cela vaut la peine de mettre à jour l'artefact si vous le partagez.

Là où c'est partiel, et quoi faire à ce sujet :

* Recherche sémantique — la recherche actuelle est basée sur les mots-clés. Le suivi des requêtes sans résultat est disponible dans les analyses (vous pouvez voir ce qui n'a retourné aucun résultat) mais n'est pas automatiquement mis en avant comme une file d'attente pour le travail de contenu. Si la recherche sémantique est un critère impératif, c'est la lacune la plus importante par rapport à des alternatives comme Mintlify ou une intégration Algolia personnalisée.
* Garantie de TTFB inférieur à 100 ms — les performances SSR de ReadMe sont généralement solides, mais vous êtes sur leur infrastructure et ne pouvez pas imposer contractuellement un SLA de TTFB. Si c'est une exigence impérative, les solutions auto-hébergées (Mintlify, Docusaurus + Vercel) vous donnent plus de contrôle.
* Gouvernance du contenu / contrôles qualité — GitHub Sync gère bien la partie révision par PR, mais la vérification des liens brisés et le linting doivent être ajoutés en CI (ex. : broken-link-checker contre votre URL de staging à chaque PR). ReadMe n'impose pas cela nativement.
* Personnalisation par schéma/pays/méthode d'intégration — l'injection de variables utilisateur (clés API, nom de l'entreprise) est excellente. Le vrai branchement conditionnel du contenu par type d'intégration n'est pas natif et nécessiterait soit des arborescences de documentation versionnées séparées, soit des blocs JS personnalisés.
* Sur la question build vs buy vs open source — ReadMe se situe clairement dans la colonne « buy » avec une solide proposition de plateforme gérée. Si des SLA de performance stricts, des fonctionnalités MCP/IA natives poussées ou des conditions de contenu avancées sont des exigences impératives, il vaut la peine de comparer Mintlify côte à côte (histoire IA native plus forte, plus de flexibilité de configuration) et Docusaurus + Vercel (contrôle total, plus d'effort d'ingénierie). Je suis disponible pour faire une comparaison directe avec l'un ou l'autre si cela est utile.