---
description: Policz VAT od każdego zlecenia z briefów za wskazany miesiąc i podaj sumę VAT ze zleceń
argument-hint: [miesiąc, np. marzec] [netto|brutto, domyślnie netto]
---

Policz VAT od zleceń z `briefy/` zgodnie z `CLAUDE.md` (briefy tylko do odczytu, wynik do `zestawienia/`).

Argumenty: $ARGUMENTS

KROK 1. Sprawdź argumenty.
- Pierwszy argument: nazwa miesiąca po polsku (styczeń … grudzień, mianownik, małymi literami). Pusty albo niepoprawny: wypisz komunikat z listą poprawnych wartości, **nie twórz żadnego pliku** i zakończ.
- Drugi argument (opcjonalny): `netto` albo `brutto` = rodzaj kwot z briefów, które nie podają go same. Brak = **netto**. Każda inna wartość: komunikat i koniec, bez pliku.
- Stawka VAT: 23%.

KROK 2. Przeczytaj briefy.
Przeczytaj wszystkie pliki w `briefy/` (nie ufaj nazwom). Miesiąc ustalaj z pola Termin. Z każdego weź klienta, kategorię, termin (RRRR-MM-DD) i budżet w zł. Pliki niebędące briefami wymień osobno.
Rodzaj kwoty: „netto” albo „brutto” w treści budżetu wygrywa z argumentem. W przeciwnym razie obowiązuje drugi argument (domyślnie netto) i dopisz to w kolumnie „Rodzaj kwoty” jako „netto (założone)”.

KROK 3. Policz VAT **osobno dla każdego zlecenia** (każdy brief = jeden wiersz, dubletów nie scalaj):
- netto: VAT = kwota × 23%,
- brutto: VAT = kwota − kwota / 1,23.
Brak kwoty = „brak danych”. Zaokrąglaj do 0,01 zł.

KROK 4. Zapisz `zestawienia/vat-<miesiąc RRRR-MM>.md`. Nie nadpisuj istniejącego pliku bez pytania. Kolumny:

| Klient | Kategoria | Termin | Kwota (zł) | Rodzaj kwoty | **VAT (zł)** | Plik źródłowy | Uwagi |
|---|---|---|---|---|---|---|---|

KROK 5. Informacja wyjściowa pod tabelą:
- **Suma całego podatku VAT ze zleceń (zł)**, z podaniem założenia (netto/brutto),
- liczba zleceń z policzonym VAT i liczba z „brak danych”,
- ile wyniosłaby suma przy przeciwnym założeniu (jedna liczba),
- uwagi: dublety, brak roku, daty dwuznaczne (z wpływem na sumę w obie strony, bez rozstrzygania), pliki niebędące briefami.

KROK 6. Kontrola: suma kolumny VAT = suma w podsumowaniu; wiersze + pliki pominięte = liczba plików w `briefy/`. Pokaż liczby.
