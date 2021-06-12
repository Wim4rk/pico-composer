---
Title: Kmom02
Description: Kursmoment 2
Template: kmom
---
# Kursmoment 2

Jag jobbar vidare med min portfolio-sida. I mitt stilla sinne undrar jag hur
rättningen går till, jag kommer ju att bygga på sidan efter hand. Om mitt arbete
rättas sent så kommer jag ju att ha hunnit gå vidare... Men jag förlitar mig på
att det kommer att ordna sig.

Arbetet går sakta. Det spelar ingen roll vilket ramverk vi har, vilken
pre-processor vi använder eller hur vi hanterar bilder. Det är inte heller
själva designen som tar tid, utan det är allt småplock i scss-filerna. Var ligger
just den inställningen som verkar köra över det jag försöker att göra? Varför
hjälper det inte ens att skriva <samp>!important</samp>? Vad är det som kan vara
mer specifikt än det som jag specificerar här? Det tar en evig tid.

## SASS

Jag har den goda turen att kunna jämföra mellan SASS och LESS. Så långt känns
SASS enklare. Kanske har det att göra med Pica kontra Anax, men SASS skapar mer
överskådliga CSS-filer.

Hittills känner jag igen syntaxen, men vi får se om vi börjar jobba med några
mix-in eller motsvarande, och hur det kommer att fungera då.

Jag hade NPM installerat sedan tidigare, och en god förståelse för hur det
fungerar.

## Font Awesome

Detta är ett väldigt användbart verktyg, och något jag behöver jobba mer med.
Jag har nu lagt till tre ikoner i min footer.

## Typografi

Det är alltid lite besvärligt för mig när det börjar talas om typografi.
Typograf är ett yrke som man inte lättvindligt skall avfärda. Det är inte alls
så att man kan gissa sig fram till god typografi.

Med detta sagt så har jag försökt att gissa mig fram till god typografi.

Nu finns det någon slags oro kring att använda serifer på webbsidor. Det framhålls
att det som fungerar bäst på skärmar är sans-serifer. Jag tar inte det för
självklart. Dels läser jag själv på en Kindle, och skärmen på min hustrus senaste
iPad är ganska annorlunda den som fanns på hennes första. Vad som fungerar bäst
på en skärm ändrar sig efter hand.

Även [SMACCS][3], som används som kursstöd har vågat bryta mot den här regeln.
Deras val &ndash; [Acuta][4] av Adobe &ndash; har en mycket lätt serif, men den finns där.

### Brödtext

Som typsnitt för min brödtext har jag därför valt [Merriweather][1] av Sorkin
Type. Det är en ett seriftypsnitt som är framtaget för att vara trevligt att
läsa på webben. Jag väljer _alltid_ typsnitt till brödtexten först. Det jag
mest av allt är ute efter är läsbarheten.

### Rubriker

Rubriker i tryck använder ofta sans-serifer, men på nätet verkar det vara helt
tvärt om. Jag kan inte förstå varför det blivit på det viset. Att det kan vara
besvärligt att läsa serifer i brödtext kan jag acceptera, men varför man tvunget
skall använda serifer i rubriken är ett mysterium.

Här valde jag verkligen att utmana mig. [Roboto Slab][2], av Christian
Robertsson är en serif-font som används flitigt till rubriker, bland andra av
Wordpress.

Därmed har jag valt serifer både till rubriker och brödtext. Och jag vet inte
om det är god typografi, men det är ett medvetet val.

## Kort och koncist

__Vad tycker du om SASS än så länge?__

Sass är smidigt än så länge. Nu när vi har börjat använda Font Awesome så har
de kompilerade css-filerna börjat att växa till sig rejält. Från under hundra rader
till gott och väl över 5000. Det känns inte rätt för mig, det är mycket kod där
som jag inte använder. Jag kanske inte behöver skriva den, men jag behöver lagra,
och &ndash; inte minst &ndash; servera den till användaren.

__Är du bekant med Node, npm eller npm scripts (t.ex. npm run lint) sedan tidigare? Vad anser du om det?__

Jag har använt det i andra kurser, och i privata projekt. Det är ett smidigt sätt
att installera de verktyg som behövs i en särskild utveckling, men antagligen inte
i alla. Här kompilerar vi SASS, på andra håll kompilerar jag LESS.

Package.json är lättläst

__Hur kändes det att kompilera SASS till CSS, var det något du reflekterade över?__

Nej, det var ganska rättframt. Jag använder _make_ i privata projekt, bland annat
när jag kompilerar C-kod för att koda mikrochipp.

__Kommentera ditt tema, hur kan man beskriva dess design och hade du några planer på “design” när du byggde ditt tema?__

Jag anar lite hur den här kursen kommer att fortskrida. Inom kort kommer vi att
börja jobba med _grid_. Jag väljer att hålla allt så enkelt som möjligt, så att
jag inte behöver ändra så mycket när vi når dit.

__Valde du att dela upp din kod? Vilka uppdelningar valde du att göra?__

Jag valde att dela upp min kod, men jag har inte följt rekommendationerna. Just
nu gör jag skillnad på layout, typografi, nav-meny och variabler för färger m.m.
Det blir genast uppenbart att jag behöver städa igenom mina filer framgent, och
då skall jag följa boken lite närmare.

__Vilken är din TIL för detta kmom?__

Design-kursen kommer att ta mer tid än vad jag hittills satt av.

[1]: https://fonts.google.com/specimen/Merriweather
[2]: https://fonts.google.com/specimen/Roboto+Slab
[3]: http://smacss.com
[4]: https://fonts.adobe.com/fonts/acuta
