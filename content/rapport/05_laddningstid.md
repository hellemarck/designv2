---
---
Analys av laddningstid på tre olika webbplatser
=========================

<h4>1 Inledning och syfte</h4>

Syftet med denna rapport är att undersöka och analysera laddningstid på tre olika webbplatser. Värden som undersöks är antal förfrågningar, total storlek, laddningstid och betyg i Google Pagespeed Insights för både mobil och desktop.

Jag har valt att analysera följande hemsidor:<br>
1) <a href="https://uppsalastadsteater.se/">Uppsala stadsteater</a>  (fortsättningsvis kallad "US")<br>
2) <a href="https://kulturhusetstadsteatern.se/">Kulturhuset Stadsteatern</a> (fortsättningsvis kallad "KS")<br>
3) <a href="https://helsingborgsstadsteater.se/">Helsingborgs stadsteater</a> (fortsättningsvis kallad "HS")

<h4>3 Metod</h4>

Webbplatsernas samlade betyg är hämtat från Google Pagespeed Insights. Jag har använt webbläsaren Chrome och verktyget Devtools (Network) för att undersöka sidornas laddningstid, storlek (transferred) och förfrågningar.  Mätningar i Devtools är gjorda med inaktiverad cache, och resultaten är genomsnitt baserat på tre sidladdningar.

<h4>4 Resultat</h4>

Excelarket för resultatsammanställning finns <a href="https://docs.google.com/spreadsheets/d/1dbav8zYwYDCbNttf4UBXn27x5kb1B1ma21sb4dFPyUI/edit#gid=0"> här.</a>

<h5>4.1 Uppsala stadsteater</h5>
[FIGURE src="image/uppsala.png?w=800" caption="Startsida Uppsala stadsteater."]

<a href="https://uppsalastadsteater.se/">Länk till startsidan</a><br>
<a href="https://uppsalastadsteater.se/om-teatern/om-oss/var-teater/">Länk till "Vår teater"</a><br>
<a href="https://uppsalastadsteater.se/forestallningar/">Länk till "Föreställningar"</a>

I Pagespeed Insights fick startsidan 79 i score på mobile och 89 på desktop. Motsvarande scores för "Vår teater" var 78 respektive 94, och för "Föreställningar" 73 respektive 93.

Startsidan hade en laddningstid på 1,65 sekunder, för "Vår teater" och "Föreställningar" gällde 3,20 respektive 3,57 sekunder. Gällande förfrågningar gjordes för startsidan 39 stycken, för "Vår teater" 53 stycken och för "Föreställningar" 69 stycken. Sidornas storlek var 1,6, 2,5 respektive 5,3 MB.

<b>Förbättringar: </b>Bättre bildhantering för kortare laddningstid. Dolda bilder och bilder som inte syns direkt vid inläsning skulle kunna läsas in med lazy loading.

<h5>4.2 Kulturhuset Stadsteatern</h5>
[FIGURE src="image/stockholm.png?w=800" caption="Startsida Kulturhuset stadsteatern."]

<a href="https://kulturhusetstadsteatern.se/">Länk till startsidan</a><br>
<a href="https://kulturhusetstadsteatern.se/Om-Kulturhuset-Stadsteatern/">Länk till "Om oss"</a><br>
<a href="https://kulturhusetstadsteatern.se/Teater/">Länk till "Teater"</a>

KS's startsida fick i Pagespeed Insights 45 i score på mobile och 85 på desktop. "Om oss" fick 66 respektive 90, och "Teater" fick 54 respektive 89.

Sidornas laddningstid var 2,85 sekunder för startsidan, 1,87 sekunder för "Om oss" och 2,17 sekunder för "Teater". Antal förfrågningar på respektive sida var 66, 48 och 65 och sidornas storlek var 2,0, 1,1 och 4,6 MB.

<b>Förbättringar:</b> Det finns resurser som blockerar renderingen, detta skulle kunna förbättras.

<h5>4.3 Helsingborgs Stadsteater</h5>
[FIGURE src="image/helsingborg.png?w=800" caption="Startsida Helsingborgs stadsteater."]

<a href="https://helsingborgsstadsteater.se/">Länk till startsidan</a><br>
<a href="https://helsingborgsstadsteater.se/om-oss/">Länk till "Om oss"</a><br>
<a href="https://helsingborgsstadsteater.se/pa-scen/">Länk till "På scen"</a>

I Pagespeed Insights fick HS's startsida score 68 på mobile och 97 på desktop, "Om oss" fick 53 respektive 94 i score och "På scen" fick motsvarande 34 respektive 78.

Sidornas laddningstid var för startsidan 3,83 sekunder, för "Om oss" 4,72 sekunder och för "På scen" 8,36 sekunder. Antal förfrågningar var för respektive sida i nämnd ordning 69, 55 och 73. Storleken på sidorna var 1,9 MB, 728 KB och 1,8 MB.

<b>Förbättringar: </b>Sidorna har väldigt långa laddningstider, särskilt "På scen". Förbättringar i svarstider på serversidan skulle kunna motverka detta något.

<h4>5 Analys</h4>
Samtliga sidor fick bra score i Pagespeed Insights på desktops; fem av nio sidor var över 90 i score och övriga inte långt efter. På mobile låg US i topp med scores på 70-80, medan KS och HS halkade efter med scores runt 40, 50 och 60-tal. Sämst ranking fick HS's sida "På scen" på 34. Sett till både mobile och desktop fick US bäst resultat.

Samtliga sidor hade väldigt lång laddningstid och det är också här förbättringsfokus måste ligga. De är tunga sidor med mycket bilder och därför behöver prioritering i inläsning tillämpas och bildhantering förbättras. Lazy loading skulle kunna vara ett alternativ.

<b>Rangordning av sidor baserat på mätvärden:</b><br>
1) Kulturhuset stadsteatern<br>
2) Uppsala Stadsteater<br>
3) Helsingborg stadsteater

Enligt sidornas mätvärden anser jag att KS fick bäst resultat med kortast sidladdningstid. Sidladdningstid kan vara kopplat till antal förfrågningar, men också hur man hanterar innehållet med t.ex. bilder. Trots att US sida "Föreställningar" var den största sidan på 5,3 MB laddade den mer än dubbelt så snabbt jämfört med den mindre "På scen" av HS - detta tyder på att de har effektivare behandling av sidans innehåll, möjligtvis med t.ex. komprimerade bilder.

US hade minst antal förfrågningar och HS's sida var minst till storlek men då KS lyckats hantera dessa något högre siffror så att sidladdningen inte blev så lidande som på övriga sidor knep de ändå förstaplatsen.

Ingen av dessa sidor imponerade dock särskilt med laddningstid. Av de nio sidor analysen omfattade var det endast två som låg under två sekunder (US's startsida och KS's "Om oss"). För användarvänligheten tycker jag inte att en sida ska ta mer än 1,5-2 sekunder att ladda, och att HS's sida "På scen" var uppe på över 8 sekunder är därför under all kritik. Laddningstid som är över 3 sekunder är för långsamt, enligt mig, 1,5-3 sekunder är godkänt och under 1,5 sekunder är en snabb sida (något ingen av dessa sidor uppnår).

<h4>Källor</h4>

<a href="https://developers.google.com/speed/pagespeed/insights/">https://developers.google.com/speed/pagespeed/insights/</a>

<h5>Skribent</h5>
Mette Hellemarck
