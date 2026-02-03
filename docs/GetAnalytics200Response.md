# Late::GetAnalytics200Response

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'late'

Late::GetAnalytics200Response.openapi_one_of
# =>
# [
#   :'AnalyticsListResponse',
#   :'AnalyticsSinglePostResponse'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'late'

Late::GetAnalytics200Response.build(data)
# => #<AnalyticsListResponse:0x00007fdd4aab02a0>

Late::GetAnalytics200Response.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `AnalyticsListResponse`
- `AnalyticsSinglePostResponse`
- `nil` (if no type matches)

