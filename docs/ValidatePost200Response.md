# Late::ValidatePost200Response

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'late'

Late::ValidatePost200Response.openapi_one_of
# =>
# [
#   :'ValidatePost200ResponseOneOf',
#   :'ValidatePost200ResponseOneOf1'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'late'

Late::ValidatePost200Response.build(data)
# => #<ValidatePost200ResponseOneOf:0x00007fdd4aab02a0>

Late::ValidatePost200Response.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `ValidatePost200ResponseOneOf`
- `ValidatePost200ResponseOneOf1`
- `nil` (if no type matches)

