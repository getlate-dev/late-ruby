# Late::CompleteTelegramConnect200Response

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'late'

Late::CompleteTelegramConnect200Response.openapi_one_of
# =>
# [
#   :'Connected',
#   :'Expired',
#   :'Pending'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'late'

Late::CompleteTelegramConnect200Response.build(data)
# => #<Connected:0x00007fdd4aab02a0>

Late::CompleteTelegramConnect200Response.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `Connected`
- `Expired`
- `Pending`
- `nil` (if no type matches)

