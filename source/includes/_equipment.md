# Equipment Information
> The functions below returns JSON structured like this:

```json
{
  "wikiUrl": "String",
  "category": "String",
  "names": {
    "en": "String",
    "cn": "String",
    "jp": "String",
    "kr": "String"
  },
  "type": { "focus": "String", "name": "String" },

  "nationality": "String",
  "image": "String",
  "fits": {
    "destroyer": "String",
    "lightCruiser": "String",
    "heavyCruiser": "String",
    "monitor": "String",
    "largeCruiser": "String",
    "battleship": "String",
    "battlecruiser": "String",
    "aviationBattleship": null,
    "aircraftCarrier": null,
    "lightCarrier": null,
    "repairShip": null,
    "submarine": "String",
    "submarineCarrier": null
  },
  "misc": {
    "obtainedFrom": "String",
    "notes": "String",
    "animation": "String"
  },
  "tiers": {
    "T0": { "tier": "String", "rarity": "String", "stars": [Object], "stats": [Object] }
  }
}
```

Same as Ships, this section contains all the stats for Equipment and resultant JSON is provided on the right. As usual, Developers should able to provide their own error checking for misspelt names and other user centric input checks prior to checking the library for the statistics
## Equipment Query By Name
###Type: Equipment(Multilingual)###
```javascript
const azurlane = require('@azurapi/azurapi')
azurlane.getEquipment('z23')
//or
import { getEquipmentByName  } from '@azurapi/azurapi' //ES6
//const { getEquipmentByName  } = require('@azurapi/azurapi') ES5
console.log(getEquipmentByName('z23'))
```
By Default, it is recommended to use the Multilingual Language to detect and display information provided by the users, it will automatically detect by its language and quary its result.

###Type: Equipment(Single Language)###
```javascript
import { getEquipmentByEnglishName  } from '@azurapi/azurapi' //ES6
//const { getEquipmentByEnglishName  } = require('@azurapi/azurapi') ES5
console.log(getEquipmentByEnglishName())
```
(For JS Referance)
This Table allows you to configure the type of language as a point of reference in name detection

| Languages | JS                         | Alternative JS       |
|-----------|----------------------------|----------------------|
| English   | getEquipmentByEnglishName  | getEquipmentByNameEn |
| Japanese  | getEquipmentByJapaneseName | getEquipmentByNameJp |
| Chinese   | getEquipmentByChineseName  | getEquipmentByNameCn |
| Korean    | getEquipmentByKoreanName   | getEquipmentByNameKr |
