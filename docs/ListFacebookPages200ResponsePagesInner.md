# Late::ListFacebookPages200ResponsePagesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Facebook Page ID | [optional] |
| **name** | **String** | Page name | [optional] |
| **username** | **String** | Page username/handle (may be null) | [optional] |
| **access_token** | **String** | Page-specific access token | [optional] |
| **category** | **String** | Page category | [optional] |
| **tasks** | **Array&lt;String&gt;** | User permissions for this page | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListFacebookPages200ResponsePagesInner.new(
  id: null,
  name: null,
  username: null,
  access_token: null,
  category: null,
  tasks: null
)
```

