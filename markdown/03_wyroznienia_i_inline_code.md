# Wyróżnienia i `inline code` — przykład „bez niejednoznaczności”

Cel: odróżnić „opisy” od nazw technicznych, statusów i pól.

---

## Wymaganie: walidacja statusu

**Decyzja:** API musi odrzucać nieznane statusy.

### Dane

- Pole: `status`
- Typ: string
- Dozwolone wartości: `NEW`, `IN_PROGRESS`, `DONE`

### Przykład payloadu (blok kodu)

```json
{
  "caseId": "C-10001",
  "status": "IN_PROGRESS",
  "updatedBy": "john.doe"
}
```

### Przykład błędu (blok kodu)

```json
{
  "code": "VALIDATION_ERROR",
  "errors": [
    { "field": "status", "message": "Unsupported status: ARCHIVED" }
  ]
}
```
