# Late::GetInboxConversationMessages200ResponseMessagesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **conversation_id** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **message** | **String** |  | [optional] |
| **sender_id** | **String** |  | [optional] |
| **sender_name** | **String** |  | [optional] |
| **direction** | **String** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **attachments** | [**Array&lt;GetInboxConversationMessages200ResponseMessagesInnerAttachmentsInner&gt;**](GetInboxConversationMessages200ResponseMessagesInnerAttachmentsInner.md) |  | [optional] |
| **subject** | **String** | Reddit message subject | [optional] |
| **story_reply** | **Boolean** | Instagram story reply | [optional] |
| **is_story_mention** | **Boolean** | Instagram story mention | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetInboxConversationMessages200ResponseMessagesInner.new(
  id: null,
  conversation_id: null,
  account_id: null,
  platform: null,
  message: null,
  sender_id: null,
  sender_name: null,
  direction: null,
  created_at: null,
  attachments: null,
  subject: null,
  story_reply: null,
  is_story_mention: null
)
```

