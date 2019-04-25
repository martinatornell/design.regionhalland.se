---
title: "Sparx"
linktitle: "Sparx"
date: 2019-02-11T09:17:43+01:00
draft: false
description: "Vi använder Sparx som verktyg för att visualisera vår IT-arkitektur."
weight: 1000
---
## Tips & tricks
### Klippa & klistra
En sak att tänka på med Sparx är när man kopierar in komponenter från ett diagram till ett annat. Om man använder CTRL-V för att klistra in en komponent (t.ex. en text ruta) så kopierar man in samma komponent. Detta medför att om man ändrar texten på ett ställe så ändras den också på det andra stället.

För att undvika detta så behöver man (om man vill att det skall vara olika objekt) använda CTRL-SHIFT-V (eller högerklicka och använd "Paste" -> "Element(s) as New)") när man klistrar in en komponent. Detta blir då ett nytt objekt som är oberoende av det gamla.

### Slå av Strict Connector Syntax
Sparx kan vara lite kinkig när det gäller att tillåta vissa relationer mellan komponenter. T.ex. så kan man i standard inställningen inte skapa en "Realization" relation mellan en "Application Component" och en "Application Service" för ArchiMate diagram.

För att möjliggöra detta gör på följande sätt:

  1. Gå in under "Start"->"Preferences"->"Links" 
  2. Klicka ur "Strict Connector Syntax" 
  3. Nu bör du kunna dra en "Realization" direkt från en "Application Component" till en "Application Service".
