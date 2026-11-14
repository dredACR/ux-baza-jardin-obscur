# Formularze i komunikaty

[Mapa wiedzy](../README.md) · [Checklista](../checklist.md)

Nie wysyłaj rzeczywistego zamówienia w ramach przeglądu. Walidację sprawdzaj w środowisku testowym lub w uzgodnionym zakresie. Brak testu wpisz jako NOT_TESTED.

## FORM-01 — Widoczne etykiety i instrukcje

**Podstawa:** WCAG 3.3.2, A. **Kryterium:** przy wymaganym wprowadzaniu danych dostępna jest etykieta lub instrukcja.

**Test:** obejrzyj pola imienia, e-maila, telefonu, kodu i komentarza. Czy wiadomo, czego oczekują, co jest obowiązkowe i jaki format podać? Placeholder znikający podczas pisania może nie wystarczać. Widoczność etykiety nie dowodzi jej powiązania z polem.

**Źródło:** [W3C: Labels or Instructions](https://www.w3.org/WAI/WCAG22/Understanding/labels-or-instructions.html).

## FORM-02 — Programowe powiązanie pola z nazwą

**Podstawa:** WCAG 4.1.2, A; techniki WAI. **Kryterium:** pole ma programowo ustaloną nazwę odpowiadającą jego celowi.

**Test:** sprawdź nazwę pola w drzewie dostępności oraz sposób nadania, np. `label for` + `id`, etykietę obejmującą pole lub `aria-labelledby`. Sam sąsiedni napis nie dowodzi powiązania; brak `id` nie dowodzi automatycznie braku nazwy. Sprawdź faktyczny wynik.

**Źródła:** [W3C: Name, Role, Value](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value.html), [WAI: Forms Tutorial](https://www.w3.org/WAI/tutorials/forms/).

## FORM-03 — Tekstowa identyfikacja błędu

**Podstawa:** WCAG 3.3.1, A. **Kryterium:** automatycznie wykryty błąd jest opisany tekstem i wskazuje błędny element.

**Test:** w bezpiecznym trybie testowym podaj niepoprawny e-mail lub pustą wymaganą wartość. Czy komunikat mówi, które pole wymaga poprawy? Sama czerwona ramka nie wystarcza. Zrzut powinien pokazywać komunikat i pole.

**Źródło:** [W3C: Error Identification](https://www.w3.org/WAI/WCAG22/Understanding/error-identification.html).

## FORM-04 — Pomoc w poprawieniu błędu

**Podstawa:** WCAG 3.3.3, AA. **Kryterium:** jeśli sposób poprawy wykrytego błędu jest znany, użytkownik otrzymuje sugestię, chyba że naruszałaby bezpieczeństwo lub cel treści.

**Test:** oceń komunikat po błędnym adresie e-mail albo kodzie. „Wpisz adres w formacie nazwa@domena.pl” jest użyteczniejsze niż „Błąd”. Nie wymagaj ujawnienia danych konta ani szczegółów obchodzących zabezpieczenia.

**Źródło:** [W3C: Error Suggestion](https://www.w3.org/WAI/WCAG22/Understanding/error-suggestion.html).

## FORM-05 — Tylko uzasadnione pola obowiązkowe

**Podstawa:** zalecenie WAI i test autorski, nie odrębny uniwersalny limit WCAG. **Kryterium:** pole obowiązkowe ma uzasadnienie w danym procesie.

**Test:** dla każdego pola zapisz cel i skutek braku danych. Sprawdź, czy komentarz naprawdę musi być obowiązkowy. Zaproponuj opcjonalność zbędnego pola; nie usuwaj danych potrzebnych do uzgodnionej dostawy.

**Źródło:** [WAI: Forms Tutorial](https://www.w3.org/WAI/tutorials/forms/).

## FORM-06 — Dostępny komunikat o zmianie

**Podstawa:** WCAG 4.1.3, AA. **Kryterium:** komunikaty statusu, które nie otrzymują fokusu, są dostępne technologiom wspomagającym przez odpowiednie role lub właściwości.

**Test:** przy zmianie liczby wyników, dodaniu produktu lub walidacji sprawdź komunikat w drzewie dostępności oraz — jeśli to możliwe — odczyt czytnikiem. Odpowiednie `role="status"` lub live region mogą pomagać; sam wzrost licznika na ekranie nie dowodzi odczytu.

**Źródło:** [W3C: Status Messages](https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html).
