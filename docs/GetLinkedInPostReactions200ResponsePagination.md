# Late::GetLinkedInPostReactions200ResponsePagination

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **has_more** | **Boolean** |  | [optional] |
| **cursor** | **String** | Offset for next page | [optional] |
| **total** | **Integer** | Total number of reactions (when available) | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetLinkedInPostReactions200ResponsePagination.new(
  has_more: null,
  cursor: null,
  total: null
)
```

