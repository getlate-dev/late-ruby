# Late::GetPostLogs200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **logs** | [**Array&lt;PostLog&gt;**](PostLog.md) |  | [optional] |
| **count** | **Integer** | Number of logs returned | [optional] |
| **post_id** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetPostLogs200Response.new(
  logs: null,
  count: null,
  post_id: null
)
```

