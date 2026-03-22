# Late::InstagramDemographicsResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **account_id** | **String** | The Zernio SocialAccount ID | [optional] |
| **platform** | **String** |  | [optional] |
| **metric** | **String** |  | [optional] |
| **timeframe** | **String** | The timeframe used for demographic data | [optional] |
| **demographics** | **Hash&lt;String, Array&lt;InstagramDemographicsResponseDemographicsValueInner&gt;&gt;** | Object keyed by breakdown dimension (age, city, country, gender) | [optional] |
| **note** | **String** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::InstagramDemographicsResponse.new(
  success: true,
  account_id: null,
  platform: instagram,
  metric: null,
  timeframe: null,
  demographics: null,
  note: Demographics show top 45 entries per dimension. Requires 100+ followers.
)
```

