# Sorting Information
> The Resultant JSON is structured like this:

```json
{
  "Same format as the result in ship information but placed in an Array"
}
```

This Section contains all the Ships/Equipment being sorted in an array according to the relevant functions indicated by the developers.

## Sorting Ships

### Sorting Ships By ID/Language
```javascript
import { getAllShips } from '@azurapi/azurapi' //ES6
//const { getAllShips } = require('@azurapi/azurapi') ES5
console.log(getAllShips())
```
```python
api.getAllShips()
```

| Type      | Method                    |
|-----------|---------------------------|
| Unfiltered| getAllShips               |
| ID        | getAllShipsById           |
| English   | getAllShipsByEnglishName  |
| Japanese  | getAllShipsByJapaneseName |
| Chinese   | getAllShipsByChineseName  |
| Korean    | getAllShipsByKoreanName   |

### Filter ships by Faction/Nationality
```javascript
const azurlane = require('@azurapi/azurapi')
azurlane.getAllShipsFromNation();
azurlane.getAllShipsFromNationality();
azurlane.getAllShipsFromFaction();
//or
import { getAllShipsFromNation, getAllShipsFromNationality, getAllShipsFromFaction } from '@azurapi/azurapi'
console.log(getAllShipsFromNation())
console.log(getAllShipsFromNationality())
console.log(getAllShipsFromFaction())
```

| Type        | Method                    |
|-------------|---------------------------|
| Nation      | getAllShipsFromNation     |
| Nationality | getAllShipsFromNationality|
| Faction     | getAllShipsFromFaction    |

## Sorting Equipment

###Sort Equipment by Name
```javascript
import { getAllEquipments  } from '@azurapi/azurapi' //ES6
//const { getAllEquipments  } = require('@azurapi/azurapi') ES5
console.log(getAllEquipments())
```
```python
api.getAllEquipments()
```
| Languages | Method                    |
|-----------|---------------------------|
| Unfiltered| getAllEquipments          |
| Official  | getEquipmentByOfficialName|
