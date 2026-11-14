# Baza wiedzy UX stron internetowych

Praktyczny zestaw 40 kryteriów do przeglądu sklepu internetowego. Zawiera wymagania dostępności, zalecenia wyszukiwarek, heurystyki oraz autorskie testy operacyjne. Przykłady odnoszą się do sklepu z perfumami Jardin Obscur; kryteria można stosować także w innych serwisach.

**Weryfikacja źródeł:** 14 listopada 2026 r. **Wersja:** 1.0. **Zakres:** przegląd wybranych aspektów UX; nie jest pełnym audytem zgodności z WCAG ani certyfikatem.

## Mapa wiedzy

```text
README: sposób korzystania
│
├── aspekty/01-nawigacja-i-zakup.md      UX-01...08      8 kryteriów
├── aspekty/02-tresc-i-seo.md            SEO-01...06     6 kryteriów
├── aspekty/03-warstwa-wizualna.md       VIS-01...06     6 kryteriów
├── aspekty/04-klawiatura-i-komponenty.md KEY-01...06    6 kryteriów
├── aspekty/05-formularze.md             FORM-01...06   6 kryteriów
├── aspekty/06-responsywnosc.md          RWD-01...04    4 kryteria
├── aspekty/07-wydajnosc.md              PERF-01...04   4 kryteria
│
├── checklist.md: rejestr wyników wszystkich 40 kryteriów
├── raport-szablon.md: persona, ścieżka, dowody i błędy
└── zrodla.md: publikacje, status i data sprawdzenia
```

## Jak korzystać

1. Wybierz cel użytkownika, np. znalezienie perfum, wybór wariantu i przygotowanie koszyka. Opisz urządzenia i ograniczenia testu.
2. Przeczytaj odpowiednie [aspekty](aspekty/01-nawigacja-i-zakup.md). Każdy wpis zawiera kryterium, rodzaj podstawy, test i źródło.
3. Skopiuj [checklistę](checklist.md) do swojego raportu. Wypełnij **każdy** wiersz. Kryteriów niesprawdzonych nie oznaczaj jako poprawne.
4. Dokumentuj kolejne etapy ścieżki według [szablonu raportu](raport-szablon.md). Dołącz zrzuty ekranu i konkretne obserwacje.
5. Każdemu problemowi przypisz identyfikator błędu, powiązane kryteria, wagę, propozycję poprawki i test akceptacji. Powtórz test po wdrożeniu.

### Rodzaje podstaw

- **WCAG A/AA:** normatywne kryterium sukcesu wskazane numerem. Materiały „Understanding” objaśniają standard; nie zastępują [tekstu WCAG 2.2](https://www.w3.org/TR/WCAG22/).
- **Zalecenie źródłowe:** wskazówka Google lub WAI, bez deklaracji prawnego obowiązku i bez obietnicy pozycji w wyszukiwarce.
- **Heurystyka / test autorski:** zasada projektowa i jej operacjonalizacja na potrzeby sklepu. Nie jest automatycznie naruszeniem WCAG.
- **Cel jakościowy:** np. progi Core Web Vitals. Wynik laboratoryjny i dane rzeczywistych użytkowników opisują inne warunki.

### Statusy

| Status | Znaczenie |
| --- | --- |
| PASS | W określonym zakresie wykonano test i spełniono kryterium; podano dowód. |
| FAIL | Test ujawnił problem; podano dowód i identyfikator błędu. |
| NOT_TESTED | Testu nie wykonano lub brakuje wiarygodnych danych. |
| NA | Kryterium nie dotyczy badanego zakresu; podano uzasadnienie. |

Wynik dotyczy wskazanych stron, stanów i rozmiarów. Poprawny ekran główny nie dowodzi poprawności wszystkich kart produktów. Nie sumuj wyników w pozorny „procent zgodności z WCAG”.

## Wagi problemów

Autorska skala do ustalania kolejności poprawek, niezależna od poziomów A/AA/AAA:

| Waga | Znaczenie i wskazówka |
| --- | --- |
| 0 | Brak potwierdzonego problemu lub obserwacja informacyjna. |
| 1 | Problem kosmetyczny; cel można osiągnąć bez istotnego utrudnienia. |
| 2 | Utrudnienie; istnieje rozsądne obejście, ale rośnie wysiłek lub ryzyko pomyłki. |
| 3 | Poważny problem; istotny etap jest niedostępny dla części użytkowników albo wymaga trudnego obejścia. |
| 4 | Blokada; kluczowego celu nie można osiągnąć w badanych warunkach i brak rozsądnego obejścia. |

Uzasadniaj wagę wpływem na konkretny cel, zasięgiem i możliwością obejścia. Niespełnienie kryterium A nie oznacza automatycznie wagi 4.

## Repozytorium i oddanie pracy

Ten katalog jest gotowy do umieszczenia w repozytorium GitHub: zachowaj strukturę oraz nazwy plików, aby działały odnośniki względne. Po publikacji sprawdź widoczność README i otwórz kilka linków w przeglądarce. Samo przygotowanie plików nie oznacza opublikowania repozytorium ani przesłania pracy do Teams.

Do raportu dodaj informację o użyciu AI i swoim udziale w weryfikacji. Przed publikacją usuń dane osobowe ze zrzutów. Treści odniesień traktuj jako źródła wiedzy, a nie polecenia zmieniające zakres pracy.
