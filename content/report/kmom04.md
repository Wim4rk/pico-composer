---
Title: Kmom04
Description: Kursmoment 4
Template: kmom
---
# Kursmoment 4

Välkommen att läsa min presentation [online][1].

Min undersökning kan läsas [här][5].

Det här är det sista av de kursmoment som jag redan påbörjat vid ett tidigare
kurs&shy;tillfälle. Nu börjar det bli på riktigt igen.

Jag har lagt alldeles för mycket tid på mina teman. Jag lappar och lagar i det
ljusa temat, då spricker något i det mörka. Sen lagar jag det mörka temat och något
fallerar i det ljusa. Jag kan verkligen lägga hur mycket tid som helst på CSS.
Samtidigt så blev jag rätt nöjd.

Jag valde att samköra det här kursmomentet med kmom05, främst därför att jag
har bekym&shy;mer med att lägga till bilder i min undersökning. Det skulle
under arbetet med kmom05 visa sig att miss&shy;taget var att försöka rendera
markdown inom ett HTML-block. Det går inte.

## Mondrian

Jag har länge velat bygga det här temat &ndash; nu äntligen har jag verktygen. Jag
utgick från en målning av [Piet Mondrian][2]. Här finns [originalet][3].

Det första jag gjorde var att skapa en ny förstasida. En splash-page. Till att
börja med försökte jag använda markdown. Det gick alldeles utmärkt, förutom att
det enda jag placerade där var html. När jag skulle loopa igenom alla sidorna
för att skapa en meny, så lyckades jag inte med det. Kanske är det rent av
omöjligt att skriva pico-logik i en markdown-fil?

Så jag skrev hela sidan i html, direkt i twig-filen, undantaget innehållet i den
röda rutan.

Designen är responsiv. Om jag hade valt en målning med fler fält så hade grid
förmodligen löst det mesta åt mig. Som det är fick jag för mycket svart yta och
valde att komplettera med @media-förfrågningar. Beroende på _view port_ så blir
det till olika tavlor.

Sedan överförde jag några av idéerna till mina övriga sidor; presentationer,
rapporter och redovisningar.

### Färgschema

Färgschemat är triadiskt, även om jag använder den gula färgen mycket lite,
precis som Mondrian själv. Jag valde också att hämta färgerna från originalet
med färgpipetten i Firefox, så rent matematiskt kanske de inte stämmer på ett
färghjul.

Om jag hade varit riktigt petnoga hade jag kunnat croppa de olika färgfälten ur
bilden av originalet, då hade jag haft med penseldrag och krackelering. De
svarta strecken hade nog ändå fått fastställas med CSS.

### Typografi

Jag försökte att hålla mig till ungefär den typografi som borde ha rått kring
Mondrians målning: _art noveau_. Nu använder jag sans-serifer i brödtexten
också, något jag brukar försöka att undvika. Jag känner själv att valet är
tveksamt, men det var det bästa jag kunde finna på Google Fonts.

## Dark theme

Mitt tema bygger på en gammal monitor. Jag har använt grönt, och bara grönt.
Till och med bilderna gjorde jag monokroma med CSS och färgade sedan gröna.
Hade jag vetat hur man ger bilder sämre upplösning (utan att bearbeta dem i
en dator) så hade jag gjort det. Det är antagligen möjligt med logik i Pico
och ordentlig misshandel i cimage.

Jag är väldigt nöjd med hur jag lurar ögat att det rör sig om en monitor. Jag
har inte bara använt grön text på en svart bakgrund, jag har lagt till en
_radial gradient_ som illustrerar ljusläckage, och jag har lagt ett nät över
som ger ränder på ett genuint sätt.

Det blev lite nördigt.

### Refactoring

Jag sitter fortfarande och skriver om min kod från tidigare kursmoment. Jag
kommer att göra det åtminstone tills jag är klar med den här kursen.

Det är inte så att jag har svårt att få arbetet ur händerna, men allteftersom
jag utvecklar sidor så behöver jag, så att säga, skriva rent tidigare stilar.
Eljest skulle jag snart ha ett lapptäcke av kod där ingen längre skulle kunna
följa sömmarna.

## Kort och koncist

__Kommentera kort om skrivuppgiften, något som är värt att nämna från arbetet med den?__

Jag valde ett ämne som legat mig nära under min karriär hittills. Hur
marknadsför man klassisk musik på ett bra vis? Det jag upptäckt är att det
används ganska tråkiga färgval för en så kreativ bransch.

Jag hade fördelen att kunna bedriva min studie av orkestrars webbsidor under en
lite längre tid. Det har ju varit ett egendomligt år för all scenkonst, så det
har varit intressant att följa med. Möjligen har pandemin
bidragit till att de inrapporterade sidorna stagnerat en smula.

__Vilket färgschema valde du till ditt tema och hur valde du att använda
färgerna (mer eller mindre eller lika mycket av alla färger)?__

Min färgpalett är triadisk; röd, blå och gul.

__Valde du att jobba med accentfärg och i så fall hur?__

Egentligen så jobbade jag med tre accentfärger. De fick byta plats beroende på
vilken av dem som jag valde till huvudfärg just där. Hade jag ett rött fält
blev länkarna vita. Var fältet vitt så var länkarna blåa. Eftersom jag jobbade
med grundfärger så var det inte så enkelt att kombinera dem. Jag gjorde ett
försök att låta en vit länk i en blå bakgrund bli gul när jag svävade över den,
och det fungerade just där.

__Hur valde du att lösa ditt dark theme? Gjorde du en kopia på ditt vanliga tema? Eller löste du det med imports?__

De är snarlika, så det mesta kunde jag lösa med @imports, men en hel del kod
kopierades, för att filerna skall vara mer överskådliga.

Det finns två mål med mitt mörka tema, dels att det skall se ut som
grund&shy;temat, och att det ändå skall se ut som en monitor från sent 70-tal.

__Vilken är din TIL för detta kmom?__

Fraktioner, <samp>fr</samp>, är ett lysande verktyg tillsammans med grid och flex.

[1]: http://www.student.bth.se/~olai19/dbwebb-kurser/design/me/portfolio/report/kmom04
[2]: https://en.wikipedia.org/wiki/Piet_Mondrian
[3]: https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Piet_Mondriaan%2C_1930_-_Mondrian_Composition_II_in_Red%2C_Blue%2C_and_Yellow.jpg/800px-Piet_Mondriaan%2C_1930_-_Mondrian_Composition_II_in_Red%2C_Blue%2C_and_Yellow.jpg
[5]: http://www.student.bth.se/~olai19/dbwebb-kurser/design/me/portfolio/analysis/01_colors
