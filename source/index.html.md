---
title: NeeuroOS SDK Documentation

language_tabs: # must be one of https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers
#  - shell
#  - ruby
#  - python
#  - javascript
  - Android
  - iOS
  - Unity
  - Windows

toc_footers:
  - <a href='#'>Sign Up for a Developer Code</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the NeeuroOS API V1
---

# Introduction

The NeeuroOS is s scalable platform for the SenzeBand. It enables the interpretation of cognitive mental states, from raw EEG signals to the development of interventions for brain health challenges.

Provided in the NeeuroOS SDK are functions that connect to the SenzeBand through Bluetooth and features that incorporate Artificial Intelligence or Machine Learning algorithms that provide insights from EEG signals.

Neeuro's own proprietary applications and solutions are built based on the NeeuroOS SDK that have had years of clinical trials, scientific evidence and patents, providing the necessary validation for the community.

This NeeuroOS SDK provides the community of developers access to Neeuro SenzeBand's capabilities and its various algorithms to create their own applications to transform lives.

Turn your vision to reality with NeeuroOS today!

# Authentication

> To authorize, use this code:

```Android
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: meowmeowmeow"
```

```iOS
require 'NeeuroOS'

api = NeeuroOS::APIClient.authorize!('meowmeowmeow')
```

```Unity
import NeeuroOS

api = NeeuroOS.authorize('meowmeowmeow')
```

```Windows
const NeeuroOS = require('NeeuroOS');

let api = NeeuroOS.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

NeeuroOS uses API keys to allow access to the API. You can register a new NeeuroOS API key at our [developer portal](http://example.com/developers).

NeeuroOS expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Kittens

## Get All Kittens

```ruby
require 'NeeuroOS'

api = NeeuroOS::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import NeeuroOS

api = NeeuroOS.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens" \
  -H "Authorization: meowmeowmeow"
```

```javascript
const NeeuroOS = require('NeeuroOS');

let api = NeeuroOS.authorize('meowmeowmeow');
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

## Get a Specific Kitten

```ruby
require 'NeeuroOS'

api = NeeuroOS::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import NeeuroOS

api = NeeuroOS.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2" \
  -H "Authorization: meowmeowmeow"
```

```javascript
const NeeuroOS = require('NeeuroOS');

let api = NeeuroOS.authorize('meowmeowmeow');
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

## Delete a Specific Kitten

```ruby
require 'NeeuroOS'

api = NeeuroOS::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import NeeuroOS

api = NeeuroOS.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```javascript
const NeeuroOS = require('NeeuroOS');

let api = NeeuroOS.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete
