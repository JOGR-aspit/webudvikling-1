# CSS Flexbox – En komplet guide

CSS **Flexbox** (Flexible Box Layout) er et layoutsystem, der gør det nemt at justere og fordele elementer i en container, selv når deres størrelse er ukendt eller dynamisk. Flexbox er særligt nyttig til at lave responsivt design.

---

## 1. Grundlæggende om Flexbox

For at bruge Flexbox skal du anvende `display: flex;` på en container. Dette gør alle direkte børn til flex-elementer.

**Eksempel:**
```css
.container {
    display: flex;
    background: lightgray;
    padding: 10px;
}
.item {
    background: steelblue;
    color: white;
    padding: 20px;
    margin: 5px;
}
```
```html
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
</div>
```

---

## 2. Hvad er et Flex Item?

Når en container har `display: flex;`, bliver alle dens **direkte børn** automatisk **flex-items**. Dette betyder, at disse elementer nu kan justeres, skaleres og justeres inden for flex-containeren ved hjælp af forskellige flexbox-egenskaber.

### Egenskaber ved Flex Items
Flex-items kan påvirkes af følgende egenskaber:

- `flex-grow`: Bestemmer hvor meget et element vokser i forhold til andre.
- `flex-shrink`: Bestemmer hvor meget et element kan krympe, hvis der ikke er plads nok.
- `flex-basis`: Angiver startstørrelsen på et flex-item.
- `align-self`: Tillader individuel vertikal justering af et flex-item.

**Vigtigt:** Kun direkte børn af en flex-container bliver flex-items. Indlejrede elementer skal også have `display: flex;`, hvis de skal fungere som flex-containere.

---

## 3. Flex Container vs. Flex Items

| Egenskab | Påvirker | Beskrivelse |
|----------|---------|-------------|
| `display: flex;` | Container | Aktiverer flexbox |
| `flex-direction` | Container | Bestemmer retningen af flex-items |
| `justify-content` | Container | Justerer elementer horisontalt |
| `align-items` | Container | Justerer elementer vertikalt |
| `align-self` | Item | Individuel vertikal justering |
| `flex-grow` | Item | Bestemmer hvor meget et element vokser |
| `flex-shrink` | Item | Bestemmer hvor meget et element krymper |
| `flex-basis` | Item | Angiver startstørrelsen på et element |

---

## 4. Flex Direction

Bestemmer om flex-elementer arrangeres vandret eller lodret.

```css
.container {
    display: flex;
    flex-direction: row; /* Standard: row (vandret) */
}
```

| Værdi | Beskrivelse |
|--------|--------------|
| `row` | Vandret (default), venstre mod højre |
| `row-reverse` | Vandret, højre mod venstre |
| `column` | Lodret, oppefra og ned |
| `column-reverse` | Lodret, nedefra og op |

---

## 5. Justering af indhold (`justify-content`)

**Justerer elementer horisontalt i containeren.**

```css
.container {
    display: flex;
    justify-content: space-between;
}
```

| Værdi | Beskrivelse |
|--------|--------------|
| `flex-start` | Venstrejusteret (standard) |
| `flex-end` | Højrejusteret |
| `center` | Centreret |
| `space-between` | Plads mellem elementer |
| `space-around` | Lige meget plads rundt om elementer |

---

## 6. Justering af elementer (`align-items`)

**Justerer elementer vertikalt i forhold til containerens højde.**

```css
.container {
    display: flex;
    align-items: center;
}
```

| Værdi | Beskrivelse |
|--------|--------------|
| `flex-start` | Top-justeret |
| `flex-end` | Bund-justeret |
| `center` | Centreret |
| `stretch` | Strækker sig til at fylde containerens højde |
| `baseline` | Justerer efter tekstens baseline |

---

## 7. Individuel justering (`align-self`)

Tillader individuel justering af et specifikt element.

```css
.item:nth-child(2) {
    align-self: flex-end;
}
```

---

## 8. Flex Grow, Shrink & Basis

### `flex-grow`
**Bestemmer hvor meget et element skal vokse i forhold til andre.**

```css
.item {
    flex-grow: 1;
}
```

### `flex-shrink`
**Bestemmer hvor meget et element skal krympe.**

```css
.item {
    flex-shrink: 2;
}
```

### `flex-basis`
**Angiver standardstørrelsen for et element.**

```css
.item {
    flex-basis: 200px;
}
```

---

## 9. Shorthand: `flex`

En forkortelse for `flex-grow`, `flex-shrink` og `flex-basis`:
```css
.item {
    flex: 1 1 100px; /* grow, shrink, basis */
}
```

---

## 10. Konklusion

- **Flexbox gør layout lettere** og giver stor fleksibilitet i moderne webdesign.
- **Container-egenskaber** styrer, hvordan elementer justeres og placeres.
- **Item-egenskaber** kan styre individuel størrelse og placering.
- **Brug shorthand `flex`** for en mere kompakt syntaks.
