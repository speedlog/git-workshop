# ABC-123: Zmiana statusów sprawy

## Cel

Ujednolicić statusy w procesie obsługi sprawy tak, aby raportowanie i API były spójne.

## Zakres

- Zmiana słownika statusów
- Walidacja na wejściu API
- Migracja mapowań w raportach

## Poza zakresem

- Nowy status `ARCHIVED` (rozważymy w kolejnej iteracji)
- Zmiany w retencji danych

## Definicje

- **Sprawa** — jednostka pracy w systemie X
- **Status** — etap przetwarzania sprawy widoczny w UI i API

## Reguły biznesowe

1. Status może przyjmować tylko wartości z listy: `NEW`, `IN_PROGRESS`, `DONE`.
2. Status nie może być pusty (`null`) po utworzeniu sprawy.
3. Zmiana `DONE` → `IN_PROGRESS` jest niedozwolona.

## Kryteria akceptacji

- [ ] Użytkownik widzi tylko 3 statusy
- [ ] API odrzuca nieznany status kodem 400
- [ ] Raporty poprawnie mapują stare statusy na nowe
