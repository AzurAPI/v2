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
import { getAllShips } from '@azurapi/azurapi' //ES6
//const { getAllShips } = require('@azurapi/azurapi') ES5
console.log(getAllShips)

//Alternative
const azurlane = require('@azurapi/azurapi') //ES5
console.log(azurlane.getAllShips)
```
```python
api.getAllShips()
```
```csharp
var ships = client.getAllShips();
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
const azurlane = require('@azurapi/azurapi')
azurlane.getAllShipsFromNation;
azurlane.getAllShipsFromNationality;
azurlane.getAllShipsFromFaction;
//or
import { getAllShipsFromNation, getAllShipsFromNationality, getAllShipsFromFaction } from '@azurapi/azurapi'
console.log(getAllShipsFromNation)
console.log(getAllShipsFromNationality)
console.log(getAllShipsFromFaction)
```

| Type        | Method                    |
|-------------|---------------------------|
| Nation      | getAllShipsFromNation     |
| Nationality | getAllShipsFromNationality|
| Faction     | getAllShipsFromFaction    |

## Sorting Equipment

### Sort Equipment by Name
```javascript
import { getAllEquipments  } from '@azurapi/azurapi' //ES6
//const { getAllEquipments  } = require('@azurapi/azurapi') ES5
console.log(getAllEquipments)

//Alternative
const azurlane = require('@azurapi/azurapi') //ES5
console.log(azurlane.getAllEquipments)
```
```python
api.getAllEquipments
```
```csharp
var equipments = client.GetAllEquipments();
```
| Languages | Method                    |
|-----------|---------------------------|
| Unfiltered| getAllEquipments          |
| Official  | getEquipmentByOfficialName|
