# Sorting Information
> The functions below returns JSON structured like this:

```json
{
  /* same as getting ships in array */
}
```

This Section contains all the Ships/Equipment being sorted in an array according to the relevant functions indicated by the developers.

## Sorting Ships
### Sort ships by ID
```javascript
const azurlane = require('@azurapi/azurapi')
azurlane.getAllShipsById()
//or
import { getAllShipsById  } from '@azurapi/azurapi'
console.log(getAllShipsById())
```

### Sort ships by Names in different languages
```javascript
import { getAllShipsByEnglishName  } from '@azurapi/azurapi' //ES6
//const { getAllShipsByEnglishName  } = require('@azurapi/azurapi') ES5
console.log(getAllShipsByEnglishName())
```
```python
api.getAllShips()
```
Reference Table for All Languages

| Languages | Method                    |
|-----------|---------------------------|
| Unfiltered| getAllShips               |
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
