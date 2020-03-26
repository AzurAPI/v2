# Ship Information
> The functions below returns JSON structured like this:

```json
{
  "wikiUrl": "String",
  "id": "String",
  "names": { "en": "String", "code": "String", "cn": "String", "jp": "String", "kr": "String" },
  "class": "String",
  "nationality": "String",
  "hullType": "String",
  "thumbnail": "String",
  "rarity": "String",
  "stars": { "stars": "String", "value": "Number" },
  "stats": {
    "level120": {
      "health": "String", "armor": "String", "reload": "String", "luck": "String",
      "firepower": "String", "torpedo": "String", "evasion": "String", "speed": "String",
      "antiair": "String", "aviation": "String", "oilConsumption": "String", "accuracy": "String",
      "antisubmarineWarfare": "String"
    },
    "level100": { /* Follow Level120 format */ },
    "baseStats": { /* Follow Level120 format */ }
  },
  "slots": {
    '1': { "type": "String", "minEfficiency": "Number", "maxEfficiency": "Number" },
    '2': { /* Follow Slot 1 */ },
    '3': { /* Follow Slot 1 */ }
  },
  "enhanceValue": { "firepower": "Number", "torpedo": "Number", "aviation": "Number", "reload": "Number" },
  "scrapValue": { "coin": "Number", "oil": "Number", "medal": "Number" },
  "skills": [
    { "icon": "String", "names": [Object], "description": "String", "color": "String" }
    /* Same Format for the Rest of the Skills */
  ],

  "limitBreaks": [
    /* Each Limit Break will have an array of upgrade stats, Example is below*/
    [
      'Number of Torpedo Bombers +1',
      'Torpedo Bombers Efficiency +5%'
    ],
    [
      'Hangar Capacity +1',
      'Number of Fighters +1',
      'Torpedo Bombers Efficiency +10%'
    ],
    [ 'Number of All Planes +1', 'Torpedo Bombers Efficiency +15%' ]
  ],
  "fleetTech": {
    "statsBonus": { "collection": [Object], "maxLevel": [Object] },
    "techPoints": { "collection": 14, "maxLimitBreak": 28, "maxLevel": 21, "total": 63 }
  },
  "construction": {
    "constructionTime": "String",
    "availableIn": { "light": "Boolean", "heavy": "Boolean", "aviation": "Boolean", "limited": "Boolean", "exchange": "Boolean" }
  },
  "gallery": [
    /* Array of Gallery Images in the following Format */
    { "description": "String", "url": "String" }
  ],
  "misc": {
    "artist": "String",
    "web": { "name": "String", "url": "String" },
    "pixiv": { "name": "String", "url": "String" },
    "twitter": { "name": "String", "url": "String" },
    "voice": { "name": "String", "url": "String" }
  },
  "skins": [
    { "name": "String", "image": "String", "background": "String", "chibi": "String", "info": [Object] }
    /* Same Format for the rest of the skins */
  ]
}
```
Work in Progress

This section contain the methods that Developers are able to use to call a ships stat. The names of the relevant ships implemented in game are provided in the resultant JSON on the right. But, Developers should able to provide their own error checking for misspelt names and other user centric input checks prior to checking the library for the statistics

## Query By Name
###Type: Multilingual###
```javascript
const azurlane = require('@azurapi/azurapi')
azurlane.getShip('z23')
//or
import { getShipByName } from '@azurapi/azurapi' //ES6
//const { getShipByName } = require('@azurapi/azurapi') ES5
console.log(getShipByName('z23'))
```
```python
api.get_ship(ship="Enterprise")
# or
api.get_ship_by_name(name="Enterprise")
```
By Default, it is recommended to use the Multilingual Language to detect and display information provided by the users, it will automatically detect by its language and quary its result.
###Type: Single Language###
```javascript
import { getShipsByEnglishName } from '@azurapi/azurapi' //ES6
//const { getShipsByEnglishName } = require('@azurapi/azurapi') ES5
console.log(getShipsByEnglishName('z23'))
```
(For JS Referance)
This Table allows you to configure the type of language as a point of reference in name detection

| Language | Method in JS          | Alternative JS Method |
| -------- | --------------------- | --------------------- |
| English  | getShipByEnglishName  | getShipByNameEn       |
| Japanese | getShipByJapaneseName | getShipByNameKr       |
| Chinese  | getShipByChineseName  | getShipByNameJp       |
| Korean   | getShipByKoreanName   | getShipByNameCn       |


## Query By ID

```javascript
//Method: Direct Library Import
azurlane.getShip('001')
//Method: Partial Function Import
import { getShipById } from '@azurapi/azurapi' //ES6
//const { getShipById } = require('@azurapi/azurapi') ES5
console.log(getShipById('001'))
```
```python
api.get_ship(ship=115)
api.get_ship(ship="115")
# or

# sid stands for "ship id" since id is a reserved function name in Python
api.get_ship_by_id(sid=115)
api.get_ship_by_id(sid="115")
```

There are 2 ways to quary by the ships id. The default settings to use is the direct library method, not only it is able to detect by the ship name, the ID of the ships can be used to collect the information of the ships
