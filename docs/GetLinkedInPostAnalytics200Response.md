# Late::GetLinkedInPostAnalytics200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_type** | **String** |  | [optional] |
| **username** | **String** |  | [optional] |
| **post_urn** | **String** |  | [optional] |
| **analytics** | [**GetLinkedInPostAnalytics200ResponseAnalytics**](GetLinkedInPostAnalytics200ResponseAnalytics.md) |  | [optional] |
| **last_updated** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetLinkedInPostAnalytics200Response.new(
  account_id: null,
  platform: linkedin,
  account_type: null,
  username: null,
  post_urn: null,
  analytics: null,
  last_updated: null
)
```

