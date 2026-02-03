# Late::GetRedditSubreddits200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subreddits** | [**Array&lt;GetRedditSubreddits200ResponseSubredditsInner&gt;**](GetRedditSubreddits200ResponseSubredditsInner.md) |  | [optional] |
| **default_subreddit** | **String** | Currently set default subreddit for posting | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetRedditSubreddits200Response.new(
  subreddits: null,
  default_subreddit: null
)
```

