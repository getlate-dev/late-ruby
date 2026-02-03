# Late::PostLogResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform_post_id** | **String** | ID returned by platform on success | [optional] |
| **platform_post_url** | **String** | URL of published post | [optional] |
| **error_message** | **String** | Error message on failure | [optional] |
| **error_code** | **String** | Platform-specific error code | [optional] |
| **raw_body** | **String** | Full response body JSON (max 5000 chars) | [optional] |

## Example

```ruby
require 'late'

instance = Late::PostLogResponse.new(
  platform_post_id: null,
  platform_post_url: null,
  error_message: null,
  error_code: null,
  raw_body: null
)
```

