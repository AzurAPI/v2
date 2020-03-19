# Ship Information
Work in Progress
## Query By Name
###Type: Multilingual###
```javascript
azurlane.getShip('z23')
//or
import { getShipByName } from '@azurapi/azurapi' //ES6
//const { getShipByName } = require('@azurapi/azurapi') ES5
console.log(getShipByName('z23'))
```
###Type: Single Language###
This Table allows you to configure the type of language as a point of reference in name detection
| Language | Method in JS          | Alternative JS Method |
| -------- | --------------------- | --------------------- |
| English  | getShipByEnglishName  | getShipByNameEn       |
| Japanese | getShipByJapaneseName | getShipByNameKr       |
| Chinese  | getShipByChineseName  | getShipByNameJp       |
| Korean   | getShipByKoreanName   | getShipByNameCn       |
```javascript
import { getShipsByEnglishName } from '@azurapi/azurapi' //ES6
//const { getShipsByEnglishName } = require('@azurapi/azurapi') ES5
console.log(getShipsByEnglishName('z23'))
```
## Query By ID
###Method: Direct Library Import###
```javascript
azurlane.getShip('001')
```
###Method: Partial Function Import###
```javascript
import { getShipById } from '@azurapi/azurapi' //ES6
//const { getShipById } = require('@azurapi/azurapi') ES5
console.log(getShipById('001'))
```
