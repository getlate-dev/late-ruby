# Late::ListLogs200ResponsePagination

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Integer** | Total number of logs matching the query | [optional] |
| **limit** | **Integer** |  | [optional] |
| **skip** | **Integer** |  | [optional] |
| **pages** | **Integer** | Total number of pages | [optional] |
| **has_more** | **Boolean** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListLogs200ResponsePagination.new(
  total: null,
  limit: null,
  skip: null,
  pages: null,
  has_more: null
)
```

