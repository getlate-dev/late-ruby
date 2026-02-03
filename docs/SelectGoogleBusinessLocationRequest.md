# Late::SelectGoogleBusinessLocationRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Profile ID from your connection flow |  |
| **location_id** | **String** | The Google Business location ID selected by the user |  |
| **temp_token** | **String** | Temporary Google access token from OAuth |  |
| **user_profile** | [**SelectGoogleBusinessLocationRequestUserProfile**](SelectGoogleBusinessLocationRequestUserProfile.md) |  | [optional] |
| **redirect_url** | **String** | Optional custom redirect URL to return to after selection | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectGoogleBusinessLocationRequest.new(
  profile_id: null,
  location_id: null,
  temp_token: null,
  user_profile: null,
  redirect_url: null
)
```

