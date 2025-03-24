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

### 1. **Child Selector (`>`)**
Vælger kun de direkte børn af et element.

**Eksempel:**
```css
div > p {
    color: green;
}
```
**HTML:**
```html
<div>
    <p>Dette afsnit bliver grønt.</p>
    <span>
        <p>Dette afsnit bliver ikke grønt.</p>
    </span>
</div>
```
Kun `p`-elementer, der er direkte børn af `div`, påvirkes.

---

### 2. **Descendant Selector (mellemrum)**
Vælger alle efterkommere af et element.

**Eksempel:**
```css
div p {
    font-style: italic;
}
```
**HTML:**
```html
<div>
    <p>Dette afsnit bliver kursiveret.</p>
    <span>
        <p>Dette afsnit bliver også kursiveret.</p>
    </span>
</div>
```
Alle `p`-elementer inden for en `div` bliver kursiverede, uanset hvor dybt de er indlejret.

---

### 3. **Adjacent Sibling Selector (`+`)**
Vælger det umiddelbart næste element af samme niveau.

**Eksempel:**
```css
h1 + p {
    font-weight: bold;
}
```
**HTML:**
```html
<h1>Overskrift</h1>
<p>Dette afsnit bliver fed.</p>
<p>Dette afsnit forbliver normalt.</p>
```
Kun det første `p`-element efter `h1` påvirkes.

---

### 4. **General Sibling Selector (`~`)**
Vælger alle søskende efter et specifikt element.

**Eksempel:**
```css
h1 ~ p {
    color: grey;
}
```
**HTML:**
```html
<h1>Overskrift</h1>
<p>Dette afsnit bliver gråt.</p>
<p>Dette afsnit bliver også gråt.</p>
```
Alle `p`-elementer, der er søskende til `h1`, påvirkes.

---

### 5. **Attribute Selector (`[attr]`)**
Vælger elementer baseret på attributter.

**Eksempel:**
```css
a[target="_blank"] {
    color: red;
}
```
**HTML:**
```html
<a href="#" target="_blank">Åbn i nyt vindue</a>
<a href="#">Normal link</a>
```
Kun links med `target="_blank"` bliver røde.

---

### 6. **Pseudo-classes**
Giver mulighed for at style elementer baseret på deres tilstand.

**Eksempel:**
```css
a:hover {
    color: orange;
}
```
```css
input:focus {
    border: 2px solid blue;
}
```
Disse regler ændrer linkfarven ved hover og fremhæver inputfelter, når de er i fokus.

---

### 7. **Pseudo-elements**
Tillader styling af specifikke dele af et element.

**Eksempel:**
```css
p::first-line {
    font-weight: bold;
}
```
```css
p::before {
    content: "★ ";
    color: gold;
}
```
Første linje af et `p`-element bliver fed, og et guldfarvet stjerneikon tilføjes før hvert afsnit.

---

## Konklusion

CSS-selectors er kraftfulde værktøjer til præcis styling af HTML-elementer. Grundlæggende selectors dækker de fleste behov, men avancerede selectors giver ekstra kontrol over strukturer og brugerinteraktioner. Brug dem klogt for at skabe fleksible og vedligeholdelsesvenlige designs!
