# Sorting Information
##Return Value
> The payload when fetching results:

```json
{
  "Same format as the result in ship information but placed in an Array"
}
```

This section contains all the ships and equipment being sorted into an Array according to the functions indicated by the libraries.

## Sorting Ships

### Sorting Ships By ID or Language
```javascript

```
```python

```
```csharp

```

| Type      | Method                    |
|-----------|---------------------------|
| Unfiltered| getAllShips               |
| ID        | getAllShipsById           |
| English   | getAllShipsByEnglishName  |
| Japanese  | getAllShipsByJapaneseName |
| Chinese   | getAllShipsByChineseName  |
| Korean    | getAllShipsByKoreanName   |

### Filter ships by Faction or Nationality
```javascript

```

| Type        | Method                    |
|-------------|---------------------------|
| Nation      | getAllShipsFromNation     |
| Nationality | getAllShipsFromNationality|
| Faction     | getAllShipsFromFaction    |

## Sorting Equipment

### Sort Equipment by Name
```javascript

```
```python

```
```csharp

```
| Languages | Method                    |
|-----------|---------------------------|
| Unfiltered| getAllEquipments          |
| Official  | getEquipmentByOfficialName|
