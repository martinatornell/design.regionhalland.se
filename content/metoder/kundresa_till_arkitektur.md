---
date: 2019-04-10T18:07:15Z
title: "Från kundresa till arkitektur"
description: Hur vi arbetar med att översätta en kundresa till arkitektur
weight: 1000
---
## Översikt

Utifrån Kundresan tar vi fram en Värdekedja, en Process och en första arkitekturskiss. Dessa visar Kundresan ur tre olika perspektiv. 

Värdekedjan fokuserar endast på VAD som sker och ger ett strategiskt verktyg för att kunna beskriva vilka Förmågor vi behöver sätta på plats eller förbättra. 

Processen fokuserar, utöver VAD, också på HUR, VEM och i VILKEN ORDNING saker och ting skall ske. Processen ger ett taktiskt verktyg för att kunna fungera för hur Kundresan skall kunna implementeras.

Arkitekturskissen visar utöver det som beskrivs i processen också vilka tjänster som kommer att användas i de olika processerna. Detta ger en start för att vi skall skunna arbeta vidare med att skapa och vidareutveckla de tjänster som behövs för att kunna realisera kundresan.

Dessa tre vyer av Kundresan ger oss grundläggande förutsättningar för att kunna arbeta vidare med för att kunna realisera denna.

Den kundresa som vi utgått i från i detta exempel är Anställningsprocessen, se nedan.
{{<figure src="https://www.figma.com/proto/N4WX0YHbF5TLa7f5CD389sOV/Anst%C3%A4llningsprocessen?node-id=4%3A46&viewport=211%2C440%2C0.105253&scaling=min-zoom&redirected=1" link="https://www.figma.com/proto/N4WX0YHbF5TLa7f5CD389sOV/Anst%C3%A4llningsprocessen?node-id=4%3A46&viewport=211%2C440%2C0.105253&scaling=min-zoom&redirected=1" title="Från kundresa till arkitektur - Värdekedja exempel">}}


## Steg 1 - Skapa en Värdekedja

1. Utgå från Kundresan
2. Skapa en Värdekedja utifrån Kundresan
3. Mappa Förmågor utifrån Kundresan till Värdekedjan. Finns inga lämpliga förmågor behövs dessa skapas. Syftet med detta steg är att skapa en strategisk översikt.  
4. Om nya Förmågor skapas skall dessa beskrivas om läggas in i Förmågeöversikten.
5. När Värdekedjan är klar har vi en övergripande bild över vilka Förmågor vi har på området som Värdekedjan beskriver samt vilka Förmågor vi behöver sätta på plats eller förbättra. Detta ger oss ett verktyg för att kunna driva dess förändringar framåt.

Den färdiga Värekedjan kan då se ut som denna:
{{<figure src="/images/metoder/fkta1.png" link="/images/metoder/fkta1.png" title="Från kundresa till arkitektur - Värdekedja exempel">}}

## Steg 2 - Skapa en Process

1. Utgå från Kundresan
2. Skapa en huvudprocess i BPMN utifrån Kundresan.
3. Skapa delprocesser för de aktviteter som behövs förtydligas.
4. När processkartorna är klara har vi ett taktiskt verktyg som möjliggör för oss att enklare kunna kommunicera kring hur kundresan skall kunna realiseras i våra verksamheter.

Den färdiga huvudprocessen kan se som som följande:
{{<figure src="/images/metoder/fkta2.png" link="/images/metoder/fkta2.png" title="Från kundresa till arkitektur - Huvudprocess exempel">}}

och en av delprocesserna skulle kunna se ut som nedan:
{{<figure src="/images/metoder/fkta3.png" link="/images/metoder/fkta3.png" title="Från kundresa till arkitektur - Delprocess exempel">}}

## Steg 3 - Skapa en Arkitekturskiss

1. Utgå från Kundresan
2. Skapa ett Archimate diagram utifrån delprocesserna som skapades i steg 2. Enligt vår metamodell använder vi Applikationstjänster för att stötta våra Processer, så det är dessa två element vi fokuserar på att få in i skissen i detta skede.
3. Notera att flödet i Arkitekturskissken inte behöver vara lika exakt som i Processkartan. Det viktiga är att få med aktiviteterna och en ungefärlig ordning här. Likaså behöver vi här inte få in roller & aktörer då de finns i Processkartan.

Den första arkitekturskissen kan då se ut som nedan:
{{<figure src="/images/metoder/fkta4.png" link="/images/metoder/fkta4.png" title="Från kundresa till arkitektur - Arkitekturskiss exempel">}}







