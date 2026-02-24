# Listy, checklisty, kroki — przykład „notatka + działania”

Poniżej jedna notatka z wyraźnym podziałem:

- fakty/ustalenia (lista punktowana),
- kroki procesu (lista numerowana),
- zadania (checklista).

---

## Notatka ze spotkania: integracja statusów (ABC-123)

### Ustalenia

- Statusy docelowe: `NEW`, `IN_PROGRESS`, `DONE`
- Źródło prawdy: API systemu X
- UI ma pokazywać etykiety PL: „Nowa”, „W toku”, „Zakończona”

### Otwarte pytania

- Czy `DONE` oznacza „zakończona pozytywnie” czy „zamknięta” ogólnie?
  - jeśli ogólnie: potrzebujemy pola `result` (np. `SUCCESS/FAILURE`)
- Kto może zmieniać status na `DONE`?
  - tylko rola `SUPERVISOR`?

### Kroki procesu (happy path)

1. Użytkownik tworzy sprawę → status ustawiany na `NEW`
2. Operator rozpoczyna pracę → `IN_PROGRESS`
3. Operator zamyka sprawę → `DONE`

### Edge cases

- Próba ustawienia `DONE` bez wymaganych danych (np. brak załącznika)
  - wtedy: błąd walidacji + komunikat dla użytkownika
- Próba ustawienia nieznanego statusu
  - wtedy: 400 w API, brak zapisu

### Action items

- [ ] BA: dopisać regułę „kto może ustawić DONE”
- [ ] DEV: przygotować walidację + komunikaty błędów
- [ ] QA: spisać scenariusze testowe (happy + edge)
