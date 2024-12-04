---
Title: Laddtid
Description: Laddtidanalys.
Template: analysis-info
---

Prestandaanalys
=======================

Vi ska titta närmare på laddtiden för ett par olika webbsidor och analysera både prestanda och användbarhet. Ligger responstiden på en acceptabel nivå, eller finns det något som kan förbättras? Om ja, vad skulle kunna justeras?

<br>
Urval
-----------------------

Jag har valt att testa dessa tre webbplatser för att analysera laddtider och användbarhet, och jag försökte få med en blandning för att täcka olika typer av sidor:<br><br>

* **[The White House](https://www.whitehouse.gov/)**  
_Jag tog med denna sida eftersom den har extremt hög trafik och troligtvis är väldigt optimerad för snabb och stabil leverans. Det kändes som en bra referenspunkt att jämföra med._

* **[NeManager](https://nemanager.com/)**  
_Detta är ett sidoprojekt som jag själv har utvecklat. Det ska bli intressant att se hur det presterar eftersom jag inte hade prestanda eller användbarhet som fokus när jag byggde det._

* **[Stockholms universitet](https://www.su.se/)**  
_Jag valde även Stockholms universitets webbplats, eftersom det är en stor sida med mycket information och många användare. Jag ville se hur den hanterar prestanda med allt sitt innehåll._ 
<br><br>

Jag försökte välja sidor som gav en bra blandning – både stora, vältrafikerade sajter och ett eget projekt – för att få lite olika perspektiv på vad som funkar och vad som kan förbättras.



<br>
Metod
-----------------------

För att genomföra analysen använde jag **Google PageSpeed Insights (PSI)** för att mäta prestandan på de utvalda webbplatserna, både för desktop och mobil. Detta verktyg ger en detaljerad överblick av hur väl optimerade sidorna är, med betyg och rekommendationer för förbättringar.<br><br>

För att komplettera dessa data och få en mer direkt insyn i laddtiderna använde jag webbläsaren **Google Chrome** och dess inbyggda inspektör. Genom att navigera till fliken **Network** kunde jag mäta den totala laddtiden för varje webbplats, räkna antalet resurser som laddas in, och notera hur mycket utrymme dessa resurser tar upp. Detta gav en tydlig bild av sidornas faktiska prestanda ur användarens perspektiv.<br><br>

För att göra resultaten lättlästa har jag sammanställt en kalkyl där de bästa resultaten markeras med **grön text** och de sämsta med **röd text**. Denna visuella presentation gör det enkelt att identifiera vilka webbplatser som presterar bäst och vilka som har störst behov av förbättringar. Genom denna kombination av verktyg och analysmetoder får vi en både djup och praktisk förståelse för hur dessa sidor presterar i verkligheten.<br><br>

<iframe title="Analyskalkyl" style="width: 100%; height: 350px;" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRbuzaA57YH4NGW27FAYqrWFK95tIK0FSMdY3S40UeyreC80NXAIceHoE571x6Y5rlJy_SUpYmRp20K/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

<br>
Resultat
-----------------------

### The White House (The White House, 2024)
![Snapshot på the white house alt ><](https://www.student.bth.se/~kaha24/dbwebb-kurser/design/me/portfolio/image/whitehouse.png&width=500)<br>

#### Analys
Prestanda på desktop är mycket imponerande, särskilt på startsidan och administrationssidan, medan mobilversionen faller efter, med en märkbar skillnad i poäng och längre laddningstider. Besökssidan (Visit) presterar sämst, vilket beror på ett högt antal resurser (73) och stor resursstorlek (10.8 MB). <br><br>

##### Förbättringar:
* Optimera bilder och media för att minska resursstorleken.
* Implementera lazy loading för media och minimera JavaScript-bibliotek som påverkar mobilprestanda.
<br><br>

### NeManager (NeManager, 2024)
![Snapshot på nemanager alt ><](https://www.student.bth.se/~kaha24/dbwebb-kurser/design/me/portfolio/image/nemanager.png&width=500)<br>

#### Analys
Som ett mindre projekt presterar webbplatsen överraskande bra. Sidan har snabba laddningstider och en låg mängd resurser, vilket ger ett optimalt resultat på både desktop och mobil. Changelog-sidan kan dock förbättras för att få jämnare poäng mellan desktop och mobil.<br><br>

##### Förbättringar:
* Öka användningen av komprimerade resurser och reducera externa skript för att stärka mobilprestandan ytterligare.

<br>

### Stockholms Universitet (Stockholms Universitet, 2024)
![Snapshot på stockholms universitet alt ><](https://www.student.bth.se/~kaha24/dbwebb-kurser/design/me/portfolio/image/su.png&width=500)<br>

#### Analys
Den här webbplatsen visar klart lägre prestanda än de andra, med en startsideprestanda på endast 79 på desktop och 47 på mobil. Hög resursanvändning (121 resurser, 17.9 MB) och lång laddtid (1.63 s) påverkar resultaten kraftigt. <br><br>

##### Förbättringar:
* Kraftigt reducera resursstorleken genom att komprimera bilder och optimera skript.
* Implementera en strategi för att minska antalet HTTP-förfrågningar genom att slå ihop filer och förbättra cachning.

<br>

Sammanfattning
-----------------------

Efter analysen av dessa tre webbplatser får jag fram följande förbättringsåtgärder som återkommer: <br><br>

* **Bildoptimering** <br>
_Reducera bildstorlek med modern komprimeringsteknik som till exempel WebP._
* **Skriptoptimering**<br>
_Minimera och kombinera CSS och JavaScript för att minska HTTP-förfrågningar._
* **Caching**<br>
_Implementera starkare cachningsstrategier för att snabba upp återbesök. Nyttja tjänster som **[CloudFlare](https://cloudflare.com/)**._
* **Mobilanpassning**<br>
_Förbättra laddning och prestanda på mobila enheter, särskilt genom lazy loading._

<br>

Genom att tänka på dessa områden kan alla tre webbplatser förbättras i prestanda och användbarhet, både för desktop och mobil. Stockholms Universitet framstår som den webbplats som har störst behov av optimering, medan The White House och NeManager har mindre men lika viktiga områden att jobba med.

<br>

Slutord
-----------------------

### Rangordning
Efter att ha jämfört värdena för prestanda, laddningstid och resursanvändning rangordnas webbplatserna på följande sätt: <br><br>

1. **NeManager**
    * _Bäst balanserad prestanda mellan desktop och mobil._
    * _Låga laddningstider och få resurser på samtliga sidor._<br><br>

2. **The White House**
    * _Hög desktopprestanda, särskilt på startsidan, men mobilprestandan ligger generellt efter._
    * _Högt resursantal och större resursstorlekar drar ner Visit-sidans resultat._<br><br>

3. **Stockholms Universitet**
    * _Betydligt längre laddningstider och hög resursförbrukning gör att webbplatsen hamnar längst ner._

<br>

**NeManager** tar hem vinsten tack vare en konsekvent bra prestanda på alla sidor och en effektiv hantering av resurser. **The White House** visar hög klass på desktop men behöver jobba mer med mobilanpassning. **Stockholms Universitet** är den tydliga förloraren, främst på grund av hög resursbelastning och långsamma laddningstider.

<br>

_Trots att jag utsett mitt eget projekt till vinnare baserat på mätvärdena, inser jag att det finns förbättringsområden, särskilt kring skalbarhet och optimering för mobila enheter. Däremot visar siffrorna att NeManager lyckas hålla låg laddningstid och resursanvändning, vilket bidrar till den positiva placeringen._

<br>

### Laddtid
Jag anser att en snabb webbplats bör ha en laddningstid under **1 sekund** och en långsam webbplats över **2 sekunder**.<br>
Utifrån denna gräns klarar två av de tre webbplatserna testet på majoriteten av sina sidor:<br><br>

* **NeManager**<br>
_Alla sidor laddar under 1 sekund, vilket jag upplever som väldigt snabbt._

* **The White House**<br>
_Två av tre sidor ligger under 1 sekund, vilket gör att webbplatsen känns snabb, även om Visit-sidan nästan når gränsen för långsam laddning._

* **Stockholms Universitet**<br>
_Här faller start- och Om-sidan över 1-sekundsgränsen, med startsidan långt över 2 sekunder. Detta påverkar användarupplevelsen negativt och gör att webbplatsen känns trög jämfört med de andra._

<br>

**NeManager** och **The White House** är båda exempel på snabba webbplatser med god användarupplevelse. **Stockholms Universitet**, å andra sidan, behöver kraftig optimering för att upplevas som snabb och användarvänlig.

<br>

Referenser
-----------------------

- The White House. (2024). *WhiteHouse.gov prestandaanalys*. [online] Available at: <https://pagespeed.web.dev/analysis/https-www-whitehouse-gov/kzuo8b8bb0> [Accessed 2 Dec. 2024].

- NeManager. (2024). *NeManager.com prestandaanalys*. [online] Available at: <https://pagespeed.web.dev/analysis/https-nemanager-com/0xjjxphb5p> [Accessed 2 Dec. 2024].

- Stockholms Universitet. (2024). *SU.com prestandaanalys*. [online] Available at: <https://pagespeed.web.dev/analysis/https-su-se/ezgaojqqhe> [Accessed 2 Dec. 2024].

<br>
---
**Karl Håkansson**  
*Publicerad: 2 december 2024*