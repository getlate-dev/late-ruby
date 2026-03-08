# Late::GetLinkedInPostReactions200ResponseReactionsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **reaction_type** | **String** | LinkedIn reaction enum (LIKE, PRAISE, EMPATHY, INTEREST, APPRECIATION, ENTERTAINMENT) | [optional] |
| **reaction_label** | **String** | User-friendly label (Like, Celebrate, Love, Insightful, Support, Funny) | [optional] |
| **reacted_at** | **Time** |  | [optional] |
| **from** | [**GetLinkedInPostReactions200ResponseReactionsInnerFrom**](GetLinkedInPostReactions200ResponseReactionsInnerFrom.md) |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetLinkedInPostReactions200ResponseReactionsInner.new(
  reaction_type: null,
  reaction_label: null,
  reacted_at: null,
  from: null
)
```

