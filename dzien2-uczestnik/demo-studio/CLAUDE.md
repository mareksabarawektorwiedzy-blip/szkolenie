# DEMO-STUDIO — zasady pracy agenta (segregacja briefów)

Główne zadanie: **segregować briefy z folderu `briefy/`** i przygotowywać z nich
zestawienia dla szefowej agencji. Kontekst firmy: `O-FIRMIE.md`.

## Zasady nadrzędne
1. Folder `briefy/` jest **tylko do odczytu**. Nie zmieniaj, nie przenoś, nie zmieniaj nazw
   i nie usuwaj tych plików. Segregacja odbywa się w zestawieniu, nie na plikach.
2. Wszystkie pliki wynikowe zapisuj w `zestawienia/`.
3. Zestawienia mają postać **tabeli**.
4. Daty zapisuj jako **RRRR-MM-DD** (np. 2026-03-05).
5. Brakującą informację oznaczaj **„brak danych”**. Nigdy nie zgaduj wartości.
6. **Nie przepisuj danych kontaktowych** (imion, nazwisk, e-maili, telefonów) do zestawień.
7. Nie rób `git commit` ani `git push` bez wyraźnego polecenia.
8. Miesiąc briefu ustalaj z pola **Termin**, nigdy z nazwy pliku.

> Jeśli ten plik różni się od `pliki-do-zadan/zadanie-2/dla-chetnych-briefy-CLAUDE.md`
> (daty DD.MM.RRRR, „-”, CSV), obowiązują powyższe zasady szefowej.

## Co segregować
Z każdego briefu wyciągnij: **klient, kategoria, termin, budżet** (+ nazwa pliku źródłowego).
Posortuj i pogrupuj według:
- **kategorii:** strona www, social media, kampania płatna, newsletter, wideo,
- **klienta** (jeden klient może mieć kilka briefów w różnych kategoriach),
- **miesiąca terminu** (z pola Termin, zasada 8).

Domyślny porządek tabeli: miesiąc → klient → kategoria. Inny porządek tylko na prośbę.

## Czego możesz się spodziewać w plikach (briefy przysyłają klienci)
- **Nazwy plików są chaotyczne** (wielkie litery, spacje, „FINAL v2”, „(kopia)”, angielski).
  Nie ufaj im, czytaj treść. Klient i kategoria są w polach `Klient:` i `Kategoria:`.
- **Terminy w wielu zapisach:** `2026-03-12`, `20.01.2026`, `10 marca 2026`,
  `5.03.2026`, `15 marca`, `03/04/2026`. Normalizuj do RRRR-MM-DD.
- **Budżety w wielu zapisach:** „6 000 zł”, „3500 zł”, „4 000 PLN”, „15 tys. zł”,
  „ok. 8 tys. zł netto”, „do ustalenia”. W tabeli podawaj liczbę w zł (np. 15000);
  „ok.”, „netto” i „do ustalenia” zachowaj w kolumnie uwag, a przy braku kwoty wpisz „brak danych”.
- **Brief po angielsku** (`Client`, `Deadline`, `Budget`) — te same pola, inne nazwy.
- **Plik, który nie jest briefem** (np. notatka ze spotkania, brak pól Klient/Budżet):
  nie wciągaj do tabeli briefów, wymień go osobno w uwagach.

## Niejednoznaczności — zgłaszaj, nie rozstrzygaj
Nie zgaduj. W takim przypadku wpisz „brak danych” w polu i dopisz uwagę:
- **Brak roku** w terminie (np. „15 marca”).
- **Data dwuznaczna** (np. `03/04/2026`: 3 kwietnia czy 4 marca?).
- **Możliwy dublet** (ten sam klient, ta sama kategoria, ten sam opis, różne terminy
  lub oznaczenia „kopia”, „v2”, „FINAL”). Wypisz oba pliki i zapytaj, który jest aktualny.
  Nie wybieraj za użytkownika i nie scalaj wierszy.
- **Ten sam klient i kategoria, ale inny opis** to osobne briefy (nie dublet).
- **Termin w przeszłości** — oznacz uwagą „po terminie” (porównuj z dzisiejszą datą,
  nie wpisuj dat na sztywno).

## Format zestawienia
Tabela Markdown w pliku `zestawienia/zestawienie-RRRR-MM.md` (miesiąc z terminu),
albo jedna tabela ogólna `zestawienia/zestawienie-wszystkie.md`. Kolumny:

| Klient | Kategoria | Termin | Budżet (zł) | Plik źródłowy | Uwagi |
|---|---|---|---|---|---|

Pod tabelą dodaj:
- **podsumowanie:** liczba briefów, liczba klientów, suma budżetów (bez „brak danych”),
- **lista uwag:** dublety, braki, daty dwuznaczne, pliki niebędące briefami.

## Sposób działania
1. Wypisz pliki w `briefy/` i policz je.
2. Przeczytaj każdy plik (nie zgaduj z nazwy).
3. Zbuduj tabelę według zasad powyżej.
4. **Sprawdź liczby:** liczba wierszy + pliki niebędące briefami = liczba plików w folderze.
5. Pokaż wynik użytkownikowi, napisz, co zgłosiłeś jako niejednoznaczne, i zapytaj, jak rozstrzygnąć.
