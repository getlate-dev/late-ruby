# Late::LinkedInMentionsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_linked_in_mentions**](LinkedInMentionsApi.md#get_linked_in_mentions) | **GET** /v1/accounts/{accountId}/linkedin-mentions | Resolve a LinkedIn profile or company URL to a URN for @mentions |


## get_linked_in_mentions

> <GetLinkedInMentions200Response> get_linked_in_mentions(account_id, url, opts)

Resolve a LinkedIn profile or company URL to a URN for @mentions

Converts a LinkedIn profile URL (person) or company page URL (organization) to a URN that can be used to @mention them in posts.  **Supports both:** - **Person mentions:** `linkedin.com/in/username` or just `username` - **Organization mentions:** `linkedin.com/company/company-name` or `company/company-name`  **⚠️ Organization Admin Required for Person Mentions Only:** Person mentions require the connected LinkedIn account to have admin access to at least one LinkedIn Organization (Company Page). Organization mentions do NOT have this requirement - any LinkedIn account can tag companies.  **IMPORTANT - Display Name Requirement:** For **person mentions** to be clickable, the display name must **exactly match** what appears on their LinkedIn profile. - Organization mentions automatically retrieve the company name from LinkedIn API - Person mentions require the exact name, so provide the `displayName` parameter  **Mention Format:** Use the returned `mentionFormat` value directly in your post content: ``` Great insights from @[Miquel Palet](urn:li:person:4qj5ox-agD) on this topic! Excited to partner with @[Microsoft](urn:li:organization:1035)! ``` 

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
url = 'miquelpalet' # String | LinkedIn profile URL, company URL, or vanity name. - Person: `miquelpalet`, `linkedin.com/in/miquelpalet` - Organization: `company/microsoft`, `linkedin.com/company/microsoft` 
opts = {
  display_name: 'Miquel Palet' # String | The exact display name as shown on LinkedIn. - **Person mentions:** Required for clickable mentions. If not provided, a name is derived from the vanity URL which may not match exactly. - **Organization mentions:** Optional. If not provided, the company name is automatically retrieved from LinkedIn. 
}

begin
  # Resolve a LinkedIn profile or company URL to a URN for @mentions
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
  # Resolve a LinkedIn profile or company URL to a URN for @mentions
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
| **url** | **String** | LinkedIn profile URL, company URL, or vanity name. - Person: &#x60;miquelpalet&#x60;, &#x60;linkedin.com/in/miquelpalet&#x60; - Organization: &#x60;company/microsoft&#x60;, &#x60;linkedin.com/company/microsoft&#x60;  |  |
| **display_name** | **String** | The exact display name as shown on LinkedIn. - **Person mentions:** Required for clickable mentions. If not provided, a name is derived from the vanity URL which may not match exactly. - **Organization mentions:** Optional. If not provided, the company name is automatically retrieved from LinkedIn.  | [optional] |

### Return type

[**GetLinkedInMentions200Response**](GetLinkedInMentions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

