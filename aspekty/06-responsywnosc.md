# Responsywność, powiększenie i cele dotykowe

[Mapa wiedzy](../README.md) · [Checklista](../checklist.md)

Przykładowa matryca autorska: 320, 390, 768 i 1440 CSS px szerokości oraz wartości tuż przed i po wykrytych breakpointach. Nie są to narzucone przez WCAG kategorie telefon/tablet/desktop. Testuj płynne zwężanie oraz zmianę układu; zanotuj wysokość viewportu i powiększenie.

## RWD-01 — Reflow

**Podstawa:** WCAG 1.4.10, AA. **Kryterium:** treść pionowo przewijana działa przy szerokości odpowiadającej 320 CSS px bez utraty informacji/funkcji i bez przewijania w dwóch kierunkach. Wyjątek dotyczy części wymagających układu dwuwymiarowego; nie obejmuje całego sklepu automatycznie.

**Test:** sprawdź home, katalog, kartę i koszyk przy 320 px; szukaj uciętego tekstu oraz poziomego przewijania. Nie zastępuj tym osobnego testu powiększenia tekstu.

**Źródło:** [W3C: Reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html).

## RWD-02 — Powiększenie tekstu

**Podstawa:** WCAG 1.4.4, AA. **Kryterium:** tekst można powiększyć do 200% bez utraty treści i funkcji; wyjątki obejmują napisy i obrazy tekstu.

**Test:** użyj obsługiwanego mechanizmu powiększenia i sprawdź etykiety, przyciski, opisy i koszyk. Zapisz metodę i skalę. Samo oglądanie strony na dużym monitorze lub zmiana screenshotu nie jest tym testem.

**Źródło:** [W3C: Resize Text](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html).

## RWD-03 — Zmiana odstępów tekstu

**Podstawa:** WCAG 1.4.12, AA. **Kryterium:** bez utraty treści/funkcji można ustawić równocześnie interlinię 1,5×, odstęp po akapicie 2×, odstęp między literami 0,12× i między słowami 0,16× rozmiaru fontu, zmieniając tylko te właściwości.

**Test:** zastosuj nadpisanie w dozwolonym narzędziu testowym i sprawdź ucięcia. To odporność na ustawienia użytkownika, a nie wymaganie, aby domyślny projekt miał dokładnie takie odstępy.

**Źródło:** [W3C: Text Spacing](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html).

## RWD-04 — Rozmiar celu wskaźnika

**Podstawa:** WCAG 2.5.8, AA. **Kryterium:** cel ma minimum 24×24 CSS px albo spełnia przewidziany wyjątek. Przy wyjątku odstępów okręgi średnicy 24 px wyśrodkowane na zbyt małych celach nie nachodzą na inny cel ani taki okrąg. Inne wyjątki: równoważna kontrolka, cel w tekście, niezmieniona kontrolka przeglądarki, istotna prezentacja.

**Test:** zmierz obszar klikalny ikon i kontrolek ilości, nie sam widoczny rysunek. 44×44 px to użyteczny cel projektowy i odrębne kryterium AAA 2.5.5, nie bezwarunkowe minimum AA.

**Źródło:** [W3C: Target Size Minimum](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html).
