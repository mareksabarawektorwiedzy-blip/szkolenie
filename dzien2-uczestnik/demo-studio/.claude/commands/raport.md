---
description: Raport miesięczny dla szefowej: sumy wg kategorii i klientów, wnioski, niepewności
argument-hint: [miesiąc RRRR-MM lub nazwa, puste = wszystkie briefy]
---

Przygotuj raport z briefów dla szefowej agencji. Zakres: $ARGUMENTS
(Puste = wszystkie briefy. Miesiąc ustalaj z pola Termin, nie z nazwy pliku.)

Zasady jak w `CLAUDE.md`: `briefy/` tylko do odczytu, daty RRRR-MM-DD, „brak danych” zamiast zgadywania, bez danych kontaktowych, bez `git commit` i `git push`.

1. Przeczytaj briefy z zakresu (nie ufaj nazwom plików) i policz wszystko z danych, nie z poprzednich zestawień.
2. Raport ma trzy tabele:
   - **wg kategorii:** kategoria | liczba briefów | suma budżetów (zł),
   - **wg klientów:** klient | liczba briefów | suma budżetów (zł),
   - **wg miesiąca terminu** (jeśli zakres obejmuje kilka miesięcy).
3. Pod tabelami krótkie wnioski (3–5 punktów), tylko to, co wynika z liczb: największa kategoria, największy klient, udział procentowy w sumie.
4. Sekcja **Niepewne**: dublety, brak roku, daty dwuznaczne, brak budżetu. Dla każdej pozycji podaj, jak zmieni się suma, gdy zostanie rozstrzygnięta w jedną lub drugą stronę. Nie rozstrzygaj sam.
5. Zapisz w `zestawienia/raport-RRRR-MM.md` (albo `raport-wszystkie.md`). Nie nadpisuj istniejącego pliku bez pytania.
6. Sprawdź liczby: suma w tabelach kategorii = suma w tabelach klientów = suma w zestawieniu. Pokaż tę kontrolę.
7. Pokaż wynik i zapytaj, czy zrobić PDF.
