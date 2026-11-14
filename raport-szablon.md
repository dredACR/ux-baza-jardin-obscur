# Raport audytu UX — szablon

**Serwis / wersja:** do uzupełnienia  
**Adresy i data:** do uzupełnienia  
**Autor / wsparcie AI:** do uzupełnienia  
**Przeglądarka, viewporty, zoom, urządzenia:** do uzupełnienia

## Cel i granice

Opisz cel użytkownika i zakres badanych stron. Wyraźnie rozróżnij audyt ekspercki, symulację persony i badanie z rzeczywistymi uczestnikami. Zapisz niedostępne środowiska, brak danych wydajności i niewykonane testy. Nie deklaruj pełnej zgodności WCAG na podstawie tej checklisty.

## Persona

Podaj potrzeby, cel, kontekst, doświadczenie i ograniczenia istotne dla zadania. Jeśli nie przeprowadzono badań, oznacz: **„Persona hipotetyczna — założenie projektowe, nie wynik wywiadów”**. Nie przypisuj fikcyjnej osobie prawdziwych wypowiedzi uczestników.

## Ścieżka i dowody

Planuj ścieżkę tak, by objąć różne ekrany oraz stany, a nie wielokrotnie tę samą stronę. Przykład: home → kategoria → filtr → karta → wariant → koszyk → korekta ilości → kod → formularz → powrót. Dodaj gałąź pustego wyniku, jeżeli funkcja istnieje.

| Etap | Pytanie użytkownika / działanie | URL i stan | Viewport | Wynik obserwowany | Zrzut |
| --- | --- | --- | --- | --- | --- |
| S01 | do uzupełnienia | do uzupełnienia | do uzupełnienia | do uzupełnienia | `screenshots/01-home.jpg` |

Każdy obraz ma podpis, etap, warunki i opis tego, co potwierdza. Przykładowa nazwa w tabeli nie oznacza, że taki plik już istnieje. Zrzuty muszą pochodzić z faktycznie wykonanej sesji; makietę oznacz jako projekt, nie dowód stanu witryny.

## Wyniki wszystkich kryteriów

Wstaw i wypełnij [40 wierszy checklisty](checklist.md). Wynik powinien odsyłać do konkretnego etapu lub pomiaru. Dla częściowo sprawdzonego kryterium rozbij wynik według ekranów i pozostaw niesprawdzony zakres jako NOT_TESTED.

## Rejestr błędów

| Błąd | Kryteria | Dowód i kroki odtworzenia | Wpływ na cel | Waga 0–4 | Proponowana poprawka | Test akceptacji |
| --- | --- | --- | --- | --- | --- | --- |
| B01 | do uzupełnienia | stan początkowy → czynność → wynik | do uzupełnienia | do uzupełnienia | konkretna zmiana | obserwowalny oczekiwany wynik |

Poziomy wag są opisane w [README](README.md#wagi-problemów). Waga dotyczy wpływu, a nie kosztu naprawy. W osobnym polu można podać szacowany wysiłek i kolejność wdrożenia.

## Weryfikacja poprawek

| Błąd | Wersja po zmianie | Powtórzony test | Wynik i nowy dowód |
| --- | --- | --- | --- |
| B01 | do uzupełnienia | do uzupełnienia | NOT_TESTED |

Odróżnij „zaproponowano” od „wdrożono” i „wdrożono” od „ponownie przetestowano”. Zakończ listą ograniczeń, spraw pozostałych do sprawdzenia i linkami do źródeł użytych w argumentacji.
