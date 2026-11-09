---
description: Zbuduj zestawienie briefów z folderu briefy/ (tabela, zasady z CLAUDE.md)
argument-hint: [opcjonalnie: miesiąc RRRR-MM | klient | kategoria]
---

Przygotuj zestawienie briefów zgodnie z `CLAUDE.md` i `O-FIRMIE.md` w tym folderze.

Zakres: $ARGUMENTS
(Puste = wszystkie briefy, jedna tabela. Miesiąc RRRR-MM = tylko ten miesiąc z pola Termin. Nazwa klienta lub kategorii = tylko ten klient lub ta kategoria.)

Kroki:
1. Wypisz i policz pliki w `briefy/`. Folder jest tylko do odczytu.
2. Przeczytaj każdy plik. Nie ufaj nazwom plików, czytaj pola Klient/Client, Kategoria/Category, Termin/Deadline, Budżet/Budget.
3. Zbuduj tabelę: Klient | Kategoria | Termin | Budżet (zł) | Plik źródłowy | Uwagi. Porządek: miesiąc → klient → kategoria (inny tylko, jeśli podałem w zakresie).
4. Daty RRRR-MM-DD, miesiąc z pola Termin. Budżet jako liczba w zł, „ok.” i „netto” w Uwagach. Braki: „brak danych”. Bez danych kontaktowych.
5. Nie wciągaj plików niebędących briefami (notatki), tylko wymień je w uwagach.
6. Dodaj podsumowanie (liczba briefów, klientów, suma budżetów bez „brak danych”) i listę uwag: dublety, brak roku, daty dwuznaczne, „po terminie” (porównaj z dzisiejszą datą).
7. Zapisz w `zestawienia/`: całość jako `zestawienie-wszystkie.md`, miesiąc jako `zestawienie-RRRR-MM.md`. Nie nadpisuj istniejących plików bez pytania. Jeśli plik już jest, zapisz pod nową nazwą i powiedz o tym.
8. Sprawdź liczby: wiersze + pliki niebędące briefami = liczba plików w `briefy/`. Pokaż tę kontrolę.
9. Pokaż wynik, wypisz niejednoznaczności i zapytaj, jak je rozstrzygnąć. Nie rozstrzygaj sam. Bez `git commit` i `git push`.
