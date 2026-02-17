# Late::ConnectApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**complete_telegram_connect**](ConnectApi.md#complete_telegram_connect) | **PATCH** /v1/connect/telegram | Check Telegram status |
| [**connect_bluesky_credentials**](ConnectApi.md#connect_bluesky_credentials) | **POST** /v1/connect/bluesky/credentials | Connect Bluesky account |
| [**get_connect_url**](ConnectApi.md#get_connect_url) | **GET** /v1/connect/{platform} | Get OAuth connect URL |
| [**get_facebook_pages**](ConnectApi.md#get_facebook_pages) | **GET** /v1/accounts/{accountId}/facebook-page | List Facebook pages |
| [**get_gmb_locations**](ConnectApi.md#get_gmb_locations) | **GET** /v1/accounts/{accountId}/gmb-locations | List GBP locations |
| [**get_linked_in_organizations**](ConnectApi.md#get_linked_in_organizations) | **GET** /v1/accounts/{accountId}/linkedin-organizations | List LinkedIn orgs |
| [**get_pending_o_auth_data**](ConnectApi.md#get_pending_o_auth_data) | **GET** /v1/connect/pending-data | Get pending OAuth data |
| [**get_pinterest_boards**](ConnectApi.md#get_pinterest_boards) | **GET** /v1/accounts/{accountId}/pinterest-boards | List Pinterest boards |
| [**get_reddit_flairs**](ConnectApi.md#get_reddit_flairs) | **GET** /v1/accounts/{accountId}/reddit-flairs | List subreddit flairs |
| [**get_reddit_subreddits**](ConnectApi.md#get_reddit_subreddits) | **GET** /v1/accounts/{accountId}/reddit-subreddits | List Reddit subreddits |
| [**get_telegram_connect_status**](ConnectApi.md#get_telegram_connect_status) | **GET** /v1/connect/telegram | Generate Telegram code |
| [**handle_o_auth_callback**](ConnectApi.md#handle_o_auth_callback) | **POST** /v1/connect/{platform} | Complete OAuth callback |
| [**initiate_telegram_connect**](ConnectApi.md#initiate_telegram_connect) | **POST** /v1/connect/telegram | Connect Telegram directly |
| [**list_facebook_pages**](ConnectApi.md#list_facebook_pages) | **GET** /v1/connect/facebook/select-page | List Facebook pages |
| [**list_google_business_locations**](ConnectApi.md#list_google_business_locations) | **GET** /v1/connect/googlebusiness/locations | List GBP locations |
| [**list_linked_in_organizations**](ConnectApi.md#list_linked_in_organizations) | **GET** /v1/connect/linkedin/organizations | List LinkedIn orgs |
| [**list_pinterest_boards_for_selection**](ConnectApi.md#list_pinterest_boards_for_selection) | **GET** /v1/connect/pinterest/select-board | List Pinterest boards |
| [**list_snapchat_profiles**](ConnectApi.md#list_snapchat_profiles) | **GET** /v1/connect/snapchat/select-profile | List Snapchat profiles |
| [**select_facebook_page**](ConnectApi.md#select_facebook_page) | **POST** /v1/connect/facebook/select-page | Select Facebook page |
| [**select_google_business_location**](ConnectApi.md#select_google_business_location) | **POST** /v1/connect/googlebusiness/select-location | Select GBP location |
| [**select_linked_in_organization**](ConnectApi.md#select_linked_in_organization) | **POST** /v1/connect/linkedin/select-organization | Select LinkedIn org |
| [**select_pinterest_board**](ConnectApi.md#select_pinterest_board) | **POST** /v1/connect/pinterest/select-board | Select Pinterest board |
| [**select_snapchat_profile**](ConnectApi.md#select_snapchat_profile) | **POST** /v1/connect/snapchat/select-profile | Select Snapchat profile |
| [**update_facebook_page**](ConnectApi.md#update_facebook_page) | **PUT** /v1/accounts/{accountId}/facebook-page | Update Facebook page |
| [**update_gmb_location**](ConnectApi.md#update_gmb_location) | **PUT** /v1/accounts/{accountId}/gmb-locations | Update GBP location |
| [**update_linked_in_organization**](ConnectApi.md#update_linked_in_organization) | **PUT** /v1/accounts/{accountId}/linkedin-organization | Switch LinkedIn account type |
| [**update_pinterest_boards**](ConnectApi.md#update_pinterest_boards) | **PUT** /v1/accounts/{accountId}/pinterest-boards | Set default Pinterest board |
| [**update_reddit_subreddits**](ConnectApi.md#update_reddit_subreddits) | **PUT** /v1/accounts/{accountId}/reddit-subreddits | Set default subreddit |


## complete_telegram_connect

> <CompleteTelegramConnect200Response> complete_telegram_connect(code)

Check Telegram status

Poll this endpoint to check if a Telegram access code has been used to connect a channel/group. Recommended polling interval: 3 seconds. Status values: pending (waiting for user), connected (channel/group linked), expired (generate a new code). 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
code = 'LATE-ABC123' # String | The access code to check status for

begin
  # Check Telegram status
  result = api_instance.complete_telegram_connect(code)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->complete_telegram_connect: #{e}"
end
```

#### Using the complete_telegram_connect_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CompleteTelegramConnect200Response>, Integer, Hash)> complete_telegram_connect_with_http_info(code)

```ruby
begin
  # Check Telegram status
  data, status_code, headers = api_instance.complete_telegram_connect_with_http_info(code)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CompleteTelegramConnect200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->complete_telegram_connect_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | The access code to check status for |  |

### Return type

[**CompleteTelegramConnect200Response**](CompleteTelegramConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## connect_bluesky_credentials

> <ConnectBlueskyCredentials200Response> connect_bluesky_credentials(connect_bluesky_credentials_request)

Connect Bluesky account

Connect a Bluesky account using identifier (handle or email) and an app password. To get your userId for the state parameter, call GET /v1/users which includes a currentUserId field. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
connect_bluesky_credentials_request = Late::ConnectBlueskyCredentialsRequest.new({identifier: 'identifier_example', app_password: 'app_password_example', state: '6507a1b2c3d4e5f6a7b8c9d0-6507a1b2c3d4e5f6a7b8c9d1'}) # ConnectBlueskyCredentialsRequest | 

begin
  # Connect Bluesky account
  result = api_instance.connect_bluesky_credentials(connect_bluesky_credentials_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->connect_bluesky_credentials: #{e}"
end
```

#### Using the connect_bluesky_credentials_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectBlueskyCredentials200Response>, Integer, Hash)> connect_bluesky_credentials_with_http_info(connect_bluesky_credentials_request)

```ruby
begin
  # Connect Bluesky account
  data, status_code, headers = api_instance.connect_bluesky_credentials_with_http_info(connect_bluesky_credentials_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectBlueskyCredentials200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->connect_bluesky_credentials_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connect_bluesky_credentials_request** | [**ConnectBlueskyCredentialsRequest**](ConnectBlueskyCredentialsRequest.md) |  |  |

### Return type

[**ConnectBlueskyCredentials200Response**](ConnectBlueskyCredentials200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_connect_url

> <GetConnectUrl200Response> get_connect_url(platform, profile_id, opts)

Get OAuth connect URL

Initiate an OAuth connection flow for any supported platform. Standard flow: call this endpoint, redirect user to the returned authUrl, Late hosts the selection UI, then redirects to your redirect_url. Headless mode (Facebook, LinkedIn, Pinterest, Google Business, Snapchat): add headless=true to this endpoint. After OAuth, the user is redirected to your redirect_url with OAuth data (profileId, tempToken, userProfile, connect_token, platform, step). Use the platform-specific selection endpoints to fetch options and save the selection. LinkedIn uses pendingDataToken instead of tempToken; call GET /v1/connect/pending-data?token=TOKEN to retrieve OAuth data (one-time use, expires in 10 minutes). 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
platform = 'facebook' # String | Social media platform to connect
profile_id = 'profile_id_example' # String | Your Late profile ID (get from /v1/profiles)
opts = {
  redirect_url: 'redirect_url_example' # String | Your custom redirect URL after connection completes. Standard mode: Late redirects here with ?connected={platform}&profileId=X&username=Y. Headless mode: pass headless=true on this endpoint. User is redirected to your URL with OAuth data (profileId, tempToken, userProfile, connect_token, platform, step). See endpoint description for details. 
}

begin
  # Get OAuth connect URL
  result = api_instance.get_connect_url(platform, profile_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_connect_url: #{e}"
end
```

#### Using the get_connect_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetConnectUrl200Response>, Integer, Hash)> get_connect_url_with_http_info(platform, profile_id, opts)

```ruby
begin
  # Get OAuth connect URL
  data, status_code, headers = api_instance.get_connect_url_with_http_info(platform, profile_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetConnectUrl200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_connect_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | Social media platform to connect |  |
| **profile_id** | **String** | Your Late profile ID (get from /v1/profiles) |  |
| **redirect_url** | **String** | Your custom redirect URL after connection completes. Standard mode: Late redirects here with ?connected&#x3D;{platform}&amp;profileId&#x3D;X&amp;username&#x3D;Y. Headless mode: pass headless&#x3D;true on this endpoint. User is redirected to your URL with OAuth data (profileId, tempToken, userProfile, connect_token, platform, step). See endpoint description for details.  | [optional] |

### Return type

[**GetConnectUrl200Response**](GetConnectUrl200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_facebook_pages

> <GetFacebookPages200Response> get_facebook_pages(account_id)

List Facebook pages

Returns all Facebook pages the connected account has access to, including the currently selected page.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 

begin
  # List Facebook pages
  result = api_instance.get_facebook_pages(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_facebook_pages: #{e}"
end
```

#### Using the get_facebook_pages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetFacebookPages200Response>, Integer, Hash)> get_facebook_pages_with_http_info(account_id)

```ruby
begin
  # List Facebook pages
  data, status_code, headers = api_instance.get_facebook_pages_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetFacebookPages200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_facebook_pages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**GetFacebookPages200Response**](GetFacebookPages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_gmb_locations

> <GetGmbLocations200Response> get_gmb_locations(account_id)

List GBP locations

Returns all Google Business Profile locations the connected account has access to, including the currently selected location.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 

begin
  # List GBP locations
  result = api_instance.get_gmb_locations(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_gmb_locations: #{e}"
end
```

#### Using the get_gmb_locations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetGmbLocations200Response>, Integer, Hash)> get_gmb_locations_with_http_info(account_id)

```ruby
begin
  # List GBP locations
  data, status_code, headers = api_instance.get_gmb_locations_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetGmbLocations200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_gmb_locations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**GetGmbLocations200Response**](GetGmbLocations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_linked_in_organizations

> <GetLinkedInOrganizations200Response> get_linked_in_organizations(account_id)

List LinkedIn orgs

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 

begin
  # List LinkedIn orgs
  result = api_instance.get_linked_in_organizations(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_linked_in_organizations: #{e}"
end
```

#### Using the get_linked_in_organizations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetLinkedInOrganizations200Response>, Integer, Hash)> get_linked_in_organizations_with_http_info(account_id)

```ruby
begin
  # List LinkedIn orgs
  data, status_code, headers = api_instance.get_linked_in_organizations_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetLinkedInOrganizations200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_linked_in_organizations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**GetLinkedInOrganizations200Response**](GetLinkedInOrganizations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_pending_o_auth_data

> <GetPendingOAuthData200Response> get_pending_o_auth_data(token)

Get pending OAuth data

Fetch pending OAuth data for headless mode. Platforms like LinkedIn store OAuth selection data (organizations, pages, etc.) server-side to prevent URI_TOO_LONG errors. After OAuth redirect, use the pendingDataToken from the URL to fetch the stored data. This endpoint is one-time use (data is deleted after fetch) and expires after 10 minutes. No authentication required, just the token. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
token = 'token_example' # String | The pending data token from the OAuth redirect URL (pendingDataToken parameter)

begin
  # Get pending OAuth data
  result = api_instance.get_pending_o_auth_data(token)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_pending_o_auth_data: #{e}"
end
```

#### Using the get_pending_o_auth_data_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetPendingOAuthData200Response>, Integer, Hash)> get_pending_o_auth_data_with_http_info(token)

```ruby
begin
  # Get pending OAuth data
  data, status_code, headers = api_instance.get_pending_o_auth_data_with_http_info(token)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetPendingOAuthData200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_pending_o_auth_data_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **token** | **String** | The pending data token from the OAuth redirect URL (pendingDataToken parameter) |  |

### Return type

[**GetPendingOAuthData200Response**](GetPendingOAuthData200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_pinterest_boards

> <GetPinterestBoards200Response> get_pinterest_boards(account_id)

List Pinterest boards

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 

begin
  # List Pinterest boards
  result = api_instance.get_pinterest_boards(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_pinterest_boards: #{e}"
end
```

#### Using the get_pinterest_boards_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetPinterestBoards200Response>, Integer, Hash)> get_pinterest_boards_with_http_info(account_id)

```ruby
begin
  # List Pinterest boards
  data, status_code, headers = api_instance.get_pinterest_boards_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetPinterestBoards200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_pinterest_boards_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**GetPinterestBoards200Response**](GetPinterestBoards200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_reddit_flairs

> <GetRedditFlairs200Response> get_reddit_flairs(account_id, subreddit)

List subreddit flairs

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 
subreddit = 'subreddit_example' # String | Subreddit name (without \"r/\" prefix) to fetch flairs for

begin
  # List subreddit flairs
  result = api_instance.get_reddit_flairs(account_id, subreddit)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_reddit_flairs: #{e}"
end
```

#### Using the get_reddit_flairs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetRedditFlairs200Response>, Integer, Hash)> get_reddit_flairs_with_http_info(account_id, subreddit)

```ruby
begin
  # List subreddit flairs
  data, status_code, headers = api_instance.get_reddit_flairs_with_http_info(account_id, subreddit)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetRedditFlairs200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_reddit_flairs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **subreddit** | **String** | Subreddit name (without \&quot;r/\&quot; prefix) to fetch flairs for |  |

### Return type

[**GetRedditFlairs200Response**](GetRedditFlairs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_reddit_subreddits

> <GetRedditSubreddits200Response> get_reddit_subreddits(account_id)

List Reddit subreddits

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 

begin
  # List Reddit subreddits
  result = api_instance.get_reddit_subreddits(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_reddit_subreddits: #{e}"
end
```

#### Using the get_reddit_subreddits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetRedditSubreddits200Response>, Integer, Hash)> get_reddit_subreddits_with_http_info(account_id)

```ruby
begin
  # List Reddit subreddits
  data, status_code, headers = api_instance.get_reddit_subreddits_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetRedditSubreddits200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_reddit_subreddits_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**GetRedditSubreddits200Response**](GetRedditSubreddits200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_telegram_connect_status

> <GetTelegramConnectStatus200Response> get_telegram_connect_status(profile_id)

Generate Telegram code

Generate a unique access code for connecting a Telegram channel or group. Flow: get an access code (valid 15 minutes), add the bot as admin in your channel/group, open a private chat with the bot, send the code + @yourchannel (e.g. LATE-ABC123 @mychannel), then poll PATCH /v1/connect/telegram?code={CODE} to check connection status. For private channels without a public username, forward any message from the channel to the bot along with the access code. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
profile_id = 'profile_id_example' # String | The profile ID to connect the Telegram account to

begin
  # Generate Telegram code
  result = api_instance.get_telegram_connect_status(profile_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_telegram_connect_status: #{e}"
end
```

#### Using the get_telegram_connect_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetTelegramConnectStatus200Response>, Integer, Hash)> get_telegram_connect_status_with_http_info(profile_id)

```ruby
begin
  # Generate Telegram code
  data, status_code, headers = api_instance.get_telegram_connect_status_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetTelegramConnectStatus200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->get_telegram_connect_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | The profile ID to connect the Telegram account to |  |

### Return type

[**GetTelegramConnectStatus200Response**](GetTelegramConnectStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## handle_o_auth_callback

> handle_o_auth_callback(platform, handle_o_auth_callback_request)

Complete OAuth callback

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
platform = 'platform_example' # String | 
handle_o_auth_callback_request = Late::HandleOAuthCallbackRequest.new({code: 'code_example', state: 'state_example', profile_id: 'profile_id_example'}) # HandleOAuthCallbackRequest | 

begin
  # Complete OAuth callback
  api_instance.handle_o_auth_callback(platform, handle_o_auth_callback_request)
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->handle_o_auth_callback: #{e}"
end
```

#### Using the handle_o_auth_callback_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> handle_o_auth_callback_with_http_info(platform, handle_o_auth_callback_request)

```ruby
begin
  # Complete OAuth callback
  data, status_code, headers = api_instance.handle_o_auth_callback_with_http_info(platform, handle_o_auth_callback_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->handle_o_auth_callback_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  |  |
| **handle_o_auth_callback_request** | [**HandleOAuthCallbackRequest**](HandleOAuthCallbackRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## initiate_telegram_connect

> <InitiateTelegramConnect200Response> initiate_telegram_connect(initiate_telegram_connect_request)

Connect Telegram directly

Connect a Telegram channel/group directly using the chat ID.  This is an alternative to the access code flow for power users who know their Telegram chat ID. The bot must already be added as an administrator in the channel/group. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
initiate_telegram_connect_request = Late::InitiateTelegramConnectRequest.new({chat_id: 'chat_id_example', profile_id: 'profile_id_example'}) # InitiateTelegramConnectRequest | 

begin
  # Connect Telegram directly
  result = api_instance.initiate_telegram_connect(initiate_telegram_connect_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->initiate_telegram_connect: #{e}"
end
```

#### Using the initiate_telegram_connect_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InitiateTelegramConnect200Response>, Integer, Hash)> initiate_telegram_connect_with_http_info(initiate_telegram_connect_request)

```ruby
begin
  # Connect Telegram directly
  data, status_code, headers = api_instance.initiate_telegram_connect_with_http_info(initiate_telegram_connect_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InitiateTelegramConnect200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->initiate_telegram_connect_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **initiate_telegram_connect_request** | [**InitiateTelegramConnectRequest**](InitiateTelegramConnectRequest.md) |  |  |

### Return type

[**InitiateTelegramConnect200Response**](InitiateTelegramConnect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_facebook_pages

> <ListFacebookPages200Response> list_facebook_pages(profile_id, temp_token)

List Facebook pages

Returns the list of Facebook Pages the user can manage after OAuth. Extract tempToken and userProfile from the OAuth redirect params and pass them here. Use the X-Connect-Token header if connecting via API key.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure API key authorization: connectToken
  config.api_key['X-Connect-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-Connect-Token'] = 'Bearer'

  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
profile_id = 'profile_id_example' # String | Profile ID from your connection flow
temp_token = 'temp_token_example' # String | Temporary Facebook access token from the OAuth callback redirect

begin
  # List Facebook pages
  result = api_instance.list_facebook_pages(profile_id, temp_token)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_facebook_pages: #{e}"
end
```

#### Using the list_facebook_pages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListFacebookPages200Response>, Integer, Hash)> list_facebook_pages_with_http_info(profile_id, temp_token)

```ruby
begin
  # List Facebook pages
  data, status_code, headers = api_instance.list_facebook_pages_with_http_info(profile_id, temp_token)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListFacebookPages200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_facebook_pages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Profile ID from your connection flow |  |
| **temp_token** | **String** | Temporary Facebook access token from the OAuth callback redirect |  |

### Return type

[**ListFacebookPages200Response**](ListFacebookPages200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_google_business_locations

> <ListGoogleBusinessLocations200Response> list_google_business_locations(profile_id, temp_token)

List GBP locations

For headless/whitelabel flows. After Google Business OAuth with headless=true, you'll be redirected to your redirect_url with tempToken and userProfile params. Call this endpoint to retrieve the list of locations the user can manage, then build your own UI to let them select one. Use the X-Connect-Token header if you initiated the connection via API key. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure API key authorization: connectToken
  config.api_key['X-Connect-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-Connect-Token'] = 'Bearer'

  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
profile_id = 'profile_id_example' # String | Profile ID from your connection flow
temp_token = 'temp_token_example' # String | Temporary Google access token from the OAuth callback redirect

begin
  # List GBP locations
  result = api_instance.list_google_business_locations(profile_id, temp_token)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_google_business_locations: #{e}"
end
```

#### Using the list_google_business_locations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListGoogleBusinessLocations200Response>, Integer, Hash)> list_google_business_locations_with_http_info(profile_id, temp_token)

```ruby
begin
  # List GBP locations
  data, status_code, headers = api_instance.list_google_business_locations_with_http_info(profile_id, temp_token)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListGoogleBusinessLocations200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_google_business_locations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Profile ID from your connection flow |  |
| **temp_token** | **String** | Temporary Google access token from the OAuth callback redirect |  |

### Return type

[**ListGoogleBusinessLocations200Response**](ListGoogleBusinessLocations200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_linked_in_organizations

> <ListLinkedInOrganizations200Response> list_linked_in_organizations(temp_token, org_ids)

List LinkedIn orgs

Fetch full organization details for custom UI. After LinkedIn OAuth in headless mode, the redirect URL only contains id, urn, and name fields. Use this endpoint to fetch full details including logos, vanity names, websites, and more. No authentication required, just the tempToken from the OAuth redirect. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
temp_token = 'temp_token_example' # String | The temporary LinkedIn access token from the OAuth redirect
org_ids = '12345678,87654321,11111111' # String | Comma-separated list of organization IDs to fetch details for (max 100)

begin
  # List LinkedIn orgs
  result = api_instance.list_linked_in_organizations(temp_token, org_ids)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_linked_in_organizations: #{e}"
end
```

#### Using the list_linked_in_organizations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListLinkedInOrganizations200Response>, Integer, Hash)> list_linked_in_organizations_with_http_info(temp_token, org_ids)

```ruby
begin
  # List LinkedIn orgs
  data, status_code, headers = api_instance.list_linked_in_organizations_with_http_info(temp_token, org_ids)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListLinkedInOrganizations200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_linked_in_organizations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **temp_token** | **String** | The temporary LinkedIn access token from the OAuth redirect |  |
| **org_ids** | **String** | Comma-separated list of organization IDs to fetch details for (max 100) |  |

### Return type

[**ListLinkedInOrganizations200Response**](ListLinkedInOrganizations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_pinterest_boards_for_selection

> <ListPinterestBoardsForSelection200Response> list_pinterest_boards_for_selection(x_connect_token, profile_id, temp_token)

List Pinterest boards

Retrieve Pinterest boards for headless selection UI. After Pinterest OAuth with headless=true, you'll be redirected to your redirect_url with tempToken and userProfile params. Call this endpoint to retrieve the list of boards the user can post to, then build your UI and call POST /v1/connect/pinterest/select-board to save the selection. Use X-Connect-Token header with the connect_token from the redirect URL. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
x_connect_token = 'x_connect_token_example' # String | Short-lived connect token from the OAuth redirect
profile_id = 'profile_id_example' # String | Your Late profile ID
temp_token = 'temp_token_example' # String | Temporary Pinterest access token from the OAuth callback redirect

begin
  # List Pinterest boards
  result = api_instance.list_pinterest_boards_for_selection(x_connect_token, profile_id, temp_token)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_pinterest_boards_for_selection: #{e}"
end
```

#### Using the list_pinterest_boards_for_selection_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListPinterestBoardsForSelection200Response>, Integer, Hash)> list_pinterest_boards_for_selection_with_http_info(x_connect_token, profile_id, temp_token)

```ruby
begin
  # List Pinterest boards
  data, status_code, headers = api_instance.list_pinterest_boards_for_selection_with_http_info(x_connect_token, profile_id, temp_token)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListPinterestBoardsForSelection200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_pinterest_boards_for_selection_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **x_connect_token** | **String** | Short-lived connect token from the OAuth redirect |  |
| **profile_id** | **String** | Your Late profile ID |  |
| **temp_token** | **String** | Temporary Pinterest access token from the OAuth callback redirect |  |

### Return type

[**ListPinterestBoardsForSelection200Response**](ListPinterestBoardsForSelection200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_snapchat_profiles

> <ListSnapchatProfiles200Response> list_snapchat_profiles(x_connect_token, profile_id, temp_token)

List Snapchat profiles

For headless/whitelabel flows. After Snapchat OAuth with headless=true, you'll be redirected to your redirect_url with tempToken, userProfile, and publicProfiles params. Call this endpoint to retrieve the list of Snapchat Public Profiles the user can post to, then build your UI and call POST /v1/connect/snapchat/select-profile to save the selection. Use X-Connect-Token header with the connect_token from the redirect URL. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
x_connect_token = 'x_connect_token_example' # String | Short-lived connect token from the OAuth redirect
profile_id = 'profile_id_example' # String | Your Late profile ID
temp_token = 'temp_token_example' # String | Temporary Snapchat access token from the OAuth callback redirect

begin
  # List Snapchat profiles
  result = api_instance.list_snapchat_profiles(x_connect_token, profile_id, temp_token)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_snapchat_profiles: #{e}"
end
```

#### Using the list_snapchat_profiles_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListSnapchatProfiles200Response>, Integer, Hash)> list_snapchat_profiles_with_http_info(x_connect_token, profile_id, temp_token)

```ruby
begin
  # List Snapchat profiles
  data, status_code, headers = api_instance.list_snapchat_profiles_with_http_info(x_connect_token, profile_id, temp_token)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListSnapchatProfiles200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->list_snapchat_profiles_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **x_connect_token** | **String** | Short-lived connect token from the OAuth redirect |  |
| **profile_id** | **String** | Your Late profile ID |  |
| **temp_token** | **String** | Temporary Snapchat access token from the OAuth callback redirect |  |

### Return type

[**ListSnapchatProfiles200Response**](ListSnapchatProfiles200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## select_facebook_page

> <SelectFacebookPage200Response> select_facebook_page(select_facebook_page_request)

Select Facebook page

Complete the headless flow. After displaying your custom UI with the list of pages from the GET endpoint, call this endpoint to finalize the connection with the user's selected page. The userProfile should be the decoded JSON object from the userProfile query param in the OAuth callback redirect URL. Use the X-Connect-Token header if you initiated the connection via API key. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure API key authorization: connectToken
  config.api_key['X-Connect-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-Connect-Token'] = 'Bearer'

  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
select_facebook_page_request = Late::SelectFacebookPageRequest.new({profile_id: 'profile_id_example', page_id: 'page_id_example', temp_token: 'temp_token_example'}) # SelectFacebookPageRequest | 

begin
  # Select Facebook page
  result = api_instance.select_facebook_page(select_facebook_page_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_facebook_page: #{e}"
end
```

#### Using the select_facebook_page_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SelectFacebookPage200Response>, Integer, Hash)> select_facebook_page_with_http_info(select_facebook_page_request)

```ruby
begin
  # Select Facebook page
  data, status_code, headers = api_instance.select_facebook_page_with_http_info(select_facebook_page_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SelectFacebookPage200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_facebook_page_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **select_facebook_page_request** | [**SelectFacebookPageRequest**](SelectFacebookPageRequest.md) |  |  |

### Return type

[**SelectFacebookPage200Response**](SelectFacebookPage200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## select_google_business_location

> <SelectGoogleBusinessLocation200Response> select_google_business_location(select_google_business_location_request)

Select GBP location

Complete the headless flow. After displaying your custom UI with the list of locations from the GET /v1/connect/googlebusiness/locations endpoint, call this endpoint to finalize the connection with the user's selected location. The userProfile should be the decoded JSON object from the userProfile query param in the OAuth callback redirect URL. It contains important token information including the refresh token. Use the X-Connect-Token header if you initiated the connection via API key. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure API key authorization: connectToken
  config.api_key['X-Connect-Token'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-Connect-Token'] = 'Bearer'

  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
select_google_business_location_request = Late::SelectGoogleBusinessLocationRequest.new({profile_id: 'profile_id_example', location_id: 'location_id_example', temp_token: 'temp_token_example'}) # SelectGoogleBusinessLocationRequest | 

begin
  # Select GBP location
  result = api_instance.select_google_business_location(select_google_business_location_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_google_business_location: #{e}"
end
```

#### Using the select_google_business_location_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SelectGoogleBusinessLocation200Response>, Integer, Hash)> select_google_business_location_with_http_info(select_google_business_location_request)

```ruby
begin
  # Select GBP location
  data, status_code, headers = api_instance.select_google_business_location_with_http_info(select_google_business_location_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SelectGoogleBusinessLocation200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_google_business_location_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **select_google_business_location_request** | [**SelectGoogleBusinessLocationRequest**](SelectGoogleBusinessLocationRequest.md) |  |  |

### Return type

[**SelectGoogleBusinessLocation200Response**](SelectGoogleBusinessLocation200Response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## select_linked_in_organization

> <SelectLinkedInOrganization200Response> select_linked_in_organization(select_linked_in_organization_request)

Select LinkedIn org

Complete the LinkedIn connection flow. After OAuth, the user is redirected with organizations in the URL params (if they have org admin access). Use this data to build your UI, then call this endpoint to save the selection. Set accountType to \"personal\" for a personal profile (omit selectedOrganization), or \"organization\" to connect as a company page. Use the X-Connect-Token header if you initiated the connection via API key. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
select_linked_in_organization_request = Late::SelectLinkedInOrganizationRequest.new({profile_id: 'profile_id_example', temp_token: 'temp_token_example', user_profile: 3.56, account_type: 'personal'}) # SelectLinkedInOrganizationRequest | 

begin
  # Select LinkedIn org
  result = api_instance.select_linked_in_organization(select_linked_in_organization_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_linked_in_organization: #{e}"
end
```

#### Using the select_linked_in_organization_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SelectLinkedInOrganization200Response>, Integer, Hash)> select_linked_in_organization_with_http_info(select_linked_in_organization_request)

```ruby
begin
  # Select LinkedIn org
  data, status_code, headers = api_instance.select_linked_in_organization_with_http_info(select_linked_in_organization_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SelectLinkedInOrganization200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_linked_in_organization_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **select_linked_in_organization_request** | [**SelectLinkedInOrganizationRequest**](SelectLinkedInOrganizationRequest.md) |  |  |

### Return type

[**SelectLinkedInOrganization200Response**](SelectLinkedInOrganization200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## select_pinterest_board

> <SelectPinterestBoard200Response> select_pinterest_board(select_pinterest_board_request)

Select Pinterest board

Complete the Pinterest connection flow. After OAuth, use this endpoint to save the selected board and complete the account connection. Use the X-Connect-Token header if you initiated the connection via API key. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
select_pinterest_board_request = Late::SelectPinterestBoardRequest.new({profile_id: 'profile_id_example', board_id: 'board_id_example', temp_token: 'temp_token_example'}) # SelectPinterestBoardRequest | 

begin
  # Select Pinterest board
  result = api_instance.select_pinterest_board(select_pinterest_board_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_pinterest_board: #{e}"
end
```

#### Using the select_pinterest_board_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SelectPinterestBoard200Response>, Integer, Hash)> select_pinterest_board_with_http_info(select_pinterest_board_request)

```ruby
begin
  # Select Pinterest board
  data, status_code, headers = api_instance.select_pinterest_board_with_http_info(select_pinterest_board_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SelectPinterestBoard200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_pinterest_board_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **select_pinterest_board_request** | [**SelectPinterestBoardRequest**](SelectPinterestBoardRequest.md) |  |  |

### Return type

[**SelectPinterestBoard200Response**](SelectPinterestBoard200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## select_snapchat_profile

> <SelectSnapchatProfile200Response> select_snapchat_profile(select_snapchat_profile_request, opts)

Select Snapchat profile

Complete the Snapchat connection flow. Save the selected Public Profile and complete the account connection. Snapchat requires a Public Profile to publish Stories, Saved Stories, and Spotlight content. After Snapchat OAuth with headless=true, you'll be redirected with tempToken, userProfile, publicProfiles, connect_token, platform=snapchat, and step=select_public_profile in the URL. Parse publicProfiles to build your custom selector UI, then call this endpoint with the selected profile. Use the X-Connect-Token header if you initiated the connection via API key. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
select_snapchat_profile_request = Late::SelectSnapchatProfileRequest.new({profile_id: 'profile_id_example', selected_public_profile: Late::SelectSnapchatProfileRequestSelectedPublicProfile.new({id: 'id_example', display_name: 'display_name_example'}), temp_token: 'temp_token_example', user_profile: 3.56}) # SelectSnapchatProfileRequest | 
opts = {
  x_connect_token: 'x_connect_token_example' # String | Short-lived connect token from the OAuth redirect (for API users)
}

begin
  # Select Snapchat profile
  result = api_instance.select_snapchat_profile(select_snapchat_profile_request, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_snapchat_profile: #{e}"
end
```

#### Using the select_snapchat_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SelectSnapchatProfile200Response>, Integer, Hash)> select_snapchat_profile_with_http_info(select_snapchat_profile_request, opts)

```ruby
begin
  # Select Snapchat profile
  data, status_code, headers = api_instance.select_snapchat_profile_with_http_info(select_snapchat_profile_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SelectSnapchatProfile200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->select_snapchat_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **select_snapchat_profile_request** | [**SelectSnapchatProfileRequest**](SelectSnapchatProfileRequest.md) |  |  |
| **x_connect_token** | **String** | Short-lived connect token from the OAuth redirect (for API users) | [optional] |

### Return type

[**SelectSnapchatProfile200Response**](SelectSnapchatProfile200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_facebook_page

> <UpdateFacebookPage200Response> update_facebook_page(account_id, update_facebook_page_request)

Update Facebook page

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 
update_facebook_page_request = Late::UpdateFacebookPageRequest.new({selected_page_id: 'selected_page_id_example'}) # UpdateFacebookPageRequest | 

begin
  # Update Facebook page
  result = api_instance.update_facebook_page(account_id, update_facebook_page_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_facebook_page: #{e}"
end
```

#### Using the update_facebook_page_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateFacebookPage200Response>, Integer, Hash)> update_facebook_page_with_http_info(account_id, update_facebook_page_request)

```ruby
begin
  # Update Facebook page
  data, status_code, headers = api_instance.update_facebook_page_with_http_info(account_id, update_facebook_page_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateFacebookPage200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_facebook_page_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **update_facebook_page_request** | [**UpdateFacebookPageRequest**](UpdateFacebookPageRequest.md) |  |  |

### Return type

[**UpdateFacebookPage200Response**](UpdateFacebookPage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_gmb_location

> <UpdateGmbLocation200Response> update_gmb_location(account_id, update_gmb_location_request)

Update GBP location

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 
update_gmb_location_request = Late::UpdateGmbLocationRequest.new({selected_location_id: 'selected_location_id_example'}) # UpdateGmbLocationRequest | 

begin
  # Update GBP location
  result = api_instance.update_gmb_location(account_id, update_gmb_location_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_gmb_location: #{e}"
end
```

#### Using the update_gmb_location_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateGmbLocation200Response>, Integer, Hash)> update_gmb_location_with_http_info(account_id, update_gmb_location_request)

```ruby
begin
  # Update GBP location
  data, status_code, headers = api_instance.update_gmb_location_with_http_info(account_id, update_gmb_location_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateGmbLocation200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_gmb_location_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **update_gmb_location_request** | [**UpdateGmbLocationRequest**](UpdateGmbLocationRequest.md) |  |  |

### Return type

[**UpdateGmbLocation200Response**](UpdateGmbLocation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_linked_in_organization

> <ConnectBlueskyCredentials200Response> update_linked_in_organization(account_id, update_linked_in_organization_request)

Switch LinkedIn account type

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 
update_linked_in_organization_request = Late::UpdateLinkedInOrganizationRequest.new({account_type: 'personal'}) # UpdateLinkedInOrganizationRequest | 

begin
  # Switch LinkedIn account type
  result = api_instance.update_linked_in_organization(account_id, update_linked_in_organization_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_linked_in_organization: #{e}"
end
```

#### Using the update_linked_in_organization_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectBlueskyCredentials200Response>, Integer, Hash)> update_linked_in_organization_with_http_info(account_id, update_linked_in_organization_request)

```ruby
begin
  # Switch LinkedIn account type
  data, status_code, headers = api_instance.update_linked_in_organization_with_http_info(account_id, update_linked_in_organization_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectBlueskyCredentials200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_linked_in_organization_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **update_linked_in_organization_request** | [**UpdateLinkedInOrganizationRequest**](UpdateLinkedInOrganizationRequest.md) |  |  |

### Return type

[**ConnectBlueskyCredentials200Response**](ConnectBlueskyCredentials200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_pinterest_boards

> <ConnectBlueskyCredentials200Response> update_pinterest_boards(account_id, update_pinterest_boards_request)

Set default Pinterest board

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 
update_pinterest_boards_request = Late::UpdatePinterestBoardsRequest.new({default_board_id: 'default_board_id_example'}) # UpdatePinterestBoardsRequest | 

begin
  # Set default Pinterest board
  result = api_instance.update_pinterest_boards(account_id, update_pinterest_boards_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_pinterest_boards: #{e}"
end
```

#### Using the update_pinterest_boards_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectBlueskyCredentials200Response>, Integer, Hash)> update_pinterest_boards_with_http_info(account_id, update_pinterest_boards_request)

```ruby
begin
  # Set default Pinterest board
  data, status_code, headers = api_instance.update_pinterest_boards_with_http_info(account_id, update_pinterest_boards_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectBlueskyCredentials200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_pinterest_boards_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **update_pinterest_boards_request** | [**UpdatePinterestBoardsRequest**](UpdatePinterestBoardsRequest.md) |  |  |

### Return type

[**ConnectBlueskyCredentials200Response**](ConnectBlueskyCredentials200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_reddit_subreddits

> <UpdateRedditSubreddits200Response> update_reddit_subreddits(account_id, update_reddit_subreddits_request)

Set default subreddit

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ConnectApi.new
account_id = 'account_id_example' # String | 
update_reddit_subreddits_request = Late::UpdateRedditSubredditsRequest.new({default_subreddit: 'default_subreddit_example'}) # UpdateRedditSubredditsRequest | 

begin
  # Set default subreddit
  result = api_instance.update_reddit_subreddits(account_id, update_reddit_subreddits_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_reddit_subreddits: #{e}"
end
```

#### Using the update_reddit_subreddits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateRedditSubreddits200Response>, Integer, Hash)> update_reddit_subreddits_with_http_info(account_id, update_reddit_subreddits_request)

```ruby
begin
  # Set default subreddit
  data, status_code, headers = api_instance.update_reddit_subreddits_with_http_info(account_id, update_reddit_subreddits_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateRedditSubreddits200Response>
rescue Late::ApiError => e
  puts "Error when calling ConnectApi->update_reddit_subreddits_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **update_reddit_subreddits_request** | [**UpdateRedditSubredditsRequest**](UpdateRedditSubredditsRequest.md) |  |  |

### Return type

[**UpdateRedditSubreddits200Response**](UpdateRedditSubreddits200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

