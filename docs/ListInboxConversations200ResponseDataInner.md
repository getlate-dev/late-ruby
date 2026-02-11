# Late::ListInboxConversations200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **account_username** | **String** |  | [optional] |
| **participant_id** | **String** |  | [optional] |
| **participant_name** | **String** |  | [optional] |
| **participant_picture** | **String** |  | [optional] |
| **last_message** | **String** |  | [optional] |
| **updated_time** | **Time** |  | [optional] |
| **status** | **String** |  | [optional] |
| **unread_count** | **Integer** | Number of unread messages | [optional] |
| **url** | **String** | Direct link to open the conversation on the platform (if available) | [optional] |
| **instagram_profile** | [**ListInboxConversations200ResponseDataInnerInstagramProfile**](ListInboxConversations200ResponseDataInnerInstagramProfile.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListInboxConversations200ResponseDataInner.new(
  id: null,
  platform: null,
  account_id: null,
  account_username: null,
  participant_id: null,
  participant_name: null,
  participant_picture: null,
  last_message: null,
  updated_time: null,
  status: null,
  unread_count: null,
  url: null,
  instagram_profile: null
)
```

