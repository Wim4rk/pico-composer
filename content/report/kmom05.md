---
Title: Kmom05
Description: Kursmoment 5
Template: kmom
---
# Kursmoment 5

Välkommen att läsa min presentation [online][1].

Min undersökning kan läsas [här][3].

Det är ganska stora kursmoment här. Jag kämpar på, men har givit upp alla
tankar på att hinna klart med kursen i tid. I och för sig har jag ganska roligt,
för en gångs skull känner jag inte att jag gör bara det nöd&shy;vändigaste utan
jag fyller ut övningarna med saker jag länge velat göra.

Kanske börjar jag komma ut ur mitt server&shy;rum för att försiktigt börja
titta på hur all min optimerade data egent&shy;ligen presenteras.

Men först till väsentligheterna.

<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/2ShyH-3xkiE?start=60" frameborder="0" allowfullscreen></iframe>
</div>

Jag lade inte mycket tid på den här övningen, förutom att jag mycket
nog&shy;grant valde ut klippet jag vill visa er.

## Undersökningen

Jag fick min undersökning gjord rätt kvickt. Bra det, när jag nu ligger så
långt efter.

Det har varit intressant att granska sajterna ordentligt i sömmarna. Jag har
blivit både imponerad och besviken.

## Responsivitet och användbarhet

Det som mest behövs för en god responsi&shy;vitet är det&shy;samma som behövs
för en god använd&shy;barhet; väl&shy;for&shy;mulerad HTML. Att därefter
app&shy;licera CSS blir så mycket enklare ju bättre kod man har att utgå ifrån.

Ett verktyg jag själv använder flitigt är _&amp;shy;_. Det anger var ord får
avstavas när det behövs. När man då ändrar storlek på view-port så ändrar
avstav&shy;ningarna sig också.

## Bildgalleriet

Bilderna jag använder är mina egna. I vanliga fall när jag skapar bilder för
nätet så konver&shy;terar jag dem från raw-formatet till jpg. Jag passar på att
göra bilderna mindre, och att dra ner kvalitén till 85%. Det brukar resultera i
filer omkring 300 kB stora.

För att nu få ett hyggligt övnings&shy;material försökte jag att göra en så rak
export som möjligt. De flesta av mina filer ligger nu mellan 500- och 700 kB.
En är på 1,2 MB. Vissa är omkring 300 kB. Upp&shy;lös&shy;ningen varierar
beroende på vilken kamera jag använt, och de flesta bilder är svart&shy;vita.

Jag skapade en ny splash-page för ett bildgalleri. Jag angav en ny maxbredd;
10&nbsp;000 px för att alltid fylla hela skärmen. I meta-datan lade jag till
klasser för att sedan få en så enkel CSS som möjligt. Jag försökte att låta bli
min header så mycket som möjligt, men den hade nog mått bra av mer
respon&shy;sivitet.

Jag fick galleriet att fungera med 26 rader kod men jag lade till lite
lull-lull för att zooma den bild man hovrar över, och för att lösa en media-query.
Filen blev slutligen 46 rader lång. Grid hjälper verkligen till mycket.

Missa inte att mitt galleri också fungerar i mitt mörka tema, men då som
mono&shy;kromatiska bilder med grön tint. Jag har också lärt mig att använda
Cimage för att försämra kvalitén.

## Cimage

Att använda Cimage är inte helt nytt för mig, men den här gången nådde jag en
bättre förståelse. Det är väldigt praktiskt att cacha upp de bilder man behöver
ha i olika format, men att ändå bara ladda upp en enda original&shy;bild.

I processen kan man också spara in på datamängden genom att inte servera mer
än vad som verkligen behövs.

Jag valde att använda _object-fit: cover;_ för att få mina bilder jämna i
galleriet. Det gjorde det mer eller mindre onödigt att använda Cimage i det
hänseendet.

I en loop är det svårt att få Cimage att rätt beskära bilder som har
olika format. Jag har till exempel bilder både i landskaps- och i
porträtt&shy;format. För att få ett riktigt bra resultat hade jag behövt
jobba direkt i html. Alternativt hade jag kunnat hämta bilderna med CSS, det
skulle vara fullt gångbart &ndash; Cimage jobbar ju utifrån url och
GET-variabler.

Det vore nu att helt börja om så jag valde att beskära alla bilder till 600
pixlars bredd, vilket är det minsta som kan användas för bilder i
landskaps&shy;läge. Jag sänkte också kvalitén till 40%. Jag borde därmed uppnå
en accep&shy;tabel kompri&shy;mering av den bild&shy;data jag sänder.

Bilderna i det mörka temat är 4% av originalets kvalité...

Jag har också sett över bilder på övriga sidor. Där är det mer rättframt
eftersom jag jobbar i html.

## Kort och koncist

__Berätta kort om erfarenheterna med din undersökning av webbplatsers laddningstid och vad du kom fram till.__

I mitt mycket smala urval fann jag att för stora bilder inte var ett problem.
Däremot föreslog [Google Pagespeed][2] att man borde använda Googles nya
bild&shy;format i alla tre fallen. Dock med om&shy;skriv&shy;ningen att man
borde använda "modernare" bild&shy;format.

__Har du några funderingar kring Cimage och dess nytta och features? Vilka bildverktyg använder du själv normalt sett?__

Jag har alltid skapat mina bilder via Adobe Lightroom &ndash; en rätt gammal
utgåva. Där kan man välja att optimera för skärm, och får filer kring 300 kb.
Till&shy;sammans med _width: 100%;_ brukar det bli responsivt med hyggligt lätta
filer.

Cimage verkar vara ett trevligt verktyg. Det roade mig att man var tvungen att
definiera formatet 1:1 själv.

__Vad är din egen allmänna uppfattning kring bilder för webben, nedladdningstider, responsiva bilder och allmänt kring bildbehandling för webben?__

Jag vill gärna ha ett verktyg som löser det åt mig, men jag vill också ha
större kontroll över _hur_ verktyget arbetar. Det krävs en ordentlig
djup&shy;dykning i Cimage för att förstå just det.

Med detta sagt så har jag använt liknande verktyg för Wordpress. Det har då
involverat något slags användargränssnitt. Resultatet har alltid handlat om
att göra bilder mindre, inte att lägga till effekter.

__Vilken är din TIL för detta kmom?__

Markdown kan inte renderas inom html-block. Om man använder html så använder man html full ut. Ända undantaget är inline-element som <code\>.

[1]: http://www.student.bth.se/~olai19/dbwebb-kurser/design/me/portfolio/report/kmom05

[2]: https://developers.google.com/speed/pagespeed/insights/

[3]: http://www.student.bth.se/~olai19/dbwebb-kurser/design/me/portfolio/analysis/02_load
