# Late::ListContacts200ResponseContactsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **company** | **String** |  | [optional] |
| **avatar_url** | **String** |  | [optional] |
| **tags** | **Array&lt;String&gt;** |  | [optional] |
| **is_subscribed** | **Boolean** |  | [optional] |
| **is_blocked** | **Boolean** |  | [optional] |
| **last_message_sent_at** | **Time** |  | [optional] |
| **last_message_received_at** | **Time** |  | [optional] |
| **messages_sent_count** | **Integer** |  | [optional] |
| **messages_received_count** | **Integer** |  | [optional] |
| **custom_fields** | **Object** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **platform_identifier** | **String** |  | [optional] |
| **display_identifier** | **String** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::ListContacts200ResponseContactsInner.new(
  id: null,
  name: null,
  email: null,
  company: null,
  avatar_url: null,
  tags: null,
  is_subscribed: null,
  is_blocked: null,
  last_message_sent_at: null,
  last_message_received_at: null,
  messages_sent_count: null,
  messages_received_count: null,
  custom_fields: null,
  notes: null,
  created_at: null,
  platform: null,
  platform_identifier: null,
  display_identifier: null
)
```

