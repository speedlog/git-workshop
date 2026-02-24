# Tabele — przykład „słownik pól + słownik statusów”

---

## Słownik pól (wejście API)

| Pole | Znaczenie | Wymagalne | Walidacja | Przykład |
|---|---|---:|---|---|
| caseId | Identyfikator sprawy | tak | format `C-\d+` | `C-10001` |
| status | Status sprawy | tak | `NEW/IN_PROGRESS/DONE` | `NEW` |
| updatedBy | Użytkownik zmieniający status | tak | niepuste | `john.doe` |
| comment | Komentarz do zmiany | nie | max 500 znaków | `Brak danych` |

## Słownik statusów (czytelny dla biznesu)

| Status | Etykieta PL | Kiedy używany | Kto ustawia |
|---|---|---|---|
| `NEW` | Nowa | sprawa utworzona | system |
| `IN_PROGRESS` | W toku | prace trwają | operator |
| `DONE` | Zakończona | prace zakończone | operator/supervisor |

Tip: jeśli tabela robi się szeroka, rozbij ją na 2 tabele (np. osobno walidacje, osobno role/uprawnienia).
