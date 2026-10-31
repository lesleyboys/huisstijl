# Lesley Boys huisstijl

Eén bron voor de vormgeving van alle Lesley Boys-sites: lesleyboys.nl, club, clock, stem, socio, fideles, esports en wat er nog bijkomt. Gebaseerd op het brandbook *Corporate Identity Lesley Boys* (Create the Brand, 3 juli 2024), zoals uitgewerkt in club.lesleyboys.nl.

- **Kleuren:** Lesley Boys-blauw `#039ED9`, zwart `#06080B`, wit.
- **Letter:** Work Sans (Google Fonts), gewichten 400–800.
- **Licht en donker:** volgt automatisch de instelling van het apparaat; forceren kan met `data-theme="light"` of `"dark"` op `<html>`.
- **Taglines:** club "Together forward", intranet en esports "Aim for excellence".

## Bestanden

| Bestand | Wat |
| --- | --- |
| `huisstijl.css` | Alles in één bestand: tokens + basis + componenten. Gebruik dit. |
| `tokens.css` | Alleen de kleuren, letter en maten als CSS-variabelen (`--blauw`, `--zwart`, `--f`, `--r` …) |
| `basis.css` | Tekst, links, focus, hulpklassen (`.eyebrow`, `.num`, `.sr-only`) |
| `componenten.css` | `.knop`, `.veld`, `.paginakop`, `.paneel`, `.kaart`, `.chip`, `.stat`, `.tegel`, `.toast` |
| `logo/` | Alle logovarianten als SVG, plus PNG's |
| `brandbook-lesley-boys.pdf` | Het brandbook |
| `voorbeeld.html` | Alle onderdelen op één pagina |

## Gebruiken in een site

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Work+Sans:wght@400;500;600;700;800&display=swap">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/lesleyboys/huisstijl@1/huisstijl.css">
```

De jsDelivr-link werkt alleen als deze repo **openbaar** is (de logo's en kleuren zijn toch al openbaar). Blijft de repo privé, kopieer dan `huisstijl.css` en `logo/` in de site.

Een eigen site past alleen aan wat écht anders is, in een eigen CSS-bestand ná `huisstijl.css`. Nooit de kleuren zelf opnieuw definiëren.

## Nieuwe versie uitbrengen

1. Wijzig de bestanden, controleer `voorbeeld.html`.
2. Commit en maak een tag: `git tag v1.1 && git push --tags`. Sites met `@1` krijgen de nieuwe versie vanzelf (jsDelivr-cache: tot 12 uur).
3. Een wijziging die sites kan breken (een klasse hernoemd) = nieuwe hoofdversie `v2.0`; sites stappen dan zelf over.

## Afspraken

- Gemaakt en beheerd vanuit de GitHub-organisatie `lesleyboys` (eigenaar developer@lesleyboys.nl).
- Het merk Lesley Boys is ondergebracht in Saeta B.V.; twijfel over gebruik van logo of naam → college Merk & communicatie.
