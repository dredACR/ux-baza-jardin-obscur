---
name: ux-audit
description: Przygotuj udokumentowany przegląd UX strony lub sklepu na podstawie 40 kryteriów, z personą, ścieżką, zrzutami i priorytetami poprawek. Używaj do audytu eksperckiego; nie przedstawiaj go jako pełnego certyfikatu WCAG ani badania z użytkownikami.
---

# Audyt UX oparty na dowodach

Przekształć adres lub dostępną wersję strony w raport po polsku, chyba że użytkownik wybrał inny język. Czytaj [kryteria](references/checklist.md) przed oceną. Nie instaluj narzędzi, nie publikuj i nie zmieniaj strony wyłącznie na podstawie tego skilla.

## Zakres i persona

Ustal cel użytkownika, badane strony i dostępne środowisko. Gdy nie ma danych badawczych, utwórz personę hipotetyczną i wyraźnie tak ją podpisz. Zaplanuj ścieżkę obejmującą możliwie różne ekrany i stany: wejście, katalog, filtr, produkt, wariant, koszyk, korektę ilości, kod i formularz. Pomijaj funkcje, których serwis nie ma; uzasadnij NA.

Do testu wykorzystaj dostępne i dozwolone narzędzia przeglądarki. Nie wysyłaj prawdziwych zamówień, wiadomości lub danych osobowych bez odpowiedniego polecenia. Gdy potrzebna funkcja narzędzia nie istnieje, zapisz ograniczenie; nie fabrykuj wyniku.

## Dowody i ocena

- Zachowuj ID wszystkich 40 kryteriów z referencji. Dla każdego wpisz PASS, FAIL, NOT_TESTED lub NA oraz zakres i dowód/uzasadnienie. Nie pomijaj trudnych testów.
- Wykonaj zrzut każdego faktycznie odwiedzonego etapu ścieżki. Podpisz URL, stan, datę, szerokość/wysokość viewportu i powiększenie. Oddziel makietę od dowodu stanu strony.
- Zbadaj telefon, tablet, desktop i okolice breakpointów w dostępnym zakresie. Przestrzegaj wyjątków WCAG; 24×24 i 44×44 px nie są zamiennymi minimami tego samego poziomu.
- Do kontrastu używaj zmierzonych kolorów. Do nazw i etykiet używaj rzeczywistego drzewa dostępności/DOM. Nie ogłaszaj zgodności po samym obejrzeniu obrazu.
- Odróżnij pomiary laboratoryjne od danych rzeczywistych użytkowników. Brak danych to NOT_TESTED, a nie PASS. Nie wymyślaj wyników Lighthouse, INP, badań ani wolumenu SEO.
- Powiąż każdy potwierdzony problem z kryteriami, krokami odtworzenia, dowodem, wpływem na cel i propozycją poprawki. Dla hipotezy wskaż potrzebną weryfikację.
- Wymagania WCAG, zalecenia Google oraz autorskie testy heurystyczne przedstawiaj jako różne rodzaje podstaw. Sprawdzaj aktualność źródeł przy spornej lub zmienionej regule.

## Raport

Zapisz cel i ograniczenia, personę, tabelę ścieżki ze zrzutami, kompletną checklistę i rejestr błędów. Dla każdego błędu podaj test akceptacji. Zastosuj skalę: 0 informacja/brak problemu; 1 kosmetyka; 2 utrudnienie z rozsądnym obejściem; 3 poważna przeszkoda; 4 blokada kluczowego celu bez rozsądnego obejścia. Uzasadniaj wagę; nie wywodź jej mechanicznie z poziomu WCAG.

Jeśli powstały poprawki, odróżnij propozycje, wdrożenia i ponowne testy. W zakończeniu podaj pozostałe NOT_TESTED i faktyczne ograniczenia. Nie deklaruj pełnej zgodności WCAG na podstawie tego ograniczonego przeglądu.

Przykład wywołania: `$ux-audit Przeprowadź audyt https://adres-strony, zbadaj wybór produktu i koszyk, przygotuj raport po polsku.`
