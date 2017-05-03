# Contacts
The Contacts resource lists contacts on an individual account or on all accounts.


### Route
``GET /<version>/contacts``

``GET /<version>/contacts/<accountid>``

### GET response


```json
{
  "result": "success",
  "contactdetails": [
    {
      "accountid": "666",
      "contactid": "1337",
      "firstname": "John",
      "lastname": "Doe",
      "companyname": "Nice Customer",
      "email": "payables@nicecustomer.co",
      "phonenumber": "",
      "subaccount": false
    },
    {
      "accountid": "666",
      "contactid": "2458",
      "firstname": "Jonh",
      "lastname": "Bull",
      "companyname": "Nice Consultant",
      "email": "john@consultants.com",
      "phonenumber": "+44-555-666-7777",
      "subaccount": true
    }
  ]
}
```
