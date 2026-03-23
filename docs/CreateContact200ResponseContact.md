# Late::CreateContact200ResponseContact

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **company** | **String** |  | [optional] |
| **tags** | **Array&lt;String&gt;** |  | [optional] |
| **is_subscribed** | **Boolean** |  | [optional] |
| **is_blocked** | **Boolean** |  | [optional] |
| **custom_fields** | **Object** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::CreateContact200ResponseContact.new(
  id: null,
  name: null,
  email: null,
  company: null,
  tags: null,
  is_subscribed: null,
  is_blocked: null,
  custom_fields: null,
  notes: null,
  created_at: null
)
```

