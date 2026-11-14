# Klawiatura i dostępne komponenty

[Mapa wiedzy](../README.md) · [Checklista](../checklist.md)

## KEY-01 — Obsługa klawiaturą

**Podstawa:** WCAG 2.1.1, A. **Kryterium:** funkcjonalność jest dostępna z klawiatury, poza czynnościami wymagającymi toru ruchu jako istotnej części działania.

**Test:** bez myszy przejdź przez menu, filtr, produkt, wariant i koszyk. Użyj Tab/Shift+Tab, Enter, Space i klawiszy właściwych dla kontrolki. Notuj funkcje niedostępne; sam fakt otrzymania fokusu nie dowodzi działania przycisku.

**Źródło:** [W3C: Keyboard](https://www.w3.org/WAI/WCAG22/Understanding/keyboard.html).

## KEY-02 — Wyjście z komponentu

**Podstawa:** WCAG 2.1.2, A. **Kryterium:** można opuścić komponent przy użyciu klawiatury; niestandardowy sposób wyjścia jest objaśniony.

**Test:** otwórz menu, karuzelę i modal koszyka, potem je opuść klawiaturą. Prawidłowe ograniczenie fokusu do otwartego modalu nie jest pułapką, jeśli dostępne jest jego zamknięcie. Zapisz metodę i miejsce powrotu fokusu.

**Źródło:** [W3C: No Keyboard Trap](https://www.w3.org/WAI/WCAG22/Understanding/no-keyboard-trap.html).

## KEY-03 — Widoczny fokus

**Podstawa:** WCAG 2.4.7, AA. **Kryterium:** użytkownik widzi, który element ma fokus klawiatury.

**Test:** przejdź całą badaną ścieżkę klawiszem Tab. Zrób zrzut przykładowego fokusu i każdego miejsca, gdzie znika. Nie utożsamiaj tego kryterium z bardziej szczegółowym 2.4.13 na poziomie AAA.

**Źródło:** [W3C: Focus Visible](https://www.w3.org/WAI/WCAG22/Understanding/focus-visible.html).

## KEY-04 — Fokus nie jest całkowicie zasłonięty

**Podstawa:** WCAG 2.4.11, AA. **Kryterium:** element otrzymujący fokus nie jest całkowicie ukryty przez treść utworzoną przez autora; obowiązują uwagi i wyjątki standardu.

**Test:** tabuluj przy stałym nagłówku, banerze i otwartym koszyku. Zapisz element i przesłaniającą warstwę. Pełna widoczność jest dobrym celem projektu, ale nie minimalnym wymaganiem tego kryterium.

**Źródło:** [W3C: Focus Not Obscured](https://www.w3.org/WAI/WCAG22/Understanding/focus-not-obscured-minimum.html).

## KEY-05 — Nazwa, rola i stan

**Podstawa:** WCAG 4.1.2, A. **Kryterium:** kontrolka udostępnia programowo nazwę, rolę i odpowiednie stany/wartości.

**Test:** obejrzyj drzewo dostępności przycisku menu, selektora wariantu, ikony koszyka i zakładki. Czy nazwa wyjaśnia cel, a stan otwarcia/wyboru jest odczytywalny? „Button” bez celu wymaga sprawdzenia i poprawy, nie domysłu.

**Źródło:** [W3C: Name, Role, Value](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value.html).

## KEY-06 — Widoczna etykieta w nazwie

**Podstawa:** WCAG 2.5.3, A. **Kryterium:** dostępna nazwa kontrolki zawiera jej widoczny tekst etykiety.

**Test:** porównaj tekst np. „Znajdź swój zapach” z dostępną nazwą, np. „Go to block”. Zapisz obie wersje. Kontrolka bez widocznej etykiety tekstowej nie podlega temu porównaniu, ale nadal wymaga odpowiedniej nazwy według KEY-05.

**Źródło:** [W3C: Label in Name](https://www.w3.org/WAI/WCAG22/Understanding/label-in-name.html).
