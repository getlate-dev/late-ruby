# Late::BulkUploadPosts200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **total_rows** | **Integer** |  | [optional] |
| **created** | **Integer** |  | [optional] |
| **failed** | **Integer** |  | [optional] |
| **errors** | [**Array&lt;BulkUploadPosts200ResponseErrorsInner&gt;**](BulkUploadPosts200ResponseErrorsInner.md) |  | [optional] |
| **posts** | [**Array&lt;Post&gt;**](Post.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::BulkUploadPosts200Response.new(
  success: null,
  total_rows: null,
  created: null,
  failed: null,
  errors: null,
  posts: null
)
```

