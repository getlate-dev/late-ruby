# Late::LinkedInMentionsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_linked_in_mentions**](LinkedInMentionsApi.md#get_linked_in_mentions) | **GET** /v1/accounts/{accountId}/linkedin-mentions | Resolve LinkedIn mention |


## get_linked_in_mentions

> <GetLinkedInMentions200Response> get_linked_in_mentions(account_id, url, opts)

Resolve LinkedIn mention

Converts a LinkedIn profile or company URL to a URN for @mentions in posts. Supports person mentions (linkedin.com/in/username or just username) and org mentions (linkedin.com/company/name or company/name). Person mentions require admin access to at least one LinkedIn Organization. Org mentions work with any account. For person mentions to be clickable, provide the displayName parameter matching the exact name on their profile. Org names are fetched automatically. Use the returned mentionFormat directly in post content. 

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
url = 'miquelpalet' # String | LinkedIn profile URL, company URL, or vanity name. Person examples: miquelpalet, linkedin.com/in/miquelpalet. Organization examples: company/microsoft, linkedin.com/company/microsoft. 
opts = {
  display_name: 'Miquel Palet' # String | The exact display name as shown on LinkedIn. Required for person mentions (for clickable mentions; if not provided, a name is derived from the vanity URL which may not match). Optional for organization mentions (company name is auto-retrieved from LinkedIn). 
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
| **url** | **String** | LinkedIn profile URL, company URL, or vanity name. Person examples: miquelpalet, linkedin.com/in/miquelpalet. Organization examples: company/microsoft, linkedin.com/company/microsoft.  |  |
| **display_name** | **String** | The exact display name as shown on LinkedIn. Required for person mentions (for clickable mentions; if not provided, a name is derived from the vanity URL which may not match). Optional for organization mentions (company name is auto-retrieved from LinkedIn).  | [optional] |

### Return type

[**GetLinkedInMentions200Response**](GetLinkedInMentions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

