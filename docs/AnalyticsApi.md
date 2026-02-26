# Late::AnalyticsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_analytics**](AnalyticsApi.md#get_analytics) | **GET** /v1/analytics | Get post analytics |
| [**get_best_time_to_post**](AnalyticsApi.md#get_best_time_to_post) | **GET** /v1/analytics/best-time | Get best times to post |
| [**get_content_decay**](AnalyticsApi.md#get_content_decay) | **GET** /v1/analytics/content-decay | Get content performance decay |
| [**get_daily_metrics**](AnalyticsApi.md#get_daily_metrics) | **GET** /v1/analytics/daily-metrics | Get daily aggregated metrics |
| [**get_follower_stats**](AnalyticsApi.md#get_follower_stats) | **GET** /v1/accounts/follower-stats | Get follower stats |
| [**get_linked_in_aggregate_analytics**](AnalyticsApi.md#get_linked_in_aggregate_analytics) | **GET** /v1/accounts/{accountId}/linkedin-aggregate-analytics | Get LinkedIn aggregate stats |
| [**get_linked_in_post_analytics**](AnalyticsApi.md#get_linked_in_post_analytics) | **GET** /v1/accounts/{accountId}/linkedin-post-analytics | Get LinkedIn post stats |
| [**get_posting_frequency**](AnalyticsApi.md#get_posting_frequency) | **GET** /v1/analytics/posting-frequency | Get posting frequency vs engagement |
| [**get_you_tube_daily_views**](AnalyticsApi.md#get_you_tube_daily_views) | **GET** /v1/analytics/youtube/daily-views | Get YouTube daily views |


## get_analytics

> <GetAnalytics200Response> get_analytics(opts)

Get post analytics

Returns analytics for posts. With postId, returns a single post. Without it, returns a paginated list with overview stats. Accepts both Late Post IDs and External Post IDs (auto-resolved). Data is cached and refreshed at most once per hour. For follower stats, use /v1/accounts/follower-stats. 

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
  post_id: 'post_id_example', # String | Returns analytics for a single post. Accepts both Late Post IDs and External Post IDs. Late IDs are auto-resolved to External Post analytics.
  platform: 'platform_example', # String | Filter by platform (default \"all\")
  profile_id: 'profile_id_example', # String | Filter by profile ID (default \"all\")
  source: 'all', # String | Filter by post source: late (posted via Late API), external (synced from platform), all (default)
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
| **post_id** | **String** | Returns analytics for a single post. Accepts both Late Post IDs and External Post IDs. Late IDs are auto-resolved to External Post analytics. | [optional] |
| **platform** | **String** | Filter by platform (default \&quot;all\&quot;) | [optional] |
| **profile_id** | **String** | Filter by profile ID (default \&quot;all\&quot;) | [optional] |
| **source** | **String** | Filter by post source: late (posted via Late API), external (synced from platform), all (default) | [optional][default to &#39;all&#39;] |
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


## get_best_time_to_post

> <GetBestTimeToPost200Response> get_best_time_to_post(opts)

Get best times to post

Returns the best times to post based on historical engagement data. Groups all published posts by day of week and hour (UTC), calculating average engagement per slot. Use this to auto-schedule posts at optimal times. Requires the Analytics add-on. 

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
  platform: 'platform_example', # String | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms.
  profile_id: 'profile_id_example' # String | Filter by profile ID. Omit for all profiles.
}

begin
  # Get best times to post
  result = api_instance.get_best_time_to_post(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_best_time_to_post: #{e}"
end
```

#### Using the get_best_time_to_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetBestTimeToPost200Response>, Integer, Hash)> get_best_time_to_post_with_http_info(opts)

```ruby
begin
  # Get best times to post
  data, status_code, headers = api_instance.get_best_time_to_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetBestTimeToPost200Response>
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_best_time_to_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | Filter by platform (e.g. \&quot;instagram\&quot;, \&quot;tiktok\&quot;). Omit for all platforms. | [optional] |
| **profile_id** | **String** | Filter by profile ID. Omit for all profiles. | [optional] |

### Return type

[**GetBestTimeToPost200Response**](GetBestTimeToPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_content_decay

> <GetContentDecay200Response> get_content_decay(opts)

Get content performance decay

Returns how engagement accumulates over time after a post is published. Each bucket shows what percentage of the post's total engagement had been reached by that time window. Useful for understanding content lifespan (e.g. \"posts reach 78% of total engagement within 24 hours\"). Requires the Analytics add-on. 

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
  platform: 'platform_example', # String | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms.
  profile_id: 'profile_id_example' # String | Filter by profile ID. Omit for all profiles.
}

begin
  # Get content performance decay
  result = api_instance.get_content_decay(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_content_decay: #{e}"
end
```

#### Using the get_content_decay_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetContentDecay200Response>, Integer, Hash)> get_content_decay_with_http_info(opts)

```ruby
begin
  # Get content performance decay
  data, status_code, headers = api_instance.get_content_decay_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetContentDecay200Response>
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_content_decay_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | Filter by platform (e.g. \&quot;instagram\&quot;, \&quot;tiktok\&quot;). Omit for all platforms. | [optional] |
| **profile_id** | **String** | Filter by profile ID. Omit for all profiles. | [optional] |

### Return type

[**GetContentDecay200Response**](GetContentDecay200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_daily_metrics

> <GetDailyMetrics200Response> get_daily_metrics(opts)

Get daily aggregated metrics

Returns daily aggregated analytics metrics and a per-platform breakdown. Each day includes post count, platform distribution, and summed metrics (impressions, reach, likes, comments, shares, saves, clicks, views). Defaults to the last 180 days. Requires the Analytics add-on. 

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
  platform: 'platform_example', # String | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms.
  profile_id: 'profile_id_example', # String | Filter by profile ID. Omit for all profiles.
  from_date: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Inclusive start date (ISO 8601). Defaults to 180 days ago.
  to_date: Time.parse('2013-10-20T19:20:30+01:00') # Time | Inclusive end date (ISO 8601). Defaults to now.
}

begin
  # Get daily aggregated metrics
  result = api_instance.get_daily_metrics(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_daily_metrics: #{e}"
end
```

#### Using the get_daily_metrics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetDailyMetrics200Response>, Integer, Hash)> get_daily_metrics_with_http_info(opts)

```ruby
begin
  # Get daily aggregated metrics
  data, status_code, headers = api_instance.get_daily_metrics_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetDailyMetrics200Response>
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_daily_metrics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | Filter by platform (e.g. \&quot;instagram\&quot;, \&quot;tiktok\&quot;). Omit for all platforms. | [optional] |
| **profile_id** | **String** | Filter by profile ID. Omit for all profiles. | [optional] |
| **from_date** | **Time** | Inclusive start date (ISO 8601). Defaults to 180 days ago. | [optional] |
| **to_date** | **Time** | Inclusive end date (ISO 8601). Defaults to now. | [optional] |

### Return type

[**GetDailyMetrics200Response**](GetDailyMetrics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_follower_stats

> <GetFollowerStats200Response> get_follower_stats(opts)

Get follower stats

Returns follower count history and growth metrics for connected social accounts. Requires analytics add-on subscription. Follower counts are refreshed once per day. 

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

Returns aggregate analytics across all posts for a LinkedIn personal account. Org accounts should use /v1/analytics instead. Requires r_member_postAnalytics scope.

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
  aggregation: 'TOTAL', # String | TOTAL (default, lifetime totals) or DAILY (time series). MEMBERS_REACHED not available with DAILY.
  start_date: Date.parse('2024-01-01'), # Date | Start date (YYYY-MM-DD). If omitted, returns lifetime analytics.
  end_date: Date.parse('2024-01-31'), # Date | End date (YYYY-MM-DD, exclusive). Defaults to today if omitted.
  metrics: 'IMPRESSION,REACTION,COMMENT' # String | Comma-separated metrics: IMPRESSION, MEMBERS_REACHED, REACTION, COMMENT, RESHARE. Omit for all.
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
| **aggregation** | **String** | TOTAL (default, lifetime totals) or DAILY (time series). MEMBERS_REACHED not available with DAILY. | [optional][default to &#39;TOTAL&#39;] |
| **start_date** | **Date** | Start date (YYYY-MM-DD). If omitted, returns lifetime analytics. | [optional] |
| **end_date** | **Date** | End date (YYYY-MM-DD, exclusive). Defaults to today if omitted. | [optional] |
| **metrics** | **String** | Comma-separated metrics: IMPRESSION, MEMBERS_REACHED, REACTION, COMMENT, RESHARE. Omit for all. | [optional] |

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

Returns analytics for a specific LinkedIn post by URN. Works for both personal and organization accounts.

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


## get_posting_frequency

> <GetPostingFrequency200Response> get_posting_frequency(opts)

Get posting frequency vs engagement

Returns the correlation between posting frequency (posts per week) and engagement rate, broken down by platform. Helps find the optimal posting cadence for each platform. Each row represents a specific (platform, posts_per_week) combination with the average engagement rate observed across all weeks matching that frequency. Requires the Analytics add-on. 

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
  platform: 'platform_example', # String | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms.
  profile_id: 'profile_id_example' # String | Filter by profile ID. Omit for all profiles.
}

begin
  # Get posting frequency vs engagement
  result = api_instance.get_posting_frequency(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_posting_frequency: #{e}"
end
```

#### Using the get_posting_frequency_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetPostingFrequency200Response>, Integer, Hash)> get_posting_frequency_with_http_info(opts)

```ruby
begin
  # Get posting frequency vs engagement
  data, status_code, headers = api_instance.get_posting_frequency_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetPostingFrequency200Response>
rescue Late::ApiError => e
  puts "Error when calling AnalyticsApi->get_posting_frequency_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | Filter by platform (e.g. \&quot;instagram\&quot;, \&quot;tiktok\&quot;). Omit for all platforms. | [optional] |
| **profile_id** | **String** | Filter by profile ID. Omit for all profiles. | [optional] |

### Return type

[**GetPostingFrequency200Response**](GetPostingFrequency200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_you_tube_daily_views

> <YouTubeDailyViewsResponse> get_you_tube_daily_views(video_id, account_id, opts)

Get YouTube daily views

Returns daily view counts for a YouTube video including views, watch time, and subscriber changes. Requires yt-analytics.readonly scope (re-authorization may be needed). Data has a 2-3 day delay. Max 90 days, defaults to last 30 days. 

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

