---
date: 2017-04-01T12:21:15Z
title: "Arkitektur"
description: Hur vi arbetar med arkitektur inom Region Halland
weight: 1000
---
## Introduktion

## Principer
Våra grundläggande arkitekturprinciper

### Hög Sammanhållning (Cohesion) och Låg Koppling (Coupling)
Inom mjukvarudesign pratar man ofta om begreppen Cohesion (sammanhållning) och Coupling (koppling). Där sammanhållning är ett mått på graden av komponentens delar som funktionellt relaterade. Det kan sägas vara i vilken grad alla element som är inriktade på att utföra en enskild uppgift finns i komponenten. Koppling är sin tur måttet på graden av ömsesidigt beroende mellan olika komponenter. Inom programvaruutveckling vill man uppnå en hög sammanhållning och en låg koppling. 

Detta beskriver också mycket väl hur vi ser på hela vårt digitala landskap. För de olika komponenterna vi har i form av system, appar, applikationer, etc. vill vi ha en hög så hör sammanhållning som möjligt och en så låg koppling som möjligt.

För att länka samman olika komponenter vill vi att detta sker genom datakoppling. Detta innebär att komponenterna kommunicerar med varandra genom att endast överföra data mellan varandra. Genom att endast överföra data mellan varandra uppnår vi en låg koppling mellan komponenterna.

Genom att försöka hålla samman all hantering kring en viss informationsmängd i en enskild komponent säkerställer vi att vi uppnår så hög sammanhållning som möjligt. Exempel på detta kan vara att ekonomidata hanteras i ett ekonomisystem, journaldata i ett journalsystem, osv. Motsatsen inträffar när en viss informationsmängd hanteras i ett flertal olika system. 


### API-first
Region Hallands grundfilosofi är API-first, vilket innebär att vi alltid tänker oss att bygga lösningar baserade på API-er snarare än klassiska client-server-lösningar. Vi förespråkar pragmatisk API design, vilket innebär att vi utgår ifrån vad det är vi försöker uppnå med vårt API och se det ur en utvecklares perspektiv och att denne ska bli så framgångsrik som möjligt i användandet av API-et. Enkelhet är den viktigaste principen i skapande av API-er. 


## Visualisering av Arkitektur

### Översikt
För att visualisera vår arkitektur använder vi [ArchiMate](https://design.regionhalland.se/verktyg/archimate/) som notationsspråk. I vissa fall räcker inte ArchiMate till för att detaljera vissa vyer, t.ex. för processer och informationsmodeller. I dessa fall använder vi BPMN (för processer) och UML (for informationsmodeller). Det verktyg som vi använder inom Region Halland för att dokumentera arkitektur är [Sparx](https://design.regionhalland.se/verktyg/sparx/).

För att visualisera vår arkitektur använder vi vyer (diagram) som är uppbyggda av en eller flera komponenter. Vi använder ett antal standardiserade vyer för att få en samanhållen bild av vår arkitektur. De vyer vi använder oss av är följande:

**Strategiska vyer**

- *Verksamhetsförmågor* - Visar de Verksamhetsförmågor som Region Halland kan leverera. En Verksamhetsfömåga beskriver VAD vi som organisation kan utföra, men inte var, hur eller av vem den utförs.

**Verksamhetsvyer**

  - *Organisationsvyer* - Visar vem som innehar en viss roll i vår IT-styrning, Systemförvaltning & Tjänsteleverans.
  - *Värdekedjor* - Beskriver hur Region Hallands kundresor är uppbyggda med hjälp av Verksamhetsförmågor.
  - *Processkartor* - Processkartorna är ett taktiskt verktyg som möjliggör för oss att enklare kunna kommunicera kring hur kundresan skall kunna realiseras i våra verksamheter.
  - *Grunduppdrag* - Visar vad grunduppdraget är för våra olika grupperingar inom vår IT-organisation. Bygger på modellen Business Model Canvas (BMC)

**Tjänstevyer**

- *Tjänsteportföljer* - Visar vilka tjänster Region Halland tillhandahåller på olika nivåer.
- *Tjänsteuppbyggnadsbeskrivningar* - Visar hur våra olika tjänster är uppbyggda.

**Applikationsvyer**

- *Applikationslandskap* - Beskriver vilka applikation respektive systemförvaltningsobjekt ansvarar för och vilka applikationer vi har i vår applikationsportfölj.
- *Integrationskartor* - Visar dels övergripande Integrationskartor, dels Integrationsbeskrivningar mellan olika system.
- *Informationsmodeller* - Visar vilka Informationsmängder vi har samt hur dessa hänger ihop.

**Infrastruktursvyer**

- TBD

### Visualisering av Strategiska vyer
I tabellen nedan visar vi vilka ArchiMate symboler vi använder för att illustrera olika typer av komponenter för de olika vyer vi använder oss av.

| Komponent          | ArchiMate Symbol | Användning i Vyer |
| ------------------ | ---------------- | -------------- |
| Verksamhetsförmåga |![Verksamhetsförmåga](/images/metoder/icon_verksamhetsformaga.png "En Verksamhetsfömåga beskriver VAD vi som organisation kan utföra.") | Verksamhetsförmågor, Värdekedjor | 
| Aktör |![Person eller grupp](/images/metoder/icon_aktor.png "En Aktör, kan vara en enskild person eller en grupp.") | Organisationsvyer  | 
| Värdekedja |![Värdekedja](/images/metoder/icon_vardekedja.png "Ett steg i en Värdekedja.") | Värdekedjor  | 
| IT-stödtjänst |![IT-stödtjänst](/images/metoder/icon_itstodtjanst.png "En IT-stödtjänst.") | Grunduppdrag  | 




### Visualisering av Tjänstevyer

### Visualisering av Applikationsvyer

### Visualisering av Infrastruktursvyer
