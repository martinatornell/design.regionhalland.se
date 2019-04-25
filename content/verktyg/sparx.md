---
title: "Sparx"
linktitle: "Sparx"
date: 2019-02-11T09:17:43+01:00
draft: false
description: "Vi använder Sparx som verktyg för att visualisera vår IT-arkitektur."
weight: 1000
---
## Tips & tricks
### Slå av Strict Connector Syntax
Sparx kan vara lite kinkig när det gäller att tillåta vissa relationer mellan komponenter. T.ex. så kan man i standard inställningen inte skapa en "Realization" relation mellan en "Application Component" och en "Application Service" för ArchiMate diagram.

För att möjliggöra detta gör på följande sätt:
1. Gå in under "Start"->"Preferences"->"Links" 
2. Klicka ur "Strict Connector Syntax" 
3. Nu bör du kunna dra en "Realization" direkt från en "Application Component" till en "Application Service".
