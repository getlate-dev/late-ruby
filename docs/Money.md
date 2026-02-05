# Late::Money

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency_code** | **String** | ISO 4217 currency code (e.g. USD, EUR) |  |
| **units** | **String** | Whole units of the amount |  |
| **nanos** | **Integer** | Nano units (10^-9) of the amount | [optional] |

## Example

```ruby
require 'late'

instance = Late::Money.new(
  currency_code: null,
  units: null,
  nanos: null
)
```

