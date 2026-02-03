# Late::YouTubeScopeMissingResponseScopeStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **has_analytics_scope** | **Boolean** |  | [optional] |
| **requires_reauthorization** | **Boolean** |  | [optional] |
| **reauthorize_url** | **String** | URL to redirect user for reauthorization | [optional] |

## Example

```ruby
require 'late'

instance = Late::YouTubeScopeMissingResponseScopeStatus.new(
  has_analytics_scope: false,
  requires_reauthorization: true,
  reauthorize_url: null
)
```

