# Late::GetYouTubeTranscript200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **video_id** | **String** |  | [optional] |
| **language** | **String** |  | [optional] |
| **full_text** | **String** |  | [optional] |
| **segments** | [**Array&lt;GetYouTubeTranscript200ResponseSegmentsInner&gt;**](GetYouTubeTranscript200ResponseSegmentsInner.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetYouTubeTranscript200Response.new(
  success: null,
  video_id: null,
  language: null,
  full_text: null,
  segments: null
)
```

