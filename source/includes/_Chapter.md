# Chapter Information
<aside class="notice">
This section is currently undergoing construction.
</aside>
## Return Value
> The payload of the information is structured as:

```json
"1": {
    "names": {
        "en": "String",
        "cn": "String",
        "jp": "String"
    },
    "normal": {
        "title": "String",
        "code": "String",
        "introduction": "String",
        "unlockRequirements": {
            "text": "String",
            "requiredLevel": "Number"
        },
        "clearRewards": {
            "cube": "Number or null",
            "coin": "Number or null",
            "oil": "Number or null"
        },
        "3-StarRewards": [
            {
                "count": "Number or null",
                "item": "String or Null"
            },
            {
                "item": "String or Null"
            }
        ],
        "enemyLevel": {
            "mobLevel": "Number",
            "bossLevel": "Number",
            "boss": "String"
        },
        "baseXP": {
            "smallFleet": "Number",
            "mediumFleet": "Number",
            "largeFleet": "Number",
            "bossFleet": "Number"
        },
        "requiredBattles": "Number",
        "bossKillsToClear": "Number",
        "starConditions": [
            "String in Array"
        ],
        "airSupremacy": {
            "actual": 6,
            "suggestedLv1": 450,
            "suggestedLv2": 150
        },
        "mapDrops": [
            "String in Array"
        ],
        "equipmentBlueprintDrops": [],
        "shipDrops": [
            "String in Array"
        ],
        "nodeMap": {
            "preview": "https://azurlane.koumakan.jp/w/images/6/67/1-1.png",
            "width": 7,
            "height": 1,
            "map": [
              // First Array in X Axis in string
              // Second Array in Y Axis in String
                [
                    "Fleet spawn",
                    "Sea",
                    "Sea",
                    "Sea",
                    "Sea",
                    "Enemy spawn",
                    "Boss spawn"
                ]
            ],
            "nodes": [
                {
                    "x": "Number",
                    "y": "Number",
                    "node": "Type in String"
                }
            ]
        }
    }
  }
```
