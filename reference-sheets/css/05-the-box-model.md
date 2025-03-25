# CSS Box Model – En detaljeret guide

CSS Box Model er grundlaget for, hvordan HTML-elementer bliver vist på en webside. Hvert element på en webside bliver betragtet som en "boks" med fire hoveddele: **Content, Padding, Border og Margin**.

---

## 1. Hvad er Box Model?

Box Model beskriver, hvordan CSS beregner størrelse og placering af elementer. Modellen består af følgende dele (indefra og ud):

- **Content (Indhold):** Selve indholdet af elementet, f.eks. tekst eller billeder.
- **Padding:** Afstanden mellem indholdet og elementets kant (border).
- **Border:** Rammen, der omgiver padding og indhold.
- **Margin:** Afstanden mellem elementet og dets omgivelser.

### Illustration af Box Model:

![Box Model](https://www.washington.edu/accesscomputing/webd2/student/unit3/images/boxmodel.gif)

---

## 2. CSS-egenskaber for Box Model

### **2.1 Content (Indhold)**
```css
width: 200px;
height: 100px;
```
**Beskrivelse:** Bestemmer indholdets bredde og højde. Dette inkluderer **ikke** padding, border eller margin.

---

### **2.2 Padding (Indvendig afstand)**
```css
padding: 10px;
```
**Beskrivelse:** Tilføjer en indvendig afstand mellem indholdet og kanten af elementet. Kan specificeres individuelt:

```css
padding-top: 10px;
padding-right: 15px;
padding-bottom: 10px;
padding-left: 5px;
```

**Shorthand:**
```css
padding: 10px 15px 10px 5px; /* Top, Right, Bottom, Left */
```

---

### **2.3 Border (Kant)**
```css
border: 2px solid black;
```
**Beskrivelse:** En kant omkring padding og indhold. Består af tre dele:
- **Tykkelse:** `2px`
- **Stil:** `solid` (kan også være `dashed`, `dotted`, `double`, etc.)
- **Farve:** `black`

Eksempel med forskellige kanter:
```css
border-top: 3px dashed red;
border-right: 5px solid blue;
border-bottom: 2px dotted green;
border-left: 4px double black;
```

---

### **2.4 Margin (Ydre afstand)**
```css
margin: 20px;
```
**Beskrivelse:** Afstand mellem dette element og dets naboer. Kan specificeres individuelt:

```css
margin-top: 20px;
margin-right: 15px;
margin-bottom: 10px;
margin-left: 5px;
```

**Shorthand:**
```css
margin: 20px 15px 10px 5px; /* Top, Right, Bottom, Left */
```

#### **Auto-centering med margin**
```css
margin: 0 auto;
```
**Forklaring:** Centrerer et blok-element vandret, hvis det har en fast bredde.

---

## 3. Box-sizing: Standard vs. Alternative Model

### **3.1 Standard Box Model (default)**
```css
box-sizing: content-box;
```
- **Beregning:** `Total bredde = width + padding + border`
- **Eksempel:**
```css
width: 200px;
padding: 10px;
border: 5px solid black;
```
> **Reel bredde = 200px + 10px (højre) + 10px (venstre) + 5px (højre) + 5px (venstre) = 230px**

---

### **3.2 Alternative Box Model**
```css
box-sizing: border-box;
```
- **Beregning:** `Total bredde = width (inkl. padding og border)`
- **Eksempel:**
```css
width: 200px;
padding: 10px;
border: 5px solid black;
box-sizing: border-box;
```
> **Reel bredde forbliver 200px, da padding og border indgår i width.**

> 💡 **Tip:** Brug `border-box` for lettere layoutstyring.

---

## 4. Eksempel på CSS Box Model i praksis

```css
div {
    width: 300px;
    height: 150px;
    padding: 20px;
    border: 5px solid black;
    margin: 30px;
    box-sizing: border-box;
}
```

**HTML:**
```html
<div>Dette er en boks</div>
```

- `width: 300px;` → Den samlede bredde er 300px (pga. `border-box`)
- `padding: 20px;` → Indhold har 20px afstand til kanten
- `border: 5px solid black;` → En tydelig kant rundt om boksen
- `margin: 30px;` → Afstand til andre elementer

---

## 5. Konklusion

- **Box Model** er essentiel for CSS-layouts.
- Brug `padding`, `border`, `margin` korrekt for at styre afstande.
- Overvej `box-sizing: border-box;` for en mere intuitiv breddeberegning.
- Eksperimentér med forskellige værdier for at få det ønskede layout!