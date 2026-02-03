# Late::GetFollowerStats200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **accounts** | [**Array&lt;AccountWithFollowerStats&gt;**](AccountWithFollowerStats.md) |  | [optional] |
| **stats** | **Hash&lt;String, Array&lt;GetFollowerStats200ResponseStatsValueInner&gt;&gt;** |  | [optional] |
| **date_range** | [**GetFollowerStats200ResponseDateRange**](GetFollowerStats200ResponseDateRange.md) |  | [optional] |
| **granularity** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetFollowerStats200Response.new(
  accounts: null,
  stats: null,
  date_range: null,
  granularity: null
)
```

