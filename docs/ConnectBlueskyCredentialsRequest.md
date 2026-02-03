# Late::ConnectBlueskyCredentialsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** | Your Bluesky handle (e.g. user.bsky.social) or email address |  |
| **app_password** | **String** | App password generated from Bluesky Settings &gt; App Passwords |  |
| **state** | **String** | Required state parameter formatted as &#x60;{userId}-{profileId}&#x60;. - &#x60;userId&#x60;: Your Late user ID (get from &#x60;GET /v1/users&#x60; → &#x60;currentUserId&#x60;) - &#x60;profileId&#x60;: The profile ID to connect the account to (get from &#x60;GET /v1/profiles&#x60;)  |  |
| **redirect_uri** | **String** | Optional URL to redirect to after successful connection | [optional] |

## Example

```ruby
require 'late'

instance = Late::ConnectBlueskyCredentialsRequest.new(
  identifier: null,
  app_password: null,
  state: 6507a1b2c3d4e5f6a7b8c9d0-6507a1b2c3d4e5f6a7b8c9d1,
  redirect_uri: null
)
```

