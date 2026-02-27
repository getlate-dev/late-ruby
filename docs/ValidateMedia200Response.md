# Late::ValidateMedia200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **valid** | **Boolean** |  | [optional] |
| **url** | **String** |  | [optional] |
| **error** | **String** | Error message if valid is false | [optional] |
| **content_type** | **String** |  | [optional] |
| **size** | **Integer** | File size in bytes | [optional] |
| **size_formatted** | **String** |  | [optional] |
| **type** | **String** |  | [optional] |
| **platform_limits** | [**Hash&lt;String, ValidateMedia200ResponsePlatformLimitsValue&gt;**](ValidateMedia200ResponsePlatformLimitsValue.md) | Per-platform size limit comparison (only present when size and type are known) | [optional] |

## Example

```ruby
require 'late'

instance = Late::ValidateMedia200Response.new(
  valid: null,
  url: null,
  error: null,
  content_type: image/jpeg,
  size: null,
  size_formatted: 245 KB,
  type: null,
  platform_limits: {&quot;instagram&quot;:{&quot;limit&quot;:8388608,&quot;limitFormatted&quot;:&quot;8.0 MB&quot;,&quot;withinLimit&quot;:true},&quot;twitter&quot;:{&quot;limit&quot;:5242880,&quot;limitFormatted&quot;:&quot;5.0 MB&quot;,&quot;withinLimit&quot;:true},&quot;bluesky&quot;:{&quot;limit&quot;:1000000,&quot;limitFormatted&quot;:&quot;977 KB&quot;,&quot;withinLimit&quot;:true}}
)
```

