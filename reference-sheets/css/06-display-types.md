# CSS Normal Flow og Display-egenskaber

CSS **Normal Flow** definerer, hvordan HTML-elementer som standard vises på en webside. For at forstå dette bedre, skal vi kigge på **block-, inline- og inline-block-elementer** samt deres forskelle.

---

## 1. Hvad er Normal Flow?

**Normal Flow** er den standard-layoutstruktur, som en browser bruger til at placere elementer, når ingen specifik positionering eller float anvendes. Dette betyder:

- **Block-elementer** starter på en ny linje og strækker sig over hele bredden af deres container.
- **Inline-elementer** forbliver på samme linje som deres omgivelser og tilpasser sig indholdets bredde.
- **Inline-block-elementer** kombinerer egenskaber fra både block og inline.

---

## 2. Block-elementer

Block-elementer fylder hele den tilgængelige bredde og starter på en ny linje. Eksempler inkluderer:

- `<div>`
- `<p>`
- `<h1>` til `<h6>`
- `<section>`
- `<article>`
- `<header>`
- `<footer>`

**Eksempel:**
```html
<div style="background: lightblue;">Dette er et block-element</div>
<p style="background: lightgreen;">Dette er et andet block-element</p>
```
**Egenskaber:**
- Strækker sig over hele containerens bredde.
- Starter altid på en ny linje.
- Kan indeholde både block- og inline-elementer.

---

## 3. Inline-elementer

Inline-elementer forbliver på samme linje som deres omkringliggende indhold og tilpasser sig indholdets størrelse. Eksempler inkluderer:

- `<span>`
- `<a>`
- `<strong>`
- `<em>`
- `<img>`
- `<code>`

**Eksempel:**
```html
<p>Dette er et <span style="background: yellow;">inline-element</span> i en sætning.</p>
```
**Egenskaber:**
- Fylder kun den nødvendige bredde.
- Forbliver på samme linje som de omkringliggende elementer.
- Kan **ikke** indeholde block-elementer.

---

## 4. Inline-block-elementer

Inline-block-elementer opfører sig som inline-elementer, men tillader justering af bredde og højde ligesom block-elementer. Eksempler inkluderer:

- `<button>`
- `<input>`
- `<select>`
- `<img>`

**Eksempel:**
```html
<span style="display: inline-block; width: 150px; height: 50px; background: orange;">Inline-block</span>
```
**Egenskaber:**
- Ligger på samme linje som andre inline-elementer.
- Tillader justering af bredde og højde.
- Kan indeholde både tekst og andre inline-elementer.

---

## 5. Sammenligning af block, inline og inline-block

| Egenskab         | Block         | Inline        | Inline-block  |
|-----------------|--------------|--------------|--------------|
| Starter på ny linje? | ✅ Ja  | ❌ Nej  | ❌ Nej  |
| Fylder hele containerens bredde? | ✅ Ja  | ❌ Nej  | ❌ Nej  |
| Kan justere bredde og højde? | ✅ Ja  | ❌ Nej  | ✅ Ja  |
| Kan indeholde block-elementer? | ✅ Ja  | ❌ Nej  | ❌ Nej  |
| Kan indeholde inline-elementer? | ✅ Ja  | ✅ Ja  | ✅ Ja  |

---

## 6. Ændring af Display-egenskaber

Man kan ændre et elements standard-display med CSS:
```css
div {
    display: inline;
}
span {
    display: block;
}
```

**Eksempel:**
```html
<p style="display: inline-block; width: 100px; height: 50px; background: pink;">Inline-block</p>
```
> **Bemærk:** Elementer som `<img>` og `<button>` har **inline-block** som standard.

---

## 7. Konklusion

- **Normal Flow** er standard-layoutet i en browser.
- **Block-elementer** starter på en ny linje og fylder hele bredden.
- **Inline-elementer** ligger på samme linje og fylder kun indholdets bredde.
- **Inline-block-elementer** kombinerer inline-adfærd med muligheden for at justere bredde og højde.
- `display`-egenskaben kan ændre et elements standard-adfærd.
