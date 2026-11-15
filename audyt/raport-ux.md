# Jardin Obscur - audyt UX

**Serwis:** https://om2r9.weblium.site/  
**Daty:** 14-15 listopada 2026 r.  
**Metoda:** przegląd ekspercki, test ścieżki zakupowej, inspekcja struktury i dostępności oraz pomiary PageSpeed Insights.

## Wyniki

18 PASS, 19 FAIL, 3 NOT_TESTED. Trzy nierozstrzygnięte kryteria dotyczą danych terenowych CrUX, których usługa nie udostępnia dla tej strony. Wynik PASS odnosi się do opisanego zakresu testu.

## Persona i cel

**Anna, 29 lat - persona projektowa.** Kupuje perfumy na prezent, najczęściej na telefonie. Porównuje nuty, pojemność, cenę i dostępność. Chce wybrać zapach, zastosować promocję oraz przygotować koszyk. Potrzebuje spójnych polskich opisów i jasnych warunków zakupu.

**Zakres:** home, 6 celów menu, katalog, karta CARMINE RUSH, koszyk, promocja, walidacja danych kontaktowych, stany pusty/zapełniony, klawiatura, 320 × 900 CSS px, zoom Chrome 200%, odstępy tekstu, wydajność home. Test zakończono przed złożeniem zamówienia.

## Ścieżka i dowody

| Etap | Działanie | Wynik | Ekran |
| --- | --- | --- | --- |
| S01 | Wejście na stronę | Rozpoznanie marki, oferty i głównego CTA. | 01 |
| S02 | Przejście do katalogu | Menu przewija do katalogu; widoczne kategorie i produkty. | 02, 29 |
| S03 | Otwarcie CARMINE RUSH | Cena 39,99 PLN, opis nut, status dostępności; brak pojemności. | 03, 30 |
| S04 | Powrót do listy | Wstecz odtwarza #catalog i pozycję produktu. | 19 |
| S05 | Dodanie jednej sztuki | Kliknięcie aktualizuje licznik i koszyk; Enter/Spacja nie dodają. | 04, 25 |
| S06 | Zmiana ilości | 2 sztuki = 79,98 PLN; powrót do 1 = 39,99 PLN. | 20 |
| S07 | Użycie WINTER15 | Kod jest odrzucany bez wyjaśnienia warunków. | 05 |
| S08 | Walidacja formularza | Pusta próba wskazuje 3 wymagane pola; Comment opcjonalny. | 21 |
| S09 | Usunięcie produktu | Pojawia się pusty koszyk. | 24 |
| S10 | Menu i koszyk na telefonie | Domyślne 320 px działa; Tab w koszyku przechodzi pod panel. | 27-32 |
| S11 | Powiększenie i odstępy | Zoom 200% zachowuje treść; zwiększone odstępy zasłaniają menu. | 33-37 |
| S12 | Szybkość wejścia | PageSpeed desktop i mobile, sprawdzenie dostępności CrUX. | 22, 38-39 |

## Problemy i poprawki

Skala: 1 - kosmetyka; 2 - utrudnienie z obejściem; 3 - poważna przeszkoda; 4 - blokada celu w badanych warunkach.

### F01 - Dodanie do koszyka nie działa klawiaturą

**Waga 4 | KEY-01 | Dowody: 25; keyboardActivation**

Na karcie CARMINE RUSH przejście Tab ustawia fokus na Add to cart. Enter i Spacja nie zmieniają licznika (0); kliknięcie tej samej kontrolki dodaje produkt (1). Blokuje to zakup osoby korzystającej wyłącznie z klawiatury.

**Poprawka:** Użyć natywnego button albo obsłużyć Enter i Spację wraz z zapobieganiem przewinięciu. Zachować widoczny fokus.

**Test akceptacji:** Po każdej aktywacji Enterem lub Spacją koszyk otrzymuje jedną sztukę; mysz działa tak samo.

### F02 - Fokus przechodzi pod otwarty koszyk

**Waga 3 | KEY-04 | Dowody: 32; modalFocus**

Przy szerokości 320 px Tab przenosi fokus na link Weblium za panelem koszyka. Jego obszar jest całkowicie zasłonięty; użytkownik traci informację o położeniu fokusu.

**Poprawka:** Po otwarciu przenieść fokus do koszyka, wyłączyć interakcję z tłem i utrzymać logiczną sekwencję wewnątrz panelu. Po zamknięciu przywrócić fokus.

**Test akceptacji:** Tab i Shift+Tab przy otwartym koszyku nie przechodzą do zasłoniętych elementów tła.

### F03 - Nazwa dostępna pomija widoczny tekst CTA

**Waga 3 | KEY-06 | Dowody: 01; homeImages; drzewo dostępności**

Widoczne Znajdź swój zapach ma nazwę Go to block, a Kup teraz w katalogu ma nazwę Add to cart. Polecenie głosowe oparte na widocznym tekście może nie wskazać kontrolki.

**Poprawka:** Usunąć ogólne aria-label nadpisujące tekst albo nadać nazwę zawierającą pełną widoczną etykietę.

**Test akceptacji:** Wyliczona nazwa każdego badanego CTA zawiera jego widoczny tekst w tej samej kolejności.

### F04 - Brak programowych nazw pól i filtra ceny

**Waga 3 | FORM-02, KEY-05 | Dowody: 21; forms; inspekcja filtra**

Podpisy formularza są widoczne, lecz pola Name, Email, Phone i Comment nie mają powiązanych label ani alternatywnych nazw ARIA; wyliczone nazwy są puste. Nazw brakuje także kontrolkom zakresu ceny.

**Poprawka:** Połączyć label[for] z unikalnym id każdego pola. Nadać rozróżnialne nazwy minimum i maksimum ceny oraz udostępnić bieżące wartości.

**Test akceptacji:** Drzewo dostępności wskazuje nazwę, rolę i wartość każdej kontrolki, również po wystąpieniu błędu.

### F05 - Zbyt niski kontrast informacji o dostępności

**Waga 2 | VIS-01 | Dowody: 03; productStyles; productBackground; contrastMeasured**

In stock ma kolor #61A854 na tle #FBFBFB przy rozmiarze 16 px. Kontrast 2,80:1 jest niższy od 4,5:1 dla zwykłego tekstu; status jest trudniejszy do odczytania.

**Poprawka:** Przyciemnić tekst statusu, zachowując jasne tło i tekstową informację o dostępności.

**Test akceptacji:** Pomiar końcowej pary kolorów daje co najmniej 4,5:1.

### F06 - Strzałki ilości mają zbyt niski kontrast

**Waga 2 | VIS-02 | Dowody: 03, 26; contrastMeasured; productStyles**

Ikony zwiększenia i zmniejszenia ilości mają #9199AB na #FBFBFB. Zmierzony kontrast 2,76:1 jest niższy od 3:1; ikony są słabo rozpoznawalne.

**Poprawka:** Przyciemnić ikony i zapewnić czytelne stany interakcji. Dla wygody można również powiększyć ich obszar.

**Test akceptacji:** Kontrast niezbędnej grafiki względem tła wynosi co najmniej 3:1. Rozmiar ocenić z uwzględnieniem równoważnego pola ilości.

### F07 - Wizualny tytuł sekcji nie jest nagłówkiem

**Waga 1 | VIS-05 | Dowody: stan-pierwotny.json: headings; inspekcja home**

Tytuł bestsellerów zapisano jako akapit; lista nagłówków pomija tę sekcję i zawiera pusty H2. Osoba nawigująca nagłówkami nie otrzymuje pełnej mapy treści.

**Poprawka:** Nadać tytułom sekcji właściwe znaczniki nagłówków i usunąć pusty H2. Główny nagłówek powinien opisywać ofertę.

**Test akceptacji:** Lista nagłówków obejmuje wszystkie sekcje w logicznej kolejności i nie ma pustych pozycji.

### F08 - Niewłaściwy język dokumentu

**Waga 2 | VIS-06 | Dowody: stan-pierwotny.json: lang**

Polska strona główna deklaruje html lang=en. Technologia wspomagająca może zastosować niewłaściwą wymowę.

**Poprawka:** Ustawić lang=pl dla polskich stron i właściwie oznaczyć rzeczywiste fragmenty obcojęzyczne.

**Test akceptacji:** Deklaracja języka opublikowanego dokumentu odpowiada dominującej treści.

### F09 - Niespójny język i zapis cen

**Waga 2 | UX-03 | Dowody: 01-05, 21, 29**

Polski katalog prowadzi do angielskiej karty, koszyka i komunikatów. Hero podaje FROM 290.99 bez waluty; katalog łączy zł i PLN. Zwiększa to wysiłek przy porównywaniu oferty.

**Poprawka:** Ujednolicić polskie etykiety i komunikaty. Stosować zapis 39,99 zł; cenę od powiązać z konkretną dostępną ofertą.

**Test akceptacji:** W ścieżce produkt → koszyk → walidacja język jest spójny, a cena ma jednoznaczną walutę i punkt odniesienia.

### F10 - Wprowadzenie katalogu opisuje inną branżę

**Waga 2 | UX-08, SEO-05 | Dowody: 02, 29; stan-pierwotny.json: text**

Tekst Produkujemy wszelkiego rodzaju produkty wspierające małe i mikroprzedsiębiorstwa nie wyjaśnia oferty perfum ani sposobu wyboru zapachu.

**Poprawka:** Zastąpić tekst opisem katalogu: rodzin zapachowych, nut i dostępnych parametrów produktów.

**Test akceptacji:** Wprowadzenie pomaga wybrać perfumy i odpowiada ofercie widocznej w katalogu.

### F11 - Tytuł i opis strony dotyczą szablonu

**Waga 2 | SEO-01, SEO-02 | Dowody: stan-pierwotny.json: title, description**

Title to Perfumes Store Website Template Demo, a meta description promuje szablon Weblium. Nazwa marki i oferta nie są właściwie opisane w metadanych.

**Poprawka:** Wpisać tytuł Jardin Obscur - perfumy i kompozycje zapachowe oraz zwięzły opis rzeczywistej oferty.

**Test akceptacji:** Opublikowane title i description opisują sklep i nie zawierają treści promującej szablon.

### F12 - Adres karty nie odpowiada nazwie produktu

**Waga 2 | SEO-03 | Dowody: 03; stan-pierwotny.json: links**

CARMINE RUSH otwiera się pod /shop/ashen-ember. Rozbieżność utrudnia rozpoznanie produktu po adresie i udostępnianie poprawnego odnośnika.

**Poprawka:** Nadać karcie opisowy adres zgodny z nazwą, zaktualizować linki wewnętrzne i przekierować stary URL.

**Test akceptacji:** Nowy i stary odnośnik prowadzą do CARMINE RUSH; brak błędu i przekierowania do innego produktu.

### F13 - Brakuje pojemności produktu

**Waga 2 | UX-06 | Dowody: 03, 30**

Na karcie CARMINE RUSH nie znaleziono pojemności. Użytkownik zna cenę, ale nie może porównać ilości produktu przed dodaniem.

**Poprawka:** Podać rzeczywistą pojemność przy nazwie lub cenie. Jeśli występują warianty, pokazać ich parametry, ceny i dostępność.

**Test akceptacji:** Pojemność wybranej wersji jest widoczna na karcie oraz identyfikowalna w koszyku.

### F14 - Kod WINTER15 nie realizuje widocznej obietnicy

**Waga 3 | UX-07 | Dowody: 05; cart.promo**

Po dodaniu CARMINE RUSH za 39,99 PLN kod WINTER15 zwraca Promo code can't be applied. Ścieżka nie wyjaśnia przyczyny ani warunków uzyskania reklamowanych 15%.

**Poprawka:** Sprawdzić aktywność i zakres kodu. Warunki pokazać przy promocji, a przy odmowie podać konkretną przyczynę. Usunąć nieaktualną obietnicę.

**Test akceptacji:** Koszyk spełniający opublikowane warunki otrzymuje 15% rabatu; pozostałe przypadki mają czytelne wyjaśnienie.

### F15 - Po zwiększeniu odstępów koszyk zasłania menu

**Waga 3 | RWD-03 | Dowody: 36-37; spacing.menu, spacing.overlap**

Przy 320 px i zwiększonych odstępach tekstu licznik koszyka przykrywa środek przycisku menu (x=261, y=101). Kliknięcie otwiera koszyk, nie nawigację. Po przywróceniu odstępów menu działa.

**Poprawka:** Pozwolić nagłówkowi rosnąć i zawijać treść bez nakładania kontrolek; rozdzielić obszary menu i koszyka.

**Test akceptacji:** Przy jednoczesnych ustawieniach 1,5 / 2 / 0,12 / 0,16 em menu oraz koszyk są osobno dostępne wskaźnikiem i klawiaturą.

### F16 - Zmiana koszyka nie ma komunikatu statusu

**Waga 2 | FORM-06 | Dowody: 04, 20; live; keyboardActivation**

Po dodaniu produktu aktualizuje się wizualny licznik. Nie ma dla tej zmiany regionu status/live ani przeniesienia fokusu do komunikatu; istniejące alerty formularza nie ogłaszają dodania.

**Poprawka:** Dodać zwięzły komunikat role=status, np. Dodano CARMINE RUSH do koszyka. Aktualizować go po dodaniu oraz zmianie ilości.

**Test akceptacji:** Zmiana koszyka ma programowo dostępny komunikat bez konieczności przenoszenia fokusu; potwierdzić odsłuch czytnikiem.

### F17 - Wolne wyświetlenie głównej treści w próbie mobilnej

**Waga 3 | PERF-04 - diagnostyka laboratoryjna | Dowody: 22, 38-39; pagespeed**

PageSpeed mobile: 55/100, LCP 50,9 s, TBT 610 ms, transfer 41 421 KiB. Desktop: 74/100 i LCP 2,7 s. Próba mobilna wskazuje ryzyko długiego oczekiwania na główną treść.

**Poprawka:** Zoptymalizować obrazy i ich warianty, priorytet zasobu LCP oraz zbędny CSS i skrypty. Powtórzyć pomiary w tych samych profilach.

**Test akceptacji:** Powtórzone próby wykazują spadek czasu LCP i transferu. Ocenę terenowych CWV wykonać po uzyskaniu danych użytkowników.

## Kolejność poprawek

1. Przywrócić dodawanie klawiaturą, poprawić fokus koszyka i etykiety kontrolek: F01-F04.
2. Usunąć nakładanie menu po zmianie odstępów i wyjaśnić promocję: F15, F14.
3. Poprawić kontrast, język, treść, dane produktu, metadane i status koszyka: F05-F13, F16.
4. Ograniczyć transfer i powtórzyć pomiary wydajności: F17.

## Pomiary wydajności

15.11.2026, PageSpeed Insights, Lighthouse 13.6.0, pojedyncze pomiary laboratoryjne przy zimnym ładowaniu. Mobile: Moto G Power / Slow 4G, godz. 12:22 GMT+2. Desktop: profil komputerowy, godz. 12:01 GMT+2.

| Metryka | Mobile | Desktop |
| --- | --- | --- |
| Performance | 55/100 | 74/100 |
| FCP | 1,5 s | 0,3 s |
| LCP | 50,9 s | 2,7 s |
| TBT | 610 ms | 260 ms |
| CLS | 0 | 0,025 |
| Speed Index | 5,2 s | 1,6 s |

Pierwszy pomiar mobile zakończył się NO_FCP i został pominięty. Brak danych CrUX uniemożliwia rozstrzygnięcie terenowego LCP, INP i CLS w 75. percentylu. TBT nie jest INP.

[Pomiar desktop](https://pagespeed.web.dev/analysis/https-om2r9-weblium-site/fxgh9wyj4r?form_factor=desktop) · [Pomiar mobile](https://pagespeed.web.dev/analysis/https-om2r9-weblium-site/82z2vgomtd?form_factor=mobile)

## Checklista i źródła

[Wyniki wszystkich 40 kryteriów](checklist-wyniki.md) · [Baza wiedzy](https://github.com/dredACR/ux-baza-jardin-obscur) · [WCAG 2.2](https://www.w3.org/TR/WCAG22/) · [Google SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) · [Web Vitals](https://web.dev/articles/vitals)
