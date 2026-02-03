# Late::SelectSnapchatProfileRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Your Late profile ID |  |
| **selected_public_profile** | [**SelectSnapchatProfileRequestSelectedPublicProfile**](SelectSnapchatProfileRequestSelectedPublicProfile.md) |  |  |
| **temp_token** | **String** | Temporary Snapchat access token from OAuth |  |
| **user_profile** | **Object** | User profile data from OAuth redirect |  |
| **refresh_token** | **String** | Snapchat refresh token (if available) | [optional] |
| **expires_in** | **Integer** | Token expiration time in seconds | [optional] |
| **redirect_url** | **String** | Custom redirect URL after connection completes | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectSnapchatProfileRequest.new(
  profile_id: null,
  selected_public_profile: null,
  temp_token: null,
  user_profile: null,
  refresh_token: null,
  expires_in: null,
  redirect_url: null
)
```

