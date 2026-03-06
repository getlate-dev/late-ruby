# Late::RecyclingState

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **enabled** | **Boolean** | Whether recycling is currently active | [optional] |
| **gap** | **Integer** | Number of interval units between reposts | [optional] |
| **gap_freq** | **String** | Interval unit (week or month) | [optional] |
| **start_date** | **Time** |  | [optional] |
| **expire_count** | **Integer** |  | [optional] |
| **expire_date** | **Time** |  | [optional] |
| **content_variations** | **Array&lt;String&gt;** | Content variations for recycled copies (if configured) | [optional] |
| **content_variation_index** | **Integer** | Current position in the content variations rotation (read-only) | [optional] |
| **recycle_count** | **Integer** | How many recycled copies have been created so far (read-only) | [optional] |
| **next_recycle_at** | **Time** | When the next recycled copy will be created (read-only) | [optional] |
| **last_recycled_at** | **Time** | When the last recycled copy was created (read-only) | [optional] |

## Example

```ruby
require 'late'

instance = Late::RecyclingState.new(
  enabled: null,
  gap: null,
  gap_freq: null,
  start_date: null,
  expire_count: null,
  expire_date: null,
  content_variations: null,
  content_variation_index: null,
  recycle_count: null,
  next_recycle_at: null,
  last_recycled_at: null
)
```

