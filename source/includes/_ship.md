# Ship Information
<aside class="precaution">Some Discord servers may consider certain skins as NSFW. If you are developing a bot for a specific server, Do discuss how the command should be implemented before designing</aside>
> The functions below returns JSON structured like this:

```json
{
  "wikiUrl": "String",
  "id": "String",
  "names": { "code": "String","en": "String", "code": "String", "cn": "String", "jp": "String", "kr": "String" },
  "class": "String",
  "nationality": "String",
  "hullType": "String",
  "thumbnail": "String",
  "rarity": "String",
  "stars": { "stars": "String", "value": "Number" },
  "stats": {
    "level120": "Refer to Stats Table",
    "level100": "Refer to Stats Table",
    "baseStats": "Refer to Stats Table",
    "level100Retrofit": "Refer to Stats Table",
    "level120Retrofit": "Refer to Stats Table"
  },
  "slots": {
    1: "Refer to Slot Table",
    2: "Refer to Slot Table",
    3: "Refer to Slot Table"
  },
  "enhanceValue": { "firepower": "Number", "torpedo": "Number", "aviation": "Number", "reload": "Number" },
  "scrapValue": { "coin": "Number", "oil": "Number", "medal": "Number" },
  "skills": [
    "Refer to Skill Table"
    /* Same Format for the Rest of the Skills */
  ],

  "limitBreaks": [
    /* Each Limit Break will have an array of upgrade stats,
    first layer = breaks, second layer = bonus */
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
    "web": "Refer to Artist Table",
    "pixiv": "Refer to Artist Table",
    "twitter": "Refer to Artist Table",
    "voice": "Refer to Artist Table"
  },
  "skins": [
    { "name": "String", "image": "String", "background": "String", "chibi": "String", "info": [Object] }
    /* Same Format for the rest of the skins */
  ]
}
```

This section contain the methods that Developers are able to use to call a ships stat. The names of the relevant ships implemented in game are provided in the resultant JSON on the right. But, Developers should able to provide their own error checking for misspelt names and other user centric input checks prior to checking the library for the statistics

Object Format for Artist

| **Artist** |            |         |            |
|------------|:----------:|---------|------------|
| **name**   | String     | **url** | String     |

Object Format for Slot

| **Slot** |            |                      |            |                      |            |
|----------|:----------:|----------------------|------------|----------------------|------------|
| **type** | String     | **minEfficiency(%)** | Number     | **maxEfficiency(%)** | Number     |

Object Format for Stats

| **Stats**                |        |                    |        |                  |        |
|--------------------------|:------:|--------------------|--------|------------------|--------|
| **health**               | string | **armor**          | string | **reload**       | string |
| **luck**                 | string | **firepower**      | string | **torpedo**      | string |
| **evasion**              | string | **speed**          | string | **antiair**      | string |
| **aviation**             | string | **oilConsumption** | string | **accuracy**     | string |
| **antisubmarineWarfare** | string |                    |        |                  |        |
|                          |        |                    |        |                  |        |
| **For Submarines**       |        |                    |        |                  |        |
| **oxygen**               | string | **ammunition**     | string | **huntingRange** | string |

Object Format for Skill

| **Skill**       |                                                 |
|-----------------|:-----------------------------------------------:|
| **icon**        | string                                          |
| **names**       | { en: string cn: string jp: string kr: string } |
| **description** | string                                          |
| **color**       | string                                          |

## Ship Query By Name
###Type: Ship(Multilingual)###
```javascript
const azurlane = require('@azurapi/azurapi')
azurlane.getShip('z23')
//or
import { getShipByName } from '@azurapi/azurapi' //ES6
//const { getShipByName } = require('@azurapi/azurapi') ES5
console.log(getShipByName('z23'))
```
```python
api.getShip(ship="Enterprise")
# or
api.getShipByName(name="Enterprise")
```
By Default, it is recommended to use the Multilingual Language to detect and display information provided by the users, it will automatically detect by its language and quary its result.
###Type: Ship(Single Language)###
```javascript
import { getShipsByEnglishName } from '@azurapi/azurapi' //ES6
//const { getShipsByEnglishName } = require('@azurapi/azurapi') ES5
console.log(getShipsByEnglishName('z23'))
```
```python
api.getShipByNameEn(ship="Enterprise")
```
This Table allows you to configure the type of language as a point of reference in name detection

| Language | Main Method           | Alternative  Method   |
| -------- | --------------------- | --------------------- |
| English  | getShipByEnglishName  | getShipByNameEn       |
| Japanese | getShipByJapaneseName | getShipByNameKr       |
| Chinese  | getShipByChineseName  | getShipByNameJp       |
| Korean   | getShipByKoreanName   | getShipByNameCn       |


## Ship Query By ID

```javascript
//Method: Direct Library Import
azurlane.getShip('001')
//Method: Partial Function Import
import { getShipById } from '@azurapi/azurapi' //ES6
//const { getShipById } = require('@azurapi/azurapi') ES5
console.log(getShipById('001'))
```
```python
api.getShip(ship=115)
api.getShip(ship="115")
# or

# sid stands for "ship id" since id is a reserved function name in Python
api.getShipById(sid=115)
api.getShipById(sid="115")
```

There are 2 ways to quary by the ships id. The default settings to use is the direct library method, not only it is able to detect by the ship name, the ID of the ships can be used to collect the information of the ships
