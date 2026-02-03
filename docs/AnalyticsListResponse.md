# Late::AnalyticsListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **overview** | [**AnalyticsOverview**](AnalyticsOverview.md) |  | [optional] |
| **posts** | [**Array&lt;AnalyticsListResponsePostsInner&gt;**](AnalyticsListResponsePostsInner.md) |  | [optional] |
| **pagination** | [**Pagination**](Pagination.md) |  | [optional] |
| **accounts** | [**Array&lt;SocialAccount&gt;**](SocialAccount.md) | Connected social accounts (followerCount and followersLastUpdated only included if user has analytics add-on) | [optional] |
| **has_analytics_access** | **Boolean** | Whether user has analytics add-on access | [optional] |

## Example

```ruby
require 'late'

instance = Late::AnalyticsListResponse.new(
  overview: null,
  posts: null,
  pagination: null,
  accounts: null,
  has_analytics_access: null
)
```

