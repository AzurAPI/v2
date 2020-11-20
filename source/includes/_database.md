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
```csharp
// dotnet add package AzurAPINet
using Jan0660.AzurAPINet;
var client = new AzurAPIClient(new AzurAPIClientOptions());
// check for update
var isUpdateAvailable = await client.DatabaseUpdateAvailableAsync();
// reload/update cached data
await client.ReloadCachedAsync();

// reload cached data to update it
await client.ReloadEverythingAsync();
```
We'll release updates accordingly when the wiki gets updated, please include the update function to update the database when needed changes are supplied.

Alternatively, you can host your own service by downloading or fetching the file that we've extracted in the table below if you don't need to use the functions we have included.

| Type                  | Link | Raw                                                                                  |
|-----------------------|------|--------------------------------------------------------------------------------------|
| Ship Infomation       | [Github](https://github.com/AzurAPI/azurapi-js-setup/blob/master/ships.json)| [Here](https://raw.githubusercontent.com/AzurAPI/azurapi-js-setup/master/ships.json) |
| Equipment Information | [Github](https://github.com/AzurAPI/azurapi-js-setup/blob/master/equipments.json)| [Here](https://raw.githubusercontent.com/AzurAPI/azurapi-js-setup/master/equipments.json) |
| Chapter Infomation    | [Github](https://github.com/AzurAPI/azurapi-js-setup/blob/master/chapters.json)| [Here](https://raw.githubusercontent.com/AzurAPI/azurapi-js-setup/master/chapters.json) |
| Voiceline Infomation  | [Github](https://github.com/AzurAPI/azurapi-js-setup/blob/master/voice_lines.json)| [Here](https://raw.githubusercontent.com/AzurAPI/azurapi-js-setup/master/voice_lines.json) |
| Barrage Infomation    | [Github](https://github.com/AzurAPI/azurapi-js-setup/blob/master/barrage.json)| [Here](https://raw.githubusercontent.com/AzurAPI/azurapi-js-setup/master/barrage.json) |
