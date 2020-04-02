# Equipment Information
> The functions below returns JSON structured like this:

```json
{
}
```
Work in Progress
## Query By Name
###Type: Multilingual###
```javascript
const azurlane = require('@azurapi/azurapi')
azurlane.getEquipment('z23')
//or
import { getEquipmentByName  } from '@azurapi/azurapi' //ES6
//const { getEquipmentByName  } = require('@azurapi/azurapi') ES5
console.log(getEquipmentByName('z23'))
```
###Type: Single Language###
```javascript
import { getEquipmentByEnglishName  } from '@azurapi/azurapi' //ES6
//const { getEquipmentByEnglishName  } = require('@azurapi/azurapi') ES5
console.log(getEquipmentByEnglishName())
```

| Languages | JS                         | Alternative JS       |
|-----------|----------------------------|----------------------|
| English   | getEquipmentByEnglishName  | getEquipmentByNameEn |
| Japanese  | getEquipmentByJapaneseName | getEquipmentByNameJp |
| Chinese   | getEquipmentByChineseName  | getEquipmentByNameCn |
| Korean    | getEquipmentByKoreanName   | getEquipmentByNameKr |