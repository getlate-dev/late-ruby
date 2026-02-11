# Late::SendInboxMessageRequestButtonsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Button type. phone is Facebook only. |  |
| **title** | **String** | Button label (max 20 chars) |  |
| **url** | **String** | URL for url-type buttons | [optional] |
| **payload** | **String** | Payload for postback-type buttons | [optional] |
| **phone** | **String** | Phone number for phone-type buttons (Facebook only) | [optional] |

## Example

```ruby
require 'late'

instance = Late::SendInboxMessageRequestButtonsInner.new(
  type: null,
  title: null,
  url: null,
  payload: null,
  phone: null
)
```

