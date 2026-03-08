# Late::GetPostReactions200ResponseReactionsInnerFrom

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **urn** | **String** | LinkedIn person or organization URN | [optional] |
| **name** | **String** | Reactor&#39;s display name | [optional] |
| **headline** | **String** | Reactor&#39;s headline/job title (LinkedIn only) | [optional] |
| **username** | **String** | LinkedIn vanity name | [optional] |
| **profile_picture** | **String** | Profile picture URL | [optional] |
| **profile_url** | **String** | Direct link to reactor&#39;s LinkedIn profile | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetPostReactions200ResponseReactionsInnerFrom.new(
  urn: null,
  name: null,
  headline: null,
  username: null,
  profile_picture: null,
  profile_url: null
)
```

