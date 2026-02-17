# Late::AnalyticsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_analytics**](AnalyticsApi.md#get_analytics) | **GET** /v1/analytics | Get post analytics |
| [**get_follower_stats**](AnalyticsApi.md#get_follower_stats) | **GET** /v1/accounts/follower-stats | Get follower stats |
| [**get_linked_in_aggregate_analytics**](AnalyticsApi.md#get_linked_in_aggregate_analytics) | **GET** /v1/accounts/{accountId}/linkedin-aggregate-analytics | Get LinkedIn aggregate stats |
| [**get_linked_in_post_analytics**](AnalyticsApi.md#get_linked_in_post_analytics) | **GET** /v1/accounts/{accountId}/linkedin-post-analytics | Get LinkedIn post stats |
| [**get_you_tube_daily_views**](AnalyticsApi.md#get_you_tube_daily_views) | **GET** /v1/analytics/youtube/daily-views | Get YouTube daily views |


## get_analytics

> <GetAnalytics200Response> get_analytics(opts)

Get post analytics

Returns analytics for posts. With `postId`, returns a single post's analytics. Without it, returns a paginated list with overview stats.  **Post ID types:** This endpoint returns External Post IDs by default. The `postId` parameter accepts both Late Post IDs (from `POST /v1/posts`) and External Post IDs. Late Post IDs are automatically resolved to External Post analytics. Use `latePostId` in responses to link analytics back to your original Late post, or `platformPostUrl` as a stable identifier.  **List response:** Use `isExternal` to identify post origin. `isExternal: true` means synced from platform, `isExternal: false` means queried by Late post ID.  For follower stats, use `/v1/accounts/follower-stats` instead.  **Platform notes:** - LinkedIn personal accounts: per-post analytics only for posts published through Late (API restriction). - Telegram: analytics not available (Bot API limitation).  **Data freshness:** Cached and refreshed at most once per hour. Stale caches trigger a background refresh. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AnalyticsApi.new
opts = {
  post_id: 'post_id_example', # String | Returns analytics for a single post. Accepts both Late Post IDs (from `POST /v1/posts`)  and External Post IDs (from this endpoint's list response). The API automatically  resolves Late Post IDs to their corresponding External Post analytics. 
  platform: 'platform_example', # String | Filter by platform (default \"all\")
  profile_id: 'profile_id_example', # String | Filter by profile ID (default \"all\")
  source: 'all', # String | Filter by post source: - `late` - Only posts scheduled/published via Late API - `external` - Only posts synced from the platform (not posted via Late) - `all` - All posts (default) 
  from_date: Date.parse('2013-10-20'), # Date | Inclusive lower bound
  to_date: Date.parse('2013-10-20'), # Date | Inclusive upper bound
  limit: 56, # Integer | Page size (default 50)
  page: 56, # Integer | Page number (default 1)
  sort_by: 'date', # String | Sort by date or engagement
  order: 'asc' # String | Sort order
}

begin
  # Get post analytics
  result = api_instance.get_analytics(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_analytics: #{e}"
end
```

#### Using the get_analytics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetAnalytics200Response>, Integer, Hash)> get_analytics_with_http_info(opts)

```ruby
begin
  # Get post analytics
  data, status_code, headers = api_instance.get_analytics_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetAnalytics200Response>
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_analytics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** | Returns analytics for a single post. Accepts both Late Post IDs (from &#x60;POST /v1/posts&#x60;)  and External Post IDs (from this endpoint&#39;s list response). The API automatically  resolves Late Post IDs to their corresponding External Post analytics.  | [optional] |
| **platform** | **String** | Filter by platform (default \&quot;all\&quot;) | [optional] |
| **profile_id** | **String** | Filter by profile ID (default \&quot;all\&quot;) | [optional] |
| **source** | **String** | Filter by post source: - &#x60;late&#x60; - Only posts scheduled/published via Late API - &#x60;external&#x60; - Only posts synced from the platform (not posted via Late) - &#x60;all&#x60; - All posts (default)  | [optional][default to &#39;all&#39;] |
| **from_date** | **Date** | Inclusive lower bound | [optional] |
| **to_date** | **Date** | Inclusive upper bound | [optional] |
| **limit** | **Integer** | Page size (default 50) | [optional][default to 50] |
| **page** | **Integer** | Page number (default 1) | [optional][default to 1] |
| **sort_by** | **String** | Sort by date or engagement | [optional][default to &#39;date&#39;] |
| **order** | **String** | Sort order | [optional][default to &#39;desc&#39;] |

### Return type

[**GetAnalytics200Response**](GetAnalytics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_follower_stats

> <GetFollowerStats200Response> get_follower_stats(opts)

Get follower stats

Returns follower count history and growth metrics for connected social accounts. **Requires analytics add-on subscription.**  **Data Freshness:** Follower counts are automatically refreshed once per day. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AnalyticsApi.new
opts = {
  account_ids: 'account_ids_example', # String | Comma-separated list of account IDs (optional, defaults to all user's accounts)
  profile_id: 'profile_id_example', # String | Filter by profile ID
  from_date: Date.parse('2013-10-20'), # Date | Start date in YYYY-MM-DD format (defaults to 30 days ago)
  to_date: Date.parse('2013-10-20'), # Date | End date in YYYY-MM-DD format (defaults to today)
  granularity: 'daily' # String | Data aggregation level
}

begin
  # Get follower stats
  result = api_instance.get_follower_stats(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_follower_stats: #{e}"
end
```

#### Using the get_follower_stats_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetFollowerStats200Response>, Integer, Hash)> get_follower_stats_with_http_info(opts)

```ruby
begin
  # Get follower stats
  data, status_code, headers = api_instance.get_follower_stats_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetFollowerStats200Response>
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_follower_stats_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_ids** | **String** | Comma-separated list of account IDs (optional, defaults to all user&#39;s accounts) | [optional] |
| **profile_id** | **String** | Filter by profile ID | [optional] |
| **from_date** | **Date** | Start date in YYYY-MM-DD format (defaults to 30 days ago) | [optional] |
| **to_date** | **Date** | End date in YYYY-MM-DD format (defaults to today) | [optional] |
| **granularity** | **String** | Data aggregation level | [optional][default to &#39;daily&#39;] |

### Return type

[**GetFollowerStats200Response**](GetFollowerStats200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_linked_in_aggregate_analytics

> <GetLinkedInAggregateAnalytics200Response> get_linked_in_aggregate_analytics(account_id, opts)

Get LinkedIn aggregate stats

Returns aggregate analytics across all posts for a LinkedIn personal account. Organization accounts should use `/v1/analytics` instead.  **Required scope:** `r_member_postAnalytics`. Missing scope returns 403 with reconnect instructions.  **Aggregation:** `TOTAL` (default, lifetime totals) or `DAILY` (time series). Use `startDate`/`endDate` to filter by date range. Note: `MEMBERS_REACHED` is not available with `DAILY` aggregation. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AnalyticsApi.new
account_id = 'account_id_example' # String | The ID of the LinkedIn personal account
opts = {
  aggregation: 'TOTAL', # String | Type of aggregation for the analytics data. - `TOTAL` (default): Returns single totals for each metric - `DAILY`: Returns daily breakdown of metrics  Note: `MEMBERS_REACHED` metric is not available with `DAILY` aggregation. 
  start_date: Date.parse('2024-01-01'), # Date | Start date for analytics data in YYYY-MM-DD format. If provided without endDate, endDate defaults to today. If omitted entirely, returns lifetime analytics. 
  end_date: Date.parse('2024-01-31'), # Date | End date for analytics data in YYYY-MM-DD format (exclusive). If provided without startDate, startDate defaults to 30 days before endDate. 
  metrics: 'IMPRESSION,REACTION,COMMENT' # String | Comma-separated list of metrics to fetch. If omitted, fetches all available metrics. Valid values: IMPRESSION, MEMBERS_REACHED, REACTION, COMMENT, RESHARE 
}

begin
  # Get LinkedIn aggregate stats
  result = api_instance.get_linked_in_aggregate_analytics(account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_linked_in_aggregate_analytics: #{e}"
end
```

#### Using the get_linked_in_aggregate_analytics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetLinkedInAggregateAnalytics200Response>, Integer, Hash)> get_linked_in_aggregate_analytics_with_http_info(account_id, opts)

```ruby
begin
  # Get LinkedIn aggregate stats
  data, status_code, headers = api_instance.get_linked_in_aggregate_analytics_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetLinkedInAggregateAnalytics200Response>
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_linked_in_aggregate_analytics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The ID of the LinkedIn personal account |  |
| **aggregation** | **String** | Type of aggregation for the analytics data. - &#x60;TOTAL&#x60; (default): Returns single totals for each metric - &#x60;DAILY&#x60;: Returns daily breakdown of metrics  Note: &#x60;MEMBERS_REACHED&#x60; metric is not available with &#x60;DAILY&#x60; aggregation.  | [optional][default to &#39;TOTAL&#39;] |
| **start_date** | **Date** | Start date for analytics data in YYYY-MM-DD format. If provided without endDate, endDate defaults to today. If omitted entirely, returns lifetime analytics.  | [optional] |
| **end_date** | **Date** | End date for analytics data in YYYY-MM-DD format (exclusive). If provided without startDate, startDate defaults to 30 days before endDate.  | [optional] |
| **metrics** | **String** | Comma-separated list of metrics to fetch. If omitted, fetches all available metrics. Valid values: IMPRESSION, MEMBERS_REACHED, REACTION, COMMENT, RESHARE  | [optional] |

### Return type

[**GetLinkedInAggregateAnalytics200Response**](GetLinkedInAggregateAnalytics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_linked_in_post_analytics

> <GetLinkedInPostAnalytics200Response> get_linked_in_post_analytics(account_id, urn)

Get LinkedIn post stats

Returns analytics for a specific LinkedIn post using its URN. Works for both personal and organization accounts.  This is useful for fetching analytics of posts that weren't published through Late, as long as you have the post URN.  **For Personal Accounts:** - Uses `memberCreatorPostAnalytics` API + `memberCreatorVideoAnalytics` for video posts - Requires `r_member_postAnalytics` scope - Available metrics: impressions, reach, likes, comments, shares, video views (video posts only) - **Clicks are NOT available** for personal accounts  **For Organization Accounts:** - Uses `organizationalEntityShareStatistics` API + `videoAnalytics` for video posts - Requires `r_organization_social` scope - Available metrics: impressions, reach, clicks, likes, comments, shares, video views (video posts only), engagement rate 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AnalyticsApi.new
account_id = 'account_id_example' # String | The ID of the LinkedIn account
urn = 'urn:li:share:7123456789012345678' # String | The LinkedIn post URN

begin
  # Get LinkedIn post stats
  result = api_instance.get_linked_in_post_analytics(account_id, urn)
  p result
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_linked_in_post_analytics: #{e}"
end
```

#### Using the get_linked_in_post_analytics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetLinkedInPostAnalytics200Response>, Integer, Hash)> get_linked_in_post_analytics_with_http_info(account_id, urn)

```ruby
begin
  # Get LinkedIn post stats
  data, status_code, headers = api_instance.get_linked_in_post_analytics_with_http_info(account_id, urn)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetLinkedInPostAnalytics200Response>
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_linked_in_post_analytics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The ID of the LinkedIn account |  |
| **urn** | **String** | The LinkedIn post URN |  |

### Return type

[**GetLinkedInPostAnalytics200Response**](GetLinkedInPostAnalytics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_you_tube_daily_views

> <YouTubeDailyViewsResponse> get_you_tube_daily_views(video_id, account_id, opts)

Get YouTube daily views

Returns historical daily view counts for a specific YouTube video. Uses YouTube Analytics API v2 to fetch daily breakdowns including views, watch time, and subscriber changes.  **Required Scope:** This endpoint requires the `yt-analytics.readonly` OAuth scope. Existing YouTube accounts may need to re-authorize to grant this permission. If the scope is missing, the response will include a `reauthorizeUrl`.  **Data Latency:** YouTube Analytics data has a 2-3 day delay. The `endDate` is automatically capped to 3 days ago.  **Date Range:** Maximum 90 days of historical data available. Defaults to last 30 days. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AnalyticsApi.new
video_id = 'video_id_example' # String | The YouTube video ID (e.g., \"dQw4w9WgXcQ\")
account_id = 'account_id_example' # String | The Late account ID for the YouTube account
opts = {
  start_date: Date.parse('2013-10-20'), # Date | Start date (YYYY-MM-DD). Defaults to 30 days ago.
  end_date: Date.parse('2013-10-20') # Date | End date (YYYY-MM-DD). Defaults to 3 days ago (YouTube data latency).
}

begin
  # Get YouTube daily views
  result = api_instance.get_you_tube_daily_views(video_id, account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_you_tube_daily_views: #{e}"
end
```

#### Using the get_you_tube_daily_views_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<YouTubeDailyViewsResponse>, Integer, Hash)> get_you_tube_daily_views_with_http_info(video_id, account_id, opts)

```ruby
begin
  # Get YouTube daily views
  data, status_code, headers = api_instance.get_you_tube_daily_views_with_http_info(video_id, account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <YouTubeDailyViewsResponse>
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_you_tube_daily_views_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** | The YouTube video ID (e.g., \&quot;dQw4w9WgXcQ\&quot;) |  |
| **account_id** | **String** | The Late account ID for the YouTube account |  |
| **start_date** | **Date** | Start date (YYYY-MM-DD). Defaults to 30 days ago. | [optional] |
| **end_date** | **Date** | End date (YYYY-MM-DD). Defaults to 3 days ago (YouTube data latency). | [optional] |

### Return type

[**YouTubeDailyViewsResponse**](YouTubeDailyViewsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

