# Late::GetInboxConversation200ResponseData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **account_username** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **participant_name** | **String** |  | [optional] |
| **participant_id** | **String** |  | [optional] |
| **last_message** | **String** |  | [optional] |
| **last_message_at** | **Time** |  | [optional] |
| **updated_time** | **Time** |  | [optional] |
| **participants** | [**Array&lt;UpdateFacebookPage200ResponseSelectedPage&gt;**](UpdateFacebookPage200ResponseSelectedPage.md) |  | [optional] |
| **instagram_profile** | [**ListInboxConversations200ResponseDataInnerInstagramProfile**](ListInboxConversations200ResponseDataInnerInstagramProfile.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetInboxConversation200ResponseData.new(
  id: null,
  account_id: null,
  account_username: null,
  platform: null,
  status: null,
  participant_name: null,
  participant_id: null,
  last_message: null,
  last_message_at: null,
  updated_time: null,
  participants: null,
  instagram_profile: null
)
```

