# Late::SelectPinterestBoardRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Your Late profile ID |  |
| **board_id** | **String** | The Pinterest Board ID selected by the user |  |
| **board_name** | **String** | The board name (for display purposes) | [optional] |
| **temp_token** | **String** | Temporary Pinterest access token from OAuth |  |
| **user_profile** | **Object** | User profile data from OAuth redirect | [optional] |
| **refresh_token** | **String** | Pinterest refresh token (if available) | [optional] |
| **expires_in** | **Integer** | Token expiration time in seconds | [optional] |
| **redirect_url** | **String** | Custom redirect URL after connection completes | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectPinterestBoardRequest.new(
  profile_id: null,
  board_id: null,
  board_name: null,
  temp_token: null,
  user_profile: null,
  refresh_token: null,
  expires_in: null,
  redirect_url: null
)
```

