---
Title: Laddtider
Description: Analys av laddtider
Template: me
---
# Laddtider på tre myndigheters hemsidor

En kort analys av laddtider för tre svenska myndigheters hemsidor.

## Urval

Jag valde att rikta in mig på tre svenska myndigheter som har ett stort
intresse av att finnas på nätet; Folkhälso&shy;myndig&shy;heten, Försvarets
Radio&shy;anstalt, samt Myndigheten för samhällsskydd och beredskap.

Hos dessa myndigheter skall användaren få aktuell, relevant och fakta&shy;granskad
information.

## Metod

Jag har använt mig utav verktygen [Google pagespeed][2] och fliken devtools i
Mozilla Firefox.

## Resultat

Utifrån laddtider rangordnar de undersökta sajterna sig såhär:

1. [FHM][3]
2. [FRA][4]
3. [MSB][5]

FHM är en klar vinnare, sidan imponerar, men alla dessa sidor har god
funktion&shy;alitet. Jag kan finna det jag letar efter och ingen sida är
särskilt långsam.

Enligt [Google pagespeed][2] kan sidorna förbättra sina laddtider genom att
göra följande besparingar (i urval). Ändringen anges i sekunder.

<table>
    <tr>
        <th></th>
        <th>FRA</th>
        <th>FHM</th>
        <th>MSB</th>
    <tr>
    <tr>
        <td>Använd modernare bildformat</td>
        <td>8,85</td>
        <td>0,15</td>
        <td>20,55</td>
    </tr>
    <tr>
        <td>Koda bilder effektivare</td>
        <td>7,5</td>
        <td></td>
        <td>11,55</td>
    </tr>
    <tr>
        <td>Ladda viktiga resurser i förväg</dh>
        <td>6,66</td>
        <td>2,58</td>
        <td></td>
    </tr>
    <tr>
        <td>Resurser blockerar rendering</td>
        <td>3,24</td>
        <td>0,64</td>
        <td></td>
    </tr>
    <tr>
        <td>Sänd bilder i rätt storlek</td>
        <td></td>
        <td>0,75</td>
        <td></td>
    </tr>
</table>

Utifrån tabellen ser jag att det problem som jag trodde skulle vara vanligast;
att bilder skickades i fel storlek endast var ett problem för FRA (en av deras
bilder var 1,6 MB stor, jag antar att den drar ner betyget). Det är ett problem
som de flesta utvecklare är medvetna om, men mitt antagande är att de som
upp&shy;daterar hemsidornas information kan begå det miss&shy;taget emellanåt.

Generellt kan man spara data genom att sända bilder i ett modernare bildformat,
något som torde vara enkelt att implementera. Att sedan koda bilderna korrekt
verkar vara lönsamt. Hur detta står sig efter att bilderna uppdaterats till ett
modernare format framgår inte i den här undersökningen.

Att ladda viktiga resurser i förväg verkar också vara en god idé.

När resurser blockerar rendering så verkar det handla om att JavaScript och
CSS sänds som egna filer. Det vore således att föredra att skicka sådan kod
skriven direkt i html-filen, men frågan är om tids&shy;besparingen är värd
arbetet? Först om man kan använda ett ramverk för sådan kon&shy;vertering vore
det att rekom&shy;mendera.

#### Desktop first

Alla undersökta myndigheter borde bättre inrikta sig på mobil&shy;telefoner.
Betyget ([Google page&shy;speed][2]) är utan undantag lägre för mobil&shy;anpassade
sidor kontra sidor för desktop. I vissa fall är diskrepansen stor.
Den enda myndighet som får ett _bra_ betyg för mobil&shy;telefoner är
Folk&shy;hälso&shy;myndig&shy;heten.

Något som man verkligen kan använda för att göra en mobil&shy;sida mer läsbar är
att inte lägga hela inne&shy;hållet i en enda hög kolumn. Försök inte att få in
hela sidans information på första&shy;sidan, utan följ FHM:s exempel och
ge stora tydliga bilder eller knappar för att nå en relevant undersida.

#### Gräns för absolut laddningstid

Jag förväntar mig att sidan skall vara laddad inom 3 sekunder. Jag tänker på
laddnings&shy;tid när den överstiger 1 sekund. Ingen av de under&shy;sökta
webb&shy;platserna överskrider 3 sekunder till en första rendering.

## Analys

Min rådata kan granskas [här][1].

### [FHM][3]

#### Folkhälsomyndigheten

FHM får mycket höga betyg av ([Google page&shy;speed][2]), som endast föreslår
smärre förbättrings&shy;punkter. Värt att nämna är att man kunde tjäna in data på
att använda ett modernt filformat, som alla de andra sidorna, men besparingen är
ringa.

<figure class="right">
    <img src="../image/fhm.jpg?w=400&q=50" alt="Folkhälsomyndighetens hemsida">
    <figcaption>Folkhälsomyndighetens hemsida</figcaption>
</figure>

Sidan är mycket snabb. Den har enkel och klar HTML. All CSS finns i
HTML-dokumentet. Här har man verkligen ansträngt sig för att optimera
data&shy;överföring och filstorlekar. Något som rimmar väl med den belastning
som jag förmodar att den här sidan stått under på senare tid.

I sin mobilvariant försöker man inte att anslå all information man har, utan
delar på ett tydligt vis in sidan i några undersidor. Först i form av bilder
som illustrerar de ämnen som avhandlas, därunder följer en lista med aktuella
artiklar. Föredömligt.

I denna undersökning imponerar Folk&shy;hälso&shy;myndig&shy;hetens hemsida.
Vid ett vanligt besök så tänker man inte alls på laddtider.

Det finns en sida med URL fhm.se, som inte drivs av
Folk&shy;hälso&shy;myndig&shy;heten. Den anslår ändå information om CoVid19
(inget annat).  Jag undrar vem som driver den. Enligt [WayBackmachine][6]
så var fhm.se till salu så sent som den 2 december 2020.

### [FRA][4]

#### Försvarets Radioanstalt

<figure class="left">
    <img src="../image/fra.jpg?w=400&q=50" alt="FRA:s hemsida">
    <figcaption>FRA:s hemsida</figcaption>
</figure>

Här har vi ett coolt tema med rörliga bilder som verkligen leder tanken till
digital säkerhet, nationellt försvar och kryp&shy;terings&shy;teknik. Sidan är
så att säga rekryterande.

När förstasidan är öppen uppstår ett referensfel varje gång som huvud&shy;bilden
laddas om. En av bilderna i "karusellen" sticker ut. Dess storlek är 1,6 MB,
trots att den är svart&shy;vit. Enligt Google Pagespeed kan man spara in 1,2 MB
data där.

Sidan laddar många resurser (45 st). Den har ett stort JavaScript-bibliotek,
och använder stora CSS-filer.

FRA har helt klart inriktat sig på desktop, och får mycket dåliga poäng för sin
mobil&shy;variant. Vid en snabb överblick verkar det som att man försöker att
anslå så mycket information som möjligt på mobil&shy;variantens första&shy;sida.

För övrigt pågår något annorlunda här. URL:en får någon slags hash eller kod.
Den verkar dock konstant när jag laddar om den med något dygn emellan.
Kanske är det ett verktyg för att förhindra DOS-attacker? Det är i alla fall
mycket svårt att nå undersidor genom att skriva in URL:er.

Enligt Mozilla devtools råkar sidan ut för ett par 404. En för en JS-fil, och
en för en favicon som verkar saknas! Det borde enkelt kunna lösas.

Jag upplever ändå sajten som snabb. Den är inom gränsen för den laddningstid
som jag instinktivt kan acceptera.

### [MSB][5]

#### Myndigheten för Samhällsskydd och Beredskap

<figure class="right">
    <img src="../image/msb.jpg?w=400&q=50" alt="MSB:s hemsida">
    <figcaption>MSB:s hemsida</figcaption>
</figure>

MSB har en ganska enkel, men inte helt oproblematisk sida. Det tar alldeles för
lång tid att ladda vissa bilder, och sidan känns en aning långsam. Helt klart
tolerabel, men märkbart långsam.

Den största besparing man kan göra här är att använda modernare bild&shy;format,
och att koda bilder bättre. Det är egentligen bara förstasidan som är direkt
bildorienterad. Det är ändå lite segt att bläddra runt på sajten.

Även MSB borde fokusera mer på mobiltelefoner. Man försöker, som FRA, att
få in så mycket infor&shy;mation som möjligt på första&shy;sidan där.

## Felkällor

Det är mycket troligt att dessa webbsidor upp&shy;daterats efter mitt arbete.
Det är därför troligt att mina resultat avviker från en senare undersökning.

Under arbetet drabbades jag av en avvikelse: undersidan
[https://www.msb.se/sv/aktuellt/](https://www.msb.se/sv/aktuellt/) tog vid ett
tillfälle över åtta sekunder att laddas. Jag valde att bortse från den mätningen
och gjorde en ny, som angav 1,5 sekunder.

Jag förstår inte den teknik som FRA använder på sin sida. Å ena sidan verkar den
imponerande, å andra sidan har den enkla 404:or. Jag skulle verkligen vilja veta
vad det är som pågår där.

## Referenser

* [Folkhälsomyndigheten][3]
* [Försvarets Radioanstalt][4]
* [Myndigheten för Samhällsskydd och Beredskap][5]

[1]: https://docs.google.com/spreadsheets/d/162ILFdKhV-uAC5aPArRbbGjT4jf5hzTHBHkDH5bqqVo/edit?usp=sharing

[2]: https://developers.google.com/speed/pagespeed/insights/

[3]: https://www.folkhalsomyndigheten.se/

[4]: https://www.fra.se/

[5]: https://www.msb.se/

[6]: https://web.archive.org/web/*/fhm.se
