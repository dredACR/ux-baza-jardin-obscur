# Materiał dowodowy audytu

**Serwis:** https://om2r9.weblium.site/

Ekrany 01-06 i 08-09: 14.11.2026. Ekrany 19-39: 15.11.2026. Wymiary w tabeli opisują pliki obrazów; szerokość CSS testu podano oddzielnie w raporcie i danych inspekcji.

| Ekran | Plik | Rozmiar obrazu |
| --- | --- | --- |
| 01 | [home-desktop](screenshots/01-home-desktop.jpg) | 1521 × 776 |
| 02 | [catalog-desktop](screenshots/02-catalog-desktop.jpg) | 1521 × 776 |
| 03 | [product-desktop](screenshots/03-product-desktop.jpg) | 1521 × 776 |
| 04 | [cart-desktop](screenshots/04-cart-desktop.jpg) | 1536 × 783 |
| 05 | [promo-desktop](screenshots/05-promo-desktop.jpg) | 1536 × 783 |
| 06 | [product-mobile](screenshots/06-product-mobile.jpg) | 375 × 811 |
| 08 | [menu-mobile](screenshots/08-menu-mobile.jpg) | 390 × 843 |
| 09 | [catalog-mobile](screenshots/09-catalog-mobile.jpg) | 375 × 811 |
| 19 | [powrot-katalog](screenshots/19-powrot-katalog.jpg) | 1521 × 831 |
| 20 | [koszyk-ilosc-2](screenshots/20-koszyk-ilosc-2.jpg) | 1536 × 839 |
| 21 | [walidacja-formularza](screenshots/21-walidacja-formularza.jpg) | 1536 × 839 |
| 22 | [pagespeed-desktop](screenshots/22-pagespeed-desktop.jpg) | 1905 × 848 |
| 23 | [lighthouse-kontrast](screenshots/23-lighthouse-kontrast.jpg) | 1905 × 848 |
| 24 | [pusty-koszyk](screenshots/24-pusty-koszyk.jpg) | 1536 × 839 |
| 25 | [przycisk-klawiatura](screenshots/25-przycisk-klawiatura.jpg) | 1521 × 831 |
| 26 | [fokus-pole-ilosci](screenshots/26-fokus-pole-ilosci.jpg) | 1521 × 831 |
| 27 | [home-320](screenshots/27-home-320.jpg) | 305 × 858 |
| 28 | [menu-klawiatura-320](screenshots/28-menu-klawiatura-320.jpg) | 320 × 900 |
| 29 | [katalog-320](screenshots/29-katalog-320.jpg) | 305 × 858 |
| 30 | [produkt-320](screenshots/30-produkt-320.jpg) | 305 × 858 |
| 31 | [koszyk-320](screenshots/31-koszyk-320.jpg) | 320 × 900 |
| 32 | [fokus-pod-koszykiem](screenshots/32-fokus-pod-koszykiem.jpg) | 320 × 900 |
| 33 | [produkt-zoom-200](screenshots/33-produkt-zoom-200.jpg) | 753 × 360 |
| 34 | [koszyk-zoom-200](screenshots/34-koszyk-zoom-200.jpg) | 761 × 364 |
| 35 | [home-zoom-200](screenshots/35-home-zoom-200.jpg) | 753 × 360 |
| 36 | [odstepy-tekstowe-320](screenshots/36-odstepy-tekstowe-320.jpg) | 305 × 858 |
| 37 | [odstepy-menu-koszyk](screenshots/37-odstepy-menu-koszyk.jpg) | 305 × 858 |
| 38 | [pagespeed-mobile](screenshots/38-pagespeed-mobile.jpg) | 1425 × 990 |
| 39 | [crux-brak-danych](screenshots/39-crux-brak-danych.jpg) | 1425 × 990 |

## Warunki testów

- Reflow: viewport 320 × 900 CSS px, zoom 100%, domyślne odstępy.
- Powiększenie: rzeczywisty zoom Chrome 200%, zarejestrowany viewport 760 × 364 CSS px.
- Odstępy tekstu: 320 × 900 CSS px, interlinia 1,5×, margines po akapicie 2×, litery 0,12 em, słowa 0,16 em. Po próbie przywrócono ustawienia domyślne.
- Kontrast: kolory wyliczone z DOM i rzeczywistego tła; obliczenie według względnej luminancji WCAG.
- PageSpeed: profile i godziny zapisane w raporcie; wyniki dotyczą strony głównej.

[Inspekcja i powtórne testy](retest-evidence.json) · [Pierwotny zapis home](stan-pierwotny.json)
