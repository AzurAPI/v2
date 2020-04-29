# Updating the Database
```python
from azurlane.azurapi import AzurAPI
api = AzurAPI()

api.updater.update()
```
```javascript
const checkForNewUpdate = require("@azurapi/azurapi")
checkForNewUpdate()
```
```kotlin
val oldDate = Atago.getVersion().lastUpdatedApi
Atago.reloadDatabase()
expect(Atago.getVersion().lastUpdatedApi > oldDate).toBe(true)
```
From time to time, We will release updates according to the time when Azur Lane wiki is updated. Do include the function to update the database as & when needed and restart the system to reflect the changes
