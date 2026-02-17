# Late::LinkedInMentionsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_linked_in_mentions**](LinkedInMentionsApi.md#get_linked_in_mentions) | **GET** /v1/accounts/{accountId}/linkedin-mentions | Resolve LinkedIn mention |


## get_linked_in_mentions

> <GetLinkedInMentions200Response> get_linked_in_mentions(account_id, url, opts)

Resolve LinkedIn mention

Converts a LinkedIn profile or company URL to a URN for @mentions in posts. Person mentions require org admin access. Use the returned mentionFormat in post content.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::LinkedInMentionsApi.new
account_id = 'account_id_example' # String | The LinkedIn account ID
url = 'miquelpalet' # String | LinkedIn profile URL, company URL, or vanity name.
opts = {
  display_name: 'Miquel Palet' # String | Exact display name as shown on LinkedIn. Required for person mentions to be clickable. Optional for org mentions.
}

begin
  # Resolve LinkedIn mention
  result = api_instance.get_linked_in_mentions(account_id, url, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling LinkedInMentionsApi->get_linked_in_mentions: #{e}"
end
```

#### Using the get_linked_in_mentions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetLinkedInMentions200Response>, Integer, Hash)> get_linked_in_mentions_with_http_info(account_id, url, opts)

```ruby
begin
  # Resolve LinkedIn mention
  data, status_code, headers = api_instance.get_linked_in_mentions_with_http_info(account_id, url, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetLinkedInMentions200Response>
rescue Late::ApiError => e
  puts "Error when calling LinkedInMentionsApi->get_linked_in_mentions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The LinkedIn account ID |  |
| **url** | **String** | LinkedIn profile URL, company URL, or vanity name. |  |
| **display_name** | **String** | Exact display name as shown on LinkedIn. Required for person mentions to be clickable. Optional for org mentions. | [optional] |

### Return type

[**GetLinkedInMentions200Response**](GetLinkedInMentions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

