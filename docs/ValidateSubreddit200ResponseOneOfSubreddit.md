# Late::ValidateSubreddit200ResponseOneOfSubreddit

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  | [optional] |
| **title** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **subscribers** | **Integer** |  | [optional] |
| **is_nsfw** | **Boolean** |  | [optional] |
| **type** | **String** |  | [optional] |
| **allow_images** | **Boolean** |  | [optional] |
| **allow_videos** | **Boolean** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ValidateSubreddit200ResponseOneOfSubreddit.new(
  name: programming,
  title: programming,
  description: Computer Programming,
  subscribers: 6844284,
  is_nsfw: null,
  type: public,
  allow_images: null,
  allow_videos: null
)
```

