---
title: Branches
deprecated: false
hidden: false
metadata:
  robots: index
---
Met branches kun je gewoon blijven bewerken zoals je altijd hebt gedaan! Branches zijn een optionele workflow die flexibiliteit biedt in je schrijfproces. Schrijvers gebruiken branches om:

* Wijzigingen aan te brengen en deze te bekijken in een preview-omgeving voordat ze live gaan.
* Wijzigingen ter beoordeling naar teamleden te sturen.
* Wijzigingen door te voeren op meerdere pagina's.

<PlanTable currentPlan="Business" />

<Callout icon="💼" theme="default">
  **Opmerking:** Aanvullende beoordelingsopties zijn alleen beschikbaar op Enterprise-abonnementen.
</Callout>

***

## Een branch aanmaken

Er zijn drie manieren om een branch aan te maken:

1. Navigeer naar het menu voor versies en branches. Daar kun je nieuwe branches aanmaken vanuit een versie.
2. Terwijl je een versie bewerkt, kun je in plaats van opslaan kiezen voor opslaan naar een nieuwe branch.
3. Als je [synchroniseert met GitHub](https://docs.readme.com/main/docs/bi-directional-sync), worden branches die in GitHub zijn aangemaakt weergegeven in ReadMe. En branches die in de ReadMe-interface zijn aangemaakt, verschijnen automatisch in GitHub!

Zodra je branch is aangemaakt, kun je beginnen met schrijven! Wijzigingen zijn pas live nadat je je branch hebt samengevoegd met een publieke versie.

<Image align="center" border={false} src="https://files.readme.io/65abcb59c51a4be0b668815cf0046ee818e93228057a6bff5ddbe4d3a4b9b97e-Getting_Started_with_Owlberts_Journeys-20250512-1502362x.webp" />

Er is geen tijdslimiet of vervaldatum voor branches. Elke beheerder in je team kan elke branch bekijken, bewerken, samenvoegen en verwijderen.

***

## Wijzigingen beoordelen

<Image align="center" alt="Review tab showing the diff between two pages line-by-line" border={false} src="https://files.readme.io/95ab92ffd9eec49ad16b279f1e4a66de1f54cc95eb121f43c381258fb1d7915e-Review-20251104-1847122x.webp" />

Tijdens het bewerken van een branch kun je het tabblad Beoordeling openen om de wijzigingen in je branch te vergelijken.

<Callout icon="☝️" theme="default">
  Bij het herordenen van bestanden worden ze weergegeven als wijzigingen in het `_order`-bestand in je documentatie. Elk item in het `_order`-bestand vertegenwoordigt een pagina in je documentatie en komt overeen met de slug van elke pagina.
</Callout>

Klanten met de beoordelingsfunctie kunnen branches ook markeren als gereed voor beoordeling. Dit voegt een badge toe in het menu voor versies en branches en start de [AI Linter](https://docs.readme.com/main/docs/linter). Gebruikers kunnen de samenvoegvereisten omzeilen door het vakje "Samenvoegen zonder vereisten" aan te vinken om de knop **Samenvoegen** in te schakelen.

***

## Wijzigingen samenvoegen

Zodra je klaar bent om de wijzigingen live te zetten, kun je samenvoegen vanuit het branchmenu:

<Image align="center" border={false} width="300px" src="https://files.readme.io/0c4c2909e376be33b974e008b8b9b9f14860b13c3eff12b5be8a377395fd68e4-Getting_Started_with_Owlberts_Journeys-20250528-1418472x.png" />

Bij het samenvoegen wordt een controle uitgevoerd om te zorgen dat er geen samenvoegconflicten zijn. Als er conflicten zijn die opgelost moeten worden, raden we aan om [de conflicten via GitHub op te lossen](https://docs.readme.com/main/docs/branches#/handling-conflicts). Als je project niet synchroniseert met GitHub, kun je het conflict negeren en de wijzigingen geforceerd samenvoegen—met voorkeur voor de wijzigingen in de branch.

Na het samenvoegen worden je branches niet verwijderd, zodat je de wijzigingen kunt bekijken voordat je ze verwijdert.

<Callout icon="💁‍♂️" theme="default">
  GitHub-gebruikers kunnen een branch ook samenvoegen met een versie—ook via Pull Requests.
</Callout>

### Samenvoegen beperken tot beheerders

Enterprise-klanten kunnen de samenvoegrechten per project beperken tot [Alleen beheerders of Beheerders & Editors](https://docs.readme.com/ent/docs/user-roles/). De instellingen zijn te vinden op de projectpagina van het Enterprise-dashboard. Open **Instellingen** > **Enterprise-naam** (onderaan) > **Projecten**

***

## Synchroniseren met GitHub

Je hoeft niet te synchroniseren met GitHub om branches te gebruiken.

Bij het aanmaken van branches vanuit GitHub moet de naam worden opgemaakt om de versie op te nemen: `{version}_{branch}`. Voorbeelden:

```
v2.0_rewrite-getting-started
v2.0_add-new-feature
v2.0_fix-typo
```

### Toegang & machtigingen

ReadMe- en GitHub-machtigingen zijn onafhankelijk van elkaar. Gebruikers met toegang tot de branches van je GitHub-project hebben toegang tot eventuele inhoudswijzigingen. Om inhoudswijzigingen die via GitHub in branches zijn aangebracht te kunnen bekijken, hebben gebruikers een ReadMe-account nodig met toegang tot de branch van je project.

### Conflicten afhandelen

Bij het samenvoegen vanuit GitHub kan de gebruiker conflicten oplossen via de GitHub-editor of de samenvoegingstool naar keuze, lokaal, voordat ze worden gepusht.

Bij het samenvoegen vanuit ReadMe komen de wijzigingen die je ziet in de preview altijd overeen met wat er live gaat bij het samenvoegen. Conflicterende wijzigingen vanuit GitHub worden niet weergegeven.

***

## Veelgestelde vragen

<Accordion title="Wie kan een branch bekijken?" icon="fa-help-circle">
  Alleen teamleden met toegang tot je project kunnen je branches bekijken—inclusief de rollen Editor en Viewer.
</Accordion>