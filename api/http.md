---
description: "Simple HTTP api"
---

# Simple yet effective HTTP api (Work in Progress!)

## Gettings started

Because of certain security measurements we will always expect a token. This token can be found in your dashboard settings.
For this example we'll use a fake token.

## Create a payment request

There is one url which we use to create a payment. The response however depends on the data you put in it.
You can redirect your user to the HTTP link and they will finish their payment and safely return to your app/website or other solution.
First you create the request.

```php
POST /api/create/
```

| Name | Type | Description |
| --- | --- | --- |
| `token` | `required` | The token you can find in your dashboard settings |
| `id` | `required` | An unique id which you can use to verify the payment |
| `amount` | `required` | The amount you want to charge the customer |
| `type` | `optional` | When not given, the url will return a payment link. When the value is `direct` the user can (and should) be redirected to the specific url. If omitted or `link` is given the url will respond with a generated payment link |
| `response` | `optional` | When not given, the payment will just show the verification page and nothing more. When an url is given the user will be redirect to that url after a payment has been completed or failed |

### Example

```json
{
  "token": "spJA4nChfSPDRSkD-Znb6iw-2WGkDR37GyxZ-GZomUo",
  "id": "PR-000012457",
  "amount": "12,25",
  "type": "direct",
  "response": "https://payrequest.io/responsehandler"
}
```

### Type = link or omitted

The response will be as shown:

```json
{
  "url": "https://link.payrequest.io/630ep3t"
}
```

### Return response

After the payment has been succesfull or failed the url will return the user to the response url when given.
The return will be `GET 200` for a succesfull payment and `GET 500` for an unsucesfull payment.
For extra check we also attach a `return_id` which will consist of the `token` + `id` encrpyted with `argon2`.

## Retrieve payment

***COMING SOON***
