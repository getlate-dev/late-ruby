# Late::SelectLinkedInOrganizationRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |
| **temp_token** | **String** |  |  |
| **user_profile** | **Object** |  |  |
| **account_type** | **String** |  |  |
| **selected_organization** | **Object** |  | [optional] |
| **redirect_url** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectLinkedInOrganizationRequest.new(
  profile_id: null,
  temp_token: null,
  user_profile: null,
  account_type: null,
  selected_organization: null,
  redirect_url: null
)
```

