# Barrage Information
<aside class="notice">
This section is currently undergoing construction.
</aside>
## Return Value
> The payload of the information is structured as:

```json
{
      "id": "String",
      "type": "String",
      "icon": "URL Link",
      "name": "String",
      "image": "URL Link",
      "ships": [
          "Array of Ships Names"
      ],
      "hull": "DD",
      "rounds": [
          // Refer to Rounds Data in Array
      ]
  },
```
### Rounds Data

<div class="center-column"></div>

```json
{
    "type": "Type in String",
    "dmgL": "Number",
    "dmgM": "Number",
    "dmgH": "Number",
    "note": "String or Null"
}
```
