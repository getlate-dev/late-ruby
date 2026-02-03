# Late::ListQueueSlots200Response

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'late'

Late::ListQueueSlots200Response.openapi_one_of
# =>
# [
#   :'ListQueueSlots200ResponseOneOf',
#   :'ListQueueSlots200ResponseOneOf1'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'late'

Late::ListQueueSlots200Response.build(data)
# => #<ListQueueSlots200ResponseOneOf:0x00007fdd4aab02a0>

Late::ListQueueSlots200Response.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `ListQueueSlots200ResponseOneOf`
- `ListQueueSlots200ResponseOneOf1`
- `nil` (if no type matches)

