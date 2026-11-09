---
description: Wypisz briefy wymagające decyzji (dublety, braki, daty dwuznaczne)
---

Przejrzyj `briefy/` (tylko odczyt) i wypisz wszystko, czego nie wolno rozstrzygać samemu, zgodnie z sekcją „Niejednoznaczności” w `CLAUDE.md`:

- brak roku w terminie,
- data dwuznaczna (np. 03/04/2026),
- możliwe dublety (ten sam klient, kategoria i opis; „kopia”, „v2”, „FINAL”): oba pliki i pytanie, który jest aktualny,
- brak budżetu („do ustalenia”) lub inne braki,
- pliki niebędące briefami.

Ten sam klient i kategoria, ale inny opis, to osobne briefy, nie dublet.

Format: numerowana lista. Przy każdej pozycji: klient, pliki, w czym problem, konkretne pytanie do mnie. Nie zapisuj plików i nie scalaj niczego.
