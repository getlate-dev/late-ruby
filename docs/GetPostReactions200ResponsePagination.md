# Late::GetPostReactions200ResponsePagination

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **has_more** | **Boolean** |  | [optional] |
| **cursor** | **String** | Offset for next page | [optional] |
| **total** | **Integer** | Total number of reactions (when available) | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetPostReactions200ResponsePagination.new(
  has_more: null,
  cursor: null,
  total: null
)
```

