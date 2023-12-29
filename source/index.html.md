---
title: NeeuroOS SDK Documentation

language_tabs: # must be one of https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers
#  - shell
#  - ruby
#  - python
#  - javascript
  - java: Android (Java)
  - objective_c: iOS (Objective C)
  - csharp: Unity (C#)

toc_footers:
  - <a href='#'>Sign Up for a Developer Code</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for NeeuroOS SDK
---

# Introduction

The NeeuroOS is s scalable platform for the SenzeBand. It enables the interpretation of cognitive mental states, from raw EEG signals to the development of interventions for brain health challenges.

Provided in the NeeuroOS SDK are functions that connect to the SenzeBand through Bluetooth and features that incorporate Artificial Intelligence or Machine Learning algorithms that provide insights from EEG signals.

Neeuro's own proprietary applications and solutions are built based on the NeeuroOS SDK that have had years of clinical trials, scientific evidence and patents, providing the necessary validation for the community.

The NeeuroOS SDK provides the community of developers access to Neeuro SenzeBand's capabilities and its various algorithms to create their own applications to transform lives.

Turn your vision to reality with NeeuroOS today!

## Release Notes

### Latest Version

The current release of NeeuroOS SDK is Version X.X.

### Previous Versions

Version 1.1 - DD MMM YYYY

- Bug fixes.
- Improvements.

Version 1.0 - DD MMM YYYY
- First release.


## System Requirements

The minimum hardware system (phone, tablet and computer) requirements needed are:

Parameter | Description
--------- | -----------
SenzeBand 1 | Bluetooth 4.0 & above (No longer supported)
SenzeBand 2 | Bluetooth 5.0 & above

Android system requirements:

Parameter | Description
--------- | -----------
Android API | Version 21 (Version 23 Recommended) & above
Android Studio | Version 4.0.1 & above

Apple iOS system requirements:

Parameter | Description
--------- | -----------
Apple Device OS | iOS 11.0 & above
Apple Xcode | Version 14 & above

Microsoft Windows requirements:

Parameter | Description
--------- | -----------
Microsoft Windows OS | Version 10 & above
Microsoft Visual Studio | Visual Studio 2022

## Data Output

The NeeuroOS SDK provides the following data output from the SenzeBand:

S/N | Parameter | Description
--- | --------- | -----------
1 | Attention | A score of 0 to 100 representing the mental state "Attention".
2 | Relaxation | A score of 0 to 100 representing the mental state "Relaxation".
3 | Mental Workload | A score of 0 to 100 representing the mental state "Mental Workload".
4 | Raw EEG Data | Raw analog EEG data at 250 samples per second.
5 | Raw EEG Data (200 ms) | Raw analog EEG data at 50 samples per 200 ms.
6 | Filtered EEG Data | Analog EEG data filtered with band pass filter (1 - 40 Hz) & 50 Hz notch filter).
7 | Accelerometer Values | X, Y and Z axis data.
8 | Normalised Frequency Waves | Normalised values for Delta, Theta, Alpha, Beta, Gamma, Low-Alpha, High-Alpha, Low-Beta & High-Beta.
9 | Raw Frequency Waves | Actual values for Delta, Theta, Alpha, Beta, Gamma, Low-Alpha, High-Alpha, Low-Beta & High-Beta.
10 | MCUID | A unique 32 character string that identifies each unique SenzeBand device.
11 | Battery Level | The remaining battery power level.


# Authentication

In order to use the NeeuroOS SDK, your app needs to use a "Developer Code" to authenticate with Neeuro's servers.

Every successful authentication will provide a "limited time" to access NeeuroOS SDK's functions.

`Authorization: NeeuroOS`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>


> To authorize, use this code:

```java
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: meowmeowmeow"
```

```objective_c
require 'NeeuroOS'

api = NeeuroOS::APIClient.authorize!('meowmeowmeow')
```

```csharp
import NeeuroOS

api = NeeuroOS.authorize('meowmeowmeow')
```
> Make sure to replace `meowmeowmeow` with your API key.

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
