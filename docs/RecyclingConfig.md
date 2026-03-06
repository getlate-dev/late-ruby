# Late::RecyclingConfig

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **enabled** | **Boolean** | Set to false to disable recycling on this post | [optional][default to true] |
| **gap** | **Integer** | Number of interval units between each repost. Required when enabling recycling. | [optional] |
| **gap_freq** | **String** | Interval unit for the gap. Defaults to &#39;month&#39;. | [optional][default to &#39;month&#39;] |
| **start_date** | **Time** | When to start the recycling cycle. Defaults to the post&#39;s scheduledFor date. | [optional] |
| **expire_count** | **Integer** | Stop recycling after this many copies have been created | [optional] |
| **expire_date** | **Time** | Stop recycling after this date, regardless of count | [optional] |
| **content_variations** | **Array&lt;String&gt;** | Array of content variations for recycled copies. On each recycle, the next variation is used in round-robin order. Recommended for Twitter and Pinterest to avoid duplicate content flags. If omitted, the original post content is used for all recycled copies. Send an empty array [] to clear existing variations. Must have 2+ entries when setting variations. Platform-level customContent still overrides the base content per platform.  | [optional] |

## Example

```ruby
require 'late'

instance = Late::RecyclingConfig.new(
  enabled: null,
  gap: 2,
  gap_freq: null,
  start_date: null,
  expire_count: 5,
  expire_date: null,
  content_variations: null
)
```

