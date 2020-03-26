# Ship Information
Work in Progress
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
