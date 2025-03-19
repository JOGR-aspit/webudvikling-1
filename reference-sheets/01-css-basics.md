# Introduktion til CSS: En Trin-for-Trin Guide

## Hvad er CSS?

CSS står for **Cascading Style Sheets**. Det er et sprog, der bruges til at style og formatere HTML-dokumenter, og dermed hjemmesider.

**Med CSS kan du:**
- Ændre farver på tekst og baggrund
- Ændre skrifttyper og tekststørrelse
- Tilføje mellemrum og rammer
- Lave layouts med flere kolonner
- Tilføje animationer og visuelle effekter

Tænk på HTML som skelettet (strukturen) af en webside, og CSS som tøjet og makeup (udseendet).

## Hvordan tilføjer man CSS til HTML

Der er tre måder at tilføje CSS til HTML:

### 1. Inline CSS
Tilføjes direkte i HTML-elementet med attributten `style`.

```html
<p style="color: blue; font-size: 18px;">Dette er blå tekst.</p>
```

### 2. Internal CSS
Tilføjes i `<head>` sektionen af HTML-dokumentet inden i et `<style>` element.

```html
<head>
  <style>
    p {
      color: blue;
      font-size: 18px;
    }
  </style>
</head>
```

### 3. External CSS (anbefalet metode)
Skrives i en separat fil med `.css` endelse og linkes til HTML-dokumentet.

```html
<head>
  <link rel="stylesheet" href="style.css">
</head>
```

Og i `style.css` filen:
```css
p {
  color: blue;
  font-size: 18px;
}
```

## CSS Syntax

CSS består af **regler**. Hver regel har to dele:
1. **Selector** (vælger) - fortæller hvilke HTML-elementer der skal styles
2. **Declarations** (deklarationer) - fortæller hvordan elementerne skal styles

```css
selector {
  property: value;
  property: value;
}
```

For eksempel:
```css
p {
  color: blue;
  font-size: 18px;
}
```

I dette eksempel:
- `p` er selectoren (vælger alle `<p>` elementer)
- `color` og `font-size` er properties (egenskaber)
- `blue` og `18px` er values (værdier)

Hver property-value par kaldes en **declaration** og afsluttes med et semikolon (`;`).

## Selectors

Selectors bruges til at vælge de HTML-elementer, du vil style.

### Element Selector
Vælger alle elementer af en bestemt type.

```css
p {
  color: blue;
}
```
Dette vælger alle `<p>` elementer på siden.

### Class Selector
Vælger elementer med en bestemt klasse. Bruges med et punktum (`.`).

```css
.highlight {
  background-color: yellow;
}
```
Dette vælger alle elementer med `class="highlight"`.

### ID Selector
Vælger et element med et bestemt ID. Bruges med et hashtag (`#`).

```css
#header {
  background-color: black;
  color: white;
}
```
Dette vælger elementet med `id="header"`.

### Kombination af Selectors
Du kan kombinere selectors:

```css
/* Alle p-elementer inde i en div */
div p {
  font-style: italic;
}

/* Alle p-elementer med klassen 'important' */
p.important {
  font-weight: bold;
}
```

## Farver i CSS

Der er flere måder at angive farver i CSS:

### Med farvenaavn
```css
h1 {
  color: red;
  background-color: lightgray;
}
```

### Med HEX-koder
```css
h1 {
  color: #FF0000; /* rød */
  background-color: #F0F0F0; /* lysegrå */
}
```

### Med RGB-værdier
```css
h1 {
  color: rgb(255, 0, 0); /* rød */
  background-color: rgb(240, 240, 240); /* lysegrå */
}
```

### Med RGBA-værdier (med gennemsigtighed)
```css
h1 {
  color: rgba(255, 0, 0, 0.5); /* halvgennemsigtig rød */
}
```

## Tekst-formatering

### Skrifttype (Font)
```css
p {
  font-family: Arial, Helvetica, sans-serif;
}
```

### Skriftstørrelse
```css
p {
  font-size: 16px;
}

h1 {
  font-size: 2em; /* 2 gange større end parent-elementet */
}
```

### Tekst-stil
```css
p {
  font-weight: bold; /* fed tekst */
  font-style: italic; /* kursiv tekst */
  text-decoration: underline; /* understreget tekst */
}
```

### Tekstjustering
```css
p {
  text-align: center; /* centreret tekst */
}

h1 {
  text-align: left; /* venstrejusteret tekst */
}

.footer {
  text-align: right; /* højrejusteret tekst */
}
```

## Margin og Padding

Margin og padding er vigtige for at skabe mellemrum mellem elementer.

- **Margin**: Mellemrum uden for elementet
- **Padding**: Mellemrum inden i elementet

```css
/* Alle sider er ens */
div {
  margin: 10px;
  padding: 20px;
}

/* Forskellig på alle sider (top, right, bottom, left) */
div {
  margin: 10px 20px 15px 5px;
  padding: 5px 10px 8px 12px;
}

/* Kun enkelte sider */
div {
  margin-top: 10px;
  padding-left: 20px;
}
```

## Borders

Du kan tilføje rammer (borders) omkring elementer:

```css
div {
  border-width: 2px;
  border-style: solid;
  border-color: black;
}

/* Eller kortere: */
div {
  border: 2px solid black;
}

/* Afrundede hjørner: */
div {
  border: 2px solid black;
  border-radius: 10px;
}
```

## Eksempler på komplette CSS-regler

### Et simpelt visitkort
```css
.card {
  width: 300px;
  padding: 20px;
  margin: 20px auto;
  background-color: #f8f8f8;
  border: 1px solid #ddd;
  border-radius: 8px;
  font-family: Arial, sans-serif;
}

.card h2 {
  color: #2c3e50;
  margin-bottom: 10px;
}

.card p {
  color: #7f8c8d;
  line-height: 1.5;
}

.card .contact {
  font-weight: bold;
  color: #3498db;
}
```

### En navigationsbar
```css
.navbar {
  background-color: #333;
  overflow: hidden;
  padding: 10px 0;
}

.navbar a {
  float: left;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-family: Arial, sans-serif;
}

.navbar a:hover {
  background-color: #ddd;
  color: black;
}

.navbar a.active {
  background-color: #4CAF50;
  color: white;
}
```

## Øvelser

1. **Opgave 1**: Lav en overskrift med rød tekst, centreret på siden.
2. **Opgave 2**: Opret et afsnit med blå tekst, skriftstørrelse på 18px og med en tynd, sort ramme.
3. **Opgave 3**: Lav en knap med afrundede hjørner, grøn baggrund og hvid tekst.

**Løsning til Opgave 1**:
```css
h1 {
  color: red;
  text-align: center;
}
```

**Løsning til Opgave 2**:
```css
p {
  color: blue;
  font-size: 18px;
  border: 1px solid black;
  padding: 10px;
}
```

**Løsning til Opgave 3**:
```css
.button {
  background-color: green;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
}
```
