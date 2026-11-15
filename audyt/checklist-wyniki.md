# Wyniki 40 kryteriów UX

**Serwis:** https://om2r9.weblium.site/ · **Daty:** 14-15.11.2026.

**18 PASS / 19 FAIL / 3 NOT_TESTED.** PASS - spełnione w opisanym zakresie; FAIL - potwierdzony problem; NOT_TESTED - brak danych do rozstrzygnięcia. Dla PERF-01-03 powodem jest brak danych terenowych CrUX.

| ID | Kryterium | Status | Dowód, zakres i wynik |
| --- | --- | --- | --- |
| UX-01 | Nazwy i cele nawigacji | PASS | Wszystkie 6 odnośników menu doprowadziło do odpowiednich sekcji; menu mobilne otwiera się klawiaturą. Dane: navigation, mobileMenu; ekran 28. |
| UX-02 | Powrót i orientacja | PASS | Powrót z CARMINE RUSH odtwarza #catalog i widoczną kartę produktu; działają logo i okruszki. Ekran 19; returnContext. |
| UX-03 | Spójny język i przyciski | FAIL | Polska strona prowadzi do angielskich etykiet karty i koszyka; hero FROM 290.99 bez waluty, katalog z podwójnym oznaczeniem. F09; ekrany 01-05. |
| UX-04 | Informacja o zmianie koszyka | PASS | Kliknięcie Dodaj do koszyka aktualizuje licznik i pozycję; ilość 2 daje 79,98 PLN. Ekrany 04, 20; dostępność komunikatu: FORM-06. |
| UX-05 | Korekta koszyka | PASS | Sprawdzono 1 → 2 → 1 sztuka: 39,99 → 79,98 → 39,99 PLN; usunięcie daje pusty koszyk. Ekrany 20, 24; cart. |
| UX-06 | Informacje potrzebne do decyzji | FAIL | Na karcie CARMINE RUSH nie podano pojemności; niejasny punkt odniesienia ceny hero. F13; ekrany 01, 03, 30. |
| UX-07 | Zgodność obietnicy i promocji | FAIL | Reklamowany WINTER15 jest odrzucany dla CARMINE RUSH bez wyjaśnienia warunków. F14; ekran 05; cart.promo. |
| UX-08 | Wiarygodna treść | FAIL | Wprowadzenie katalogu mówi o wspieraniu małych i mikroprzedsiębiorstw zamiast o perfumach. F10; ekrany 02, 29. |
| SEO-01 | Opisowy tytuł strony | FAIL | Tytuł home: Perfumes Store Website Template Demo. F11; stan-pierwotny.json: title. |
| SEO-02 | Opis w metadanych | FAIL | Meta description opisuje szablon Weblium zamiast oferty Jardin Obscur. F11; stan-pierwotny.json: description. |
| SEO-03 | Adres opisujący zawartość | FAIL | CARMINE RUSH działa pod /shop/ashen-ember; nazwa i adres nie opisują tego samego zapachu. F12; ekran 03, links. |
| SEO-04 | Nagłówek odpowiada tematowi | PASS | Tekst hero dotyczy zapachów, karta nazywa CARMINE RUSH. Ocena zgodności tematu; struktura nagłówków osobno w VIS-05. Ekrany 01, 03. |
| SEO-05 | Użyteczny tekst dla intencji | FAIL | Tekst wprowadzenia nie odpowiada intencji wyboru perfum. F10; ekrany 02, 29. |
| SEO-06 | Odkrywalne odnośniki | PASS | Link katalog → CARMINE RUSH ma href i otwiera kartę; powrót działa. Ekrany 02, 03, 19; links. Zakres: badane przejście. |
| VIS-01 | Kontrast tekstu | FAIL | In stock: #61A854 na #FBFBFB, 16 px, kontrast 2,80:1 przy progu 4,5:1. F05; productStyles, productBackground, contrastMeasured. |
| VIS-02 | Kontrast elementów i stanów | FAIL | Strzałki ilości: #9199AB na #FBFBFB, kontrast 2,76:1 przy progu 3:1. F06; contrastMeasured. Rozmiar celu oceniono oddzielnie. |
| VIS-03 | Informacja poza kolorem | PASS | Stan dostępności ma tekst In stock, błędy mają treść, pola obowiązkowe gwiazdkę. Sprawdzone stany nie polegają wyłącznie na kolorze. Ekrany 03, 21. |
| VIS-04 | Alternatywy dla obrazów | PASS | Zdjęcie CARMINE RUSH i badane obrazy-linki katalogu mają alternatywy z nazwami produktów. Zakres: obrazy produktów w ścieżce; homeImages i karta 03. |
| VIS-05 | Relacje zapisane w strukturze | FAIL | Wizualny tytuł sekcji bestsellerów jest akapitem, a lista nagłówków zawiera pusty H2. F07; inspekcja struktury home, stan-pierwotny.json: headings. |
| VIS-06 | Język dokumentu | FAIL | Dominująca treść home jest polska, html deklaruje lang=en. F08; stan-pierwotny.json: lang. |
| KEY-01 | Obsługa klawiaturą | FAIL | Fokus dociera do Add to cart, ale Enter i Spacja nie dodają produktu; kliknięcie dodaje. F01; ekran 25; keyboardActivation. |
| KEY-02 | Wyjście z komponentu | PASS | Menu otwarto Enterem i zamknięto Enterem na przycisku Close. Koszyk zamyka Esc. Sam Esc nie zamyka menu. Ekran 28; mobileMenu. |
| KEY-03 | Widoczny fokus | PASS | W badanej sekwencji Tab/Shift+Tab widoczny fokus na linkach i przyciskach; pole ilości otrzymuje kursor edycji. Ekrany 25-26; keyboard, quantityFocus. |
| KEY-04 | Fokus nie jest całkowicie zasłonięty | FAIL | Przy otwartym koszyku Tab przechodzi do linku Weblium pod panelem; element jest całkowicie zasłonięty. F02; ekran 32; modalFocus. |
| KEY-05 | Nazwa, rola i stan | FAIL | Kontrolki filtra ceny bez wyliczonych nazw; także pola koszyka mają puste nazwy dostępne. F04; inspekcja dostępności i forms; ekran 21. |
| KEY-06 | Widoczna etykieta w nazwie | FAIL | CTA Znajdź swój zapach ma nazwę Go to block; Kup teraz ma nazwę Add to cart. F03; ekran 01, homeImages. |
| FORM-01 | Widoczne etykiety i instrukcje | PASS | Widoczne podpisy Name, Email, Phone, Comment; gwiazdki oznaczają 3 wymagane pola. Komentarz opcjonalny. Ekrany 21, 31; formsAfterValidation. |
| FORM-02 | Programowe powiązanie pola z nazwą | FAIL | Widoczne podpisy nie są powiązane z polami; brak label/id, aria-label i aria-labelledby; nazwy w drzewie dostępności są puste. F04; forms. |
| FORM-03 | Tekstowa identyfikacja błędu | PASS | Po pustej próbie Buy błędy tekstowe wskazują Name, Email i Phone, pola mają aria-invalid=true; komunikaty role=alert. Ekran 21; formsAfterValidation. |
| FORM-04 | Pomoc w poprawieniu błędu | PASS | Dla brakującego imienia oraz błędnego e-maila/telefonu komunikaty wskazują potrzebną korektę. Zakres: walidacja danych kontaktowych. Ekran 21. |
| FORM-05 | Tylko uzasadnione pola obowiązkowe | PASS | Wymagane są dane kontaktowe Name, Email, Phone; Comment ma required=false i nie generuje widocznego błędu. Ekran 21; formsAfterValidation. |
| FORM-06 | Dostępny komunikat o zmianie | FAIL | Dodanie produktu zmienia wizualny licznik koszyka bez regionu status/live i bez przeniesienia fokusu do komunikatu. F16; live, keyboardActivation. |
| RWD-01 | Reflow | PASS | Przy 320 × 900 CSS px home, katalog, karta i pola koszyka pozostają dostępne w układzie pionowym. Ekrany 27-31; reflow. Domyślne odstępy. |
| RWD-02 | Powiększenie tekstu | PASS | Rzeczywisty zoom Chrome 200%: home, karta i koszyk zachowują treść i kontrolki. Ekrany 33-35; zoom. Nie zastąpiono zoomu zmianą rozmiaru obrazu. |
| RWD-03 | Zmiana odstępów tekstu | FAIL | Po zmianie 4 odstępów tekstu przy 320 px licznik koszyka przykrywa przycisk menu; kliknięcie otwiera koszyk. F15; ekrany 36-37; spacing. |
| RWD-04 | Rozmiar celu wskaźnika | PASS | Zmierzone cele: menu 40 × 40, social 30 × 30 CSS px. Strzałki 10 × 6 mają równoważne pole ilości 39,4 × 26,4; zastosowano wyjątek równoważnej kontrolki. productStyles. |
| PERF-01 | Ładowanie głównej treści | NOT_TESTED | Brak danych CrUX do oceny terenowego LCP w 75. percentylu. Lab: mobile 50,9 s, desktop 2,7 s. Ekrany 38-39; nie zastępują wyniku terenowego. |
| PERF-02 | Reakcja na interakcję | NOT_TESTED | Brak terenowego INP i próby użytkowników. TBT lab 610/260 ms służy diagnostyce, nie jest INP. Ekran 39; pagespeed. |
| PERF-03 | Stabilność układu | NOT_TESTED | Brak terenowego CLS. W pojedynczych próbach lab: mobile 0, desktop 0,025. Ekrany 38-39; brak podstaw do oceny 75. percentyla. |
| PERF-04 | Rzetelność pomiaru | PASS | Zapisano datę, profile, Lighthouse 13.6.0, wyniki lab i brak CrUX; nieudana pierwsza próba mobile NO_FCP została odrzucona. Ekrany 22, 38-39; pagespeed. |

Dane techniczne: retest-evidence.json i stan-pierwotny.json. Numery ekranów odpowiadają plikom w screenshots/.
