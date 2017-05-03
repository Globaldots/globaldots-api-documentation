# Accounts

The accounts resource allows an application to list the accounts associated with a customer, and to view detailed information about the account. 

### Routes
A list of accounts associated with the API key

``GET /<version>/accounts``

A single account by accountid

``GET /<version>/accounts/<accountid>``

### GET response
If more than one accounts are associated with the API key, they will be in the `clientsdetails` response list. 
```json
{
  "result": "success",
  "clientsdetails": [
    {
      "id": "666",
      "firstname": "Jane",
      "lastname": "Doe",
      "companyname": "Nice Customer",
      "email": "jdoe@nicecustomer.co",
      "address1": "81 rue Raymond Lefoo",
      "address2": "",
      "city": "Nice",
      "state": "",
      "postcode": "7777",
      "country": "FR",
      "phonenumber": "",
      "datecreated": "2014-02-05",
      "lastlogin": "2015-11-24 09:45:08",
      "status": "Active",
      "language": "",
      "emailoptout": "0",
      "groupname": "Danidin Ltd",
      "salesman": "Eric Sciocchetti",
      "currency_name": "EUR"
    }
  ]
}
```