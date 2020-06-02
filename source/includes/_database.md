# Updating the database
```python
from azurlane.azurapi import AzurAPI
api = AzurAPI()

api.updater.update()
```
```javascript
const { checkForNewUpdate } = require("@azurapi/azurapi") //es5
checkForNewUpdate()
```
```kotlin
val oldDate = Atago.getVersion().lastUpdatedApi
Atago.reloadDatabase()
expect(Atago.getVersion().lastUpdatedApi > oldDate).toBe(true)
```

We'll release updates accordingly when the wiki gets updated, please include the update function to update the database when needed changes are supplied.

Alternatively, you can host your own service by downloading the file that we've extracted [here](https://github.com/AzurAPI/azurapi-js-setup/blob/master/ships.json) to access the database if you don't need to use the functions below.