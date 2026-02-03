# Late::GetPendingOAuthData200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | The platform (e.g., \&quot;linkedin\&quot;) | [optional] |
| **profile_id** | **String** | The Late profile ID | [optional] |
| **temp_token** | **String** | Temporary access token for the platform | [optional] |
| **refresh_token** | **String** | Refresh token (if available) | [optional] |
| **expires_in** | **Float** | Token expiry in seconds | [optional] |
| **user_profile** | **Object** | User profile data (id, username, displayName, profilePicture) | [optional] |
| **selection_type** | **String** | Type of selection data | [optional] |
| **organizations** | [**Array&lt;GetPendingOAuthData200ResponseOrganizationsInner&gt;**](GetPendingOAuthData200ResponseOrganizationsInner.md) | LinkedIn organizations (when selectionType is \&quot;organizations\&quot;) | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetPendingOAuthData200Response.new(
  platform: null,
  profile_id: null,
  temp_token: null,
  refresh_token: null,
  expires_in: null,
  user_profile: null,
  selection_type: null,
  organizations: null
)
```

