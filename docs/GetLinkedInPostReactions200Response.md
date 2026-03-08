# Late::GetLinkedInPostReactions200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_type** | **String** |  | [optional] |
| **username** | **String** |  | [optional] |
| **post_urn** | **String** |  | [optional] |
| **reactions** | [**Array&lt;GetLinkedInPostReactions200ResponseReactionsInner&gt;**](GetLinkedInPostReactions200ResponseReactionsInner.md) |  | [optional] |
| **pagination** | [**GetLinkedInPostReactions200ResponsePagination**](GetLinkedInPostReactions200ResponsePagination.md) |  | [optional] |
| **last_updated** | **Time** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetLinkedInPostReactions200Response.new(
  account_id: null,
  platform: linkedin,
  account_type: organization,
  username: null,
  post_urn: null,
  reactions: null,
  pagination: null,
  last_updated: null
)
```

