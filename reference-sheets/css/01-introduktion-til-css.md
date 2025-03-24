# CSS Cheat Sheet

## Hvad er CSS?
CSS (Cascading Style Sheets) bruges til at styre udseendet og layoutet af en HTML-side. Med CSS kan du:
- Ændre farver, skrifttyper og baggrunde
- Styre layoutet af elementer (f.eks. marginer, padding, flexbox, grid)
- Tilføje animationer og overgange
- Gøre hjemmesider responsive (tilpasse sig forskellige skærmstørrelser)

## Måder at linke CSS til en HTML-side

### 1. **Ekstern CSS** (Anbefalet)
Du kan linke en ekstern CSS-fil til din HTML-side ved at bruge `<link>`-tagget i `<head>`-sektionen - som i Line 7 herunder:

```html
<!DOCTYPE html>
<html lang="da">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Min Webside</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Hello World!</h1>
</body>
</html>
```

Fordele:
- Holder HTML og CSS adskilt (bedre struktur)
- Nem at genbruge CSS på flere sider
- Bedre ydeevne (CSS kan caches af browseren)

### 2. **Intern CSS**
Du kan skrive CSS direkte i din HTML-fil inden for `<style>`-tagget i `<head>`:

```html
<head>
    <style>
        body {
            background-color: lightblue;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
```

Fordele:
- Godt til små projekter eller hurtige ændringer

Ulemper:
- Bliver rodet, hvis der er meget CSS
- Sværere at genbruge på flere sider

### 3. **Inline CSS**
CSS kan også tilføjes direkte til et HTML-element ved hjælp af `style`-attributten:

```html
<h1 style="color: red; font-size: 24px;">Hej Verden!</h1>
```

Fordele:
- Hurtigt at anvende på enkelte elementer

Ulemper:
- Svært at vedligeholde i større projekter
- Mindre fleksibelt end eksterne og interne CSS-metoder

---

Brug altid **ekstern CSS**, når det er muligt, for bedre organisering og vedligeholdelse af din kode!
