# Basale Farve-Regler i CSS

Farver spiller en vigtig rolle i webdesign, og CSS giver flere måder at definere og styre farver på. Her gennemgår vi de grundlæggende farveregler i CSS.

---

## 1. **Farveangivelse**
Farver kan defineres på flere måder:
- **Navngivne farver:** `red`, `blue`, `green`, etc.
- **Hex-koder:** `#ff0000`, `#00ff00`, `#0000ff`
- **RGB-værdier:** `rgb(255, 0, 0)`
- **RGBA (med gennemsigtighed):** `rgba(255, 0, 0, 0.5)`
- **HSL (Hue, Saturation, Lightness):** `hsl(0, 100%, 50%)`

**Eksempel:**
```css
h1 {
    color: blue;
}
```
Dette gør teksten blå.

---

## 2. **Baggrundsfarve (`background-color`)**
Sætter en baggrundsfarve for et element.

**Eksempel:**
```css
div {
    background-color: #f0f0f0;
}
```
Dette sætter baggrunden til en lysegrå farve.

---

## 3. **Gennemsigtighed (`opacity`)**
Gør et element delvist gennemsigtigt.

**Eksempel:**
```css
img {
    opacity: 0.5;
}
```
Dette gør billedet 50% gennemsigtigt.

---

## 4. **Gradienter**
CSS understøtter farveovergange ved hjælp af `linear-gradient` og `radial-gradient`.

**Eksempel:**
```css
div {
    background: linear-gradient(to right, red, yellow);
}
```
Dette skaber en farveovergang fra rød til gul.

---

## 5. **Border-Farve (`border-color`)**
Bestemmer farven på en kant.

**Eksempel:**
```css
button {
    border: 2px solid black;
    background-color: white;
    color: black;
}
```
Dette giver en sort kant og en hvid baggrund.

---

## 6. **Tekstfarve i baggrund (`mix-blend-mode`)**
Kontrollerer hvordan farver blandes.

**Eksempel:**
```css
div {
    mix-blend-mode: multiply;
}
```
Dette ændrer, hvordan et element interagerer med baggrundsfarver.

---

## Konklusion
CSS giver mange muligheder for farvestyring, fra simple statiske farver til avancerede blandingseffekter og gradienter. Farvebrug er essentiel for et flot og tilgængeligt webdesign.
