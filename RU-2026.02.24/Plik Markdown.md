# Plik testowy do skilli Markdown

## Tutaj mamy sekcje poświęconą obróbce tekst

### **pogrubienie**
### *kursywa*

Test paragrafu
> to jest test
i tutaj bez (potem przerwa)

> test nest
>> i jak to będzie działać
> i tutaj testu (wracamy poziom mniej)
aaa to będzie cytowanie (ta sekcja nie miała znacznika)

### Test punktowania (znaczniki)
- pozycja jeden
- pozycja dwa
- pozycja trzy

* pozycja jeden
* pozycja dwa
* pozycja trzy

### Test numeracji
1. Numeracja 1
1. Numeracja 2
2. Numeracja 3
6. Numeracja 4

### tabela:

| Kol 1 | Kol 2 |
|---|---|
| Bardzo długi teskt dla testu | . |
| . | Bardzo długi teskt dla testu |

### Kopia tabeli z przykładu

| Pole | Znaczenie | Wymagalne | Walidacja | Przykład |
|---|---|---:|---|---|
| caseId | Identyfikator sprawy | tak | format `C-\d+` | `C-10001` |
| status | Status sprawy | tak | `NEW/IN_PROGRESS/DONE` | `NEW` |
| updatedBy | Użytkownik zmieniający status | tak | niepuste | `john.doe` |
| comment | Komentarz do zmiany | nie | max 500 znaków | `Brak danych` |

### Dodajemy obrazek
![Obrazek](Placeholder.png)


### Check list
- [ ] Zadanie 1
- [x] Zadanie 2
- [ ] Zadanie 3


### Przykład cytatu (kodu)

```json
{
  "caseId": "C-10001",
  "status": "IN_PROGRESS",
  "updatedBy": "john.doe"
}