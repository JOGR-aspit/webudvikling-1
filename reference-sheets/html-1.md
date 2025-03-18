# Introduktion til HTML: En Trin-for-Trin Guide

HTML (HyperText Markup Language) er fundamentet for alle hjemmesider, du ser online. Tænk på det som skelettet, der giver struktur til webindhold. I denne guide gennemgår vi det grundlæggende i HTML på en klar og organiseret måde med masser af eksempler.

## Hvad er HTML?

HTML er teknisk set et "opmærkningssprog" (Markup Language), ikke et "programmeringssprog". Det betyder, at det bruger særlige tags til at "markere" eller navngive forskellige dele af et dokument, eller en hjemmeside. Disse tags fortæller webbrowsere (som Chrome, Firefox eller Safari), hvordan indholdet skal vises.

I modsætning til programmeringssprog, der kan udføre beregninger eller træffe beslutninger, beskriver HTML blot, hvad ting er. For eksempel fortæller HTML browseren "denne tekst er en overskrift" eller "dette er et afsnit" eller "dette er et billede." Browseren beslutter derefter, hvordan disse elementer skal vises baseret på dens standardindstillinger.

## Forståelse af Kodeindrykning

Du har noget bidt mærke i, at kode (også HTML) ofte skrives med nogle linjer indrykket (flyttet til højre) ved hjælp af mellemrum eller tabulatorer (tabs). Denne indrykning tjener flere vigtige formål:

1. **Læsbarhed**: Indrykning gør koden lettere at læse ved visuelt at vise, hvilke elementer der er indeholdt i andre. Dette er især nyttigt, når du har mange indlejrede elementer.

2. **Struktur**: Indrykning afspejler HTML's hierarkiske struktur. Når et element er inde i et andet element, indrykker vi det for at vise dette forælder-barn forhold (ja, forælder-barn, eller parent-child, er officiel terminologi).

3. **Lettere Fejlfinding**: Når din kode har korrekt indrykning, er det meget lettere at opdage fejl, såsom manglende afsluttende tags.

Her er et eksempel på indrykket HTML-kode:

```html
<body>
  <div>
    <h1>Hovedoverskrift</h1>
    <p>Dette er et afsnit inde i div'en.</p>
  </div>
</body>
```

I dette eksempel er `<h1>` og `<p>` elementerne indrykket, fordi de er inde i `<div>` elementet, som selv er inde i `<body>` elementet. Denne indrykning gør det klart, at disse elementer er indlejret i hinanden, og har et vidst forhold til hinanden.

Indrykning påvirker ikke, hvordan hjemmesiden ser ud i browseren - det er udelukkende for at hjælpe mennesker med at læse og skrive koden mere effektivt. Tænk på det som afsnit og mellemrum i almindelig skrivning - de ændrer ikke betydningen, men de gør det meget lettere at læse.

## Hvordan HTML-filer fungerer

HTML-filer er grundlæggende set tekstfiler med en `.html` filendelse. Du kan oprette dem ved hjælp af enhver teksteditor som Notepad, Visual Studio Code eller Sublime Text. Vi vil bruge Visual Studio Code i 99% af tilfældene.

Når du opretter en HTML-fil, skriver du i bund og grund instruktioner til webbrowsere. Når nogen besøger din hjemmeside, downloader deres browser din HTML-fil, læser den linje for linje og bygger hjemmesiden i henhold til dine instruktioner.

For eksempel, hvis du har `<h1>Velkommen til Min Hjemmeside</h1>` i din HTML-fil, forstår browseren, at "Velkommen til Min Hjemmeside" skal vises som en stor overskrift. Browseren håndterer alt arbejdet med at fortolke din HTML og gengive den visuelt.

## Grundlæggende Struktur i et HTML-dokument

Ethvert HTML-dokument følger denne grundlæggende struktur:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Min Første Hjemmeside</title>
  </head>
  <body>
    <h1>Hej Verden!</h1>
    <p>Dette er min første hjemmeside.</p>
  </body>
</html>
```

Lad os gennemgå, hvad hver del gør i detaljer:

- `<!DOCTYPE html>` - Denne "erklæring" kommer først i et HTML-dokument. Det er faktisk ikke et HTML-tag; det er en instruktion til browseren om, hvilken version af HTML du bruger. Erklæringen `<!DOCTYPE html>` indikerer, at du bruger HTML5, den nyeste version af HTML. Dette hjælper browsere med at displaye din side korrekt.

- `<html>` - Dette er rod-elementet, der indeholder alle andre HTML-elementer. Hvert eneste element på din side skal være inde i dette tag. Det er som beholderen for hele dokumentet. Det afsluttende `</html>` tag kommer helt til sidst i dit dokument.

- `<head>` - Denne sektion indeholder meta-information om dokumentet—information, der ikke direkte vises på hjemmesiden. Dette inkluderer ting som sidetitlen, links til CSS-stylesheets, JavaScript-filer, tegnsætinformation og instruktioner om, hvordan siden skal opføre sig på forskellige enheder. Tænk på det som "bag kulisserne" information.

- `<title>` - Dette indstiller titlen, der vises i browser-fanen. Den bruges også af søgemaskiner, når de viser din side i søgeresultater. Hvert HTML-dokument bør have en meningsfuld titel, der beskriver sidens indhold.

- `<body>` - Dette indeholder alt det indhold, der er synligt på hjemmesiden. Alt hvad brugeren ser og interagerer med - tekst, billeder, links, formularer - er inde i body-elementet. Hvis det er synligt på din hjemmeside, hører det til i body.

## Forståelse af HTML-tags

HTML-tags er byggestenene i HTML. De kommer typisk i par: et åbnings-tag og et luknings-tag. Åbnings-tagget signalerer, hvor et element begynder, og luknings-tagget signalerer, hvor det slutter.

```html
<tagnavn>Indhold her</tagnavn>
```

- Åbnings-tagget starter med `<` efterfulgt af tag-navnet og slutter med `>`. For eksempel: `<p>`.
- Luknings-tagget starter med `</` efterfulgt af det samme tag-navn og slutter med `>`. For eksempel: `</p>`.
- Indholdet går mellem disse tags. Dette kan være tekst, billeder eller endda andre HTML-elementer.

Når et element indeholder et andet element, kalder vi det "indlejring", eller "nesting". For eksempel:

```html
<p>Dette er et afsnit med <strong>fed tekst</strong> indeni.</p>
```

Her er `<strong>` elementet indlejret i `<p>` elementet.

Nogle tags behøver ikke at blive lukket, fordi de ikke indeholder indhold. Disse kaldes selvlukkende tags eller tomme elementer:

```html
<img src="billede.jpg" alt="En beskrivelse af billedet">
<br>
<hr>
```

Disse tags repræsenterer elementer, der ikke omslutter indhold:
- `<img>` indsætter et billede
- `<br>` skaber et linjeskift
- `<hr>` skaber en vandret linje

## Almindelige HTML-tags

### Overskrifter

HTML tilbyder seks niveauer af overskrifter, fra `<h1>` (mest vigtig) til `<h6>` (mindst vigtig). Tænk på disse som overskrifterne i en bog eller artikel - med hovedtitler, kapiteltitler, sektionsoverskrifter og så videre.

```html
<h1>Dette er en Niveau 1 Overskrift</h1>
<h2>Dette er en Niveau 2 Overskrift</h2>
<h3>Dette er en Niveau 3 Overskrift</h3>
<h4>Dette er en Niveau 4 Overskrift</h4>
<h5>Dette er en Niveau 5 Overskrift</h5>
<h6>Dette er en Niveau 6 Overskrift</h6>
```

Hver overskrift vises i en forskellig størrelse, hvor `<h1>` er den største og mest fremtrædende. Korrekt brug af overskrift-tags er vigtig for både læsbarhed og tilgængelighed - skærmlæsere bruger overskriftsniveauer til at hjælpe brugere med at navigere i sidestrukturen.

Det er bedst at bruge kun én `<h1>` pr. side (normalt til hovedtitlen) og at bruge overskrifter i hierarkisk rækkefølge uden at springe niveauer over (f.eks. spring ikke fra `<h1>` til `<h3>` uden en `<h2>` imellem).

### Afsnit

For at lave et tekstafsnit skal du bruge `<p>` tagget:

```html
<p>Dette er et tekstafsnit. Det kan indeholde flere sætninger og vil blive vist som en tekstblok af browseren.</p>
```

Afsnit er et af de mest almindelige HTML-elementer. Hvert afsnit starter automatisk på en ny linje med lidt plads før og efter. Dette gør din tekst mere læsbar.

Hvis du skriver flere afsnit, skal hvert have sine egne `<p>` tags:

```html
<p>Dette er det første afsnit.</p>
<p>Dette er det andet afsnit.</p>
```

Browseren vil vise disse som separate tekstblokke, med mellemrum imellem dem.

### Tekstformatering

Du kan fremhæve eller formatere tekst ved hjælp af forskellige tags. Disse tags hjælper med at formidle betydning og vigtighed:

```html
<strong>Denne tekst er fed</strong>
```
`<strong>` tagget indikerer, at tekst er vigtig. Browsere viser typisk dette som fed tekst.

```html
<em>Denne tekst er kursiv</em>
```
`<em>` tagget fremhæver tekst, og browsere viser typisk dette som kursiv tekst.

```html
<u>Denne tekst er understreget</u>
```
`<u>` tagget understreger tekst, hvilket kan være nyttigt til fremhævning, selvom det nogle gange forveksles med links.

```html
<mark>Denne tekst er fremhævet</mark>
```
`<mark>` tagget fremhæver tekst, normalt med en gul baggrund, ligesom når man bruger en markeringspen på papir.

Disse formateringstags kan kombineres og indlejres:

```html
<p>Dette er <strong>meget <em>vigtig</em></strong> information.</p>
```

Dette producerer: Dette er **meget _vigtig_** information.

### Lister

HTML understøtter to typer af lister, som er meget nyttige til at organisere information:

**Ordnede lister (nummererede):**
Ordnede lister bruges, når rækkefølgen af punkter er vigtig, som trin i en proces eller rangering af punkter.

```html
<ol>
  <li>Første punkt</li>
  <li>Andet punkt</li>
  <li>Tredje punkt</li>
</ol>
```

`<ol>` tagget opretter den ordnede listebeholder, og hvert `<li>` (listepunkt) tag opretter et punkt på listen. Browseren nummererer automatisk punkterne sekventielt.

**Uordnede lister (punkttegn):**
Uordnede lister bruges, når punkterne ikke har en specifik rækkefølge eller sekvens.

```html
<ul>
  <li>Æble</li>
  <li>Banan</li>
  <li>Appelsin</li>
</ul>
```

`<ul>` tagget opretter den uordnede listebeholder, og igen opretter hvert `<li>` tag et punkt. Browseren viser disse med punkttegn i stedet for numre.

Lister kan også indlejres i hinanden for at skabe flerniveau-lister:

```html
<ul>
  <li>Frugter
    <ul>
      <li>Æbler</li>
      <li>Bananer</li>
    </ul>
  </li>
  <li>Grøntsager
    <ul>
      <li>Gulerødder</li>
      <li>Spinat</li>
    </ul>
  </li>
</ul>
```

Dette skaber et hierarki, hvor de indlejrede lister er indrykket og typisk bruger en anden punkttegnsstil.

### Links

Links (eller hyperlinks) er det, der gør nettet til et "net" - de forbinder forskellige sider sammen. Links oprettes ved hjælp af `<a>` (anchor) tagget:

```html
<a href="https://www.eksempel.com">Klik her for at besøge Eksempel.com</a>
```

`<a>` tagget opretter linket, men det har brug for en `href`-attribut, der angiver, hvor linket skal føre hen. Teksten mellem åbnings- og lukningstaggene bliver til den klikkable linktekst, som brugerne ser.

Links kan pege på:
- **Eksterne hjemmesider**: `<a href="https://www.google.com">Google</a>`
- **Andre sider på din hjemmeside**: `<a href="om-os.html">Om Os</a>`
- **Specifikke sektioner på en side**: `<a href="#sektion2">Spring til Sektion 2</a>` (Dette kræver et element med `id="sektion2"` et sted på siden)
- **E-mail adresser**: `<a href="mailto:eksempel@eksempel.com">E-mail Os</a>` (Dette åbner brugerens e-mail program)

### Billeder

Billeder gør hjemmesider mere engagerende og kan hjælpe med at formidle information mere effektivt. Billeder tilføjes ved hjælp af `<img>` tagget:

```html
<img src="kat.jpg" alt="En sød kat">
```

`<img>` tagget har to essentielle attributter:
- `src` (kilde) attributten fortæller browseren, hvor billedfilen findes. Dette kan være en relativ sti (som "billeder/kat.jpg") eller en fuld URL (som "https://eksempel.com/billeder/kat.jpg").
- `alt` (alternativ tekst) attributten giver en tekstbeskrivelse af billedet. Dette er afgørende for:
  - Tilgængelighed: Skærmlæsere læser denne tekst for synshandicappede brugere
  - SEO: Søgemaskiner bruger denne tekst til at forstå, hvad billedet handler om
  - Fallbacks: Hvis billedet ikke kan indlæses, vises denne tekst i stedet

Du kan også kontrollere et billedes størrelse ved hjælp af `width` og `height` attributterne:

```html
<img src="kat.jpg" alt="En sød kat" width="300" height="200">
```

Dog er det generelt bedre at kontrollere billedstørrelser ved hjælp af CSS (hvilket kommer senere) i stedet for HTML-attributter.

## HTML-attributter

Attributter giver yderligere information om HTML-elementer og ændrer, hvordan de opfører sig eller vises. De er altid angivet i åbningstagget og følger dette format:

```html
<tag attribute="værdi">Indhold</tag>
```

Tænk på attributter som justerbare indstillinger for HTML-elementer. Forskellige elementer understøtter forskellige attributter, men nogle almindelige inkluderer:

- `id` - Giver et element en unik identifikator, som kan bruges til at målrette det med CSS, JavaScript eller links inden for siden. Hvert `id` skal være unik på siden.
  ```html
  <p id="introduktion">Dette afsnit har en ID der hedder "introduktion".</p>
  ```

- `class` - Tildeler en eller flere CSS-klasser til et element. I modsætning til ID'er kan flere elementer dele samme klasse, hvilket gør dem nyttige til styling af grupper af elementer.
  ```html
  <p class="fremhævet vigtig">Dette afsnit har to klasser - `fremhævet` og `vigtig`.</p>
  ```

- `style` - Anvender inline CSS-styling direkte på et element. Dette overskriver eventuelle styles fra eksterne stylesheets.
  ```html
  <p style="color: blue; font-size: 18px;">Dette afsnit er blåt og større.</p>
  ```

- `title` - Giver yderligere information som et tooltip, der vises, når brugere holder musen over elementet.
  ```html
  <p title="Dette vil vises, når du holder musen over teksten">Hold musen over mig for at se mere information.</p>
  ```

Her er et eksempel, der kombinerer flere attributter:
```html
<p id="intro" class="fremhævet" style="color: blue;" title="Introduktionsafsnit">
  Dette er et introduktionsafsnit med flere attributter.
</p>
```

Attributter gør HTML mere kraftfuldt og fleksibelt, hvilket giver dig mulighed for at tilpasse, hvordan elementer opfører sig og vises.

## Oprettelse af en Simpel Hjemmeside

Lad os samle det hele for at lave en simpel hjemmeside:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mine Kæledyr</title>
  </head>
  <body>
    <h1>Mine Yndlingskæledyr</h1>
    
    <h2>Katte</h2>
    <p>Jeg har to katte ved navn <strong>Cooper</strong> og <strong>Mia</strong>.</p>
    <p>De er begge redningskatte, som jeg adopterede fra det lokale internat for to år siden.</p>
    <img src="katte.jpg" alt="Mine to katte der sidder sammen">
    
    <h2>Hunde</h2>
    <p>Jeg har også en hund ved navn <strong>Molly</strong>.</p>
    <p>Molly er en golden retriever, som elsker at lege og gå lange ture i parken.</p>
    <img src="hund.jpg" alt="Min hund Buddy der leger i parken">
    
    <h3>Mollys Yndlingsaktiviteter:</h3>
    <ul>
      <li>At gå ture</li>
      <li>At lege apport</li>
      <li>At svømme i søen</li>
    </ul>
    
    <p>Lær mere om <a href="https://www.eksempel.com/kaeledyr-pleje">kæledyrspleje</a>.</p>
  </body>
</html>
```

Denne simple hjemmeside viser eksempler på:
- Den grundlæggende HTML-struktur
- Overskrifter på forskellige niveauer (h1, h2, h3)
- Afsnit med formateret tekst
- Billeder med beskrivende alt-tekst
- En uordnet liste
- Et hyperlink til en anden hjemmeside

Hvis du gemmer denne kode som "kaeledyr.html" og åbner den i en webbrowser, ville du se en formateret hjemmeside om kæledyr. Browseren fortolker HTML-taggene og viser indholdet i henhold til den struktur, du har defineret.

## HTML-kommentarer

Kommentarer er noter i koden, der ikke vises på hjemmesiden. De er kun synlige, når man ser HTML-kildekoden. Kommentarer tjener flere vigtige formål:

1. **Dokumentation**: De hjælper dig og andre med at forstå, hvad forskellige dele af koden gør
2. **Planlægning**: Du kan skitsere din hjemmesidestruktur med kommentarer, før du skriver den egentlige kode
3. **Fejlfinding**: Du kan midlertidigt "kommentere ud" dele af din kode for at finde problemer
4. **Kommunikation**: De giver dig mulighed for at efterlade noter til andre udviklere, der måske arbejder med koden

Kommentarer starter med `<!--` og slutter med `-->`:

```html
<!-- Dette er en kommentar. Den vil ikke blive vist på hjemmesiden. -->

<!-- 
Dette er en flerlinjet kommentar.
Du kan skrive så mange linjer, som du har brug for.
Browseren vil ignorere al denne tekst.
-->

<p>Dette afsnit vil blive vist <!-- denne kommentar vil ikke være synlig --> på hjemmesiden.</p>
```

Kommentarer kan placeres næsten hvor som helst i dit HTML-dokument og kan spænde over flere linjer. De er særligt nyttige i længere, mere komplekse dokumenter for at hjælpe med at opretholde organisation og klarhed.

## Specialtegn

Nogle tegn har særlig betydning i HTML, såsom `<`, `>` og `&`. Hvis du vil vise disse tegn som en del af dit indhold (i stedet for at få dem fortolket som kode), skal du bruge specielle koder kaldet HTML-entiteter.

HTML-entiteter starter altid med en ampersand (`&`) og slutter med et semikolon (`;`). Her er de mest almindelige:

- `&lt;` vises som `<` (mindre end)
- `&gt;` vises som `>` (større end)
- `&amp;` vises som `&` (ampersand)
- `&quot;` vises som `"` (citationstegn)
- `&apos;` vises som `'` (apostrof)
- `&nbsp;` vises som et ubrydbart mellemrum (et mellemrum, der ikke kollapser eller ombrydes)

For eksempel, hvis du vil forklare HTML-tags i dit indhold, kunne du skrive:

```html
<p>I HTML skrives tags som &lt;p&gt; og &lt;/p&gt;.</p>
```

Dette ville vises som: `I HTML skrives tags som <p> og </p>.`

Uden entiteterne ville browseren fortolke `<p>` som et faktisk HTML-tag i stedet for tekst, der skal vises.

HTML-entiteter bruges også til tegn, der ikke let kan indtastes på et tastatur, såsom:
- `&copy;` for © (copyright-symbol)
- `&reg;` for ® (registreret varemærke)
- `&trade;` for ™ (varemærke)
- `&euro;` for € (euro)
- `&pound;` for £ (pund)

## Vigtige Punkter at Huske

1. **HTML handler om struktur, ikke udseende**: HTML definerer, hvad ting er, ikke hvordan de ser ud. For at kontrollere udseendet vil du efterhånden lære CSS (Cascading Style Sheets).

2. **Luk altid dine tags korrekt**: De fleste HTML-elementer kræver både åbnings- og lukningstags. Hvis du glemmer at lukke tags, kan det forårsage uventede problemer.

3. **Indrykning er vigtig for læsbarhed**: Selvom browseren ikke bekymrer sig om indrykning, er korrekt indrykket kode meget lettere for mennesker at læse og vedligeholde.

4. **Brug semantisk HTML**: Vælg tags, der beskriver betydningen af indholdet, ikke bare hvordan det skal se ud. For eksempel, brug `<h1>` til hovedoverskrifter, ikke bare for at gøre teksten stor.

5. **Inkluder alternativ tekst til billeder**: Tilføj altid beskrivende `alt`-tekst til billeder. Dette hjælper brugere med synshandicap og forbedrer SEO.

6. **HTML er tilgivende**: Browsere vil forsøge at vise din side, selv hvis der er fejl i din HTML, men dette kan føre til uensartede resultater. Stræb efter gyldig, velformet HTML.

7. **Test din HTML i forskellige browsere**: Forskellige browsere kan gengive den samme HTML lidt forskelligt, så det er god praksis at teste dine sider i flere browsere.

## Øvelser

For at forstærke din læring, prøv disse simple øvelser:



2. **Opret en side om din yndlingshobby**: Inkluder:
   - En hovedoverskrift med hobbynavnet
   - Flere underoverskrifter for forskellige aspekter
   - Afsnit, der forklarer hvert aspekt
   - En liste over udstyr eller materialer, der er nødvendige
   - Mindst ét billede med passende alt-tekst
   - Et link til en hjemmeside med mere information om hobbyen

3. **Opret en simpel opskriftsside**: Inkluder:
   - En overskrift med opskriftens navn
   - Et kort introduktionsafsnit
   - En liste over ingredienser
   - Trin-for-trin instruktioner ved hjælp af en ordnet liste
   - Et billede af den færdige ret med alt-tekst

Husk, den bedste måde at lære HTML på er ved at øve sig. Start med simple sider og byg gradvist mere komplekse sider, efterhånden som du bliver mere komfortabel med syntaksen. Bekymr dig ikke om at få siderne til at se pæne ud endnu—fokuser på at lære den korrekte HTML-struktur og syntaks først.
