# ![LOGO](logo.png) GOV.UK Pay **flow**ground Connector

## Description

A generated **flow**ground connector for the GOV.UK Pay API (version 1.0.2).

Generated from: https://api.apis.guru/v2/specs/payments.service.gov.uk/payments/1.0.2/swagger.json<br/>
Generated at: 2019-05-07T17:43:38+03:00

## API Description

GOV.UK Pay API

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Search payments

> Search payments by reference, state, 'from' and 'to' date. The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'

#### Input Parameters
* `reference` - _optional_ - Your payment reference to search
* `email` - _optional_ - The user email used in the payment to be searched
* `state` - _optional_ - State of payments to be searched. Example=success
    Possible values: created, started, submitted, success, failed, cancelled, error.
* `card_brand` - _optional_ - Card brand used for payment. Example=master-card
* `from_date` - _optional_ - From date of payments to be searched (this date is inclusive). Example=2015-08-13T12:35:00Z
* `to_date` - _optional_ - To date of payments to be searched (this date is exclusive). Example=2015-08-14T12:35:00Z
* `page` - _optional_ - Page number requested for the search, should be a positive integer (optional, defaults to 1)
* `display_size` - _optional_ - Number of results to be shown per page, should be a positive integer (optional, defaults to 500, max 500)
* `cardholder_name` - _optional_ - Name on card used to make payment
* `first_digits_card_number` - _optional_ - First six digits of the card used to make payment
* `last_digits_card_number` - _optional_ - Last four digits of the card used to make payment

### Create new payment

> Create a new payment for the account associated to the Authorisation token. The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'

### Find payment by ID

> Return information about the payment The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'

#### Input Parameters
* `paymentId` - _required_ - Payment identifier

### Cancel payment

> Cancel a payment based on the provided payment ID and the Authorisation token. The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'. A payment can only be cancelled if it's in a state that isn't finished.

#### Input Parameters
* `paymentId` - _required_ - Payment identifier

### Capture payment

> Capture a payment based on the provided payment ID and the Authorisation token. The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'. A payment can only be captured if it's in 'submitted' state

#### Input Parameters
* `paymentId` - _required_ - Payment identifier

### Return payment events by ID

> Return payment events information about a certain payment The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'

#### Input Parameters
* `paymentId` - _required_ - Payment identifier

### Get all refunds for a payment

> Return refunds for a payment. The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'

*Tags:* `refunds`

#### Input Parameters
* `paymentId` - _required_

### Submit a refund for a payment

> Return issued refund information. The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'

*Tags:* `refunds`

#### Input Parameters
* `paymentId` - _required_ - paymentId

### Find payment refund by ID

> Return payment refund information by Refund ID The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'

*Tags:* `refunds`

#### Input Parameters
* `paymentId` - _required_
* `refundId` - _required_

### Search refunds

> Search refunds by 'from' and 'to' date. The Authorisation token needs to be specified in the 'authorization' header as 'authorization: Bearer YOUR_API_KEY_HERE'

*Tags:* `refunds`

#### Input Parameters
* `from_date` - _optional_ - From date of refunds to be searched (this date is inclusive). Example=2015-08-13T12:35:00Z
* `to_date` - _optional_ - To date of refunds to be searched (this date is exclusive). Example=2015-08-14T12:35:00Z
* `page` - _optional_ - Page number requested for the search, should be a positive integer (optional, defaults to 1)
* `display_size` - _optional_ - Number of results to be shown per page, should be a positive integer (optional, defaults to 500, max 500)

## License

**flow**ground :- Telekom iPaaS / payments-service-gov-uk-payments-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
