# Updating the Database
```Python
from azurlane import AzurApi
api = AzurApi()

api.updater.update_check()
```
```javascript
const updateShipsData = require("@azurapi/azurapi")
updateShipsData()
```
From time to time, We will release updates according to the time when Azur Lane wiki is updated. Do include the function to update the database as & when needed and restart the system to reflect the changes
