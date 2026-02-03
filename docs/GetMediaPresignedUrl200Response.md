# Late::GetMediaPresignedUrl200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **upload_url** | **String** | Presigned URL to PUT your file to (expires in 1 hour) | [optional] |
| **public_url** | **String** | Public URL where the file will be accessible after upload | [optional] |
| **key** | **String** | Storage key/path of the file | [optional] |
| **type** | **String** | Detected file type based on content type | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetMediaPresignedUrl200Response.new(
  upload_url: null,
  public_url: null,
  key: null,
  type: null
)
```

