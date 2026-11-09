---
description: Sprawdź gotowe zestawienie z briefami źródłowymi (liczby, daty, sumy)
argument-hint: [opcjonalnie: nazwa pliku z zestawienia/]
---

Skontroluj zestawienie: $ARGUMENTS
(Puste = najnowszy plik .md w `zestawienia/`, oprócz README.)

Nie edytuj niczego, tylko raportuj.

1. Przeczytaj `briefy/` od nowa, niezależnie od zestawienia, i zbuduj własną listę: klient, kategoria, termin (RRRR-MM-DD), budżet.
2. Porównaj wiersz po wierszu z zestawieniem. Zgłoś każdą różnicę: klient, kategoria, termin, budżet, plik źródłowy.
3. Przelicz sumy miesięczne i łączną (bez „brak danych”) oraz liczbę briefów i klientów.
4. Sprawdź kontrolę: wiersze + pliki niebędące briefami = liczba plików w `briefy/`.
5. Sprawdź zasady: format dat RRRR-MM-DD, brak danych kontaktowych (imiona, nazwiska, e-maile, telefony), „brak danych” zamiast zgadywania, miesiąc z pola Termin.
6. Sprawdź, czy zgłoszono wszystkie niejednoznaczności: brak roku, dwuznaczne daty, możliwe dublety, „po terminie”.

Na końcu tabela: sprawdzenie | wynik (OK / różnica) | szczegóły. Podaj liczby, nie samo „OK”.
