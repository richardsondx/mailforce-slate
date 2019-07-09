---
title: Mailforce API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Mailforce API! You can use our API to access Mailforce API endpoints.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/lord/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Mailforce uses API keys to allow access to the API. You can register a new Mailforce API key at our [developer portal](http://localhost:3000/developers).

Mailforce expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Plans

## Show all plans

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Show specific plan

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

# Authentication

This is done via the front-end but the gmail authorization is then passed to the back-end

# Users

## Show Profile

Show information about the loggeg in user

# Accounts

## Add Account

Handle The gmail response from the front-end process in order to create an account in the backend

## Delete Account

Remove an email account from the account

# Emails

## List all Drafts

Shows draft (that have the label mailforce) from the email account

## Show a Specific Draft

Show a specific draft  (that has  the label mailforce) from the email account

## Show Specific Email

Assistant can view a specific email from an account based on access scope

## Show Account Emails

Assistant can view a list of all email from an account based on access scope

## Send Draft

Send a specific email from the accocunt. An assistant can send an email if they have the right authorization

## Show Thread

Show an entire email thread from an account

## Show Thread Item

Show specific email from a thread

## Reply to Email

# Assistant

## Add Assistant

Add an assistant to an account

## Remove Assistant

Remove assistant from an account

## Update Assistant Settings

- Update the access right of an assistant in an account: read only access, write only access, read & write access
- or Change Access Scope (everyone, only, custom)
- or review_required (boolean)


# Pending Review

Manage emails that need reviews

## List draft that need review

Show all the drafts that nee dreview

## Show specific draft that need review

Show specific draft

## Approve Draft 

Once a draft is approved it is sent

## Reject a draft

When a draft is rejected it is not sent and its status is updated to revied.


# Subscription

## Subscribe to a plan

Create a new subscription for a user

## Cancel Subscription

Cancel a user subscription

## Add Credit Card

Add a new credit card to the email account

## Remove Credit Card

Remove credit card from the email account

## Update Default Credit Card

Change the curren card a user has associated to his account

# Payments

## Make a Payment

Process a payment request
