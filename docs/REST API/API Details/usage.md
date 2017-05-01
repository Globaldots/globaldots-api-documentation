# Usage

The usage resource provides details about the aggregate monthly usage on an account, as pulled by Globaldots integration systems.

Usage data is updated on a MONTHLY basis. 

### Routes
Usage on an account by accountid
``GET /usage/<accountid>``

#### GET Response

```json
{
  "result": "success",
  "accountid": "666",
  "usagedetails": [
    {
      "reporting_period": "2017-01-01 00:00:00",
      "vendor": "cdnetworks",
      "vendorid": "DDB56B98384A85ACA16B22B5340F241F",
      "account_type": "subaccount",
      "servicename": "Nice Customer",
      "serviceid": "cdn",
      "service": "Content Acceleration",
      "region": "global",
      "uom": "GB",
      "qty": "123456.000000"
    },
    {
      "reporting_period": "2017-01-01 00:00:00",
      "vendor": "chinanetcenter",
      "vendorid": "Nice-Customer",
      "account_type": "account",
      "servicename": "Nice Customer",
      "serviceid": "cdn",
      "service": "cdn",
      "region": "cn",
      "uom": "GB",
      "qty": "678.310000"
    },
    {
      "reporting_period": "2017-01-01 00:00:00",
      "vendor": "level3",
      "vendorid": "234678",
      "account_type": "subaccount",
      "servicename": "NiceCustomer",
      "serviceid": "cdn",
      "service": "caching",
      "region": "global",
      "uom": "GB",
      "qty": "157.114860"
    },
    {
      "reporting_period": "2017-01-01 00:00:00",
      "vendor": "level3",
      "vendorid": "234678",
      "account_type": "subaccount",
      "servicename": "NiceCustomer",
      "serviceid": "cdn",
      "service": "caching",
      "region": "global",
      "uom": "hits",
      "qty": "2670936.000000"
    }
  ]
}
```

#### Response Details

- `isVoiceEnabled`: Is EVE Voice enabled.
- `motd`: Fleet MOTD in CCP flavoured HTML.
- `isFreeMove`: Is free-move enabled.
- `isRegistered`: Does the fleet have an active fleet advertisement.
- `members`: Contains link to the fleet's members collection.
- `wings`: Contains link to the fleet's wings collection.

### PUT

- **Scope:** `fleetWrite`

#### Sample Request

**Media type:** `application/vnd.ccp.eve.FleetUpdate-v1+json`

```json
{
	"isFreeMove": true,
	"motd": "This is an <b>awesome</b> fleet, and it needs an even <font size=24 color=#ffff0000>more awesome</font> MOTD!!!"
}
```

#### Request Details

- `isFreeMove`: Should free-move be enabled in the fleet. Optional.
- `motd`: New fleet MOTD in CCP flavoured HTML. Optional.

## References

- [Patch notes](https://community.eveonline.com/news/patch-notes/patch-notes-for-eve-online-citadel) for EVE Online: Citadel
