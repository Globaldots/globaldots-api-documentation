# Billing

The billing resource lists the invoices existing on an account.


### Route
``GET /<version>/billing/<accountid>``


### GET response

```json
{
  "result": "success",
  "accountid": "666",
  "clientinvoices": [
    {
      "invoiceid": "6666",
      "invoicenum": "10666",
      "accountid": "666",
      "date": "2017-04-02",
      "duedate": "2017-05-01",
      "subtotal": "912.82",
      "tax": 0,
      "total": "912.82",
      "status": "Unpaid",
      "notes": "Some notes",
      "currencycode": "EUR",
      "items": [
        {
          "id": "13335",
          "description": "EdgeCast Standard CDN (01/04/2017 - 30/04/2017)",
          "amount": "6750.00",
          "taxed": true
        },
        {
          "id": "13336",
          "description": "Addon - EC Rules Engine (01/04/2017 - 30/04/2017)",
          "amount": "350.00",
          "taxed": true
        },
        {
          "id": "13337",
          "description": "Ngenix CDN Domain (01/04/2017 - 30/04/2017)",
          "amount": "777.00",
          "taxed": true
        },
        {
          "id": "13338",
          "description": "CNC CDN Services (01/04/2017 - 30/04/2017)\nCommitment Quantity: 10 MBPS",
          "amount": "1200.00",
          "taxed": true
        },
        {
          "id": "13339",
          "description": "Usage for 02-2017 : Edgecast CDN, 5069.30 GB X 0.06",
          "amount": "304.2",
          "taxed": true
        },
        {
          "id": "13340",
          "description": "Usage for 02-2017 : Ngenix CDN, 1241.4 GB X 0.3",
          "amount": "372.4",
          "taxed": true
        },
        {
          "id": "13341",
          "description": "Usage for 02-2017 : Ngenix Requests, 5080.9 GB X 0.02",
          "amount": "101.6",
          "taxed": true
        }
      ]
    }, 
	....
      ]
    }
  ]
}
```
