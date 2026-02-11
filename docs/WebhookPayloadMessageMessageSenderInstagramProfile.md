# Late::WebhookPayloadMessageMessageSenderInstagramProfile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **is_follower** | **Boolean** | Whether the sender follows your Instagram business account | [optional] |
| **is_following** | **Boolean** | Whether your Instagram business account follows the sender | [optional] |
| **follower_count** | **Integer** | The sender&#39;s follower count on Instagram | [optional] |
| **is_verified** | **Boolean** | Whether the sender is a verified Instagram user | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadMessageMessageSenderInstagramProfile.new(
  is_follower: null,
  is_following: null,
  follower_count: null,
  is_verified: null
)
```

