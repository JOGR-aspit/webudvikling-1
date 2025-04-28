# To-Do Liste
Du skal udvikle en simpel men funktionel to-do liste applikation, hvor brugeren kan oprette, markere som færdig, og slette opgaver — al data gemmes lokalt i browseren uden brug af server eller backend.

## Kravspecifikation
1. Funktionelle krav (hvad applikationen skal kunne)
* Tilføj opgave	
    * Brugeren skal kunne skrive en opgave i et tekstfelt og trykke "Tilføj" for at tilføje den til listen.
* Vis opgaver
    * Alle tilføjede opgaver skal vises på en liste på siden.
* Marker som færdig
    * Brugeren skal kunne klikke på en opgave for at markere den som "færdig" (fx ved gennemstregning eller farveskift).
* Slet opgave
    * Brugeren skal kunne slette en opgave fra listen.
* Gem opgaver lokalt
    * Applikationen skal gemme opgaverne i LocalStorage så de ikke forsvinder, når brugeren lukker og åbner siden igen.

2. Ikke-funktionelle krav (hvordan applikationen skal være)
* Responsivt design
    * Applikationen skal kunne bruges både på computer og mobil.
* Enkel brugergrænseflade
    * Designet skal være overskueligt og nemt at bruge uden instruktion.
* Klar feedback
    * Når brugeren tilføjer, markerer eller sletter en opgave, skal systemet give tydelig visuel feedback (fx animation, farveskift).
* Ingen fejl ved tom input
    * Hvis brugeren prøver at tilføje en tom opgave, skal der komme en fejlbesked eller advarsel.

3. Tekniske krav
* HTML
    * Brug semantic HTML5 elementer (`<form>`, `<input>`, `<ul>`, `<li>`, `<button>` osv.)
* CSS
    * Stil applikationen med en simpel men brugervenlig styling. Brug evt. flexbox eller grid.
* JavaScript
    * Brug vanilla JavaScript (ingen biblioteker som jQuery).
* LocalStorage
    * Gem og hent opgaver med localStorage API.

## Udvidelsesidéer (hvis du bliver færdig hurtigt)
* Tilføj mulighed for at redigere en opgave.
* Lav flere temaer (mørk/lys visning).
* Tilføj en tæller der viser hvor mange opgaver er tilbage.
* Tilføj en deadline (dato/tid) for hver opgave.

## Pseudo-kode til hovedfunktioner
Jeg har besluttet at give jer noget pseudo-kode til nogle af hovedfunktionerne, som i kan læne jer op af hvis i mangler overblikket. Jeg foretrækker dog selvfølgelig at i prøver selv først.

### Tilføj ny opgave
```js
function addTodo():
    hvis input-felt er tomt:
        vis fejlbesked
        stop
    ellers:
        lav en opgave-objekt med tekst og "ikke færdig"
        tilføj opgaven til listen over opgaver
        gem listen i LocalStorage
        opdater visningen på siden
        ryd input-feltet
```

### Slet en opgave
```js
function deleteTodo(opgaveId):
    find opgaven i listen med det givne id
    fjern opgaven fra listen
    gem listen i LocalStorage
    opdater visningen på siden
```

### Markér opgave som færdig/ikke færdig
```js
function toggleComplete(opgaveId):
    find opgaven i listen med det givne id
    skift opgavens "færdig" status (true/false)
    gem listen i LocalStorage
    opdater visningen på siden
```

### Gem opgave i LocalStorage
```js
function saveTodos():
    konverter listen af opgaver til JSON tekst
    gem JSON teksten i LocalStorage under en nøgle som f.eks. "todos"
```

### Hent opgaver fra LocalStorage
```js
function loadTodos():
    hent JSON tekst fra LocalStorage under nøgle "todos"
    hvis der findes data:
        konverter JSON teksten tilbage til en liste af opgaver
    ellers:
        start med en tom liste
    opdater visningen på siden
```

### Hovedprogram "Flow"
```js
når siden indlæses:
    kald loadTodos()

når bruger trykker på "Tilføj" knap:
    kald addTodo()

når bruger klikker på en opgave:
    kald toggleComplete()

når bruger klikker på en "Slet" knap:
    kald deleteTodo()
```