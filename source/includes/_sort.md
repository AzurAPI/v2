# Sorting/Filter Information
##Return Value
> The payload when fetching results:

```json
{
  "Same format as the result in ship information but placed in an Array"
}
```

This section contains all the ships and equipment being sorted into an Array according to the functions indicated by the libraries.

### Filter ships by Faction or Nationality
```javascript
client.ships.hull(/*STRING (hull)*/); // GET SHIP BY HULL
client.ships.nationality(/*STRING (nationality)*/); // GET SHIP BY NATIONALITY
client.ships.getAll(/*STRING (query)*/); // QUERY EVERYTHING
```
