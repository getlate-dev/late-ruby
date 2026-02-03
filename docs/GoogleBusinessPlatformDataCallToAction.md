# Late::GoogleBusinessPlatformDataCallToAction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Button action type: - LEARN_MORE: Link to more information - BOOK: Booking/reservation link - ORDER: Online ordering link - SHOP: E-commerce/shopping link - SIGN_UP: Registration/signup link - CALL: Phone call action  |  |
| **url** | **String** | Destination URL for the CTA button (required when callToAction is provided) |  |

## Example

```ruby
require 'late'

instance = Late::GoogleBusinessPlatformDataCallToAction.new(
  type: null,
  url: null
)
```

