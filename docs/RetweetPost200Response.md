# Late::RetweetPost200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **tweet_id** | **String** |  | [optional] |
| **retweeted** | **Boolean** |  | [optional] |
| **platform** | **String** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::RetweetPost200Response.new(
  status: success,
  tweet_id: null,
  retweeted: null,
  platform: twitter
)
```

