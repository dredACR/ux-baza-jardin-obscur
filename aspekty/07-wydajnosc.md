# Wydajność i stabilność

[Mapa wiedzy](../README.md) · [Checklista](../checklist.md)

Podstawa: [Google/web.dev: Web Vitals](https://web.dev/articles/vitals). To cele jakościowe, nie gwarancja pozycji w wyszukiwarce. Dla oceny Core Web Vitals stosuje się 75. percentyl rzeczywistych odsłon, osobno dla mobile i desktop. Przy braku danych terenowych oznacz wynik jako NOT_TESTED i opisz pomiar laboratoryjny oddzielnie.

## PERF-01 — Ładowanie głównej treści

**Kryterium:** LCP ≤ 2,5 s w danych terenowych.

**Test:** odnotuj źródło, okres agregacji, poziom URL/origin, urządzenie i wartość. Nie zastępuj brakującego wyniku URL wynikiem całej domeny bez wyraźnego oznaczenia. Laboratoryjny LCP służy diagnozie konkretnego uruchomienia.

## PERF-02 — Reakcja na interakcję

**Kryterium:** INP ≤ 200 ms w danych terenowych.

**Test:** odczytaj właściwą metrykę i zakres danych. Dodatkowo sprawdź filtry, wybór wariantu i koszyk w realnej sesji. Wynik TBT lub subiektywne „działa szybko” nie są pomiarem INP.

## PERF-03 — Stabilność układu

**Kryterium:** CLS ≤ 0,1 w danych terenowych.

**Test:** zapisz wynik i obserwowane przesunięcia podczas ładowania zdjęć/fontów. Wskazanie przesunięcia na filmie jest materiałem diagnostycznym; nie wyliczaj z niego umownego wyniku CLS.

## PERF-04 — Rzetelność pomiaru

**Kryterium:** raport odróżnia dane terenowe od laboratoryjnych.

**Test:** przy każdym pomiarze podaj narzędzie, datę, badany adres i warunki. Nie nazywaj jednego wyniku Lighthouse oceną wszystkich użytkowników. Brak odpowiedniej próby jest ograniczeniem danych, a nie dowodem wysokiej wydajności.
