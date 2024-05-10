
# Introduction

noQ startade 2017 som en dålig smak i munnen när Ove som inhyrd konsult på Stockholms stad skulle utreda faktureringsrutiner för hemlösa. Han fick inte bara se hur faktureringen kunde förbättras men träffade framför allt många hemlösa, härbärgen och administratörer som alla led av det obefintliga samarbetet.

Vi tror att en IT-lösning för sovplatser kan förenkla för

  * Hemlösa att hitta en trygg sovplats för natten

  * Härbärgen att enkelt kunna administrera dessa sovplatser inklusive fakturering.

  * Administratörer på stadsdelsförvaltningarna att kunna hålla koll på hur och var hemlösa finns men även enkel fakturering.


# Tekniska komponenter

Då noQ har en hög omsättning av deltagare så har vi beslutat att använda en begränsad tech-stack. För front-end använder vi oss av [React](https://github.com/facebook/react) och för back-end använder vi oss av [Python](https://www.python.org/). Om en database behöver användas i någon av våra tjänster så använder vi [PostgreSQL](https://www.postgresql.org/).

Vi förutsätter att alla tjänster som byggs också innehåller stöd för att paketeras som en container bild och som är kompatibel med Kubernetes.

# Infrastruktur

Så fort en tjänst ska exponeras för en slutanvändare så behöver den först driftas inom den Microsoft Azure miljö som finns uppsatt för noQ. Vi använder oss av Microsoft datacenter 'Sweden Central' och alla tjänster hostas på [Azure Container Apps](https://azure.microsoft.com/en-us/products/container-apps) som är en fullt managerad Kubernetes miljö.

*All källkod för noQ hanteras via GitHub och organisationen noQ-sweden.**

# Säkerhet

När en tjänst ska exponeras för en slutanvändare så behöver följande ha dokumenterats och uppfyllas:

  * Hur eventuella känsligt data kommer hanteras och sparas över tid.
  * Tjänsten implementerar stöd av säkerhetsåtgärder som HTTPS, användarautentisering och auktorisering samt datakryptering.
  * All källkod som används granskas av GitHub Advanced Security processen innan den publiceras till en produktionsmiljö.

# GitHub

Vi använder oss av ett enkelt arbetsflöde när det kommer til GitHub. `GitHub Flow` finns väl dokumenterat [här](https://docs.github.com/en/get-started/using-github/github-flow). I huvudsak handlar det om:

  1. Skapa en `feature-branch` och ge den ett beskrivande namn som tydligt knyter den till den user-story som du arbetar med.
  2. Implementera och testa de ändringar som krävs för att uppfylla acceptanskriterierna.
  3. Skapa en `pull-request` där du beskriver gjorda ändringar, bjud in en kollega för att en kodgenomgång.
  4. Hantera ev. kommentarer från kodgenomgången.
  5. Avsluta din `pull-request` genom att göra en `squash-merge`.
  6. Radera din `feature-branch`.

Innan du stänger din user-story helt bör relevant dokumentation finns tillgänglig i den Wiki på GitHub som hör till repot som du arbetar med.

# Ytterligare resurser
[Onboardinglistan](https://sites.google.com/noq.nu/intranet/onboarding?authuser=4)

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
