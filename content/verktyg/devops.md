---
title: "I Azure DevOps följer vi våra utvecklingsprojekt från idé till produktion"
linktitle: "Azure DevOps"
date: 2019-02-11T09:17:43+01:00
draft: false
description: "I Azure DevOps följer vi statusen för våra digitala utvecklingsprojekt."
weight: 1000
---
För att kunna följa arbetet med våra olika utveklingsinitivativ, lagra källkod och säkerställa gemensamma arbetsätt använder vi verktyget Azure DevOps.

{{< button icon="external-link" url="https://regionhalland.visualstudio.com" label="Logga in i DevOps" >}}


## Begrepp i DevOps

### Backlog
Devops är bl.a. ett verktyg för att hantera backlogs. Enkelt kan en backlogg beskrivas som det kommande arbetet för ett team eller projekt. Det är i backloggen man samlar på sig och prioriterar arbetsuppgifter (workitems). På många sätt kan backloggen ses som en kravlista men med skillanden att backloggen är ett leveande dokument. Man jobbar med andra ord inte med låsta scope utan om prioriteter kontinuerligt beroende på hur arbetet går i [utvecklingssprintarna](/metoder/utvecklingssprint/).

#### Workitems
I DevOps finns ett antal olika workitems, de vi primärt använder beskrivs nedan. Ett workitem är helt enkelt en beskrivning över vad som behöver göras.

##### Epics
En Epic är den största abstraktionen vi har av en förmåga som vi vill realisera. När vi skriver en ny Epic bör vi sträva efter att låta namnet och omfånget återspegla det behov man ämnar lösa. Exempel på bra Epics kan vara "Ankomstregistrering", "Digitala videomöten", "Gemensam tidbok". En satsning kan bestå av ett flertal Epics och kan då länkas samman med en eller flera taggar och/eller länkning i DevOps. 

Vi använder Epics för att på helikopternivå kunna följa våra olika satsningar och se att vår gemensamma portfölj ligger i synk. Det är därför viktigt att varje Epic som hamnar i den gemensamma portföljen har passerat igenom processen [Från idé till produktion](/metoder/ide_till_produktion/) där vi analyserar behovet av förmågan i fråga. Vanligvis skrivs och hanteras Epics av Objektägaren tillsammans med Digitaliseringsenheten.

##### Features
En Epic består av flera features. En feature beskriver en funktion som krävs för att uppnå den övergripande förmågan som en tjänst ska leverera. Exempel på features kan vara "Formulär för att registrera ankomst på regionhalland.se" eller "Visa lediga tider för videomöten i Region Hallands App". En Feature består i sin tur av flera Stories. Vanligtvis skrivs både features och stories av Objektledaren. En bra måttstock är att en feature kan levereras inom 1-2 sprintar. Är featuren större än så bör den delas upp i flera features.

##### User Stories
Stories i DevOps är kanske den viktigaste pusselbiten då det är här man konkretiserar vad som de facto ska produceras. Formatet bör vara att man skriver [user stories](/metoder/userstories/) med tydliga [acceptanskriterier](/metoder/userstories/#acceptanskriterier). Även här bör man tänka på storleken och inte låta user storien bli större än någon/några veckors jobb.

##### Tasks
Om en produktägare, eller objektledare, är den som skriver Features och Stories så bör arbetet med Tasks hanteras av det utförande teamet. Tasks är teamets chans att i varje sprint själva tydliggöra och fördela arbetet kring hur man uppfyller acceptanskriterierna på en viss Story. Vi skriver alltid minst en Task per Story, detta ger oss också bl.a. möjligheten att följa upp tiden i burn-down charts då tiden läggs per Task. 

### Pipelines
En pipeline är den process man sätter upp i Azure DevOps för att lansera/bygga en tjänst. En typisk pipeline kan vara att man kompilerar all kod som driver tjänsten, kör ett antal tester för att kontrollera att allt fungerar och publicerar sedan tjänsten på en server så att användarna får en ny version.

### Area Paths
För att kunna skicka en workitem till ett team så anväder vi Area Paths. Vi har definerat en Area Path struktur som bygger på att ett team kan vara av någon av typerna App (ett produktteam), Org (ett organisationsteam, t.ex. ett Objekt) eller Projekt (ett projektteam). Under respektive kategori finns det sedan underkategorier. För att flytta en workitem från ett team till ett annat så byter man bara Area Path så dyker workitem upp i rätt teams backlog.

### Iteration Paths
Vi använder iteration paths för att definiera tidslängden på våra sprintar. VI har ett gemensamt iteration path bibliotek utifrån vilket varje team kan välja tidsrymden för sina sprintar. Vi försöker hålla oss till samma "tick" för alla team och för närvarande använder vi oss av månadssprintar och halvmånadssprintar. Månadssprintar benämns "Sprint 2019.02", "Sprint 2019.03", osv. Under dessa finns våra halvmånadssprintar där den första sprinten går från den 1:e till den 15:e varje månad och den andra sprinten går från den 16:e till den sista varje månad. 
