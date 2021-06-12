---
Title: Kmom03
Description: Kursmoment 3
Template: kmom
---
# Kursmoment 3

Välkommen att läsa min presentation [online][1].

Rutnätet har funnits så länge som vi skrivit böcker. Även gamla handskrifter
från tiden innan bokpressen höll en strikt visuell form. Det är en uråldrig
form som tilltalar människans förkärlek för symmetri, och som har finslipats
genom hundratals år.

Det faktum att vi fortfarande kämpar för att få den här grundläggande tekniken
att fungera i våra webbläsare är ett tecken på hur tidigt i utvecklingen vi
fortfarande är. Och hur lite vi har prioriterat de här frågorna. Visst talas
det om hur olika det är att läsa text på en skärm kontra att läsa den i tryck,
men det känns ofta som att lösningen har varit att bryta alla regler som vi
samlat på oss genom dessa sekler.

## Grid och flexbox

Jag har ägnat ganska mycket tid åt att läsa om- och experimentera med grid den
här gången. Det finns många bra instruktioner att läsa på nätet och mycket fin
inspiration på många sajter.

Det kan vara svårt, tycker jag, att blanda flexbox med grid, men uppenbarligen
så går det. Nu har jag bara kvar flexbox i min header, redovisningarna styrs
upp med hjälp av ett grid. Min förstasida och min om-sida är ännu så länge
bara några _div_, men jag har planer för dem.

Egentligen förstår jag inte grid mer än jag förstår flex-box, men jag har lättare
att visualisera i form av rutnät &ndash; kanske längtar jag tillbaks till att
designa i tabeller? (Antagligen inte...)

## Uppgiften

Under arbetet med min redovisnings&shy;sida fann jag äntligen något jag länge letat
efter; _grid order_. Jag skulle kunna lägga inne&shy;hålls&shy;förteckningen efter
inne&shy;hållet
i min html (.twig), och ändå presentera den till vänster på skärmen. Alternativa
skärm&shy;läsare som presenterar innehållet i braille eller talsyntes behöver inte
traggla igenom innehållsförteckningen först på varje sida.

Det spökade dock till det med tab-ordningen och buggade ordentligt om man försökte
markera text, så jag övergav projektet. Jag lade innehålls&shy;förteckningen först i
html-dokumentet.

Enligt specen så skall innehållsförteckningen ligga till vänster. I annat fall
hade jag föredragit att ha den till höger. Då hade den helt enkelt fallit ner
under huvudinnehållet när man går ner på mindre skärmar.

Jag behöver däremot inte gömma den helt på en mindre skärm. Jag kan flytta ner
den till slutet av sidan med _grid-order_. Den finns till hands, och användaren
behöver ändå inte scrolla femton centimeter innan själva innehållet.

### Refactoring

Jag har börjat inse att jag kommer att slipa vidare på allting under kursens
gång. Det är ingen mening att ta något längre än specen. Till exempel så har
jag klarat kravet för min _landing-site_, men jag kommer jobba vidare med
typografi och färger framgent.

När jag fick griddet på plats ville jag försöka att ta min typografi ett steg längre.
Jag skapade en _mixin_ som räknar ut rätt radhöjd utifrån font-size för att
närma sig en multipel av "det magiska talet".

För att få det riktigt bra skulle jag vilja lägga till ett horisontellt
grid &ndash; rader för att nivellera radhöjder mellan olika element. Vi hade en
bra modell i förra versionen av den här kursen. Det borde finnas något som
fungerar tillsammans med SASS.

## Skapa och skriva

Ibland ser jag för mycket på den här kursen ur en skribents per&shy;spektiv. Jag glömmer
ibland är att _jag_ skall vara länken mellan den som skapar och publik&shy;ationen på
nätet. _Jag_ skall göra det enkelt att publicera. Alla de betänklig&shy;heter som jag
har är det upp till mig att lösa. Jag ska inte bekymra mig så mycket för innehåll
som jag gör.

Målbilden är att uppdragsgivaren kan använda sin sajt utan att behöva tänka på
allt det som jag tänker på just nu. Sajten skall vara ett verktyg, inte ett
problem.

## Linting

Jag får igenom all min SASS-kod i lintern, utom den som rör den responsiva
menyn. Den är dock skapad som någon slags Pico-mall, så jag vet inte riktigt
hur jag skall gå vidare med den. Jag behöver verkligen lära mig att skapa egna
menyer.

## Kort och koncist

__Hur har det gått att jobba med CSS-Grid/Flexbox?__

Det har gått alldeles utmärkt.

__Har du jobbat med dessa tekniker sedan tidigare? Vad anser du om det?__

Jag har gjort stora delar av den här kursen i föregående version. Den gången
jobbade vi med @desinax, vilket gav oss synliga rutnät både vågrätt och lodrätt.
Det är något jag saknar den här gången, och jag har försökt hitta motsvarande
moduler för SASS. Utan större resultat.

Jag försöker ändå att följa reglerna för lodrät och vågrät rytm. Man får titta
på sin skärm i en brant vinkel för att försöka se om raderna ligger i våg.

__Har du försökt dela upp din SASS-kod i olika moduler? Kanske har du skapat en
ny modul som är din layout?__

Jag har börjat städa upp i min SASS-kod. Jag försöker att lägga färger med
färger, typografi med typografi och ha en egen fil för layout.

Just nu går gemensamma- och tema-specifika regler för mycket i varandra. Jag har
mer att städa upp.

__Valde du att göra om din sidas layout eller nöjde du dig med report sidan?__

Jag valde att bara göra om report-sidan. Jag har en plan för förstasidan som jag
vill implementera när vi talar om färger. Jag råkade dock göra extrauppgiften
genom att använda grid även i footern.

__Vilken är din TIL för detta kmom?__

På en bra hemsida behöver man inte tänka så mycket. Materialet finns på rätt
plats, och den är enkel att uppdatera.

[1]: http://www.student.bth.se/~olai19/dbwebb-kurser/design/me/portfolio/report/kmom03
