# Late::TranscriptResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **transcript** | **String** |  | [optional] |
| **segments** | [**Array&lt;TranscriptSegment&gt;**](TranscriptSegment.md) |  | [optional] |
| **language** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::TranscriptResponse.new(
  transcript: null,
  segments: null,
  language: null
)
```

