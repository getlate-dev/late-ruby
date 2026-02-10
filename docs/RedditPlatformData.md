# Late::RedditPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subreddit** | **String** | Target subreddit name (without \&quot;r/\&quot; prefix). Overrides the default subreddit configured on the account connection. Use GET /api/v1/accounts/{id}/reddit-subreddits to list available subreddits.  | [optional] |
| **title** | **String** | Post title. Defaults to the first line of content, truncated to 300 characters. | [optional] |
| **url** | **String** | URL for link posts. If provided (and forceSelf is not true), creates a link post instead of a text post. | [optional] |
| **force_self** | **Boolean** | When true, creates a text/self post even when a URL or media is provided. | [optional] |

## Example

```ruby
require 'late'

instance = Late::RedditPlatformData.new(
  subreddit: socialmedia,
  title: null,
  url: null,
  force_self: null
)
```

