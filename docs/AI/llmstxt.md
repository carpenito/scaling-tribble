---
title: LLMs.txt
deprecated: false
hidden: false
metadata:
  robots: index
---
## Overzicht

Met onze nieuwe [LLMs.txt](https://llmstxt.org/)-functie kun je AI-modellen leren hoe ze je API-documentatie correct moeten begrijpen en weergeven. Hiermee geef je AI-assistenten zoals ChatGPT of Claude de context die ze nodig hebben om nauwkeurig vragen over je API te beantwoorden zonder te hallucineren (dingen te verzinnen). Het instellen duurt letterlijk seconden – zet gewoon een schakelaar om en wij genereren het configuratiebestand automatisch. Op de achtergrond maken we metadata aan die AI-systemen helpt de structuur, terminologie en meest actuele informatie van je documentatie te begrijpen. LLMs.txt is beschikbaar op alle abonnementen.

Het resultaat? Ontwikkelaars krijgen nauwkeurige antwoorden over je API, zelfs wanneer ze AI-tools raadplegen in plaats van je documentatie rechtstreeks te lezen. Het is documentatie die overal werkt waar jouw ontwikkelaars werken!

## Voordelen

* **Nauwkeurigheid**: Helpt AI-modellen je documentatie correct weer te geven
* **Consistentie**: Zorgt voor de juiste terminologie en versie-informatie
* **Relevantie**: Stuurt AI-modellen naar de meest actuele informatie
* **Nul onderhoud**: Automatisch gegenereerd op basis van je bestaande documentatie

## Hoe het werkt

LLMs.txt werkt als een configuratiebestand in de root van je documentatiesite dat AI-taalmodellen kunnen raadplegen en interpreteren. Dit bestand fungeert als een technische handleiding die AI-systemen instrueert hoe ze je content correct moeten lezen en raadplegen.

Wanneer ingeschakeld, genereert ReadMe dit configuratiebestand automatisch op basis van je bestaande documentatiestructuur. Het bestand bevat metadata over:

* De organisatie van je documentatie (handleidingen, API-referentie, recepten, enz.)
* Versie-informatie om ervoor te zorgen dat AI-modellen de meest actuele documentatie raadplegen
* Belangrijke terminologie die specifiek is voor je API
* Hiërarchische structuur van je content

AI-modellen die LLMs.txt ondersteunen, controleren op dit bestand voordat ze antwoorden genereren over je API. Wanneer ze het vinden, gebruiken ze de instructies om nauwkeurigere informatie te geven, waardoor de kans op verouderde verwijzingen of onjuiste terminologie wordt verkleind.

Als je bijvoorbeeld onlangs endpoints hebt hernoemd of parametersvereisten hebt gewijzigd, helpt LLMs.txt ervoor te zorgen dat AI-assistenten geen verouderde informatie verstrekken aan ontwikkelaars die je API gebruiken.

## Aan de slag

Schakel LLMs.txt in met slechts een paar klikken om AI-modellen te helpen je API-documentatie nauwkeurig weer te geven.

#### ReadMe Refactored

Voor projecten die de ReadMe Refactored-interface gebruiken:

1. Navigeer naar je projecthub.
2. Klik op **AI-instellingen (✨ Sparkle-pictogram)** in het menu rechtsboven.
3. Zet **LLMs.txt inschakelen** op AAN.
4. Klik op **Opslaan**.

#### ReadMe Legacy

1. Ga naar **Configuratie** > **AI-instellingen**.
2. Zet **LLMs.txt inschakelen** op AAN.
3. Klik op **Opslaan**.