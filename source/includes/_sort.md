# Sorting Information
> The Resultant JSON is structured like this:

```json
{
  /* same as getting ships in array */
}
```

This Section contains all the Ships/Equipment being sorted in an array according to the relevant functions indicated by the developers.

## Sorting Ships

### Sorting Ship information
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
