# Late::DownloadResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** |  | [optional] |
| **title** | **String** |  | [optional] |
| **thumbnail** | **String** |  | [optional] |
| **duration** | **Integer** |  | [optional] |
| **formats** | [**Array&lt;DownloadFormat&gt;**](DownloadFormat.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::DownloadResponse.new(
  url: null,
  title: null,
  thumbnail: null,
  duration: null,
  formats: null
)
```

