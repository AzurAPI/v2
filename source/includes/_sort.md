# Sorting Information
> The functions below returns JSON structured like this:

```json
{
  /* same as getting ships in array */
}
```
Work in Progress
## Sort by ID
```javascript
const azurlane = require('@azurapi/azurapi')
azurlane.getAllShipsById()
//or
import { getAllShipsById  } from '@azurapi/azurapi'
console.log(getAllShipsById())
```

## Sort by Names in different languages
```javascript
import { getAllShipsByEnglishName  } from '@azurapi/azurapi' //ES6
//const { getAllShipsByEnglishName  } = require('@azurapi/azurapi') ES5
console.log(getAllShipsByEnglishName())
```

| Languages | JS                        |
|-----------|---------------------------|
| English   | getAllShipsByEnglishName  |
| Japanese  | getAllShipsByJapaneseName |
| Chinese   | getAllShipsByChineseName  |
| Korean    | getAllShipsByKoreanName   |

## Filter by Faction/Nationality
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
