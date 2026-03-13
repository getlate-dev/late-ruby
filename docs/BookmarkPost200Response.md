# Late::BookmarkPost200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **tweet_id** | **String** |  | [optional] |
| **bookmarked** | **Boolean** |  | [optional] |
| **platform** | **String** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::BookmarkPost200Response.new(
  status: success,
  tweet_id: null,
  bookmarked: null,
  platform: twitter
)
```

