# Late::GetTikTokCreatorInfo200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **creator** | [**GetTikTokCreatorInfo200ResponseCreator**](GetTikTokCreatorInfo200ResponseCreator.md) |  | [optional] |
| **privacy_levels** | [**Array&lt;GetTikTokCreatorInfo200ResponsePrivacyLevelsInner&gt;**](GetTikTokCreatorInfo200ResponsePrivacyLevelsInner.md) | Available privacy level options for this creator | [optional] |
| **posting_limits** | [**GetTikTokCreatorInfo200ResponsePostingLimits**](GetTikTokCreatorInfo200ResponsePostingLimits.md) |  | [optional] |
| **commercial_content_types** | [**Array&lt;GetTikTokCreatorInfo200ResponseCommercialContentTypesInner&gt;**](GetTikTokCreatorInfo200ResponseCommercialContentTypesInner.md) | Available commercial content disclosure options | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetTikTokCreatorInfo200Response.new(
  creator: null,
  privacy_levels: null,
  posting_limits: null,
  commercial_content_types: null
)
```

