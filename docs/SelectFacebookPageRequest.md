# Late::SelectFacebookPageRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Profile ID from your connection flow |  |
| **page_id** | **String** | The Facebook Page ID selected by the user |  |
| **temp_token** | **String** | Temporary Facebook access token from OAuth |  |
| **user_profile** | [**SelectFacebookPageRequestUserProfile**](SelectFacebookPageRequestUserProfile.md) |  | [optional] |
| **redirect_url** | **String** | Optional custom redirect URL to return to after selection | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectFacebookPageRequest.new(
  profile_id: null,
  page_id: null,
  temp_token: null,
  user_profile: null,
  redirect_url: null
)
```

