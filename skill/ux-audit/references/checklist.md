# Kryteria audytu UX — wersja 1.0

Źródła sprawdzono 14.11.2026. Zachowaj wszystkie **40** ID w wynikach. Statusy: PASS = sprawdzono i spełniono w opisanym zakresie; FAIL = potwierdzony problem; NOT_TESTED = brak testu/danych; NA = nie dotyczy, z uzasadnieniem.

WCAG A/AA oznacza wskazane kryterium [normatywnego standardu](https://www.w3.org/TR/WCAG22/); Understanding objaśnia je. Pozostałe pozycje są zaleceniami, celami jakościowymi lub testami autorskimi. Zestaw nie wyczerpuje WCAG.

## Nawigacja i zakup — testy autorskie

Podstawa inspirująca: [heurystyki Nielsena](https://www.nngroup.com/articles/ten-usability-heuristics/). Operacjonalizacja poniżej jest własną checklistą dla sklepu.

| ID | Sprawdź i udokumentuj |
| --- | --- |
| UX-01 | Otwórz każdą pozycję menu; porównaj jej nazwę z rzeczywistym celem. |
| UX-02 | Wróć z produktu do kategorii i home; oceń orientację oraz zachowanie kontekstu. |
| UX-03 | Porównaj język i nazwy działań w katalogu, karcie oraz koszyku; wypisz niespójności. |
| UX-04 | Dodaj produkt; sprawdź informację o zmianie i zgodność pozycji koszyka. |
| UX-05 | Zmień ilość i usuń pozycję; porównaj sumę, zamknij koszyk i wróć do listy. |
| UX-06 | Odszukaj nazwę, cenę/walutę, pojemność, dostępność, rodzaj i opis produktu; sprawdź warianty, jeśli istnieją. |
| UX-07 | Porównaj reklamowaną promocję, widoczne warunki i działanie kodu w kwalifikującym się koszyku. |
| UX-08 | Wyszukaj teksty obcej branży i niepotwierdzone obietnice; oddziel demonstracyjne opinie od zweryfikowanych. |

## Treść i SEO — zalecenia

| ID | Warunek i test | Źródło |
| --- | --- | --- |
| SEO-01 | Porównaj `title` z treścią każdej badanej podstrony; usuń tytuły szablonu. Brak uniwersalnego limitu 60 znaków. | [Google](https://developers.google.com/search/docs/appearance/title-link) |
| SEO-02 | Sprawdź trafny meta description; Google może wybrać inny snippet. | [Google](https://developers.google.com/search/docs/appearance/snippet) |
| SEO-03 | Porównaj nazwę z URL; adres nie powinien sugerować innego produktu. Zmianę istniejącego adresu planuj z przekierowaniem. | [Google](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) |
| SEO-04 | Główny nagłówek opisuje temat; nie traktuj liczby H1 jako samodzielnego testu zgodności. | [Google](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) |
| SEO-05 | Tekst odpowiada intencji i opisuje faktyczną ofertę; brak upychania fraz oraz wymyślonych parametrów. | [Google](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) |
| SEO-06 | Ważne podstrony mają odnośniki `a` z poprawnym `href`; tekst wyjaśnia cel. | [Google](https://developers.google.com/search/docs/crawling-indexing/links-crawlable) |

## Warstwa wizualna i struktura — WCAG

| ID | Kryterium i test | Źródło |
| --- | --- | --- |
| VIS-01 | 1.4.3 AA: kontrast tekstu ≥4,5:1, dużego ≥3:1. Duży: ≥24 CSS px lub ≥18,67 px bold. Uwzględnij wyjątki, np. logo. Zmierz kolory. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) |
| VIS-02 | 1.4.11 AA: istotna informacja wizualna kontrolki/stanu/grafiki ≥3:1 z sąsiednim kolorem; sprawdź wyjątki, m.in. stan nieaktywny. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html) |
| VIS-03 | 1.4.1 A: kolor nie jest jedyną wizualną informacją; zbadaj błędy i warianty. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html) |
| VIS-04 | 1.1.1 A: istotne obrazy mają równoważne alternatywy; dekoracje są pomijane; nazwa ikony opisuje czynność. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html) |
| VIS-05 | 1.3.1 A: porównaj wizualne relacje z semantyką nagłówków, list i grup. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/info-and-relationships.html) |
| VIS-06 | 3.1.1 A: język dokumentu można ustalić programowo; porównaj np. `lang` z dominującą treścią. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/language-of-page.html) |

## Klawiatura i komponenty — WCAG

| ID | Kryterium i test | Źródło |
| --- | --- | --- |
| KEY-01 | 2.1.1 A: wykonaj funkcje klawiaturą; wyjątek dotyczy istotnego toru ruchu, nie zwykłego przycisku. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/keyboard.html) |
| KEY-02 | 2.1.2 A: opuść komponent klawiaturą; modal z dostępnym zamknięciem nie jest automatycznie pułapką. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/no-keyboard-trap.html) |
| KEY-03 | 2.4.7 AA: fokus jest widoczny podczas tabulacji; zachowaj zrzut. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/focus-visible.html) |
| KEY-04 | 2.4.11 AA: fokusowany element nie jest całkowicie ukryty przez treść autora; uwzględnij uwagi standardu. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/focus-not-obscured-minimum.html) |
| KEY-05 | 4.1.2 A: sprawdź rzeczywistą dostępną nazwę, rolę i stany kontrolek. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value.html) |
| KEY-06 | 2.5.3 A: dostępna nazwa zawiera widoczną etykietę tekstową; porównaj oba ciągi. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/label-in-name.html) |

## Formularze

| ID | Kryterium i test | Źródło |
| --- | --- | --- |
| FORM-01 | 3.3.2 A: pola wymagające danych mają etykiety lub instrukcje; sprawdź jasność wymagań. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/labels-or-instructions.html) |
| FORM-02 | 4.1.2 A: sprawdź programową nazwę pola. Sąsiedni napis nie dowodzi powiązania; brak `id` nie dowodzi braku nazwy. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value.html) |
| FORM-03 | 3.3.1 A: wykryty błąd wskazuje pole i jest opisany tekstem. Testuj bez tworzenia prawdziwego zamówienia. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/error-identification.html) |
| FORM-04 | 3.3.3 AA: podaj znaną sugestię poprawy, z wyjątkiem zagrożenia bezpieczeństwa lub celu treści. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/error-suggestion.html) |
| FORM-05 | Zalecenie: uzasadnij każde obowiązkowe pole, szczególnie komentarz; brak uniwersalnego limitu pól WCAG. | [WAI](https://www.w3.org/WAI/tutorials/forms/) |
| FORM-06 | 4.1.3 AA: status bez przejęcia fokusu jest programowo dostępny; sprawdź live region/role i możliwy odczyt. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html) |

## Responsywność — WCAG

| ID | Kryterium i test | Źródło |
| --- | --- | --- |
| RWD-01 | 1.4.10 AA: pionowa treść przy odpowiedniku 320 CSS px bez utraty funkcji i przewijania w dwóch wymiarach; wyjątek dla części wymagających układu 2D. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html) |
| RWD-02 | 1.4.4 AA: powiększ tekst do 200%; sprawdź utratę treści/funkcji. Uwzględnij wyjątki napisów i obrazów tekstu. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html) |
| RWD-03 | 1.4.12 AA: równocześnie ustaw interlinię 1,5×, odstęp po akapicie 2×, litery 0,12×, słowa 0,16× fontu; brak utraty treści/funkcji. To test odporności, nie domyślny styl. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html) |
| RWD-04 | 2.5.8 AA: cel ≥24×24 CSS px lub wyjątek: odstępy, odpowiednik, inline, kontrolka przeglądarki, istotna prezentacja. Dla odstępów sprawdź okręgi średnicy 24 px. 44×44 to odrębne AAA. | [W3C](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html) |

## Wydajność — cele jakościowe

Źródło: [web.dev Web Vitals](https://web.dev/articles/vitals). Zapisz narzędzie, datę, URL/origin, okres i rodzaj danych. Progi dotyczą 75. percentyla rzeczywistych odsłon, osobno mobile/desktop. Brak danych terenowych = NOT_TESTED dla progu terenowego.

| ID | Test |
| --- | --- |
| PERF-01 | Odczytaj terenowy LCP, cel ≤2,5 s. |
| PERF-02 | Odczytaj terenowy INP, cel ≤200 ms; nie zastępuj go TBT. |
| PERF-03 | Odczytaj terenowy CLS, cel ≤0,1. |
| PERF-04 | Oddziel dane terenowe od laboratoriów; jeden Lighthouse nie opisuje wszystkich użytkowników. |
