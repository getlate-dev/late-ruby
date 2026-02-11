# Late::SendInboxMessageRequestTemplateElementsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **String** | Element title (max 80 chars) |  |
| **subtitle** | **String** | Element subtitle | [optional] |
| **image_url** | **String** | Element image URL | [optional] |
| **buttons** | [**Array&lt;SendInboxMessageRequestTemplateElementsInnerButtonsInner&gt;**](SendInboxMessageRequestTemplateElementsInnerButtonsInner.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::SendInboxMessageRequestTemplateElementsInner.new(
  title: null,
  subtitle: null,
  image_url: null,
  buttons: null
)
```

