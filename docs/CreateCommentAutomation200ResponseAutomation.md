# Late::CreateCommentAutomation200ResponseAutomation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **platform_post_id** | **String** |  | [optional] |
| **keywords** | **Array&lt;String&gt;** |  | [optional] |
| **match_mode** | **String** |  | [optional] |
| **dm_message** | **String** |  | [optional] |
| **comment_reply** | **String** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **stats** | [**CreateCommentAutomation200ResponseAutomationStats**](CreateCommentAutomation200ResponseAutomationStats.md) |  | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::CreateCommentAutomation200ResponseAutomation.new(
  id: null,
  name: null,
  platform: null,
  platform_post_id: null,
  keywords: null,
  match_mode: null,
  dm_message: null,
  comment_reply: null,
  is_active: null,
  stats: null,
  created_at: null
)
```

