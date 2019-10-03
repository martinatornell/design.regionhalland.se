## Inledning 
Detta dokument är en bilaga till utvecklingshandboken och syftar till att beskriva hur vi versionshanterar systemutveckling. Vissa delar är generella och andra mer specifika och beroende av teknikstack. 


## Versionshantering 
Vi versionshanterar våra webbapplikationer enligt standarden Semantic Versioning, https://semver.org/  

För versioner som sätts i produktion använder vi de tre textrutorna längst till vänster, major, minor och build (patch). Alla tre versionsdelarna saknar individuell övre gräns och stegs upp oberoende av varandra, vilket innebär att ett versionsnummer skulle kunna vara 1.25.104. Versionsnummer stegas enligt följande exempel: 

- 0.9.9 => 0.9.10 (tidig version för system som aldrig produktionssatts) 
- 1.0.0 => 1.0.1 eller 1.1.0 eller 2.0.0 beroende på typ av förändring. 
- 1.1.0 => 1.1.1 eller 1.2.0 eller 2.0.0 beroende på typ av förändring. 
- 1.1.1 => 1.1.2 eller 1.2.0 eller 2.0.0 beroende på typ av förändring. 

För ”alfa- och betaversioner” använder vi en tidsstämpel till höger om samtliga versionssiffror, separerad med bindestreck. En ”alfa-/betaversion” enligt ovanstående exempel blir alltså ”1.25.104-201812101013” innan den slutgiltiga versionen 1.25.104 lanseras. 

Observera att versionen 1.0.0 är större än 1.0.0-201905201252 eftersom den senare är en förhandsversion till den förra. 

Motsvarande värden för versionsnumrering ska användas för applikationens databas. Applikationen och dess tillhörande databas behöver dock inte ha exakt samma versionsnumrering utan har sina egna uppskrivningar av versionsnummer. Undantaget är vid ändring av major och minor, som innebär ”breaking change” och därmed ökas major- och/eller minorversionen. En kontroll görs automatiskt i alla våra webbapplikationer där siffrorna för major och minor i applikationen jämförs med major och minor i databasen och dessa siffror måste stämma överens. Skillnader i vad som är en ”breaking change”: 

- En breaking change är då en datatyp i en tabell förändras alternativt då en kolumn eller databasobjekt tas bort.  
- En breaking change är INTE då nya kolumner eller databasobjekt läggs till. 


## Exempel 
Om vi har en version 1.0.0 och bara lägger till saker, schemamässigt i databasen, då stegas versionen inom enbart i minor. 

Så fort vi tar bort något som påverkar schema i databasen, eller ändrar datatyp för en kolumn så stegas ovanstående exempel i major. 


## Visual Studio
Vi använder egenskapsparametrarna i respektive projekt för att ange versionssiffrorna. I huvudsak handlar det om ”Assembly version” men för att få till tidsstämpel så har vi valt att även utnyttja fältet ”Trademark”. Översättningen mellan standarden för Semantic Versioning och Visual Studio blir då:

{{<figure src="/images/metoder/versionshantering1.png" link="/images/metoder/versionshantering1.png" title="Versionshantering i Visual Studio">}}

Vi använder både Assembly och File Version. Assembly Version är den som kommer att visas i programmet och File Version visas på klassbibliotekens kompilerade filer. Assembly och File Version ska alltid vara samma, både i varje projekt och mellan projekten i en Solution.

I samband med att applikationen släpps till test och/eller produktion så ska den checkas in och en label ska sättas på incheckningen. Detta görs via File | Source Control | Advanced | Apply label. En sådan label ska vara ”Version 1.25.104”.
