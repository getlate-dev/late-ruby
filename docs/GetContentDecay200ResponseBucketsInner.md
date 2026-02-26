# Late::GetContentDecay200ResponseBucketsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bucket_order** | **Integer** | Sort order (0 &#x3D; earliest, 6 &#x3D; latest) | [optional] |
| **bucket_label** | **String** | Human-readable label | [optional] |
| **avg_pct_of_final** | **Float** | Average % of final engagement reached (0-100) | [optional] |
| **post_count** | **Integer** | Number of posts with data in this bucket | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetContentDecay200ResponseBucketsInner.new(
  bucket_order: null,
  bucket_label: null,
  avg_pct_of_final: null,
  post_count: null
)
```

