# Warstwa wizualna, semantyka i język

[Mapa wiedzy](../README.md) · [Checklista](../checklist.md)

## VIS-01 — Kontrast tekstu

**Podstawa:** WCAG 1.4.3, AA. **Kryterium:** co najmniej 4,5:1 dla zwykłego tekstu; 3:1 dla dużego tekstu (od 18 pt, czyli 24 CSS px, lub od 14 pt bold, czyli ok. 18,67 CSS px). Standard przewiduje wyjątki, m.in. logotypy i nieaktywne elementy.

**Test:** zmierz rzeczywiste kolory tekstu i tła; dla zdjęcia sprawdź najgorszy fragment pod tekstem. Zapisz parę kolorów, rozmiar, wagę i wynik. Zrzut ekranu sam nie dowodzi wartości kontrastu.

**Źródło:** [W3C: Contrast Minimum](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html).

## VIS-02 — Kontrast elementów i stanów

**Podstawa:** WCAG 1.4.11, AA. **Kryterium:** informacje wizualne konieczne do rozpoznania kontrolki/stanu oraz istotne części grafiki mają kontrast minimum 3:1 z sąsiednimi kolorami. Wyjątki obejmują m.in. nieaktywne kontrolki i niezmodyfikowany wygląd kontrolki przeglądarki.

**Test:** zmierz np. granicę pola, zaznaczenie wariantu i istotną ikonę. Nie wymagaj mechanicznie kontrastowej ramki każdego przycisku, gdy inna informacja wystarcza do jego rozpoznania.

**Źródło:** [W3C: Non-text Contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html).

## VIS-03 — Informacja poza kolorem

**Podstawa:** WCAG 1.4.1, A. **Kryterium:** kolor nie jest jedynym wizualnym nośnikiem informacji.

**Test:** sprawdź błędy formularza, warianty i stany dostępności. Czy oprócz czerwieni/zieleni istnieje tekst, symbol lub inny wyróżnik? Zapisz konkretny stan. Symulacja zaburzeń widzenia kolorów pomaga w ocenie, ale nie zastępuje sprawdzenia komunikatu.

**Źródło:** [W3C: Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html).

## VIS-04 — Alternatywy dla obrazów

**Podstawa:** WCAG 1.1.1, A. **Kryterium:** istotny obraz ma odpowiednik tekstowy realizujący ten sam cel; dekoracja jest pomijana przez technologie wspomagające.

**Test:** odczytaj alternatywy zdjęć produktu i nazwy obrazów będących linkami. Czy informują o produkcie/celu? Dla dekoracji sprawdź np. pusty `alt`, nie opis każdego ornamentu. Funkcjonalna ikona potrzebuje nazwy czynności, a nie opisu kształtu.

**Źródło:** [W3C: Non-text Content](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html).

## VIS-05 — Relacje zapisane w strukturze

**Podstawa:** WCAG 1.3.1, A. **Kryterium:** struktura przekazywana wyglądem jest dostępna programowo lub tekstowo.

**Test:** porównaj widoczny podział z nagłówkami, listami, grupami formularza i tabelami w drzewie dostępności/DOM. Nagłówek wyglądający jak zwykły akapit może utrudniać nawigację. Liczba H1 sama w sobie nie rozstrzyga wyniku kryterium.

**Źródło:** [W3C: Info and Relationships](https://www.w3.org/WAI/WCAG22/Understanding/info-and-relationships.html).

## VIS-06 — Język dokumentu

**Podstawa:** WCAG 3.1.1, A. **Kryterium:** dominujący język strony można ustalić programowo.

**Test:** sprawdź deklarację języka, np. `html lang="pl"`, i porównaj z treścią. Zapisz wynik dla każdej badanej podstrony. Sam fakt występowania angielskich nazw produktów nie oznacza błędnego języka dokumentu; spójność tłumaczeń ocenia UX-03.

**Źródło:** [W3C: Language of Page](https://www.w3.org/WAI/WCAG22/Understanding/language-of-page.html).
