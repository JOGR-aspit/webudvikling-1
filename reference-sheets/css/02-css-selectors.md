# CSS Selectors – En grundig gennemgang

CSS-selectors bruges til at vælge og style HTML-elementer. De gør det muligt at målrette specifikke elementer baseret på deres type, attributter, relationer til andre elementer og deres tilstande. I dette dokument gennemgår vi både basale og avancerede selectors med eksempler og forklaringer.

---

## Grundlæggende Selectors

### 1. **Element Selector**
Vælger alle HTML-elementer af en bestemt type.

**Eksempel:**
```css
p {
    color: blue;
}
```
Dette vil ændre farven på al tekst i `<p>`-elementer til blå.

**HTML:**
```html
<p>Dette er et afsnit.</p>
```

---

### 2. **Class Selector (`.`)**
Vælger alle elementer, der har en bestemt klasse.

**Eksempel:**
```css
.highlight {
    background-color: yellow;
}
```
**HTML:**
```html
<p class="highlight">Dette afsnit er fremhævet.</p>
```

Klasser kan genbruges på flere elementer for konsistent styling.

---

### 3. **ID Selector (`#`)**
Vælger et unikt element med en specifik `id`.

**Eksempel:**
```css
#main-title {
    font-size: 24px;
    color: red;
}
```
**HTML:**
```html
<h1 id="main-title">Min Overskrift</h1>
```
Et ID skal være unikt på en side, mens klasser kan genbruges.

---

### 4. **Universal Selector (`*`)**
Vælger alle elementer på siden.

**Eksempel:**
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
Dette kan være nyttigt for at nulstille standardmarginer og paddings.

---

### 5. **Group Selector (`A, B, C`)**
Anvender samme stil på flere elementer.

**Eksempel:**
```css
h1, h2, h3 {
    font-family: Arial, sans-serif;
    color: navy;
}
```
**HTML:**
```html
<h1>Overskrift 1</h1>
<h2>Overskrift 2</h2>
<h3>Overskrift 3</h3>
```

---

## Avancerede Selectors

### **Struktur-baserede Selectors**

#### **`:first-child`, `:last-child`, `:nth-child(n)`**
Disse selectors vælger et element baseret på dets position blandt søskende-elementer.

**Eksempel:**
```css
p:first-child {
    color: blue;
}
p:last-child {
    color: red;
}
p:nth-child(2) {
    font-weight: bold;
}
```
**Forklaring:**
- `:first-child` vælger det første barn af en forælder.
- `:last-child` vælger det sidste barn.
- `:nth-child(n)` vælger et specifikt barn baseret på position.

**HTML:**
```html
<div>
    <p>Bliver blå</p>
    <p>Bliver fed</p>
    <p>Bliver rød</p>
</div>
```

---

#### **`:first-of-type`, `:nth-of-type(n)`**
Disse selectors vælger det første eller nth element af en bestemt type, uanset andre elementtyper.

**Eksempel:**
```css
p:first-of-type {
    text-decoration: underline;
}
p:nth-of-type(2) {
    background-color: lightgray;
}
```
**HTML:**
```html
<div>
    <span>Ikke påvirket</span>
    <p>Bliver understreget</p>
    <span>Ikke påvirket</span>
    <p>Bliver grå baggrund</p>
</div>
```

**Forklaring:**
- `:first-of-type` vælger det første forekommende element af en given type.
- `:nth-of-type(n)` vælger det n’te element af en given type.

---

#### **`:empty`**
Vælger elementer, der ikke indeholder nogen indhold (hverken tekst eller andre HTML-elementer).

**Eksempel:**
```css
p:empty {
    display: none;
}
```
**HTML:**
```html
<p></p> <!-- Skjules -->
<p>Har tekst</p> <!-- Visibles -->
```

**Forklaring:**
- Hvis et element ikke har nogen børn eller tekstindhold, påvirkes det af `:empty`.

---

#### **`:not(X)`**
Denne selector ekskluderer bestemte elementer fra at blive påvirket af styling.

**Eksempel:**
```css
p:not(.special) {
    color: gray;
}
```
**HTML:**
```html
<p>Bliver grå</p>
<p class="special">Bliver ikke grå</p>
```

**Forklaring:**
- `:not(X)` udelukker de elementer, der matcher betingelsen (`X`).
- I eksemplet ovenfor påvirkes alle `p`-elementer undtagen dem med klassen `.special`.

---

## Konklusion

CSS-selectors er kraftfulde værktøjer til præcis styling af HTML-elementer. Grundlæggende selectors dækker de fleste behov, men avancerede selectors giver ekstra kontrol over strukturer og brugerinteraktioner. Brug dem klogt for at skabe fleksible og vedligeholdelsesvenlige designs!
