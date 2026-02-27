# Late::ValidatePostLength200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** |  | [optional] |
| **platforms** | [**Hash&lt;String, ValidatePostLength200ResponsePlatformsValue&gt;**](ValidatePostLength200ResponsePlatformsValue.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ValidatePostLength200Response.new(
  text: null,
  platforms: {&quot;twitter&quot;:{&quot;count&quot;:51,&quot;limit&quot;:280,&quot;valid&quot;:true},&quot;twitterPremium&quot;:{&quot;count&quot;:51,&quot;limit&quot;:25000,&quot;valid&quot;:true},&quot;instagram&quot;:{&quot;count&quot;:51,&quot;limit&quot;:2200,&quot;valid&quot;:true},&quot;bluesky&quot;:{&quot;count&quot;:51,&quot;limit&quot;:300,&quot;valid&quot;:true},&quot;snapchat&quot;:{&quot;count&quot;:51,&quot;limit&quot;:160,&quot;valid&quot;:true}}
)
```

