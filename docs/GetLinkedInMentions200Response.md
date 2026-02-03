# Late::GetLinkedInMentions200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **urn** | **String** | The LinkedIn URN (person or organization) | [optional] |
| **type** | **String** | The type of entity (person or organization) | [optional] |
| **display_name** | **String** | Display name (provided, from API, or derived from vanity URL) | [optional] |
| **mention_format** | **String** | Ready-to-use mention format for post content | [optional] |
| **vanity_name** | **String** | The vanity name/slug (only for organization mentions) | [optional] |
| **warning** | **String** | Warning about clickable mentions (only present for person mentions if displayName was not provided) | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetLinkedInMentions200Response.new(
  urn: urn:li:person:4qj5ox-agD,
  type: person,
  display_name: Miquel Palet,
  mention_format: @[Miquel Palet](urn:li:person:4qj5ox-agD),
  vanity_name: microsoft,
  warning: For clickable person mentions, provide the displayName parameter with the exact name as shown on their LinkedIn profile.
)
```

