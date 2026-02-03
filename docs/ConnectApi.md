# Late::ConnectApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**complete_telegram_connect**](ConnectApi.md#complete_telegram_connect) | **PATCH** /v1/connect/telegram | Check Telegram connection status |
| [**connect_bluesky_credentials**](ConnectApi.md#connect_bluesky_credentials) | **POST** /v1/connect/bluesky/credentials | Connect Bluesky using app password |
| [**get_connect_url**](ConnectApi.md#get_connect_url) | **GET** /v1/connect/{platform} | Start OAuth connection for a platform |
| [**get_facebook_pages**](ConnectApi.md#get_facebook_pages) | **GET** /v1/accounts/{accountId}/facebook-page | List available Facebook pages for a connected account |
| [**get_gmb_locations**](ConnectApi.md#get_gmb_locations) | **GET** /v1/accounts/{accountId}/gmb-locations | List available Google Business Profile locations for a connected account |
| [**get_linked_in_organizations**](ConnectApi.md#get_linked_in_organizations) | **GET** /v1/accounts/{accountId}/linkedin-organizations | Get available LinkedIn organizations for a connected account |
| [**get_pending_o_auth_data**](ConnectApi.md#get_pending_o_auth_data) | **GET** /v1/connect/pending-data | Fetch pending OAuth selection data (Headless Mode) |
| [**get_pinterest_boards**](ConnectApi.md#get_pinterest_boards) | **GET** /v1/accounts/{accountId}/pinterest-boards | List Pinterest boards for a connected account |
| [**get_reddit_subreddits**](ConnectApi.md#get_reddit_subreddits) | **GET** /v1/accounts/{accountId}/reddit-subreddits | List Reddit subreddits for a connected account |
| [**get_telegram_connect_status**](ConnectApi.md#get_telegram_connect_status) | **GET** /v1/connect/telegram | Generate Telegram access code |
| [**handle_o_auth_callback**](ConnectApi.md#handle_o_auth_callback) | **POST** /v1/connect/{platform} | Complete OAuth token exchange manually (for server-side flows) |
| [**initiate_telegram_connect**](ConnectApi.md#initiate_telegram_connect) | **POST** /v1/connect/telegram | Direct Telegram connection (power users) |
| [**list_facebook_pages**](ConnectApi.md#list_facebook_pages) | **GET** /v1/connect/facebook/select-page | List Facebook Pages after OAuth (Headless Mode) |
| [**list_google_business_locations**](ConnectApi.md#list_google_business_locations) | **GET** /v1/connect/googlebusiness/locations | List Google Business Locations after OAuth (Headless Mode) |
| [**list_linked_in_organizations**](ConnectApi.md#list_linked_in_organizations) | **GET** /v1/connect/linkedin/organizations | Fetch full LinkedIn organization details (Headless Mode) |
| [**list_pinterest_boards_for_selection**](ConnectApi.md#list_pinterest_boards_for_selection) | **GET** /v1/connect/pinterest/select-board | List Pinterest Boards after OAuth (Headless Mode) |
| [**list_snapchat_profiles**](ConnectApi.md#list_snapchat_profiles) | **GET** /v1/connect/snapchat/select-profile | List Snapchat Public Profiles after OAuth (Headless Mode) |
| [**select_facebook_page**](ConnectApi.md#select_facebook_page) | **POST** /v1/connect/facebook/select-page | Select a Facebook Page to complete the connection (Headless Mode) |
| [**select_google_business_location**](ConnectApi.md#select_google_business_location) | **POST** /v1/connect/googlebusiness/select-location | Select a Google Business location to complete the connection (Headless Mode) |
| [**select_linked_in_organization**](ConnectApi.md#select_linked_in_organization) | **POST** /v1/connect/linkedin/select-organization | Select LinkedIn organization or personal account after OAuth |
| [**select_pinterest_board**](ConnectApi.md#select_pinterest_board) | **POST** /v1/connect/pinterest/select-board | Select a Pinterest Board to complete the connection (Headless Mode) |
| [**select_snapchat_profile**](ConnectApi.md#select_snapchat_profile) | **POST** /v1/connect/snapchat/select-profile | Select a Snapchat Public Profile to complete the connection (Headless Mode) |
| [**update_facebook_page**](ConnectApi.md#update_facebook_page) | **PUT** /v1/accounts/{accountId}/facebook-page | Update selected Facebook page for a connected account |
| [**update_gmb_location**](ConnectApi.md#update_gmb_location) | **PUT** /v1/accounts/{accountId}/gmb-locations | Update selected Google Business Profile location for a connected account |
| [**update_linked_in_organization**](ConnectApi.md#update_linked_in_organization) | **PUT** /v1/accounts/{accountId}/linkedin-organization | Switch LinkedIn account type (personal/organization) |
| [**update_pinterest_boards**](ConnectApi.md#update_pinterest_boards) | **PUT** /v1/accounts/{accountId}/pinterest-boards | Set default Pinterest board on the connection |
| [**update_reddit_subreddits**](ConnectApi.md#update_reddit_subreddits) | **PUT** /v1/accounts/{accountId}/reddit-subreddits | Set default subreddit on the connection |


## complete_telegram_connect

> <CompleteTelegramConnect200Response> complete_telegram_connect(code)

Check Telegram connection status

Poll this endpoint to check if a Telegram access code has been used to connect a channel/group.  **Recommended polling interval:** 3 seconds  **Status values:** - `pending`: Code is valid, waiting for user to complete connection - `connected`: Connection successful - channel/group is now linked - `expired`: Code has expired, generate a new one 

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
  # Check Telegram connection status
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
  # Check Telegram connection status
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

Connect Bluesky using app password

Connect a Bluesky account using identifier (handle or email) and an app password.  To get your userId for the state parameter, call `GET /v1/users` - the response includes a `currentUserId` field. 

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
  # Connect Bluesky using app password
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
  # Connect Bluesky using app password
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

Start OAuth connection for a platform

Initiate an OAuth connection flow for any supported social media platform.  **Standard Flow (Hosted UI):** For Facebook connections, Late hosts the page selection UI:  1. Call this endpoint with your API key and `redirect_url` (optional) 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected to Late’s hosted page selector at      `/connect/facebook/select-page?profileId=X&tempToken=Y&userProfile=Z&redirect_url=YOUR_URL&connect_token=CT` 4. After they pick a page, Late saves the connection and finally redirects to your `redirect_url` (if provided)  **Headless/Whitelabel Mode (Facebook, LinkedIn, Pinterest & Google Business Profile):** Build your own fully branded selection UI while Late handles OAuth:  **Facebook:** 1. Call this endpoint with your API key and add `&headless=true`, e.g.      `GET /v1/connect/facebook?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected directly to **your** `redirect_url` with:    - `profileId` – your Late profile ID      - `tempToken` – temporary Facebook access token      - `userProfile` – URL‑encoded JSON user profile      - `connect_token` – short‑lived connect token (for API auth)      - `platform=facebook`      - `step=select_page` 4. Use `tempToken`, `userProfile`, and the `X-Connect-Token` header with:    - `GET /v1/connect/facebook/select-page` to fetch pages    - `POST /v1/connect/facebook/select-page` to save the selected page 5. In this mode, users never see Late's hosted page selector – only your UI.  **LinkedIn:** 1. Call this endpoint with `&headless=true`, e.g.    `GET /v1/connect/linkedin?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected directly to **your** `redirect_url` with:    - `profileId` – your Late profile ID    - `pendingDataToken` – token to fetch OAuth data via API (see step 4)    - `connect_token` – short-lived connect token (for API auth)    - `platform=linkedin`    - `step=select_organization` 4. Call `GET /v1/connect/pending-data?token=PENDING_DATA_TOKEN` to fetch the OAuth data:    - `tempToken` – temporary LinkedIn access token    - `userProfile` – JSON object with `id`, `username`, `displayName`, `profilePicture`    - `organizations` – JSON array with `id`, `urn`, `name`, `vanityName` for each org    - `refreshToken` / `expiresIn` – token metadata    This endpoint is one-time use and data expires after 10 minutes. 5. **Optional:** To fetch full organization details (logos, website, industry, description), call `GET /v1/connect/linkedin/organizations?tempToken=X&orgIds=id1,id2,...` 6. Call `POST /v1/connect/linkedin/select-organization` with the `X-Connect-Token` header to save the selection. 7. In this mode, users never see Late's hosted organization selector – only your UI. 8. Note: If the user has no organization admin access, `step=select_organization` will NOT be present,    and the account will be connected directly as a personal account.  **Pinterest:** 1. Call this endpoint with `&headless=true`, e.g.    `GET /v1/connect/pinterest?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected directly to **your** `redirect_url` with:    - `profileId` – your Late profile ID    - `tempToken` – temporary Pinterest access token    - `userProfile` – URL‑encoded JSON user profile    - `connect_token` – short‑lived connect token (for API auth)    - `platform=pinterest`    - `step=select_board` 4. Use `tempToken`, `userProfile`, and the `X-Connect-Token` header with:    - `GET /v1/connect/pinterest/select-board` to fetch boards    - `POST /v1/connect/pinterest/select-board` to save the selected board 5. In this mode, users never see Late's hosted board selector – only your UI.  **Google Business Profile:** 1. Call this endpoint with `&headless=true`, e.g.    `GET /v1/connect/googlebusiness?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected directly to **your** `redirect_url` with:    - `profileId` – your Late profile ID    - `tempToken` – temporary Google access token    - `userProfile` – URL‑encoded JSON user profile (includes refresh token info)    - `connect_token` – short‑lived connect token (for API auth)    - `platform=googlebusiness`    - `step=select_location` 4. Use `tempToken`, `userProfile`, and the `X-Connect-Token` header with:    - `GET /v1/connect/googlebusiness/locations` to fetch business locations    - `POST /v1/connect/googlebusiness/select-location` to save the selected location 5. In this mode, users never see Late's hosted location selector – only your UI. 

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
  redirect_url: 'redirect_url_example' # String | Optional: Your custom redirect URL after connection completes.  **Standard Mode:** Omit `headless=true` to use our hosted page selection UI.   After the user selects a Facebook Page, Late redirects here with:   `?connected=facebook&profileId=X&username=Y`  **Headless Mode (Facebook, LinkedIn, Pinterest, Google Business Profile & Snapchat):** Pass `headless=true` as a query parameter on this endpoint (not inside `redirect_url`), e.g.: `GET /v1/connect/facebook?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` `GET /v1/connect/linkedin?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` `GET /v1/connect/pinterest?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` `GET /v1/connect/googlebusiness?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` `GET /v1/connect/snapchat?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true`  After OAuth, the user is redirected directly to your `redirect_url` with OAuth data: - **Facebook:** `?profileId=X&tempToken=Y&userProfile=Z&connect_token=CT&platform=facebook&step=select_page` - **LinkedIn:** `?profileId=X&pendingDataToken=TOKEN&connect_token=CT&platform=linkedin&step=select_organization`   Use `GET /v1/connect/pending-data?token=TOKEN` to fetch tempToken, userProfile, organizations, refreshToken. - **Pinterest:** `?profileId=X&tempToken=Y&userProfile=Z&connect_token=CT&platform=pinterest&step=select_board` - **Google Business:** `?profileId=X&tempToken=Y&userProfile=Z&connect_token=CT&platform=googlebusiness&step=select_location` - **Snapchat:** `?profileId=X&tempToken=Y&userProfile=Z&publicProfiles=PROFILES&connect_token=CT&platform=snapchat&step=select_public_profile`   (publicProfiles contains `id`, `display_name`, `username`, `profile_image_url`, `subscriber_count`)  Then use the respective endpoints to build your custom UI: - Facebook: `/v1/connect/facebook/select-page` (GET to fetch, POST to save) - LinkedIn: `/v1/connect/linkedin/organizations` (GET to fetch logos), `/v1/connect/linkedin/select-organization` (POST to save) - Pinterest: `/v1/connect/pinterest/select-board` (GET to fetch, POST to save) - Google Business: `/v1/connect/googlebusiness/locations` (GET) and `/v1/connect/googlebusiness/select-location` (POST) - Snapchat: `/v1/connect/snapchat/select-profile` (POST to save selected public profile)  Example: `https://yourdomain.com/integrations/callback` 
}

begin
  # Start OAuth connection for a platform
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
  # Start OAuth connection for a platform
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
| **redirect_url** | **String** | Optional: Your custom redirect URL after connection completes.  **Standard Mode:** Omit &#x60;headless&#x3D;true&#x60; to use our hosted page selection UI.   After the user selects a Facebook Page, Late redirects here with:   &#x60;?connected&#x3D;facebook&amp;profileId&#x3D;X&amp;username&#x3D;Y&#x60;  **Headless Mode (Facebook, LinkedIn, Pinterest, Google Business Profile &amp; Snapchat):** Pass &#x60;headless&#x3D;true&#x60; as a query parameter on this endpoint (not inside &#x60;redirect_url&#x60;), e.g.: &#x60;GET /v1/connect/facebook?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60; &#x60;GET /v1/connect/linkedin?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60; &#x60;GET /v1/connect/pinterest?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60; &#x60;GET /v1/connect/googlebusiness?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60; &#x60;GET /v1/connect/snapchat?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60;  After OAuth, the user is redirected directly to your &#x60;redirect_url&#x60; with OAuth data: - **Facebook:** &#x60;?profileId&#x3D;X&amp;tempToken&#x3D;Y&amp;userProfile&#x3D;Z&amp;connect_token&#x3D;CT&amp;platform&#x3D;facebook&amp;step&#x3D;select_page&#x60; - **LinkedIn:** &#x60;?profileId&#x3D;X&amp;pendingDataToken&#x3D;TOKEN&amp;connect_token&#x3D;CT&amp;platform&#x3D;linkedin&amp;step&#x3D;select_organization&#x60;   Use &#x60;GET /v1/connect/pending-data?token&#x3D;TOKEN&#x60; to fetch tempToken, userProfile, organizations, refreshToken. - **Pinterest:** &#x60;?profileId&#x3D;X&amp;tempToken&#x3D;Y&amp;userProfile&#x3D;Z&amp;connect_token&#x3D;CT&amp;platform&#x3D;pinterest&amp;step&#x3D;select_board&#x60; - **Google Business:** &#x60;?profileId&#x3D;X&amp;tempToken&#x3D;Y&amp;userProfile&#x3D;Z&amp;connect_token&#x3D;CT&amp;platform&#x3D;googlebusiness&amp;step&#x3D;select_location&#x60; - **Snapchat:** &#x60;?profileId&#x3D;X&amp;tempToken&#x3D;Y&amp;userProfile&#x3D;Z&amp;publicProfiles&#x3D;PROFILES&amp;connect_token&#x3D;CT&amp;platform&#x3D;snapchat&amp;step&#x3D;select_public_profile&#x60;   (publicProfiles contains &#x60;id&#x60;, &#x60;display_name&#x60;, &#x60;username&#x60;, &#x60;profile_image_url&#x60;, &#x60;subscriber_count&#x60;)  Then use the respective endpoints to build your custom UI: - Facebook: &#x60;/v1/connect/facebook/select-page&#x60; (GET to fetch, POST to save) - LinkedIn: &#x60;/v1/connect/linkedin/organizations&#x60; (GET to fetch logos), &#x60;/v1/connect/linkedin/select-organization&#x60; (POST to save) - Pinterest: &#x60;/v1/connect/pinterest/select-board&#x60; (GET to fetch, POST to save) - Google Business: &#x60;/v1/connect/googlebusiness/locations&#x60; (GET) and &#x60;/v1/connect/googlebusiness/select-location&#x60; (POST) - Snapchat: &#x60;/v1/connect/snapchat/select-profile&#x60; (POST to save selected public profile)  Example: &#x60;https://yourdomain.com/integrations/callback&#x60;  | [optional] |

### Return type

[**GetConnectUrl200Response**](GetConnectUrl200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_facebook_pages

> <GetFacebookPages200Response> get_facebook_pages(account_id)

List available Facebook pages for a connected account

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
  # List available Facebook pages for a connected account
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
  # List available Facebook pages for a connected account
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

List available Google Business Profile locations for a connected account

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
  # List available Google Business Profile locations for a connected account
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
  # List available Google Business Profile locations for a connected account
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

Get available LinkedIn organizations for a connected account

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
  # Get available LinkedIn organizations for a connected account
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
  # Get available LinkedIn organizations for a connected account
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

Fetch pending OAuth selection data (Headless Mode)

**Fetch Pending OAuth Data for Headless Mode**  In headless mode, platforms like LinkedIn store OAuth selection data (organizations, pages, etc.) in the database instead of passing it via URL parameters. This prevents URI_TOO_LONG errors when users have many organizations/pages to select from.  After OAuth redirect, use the `pendingDataToken` from the URL to fetch the stored data.  **Important:** - This endpoint is one-time use: data is deleted after being fetched - Data expires automatically after 10 minutes if not fetched - No authentication required, just the token from the redirect URL 

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
token = 'token_example' # String | The pending data token from the OAuth redirect URL (`pendingDataToken` parameter)

begin
  # Fetch pending OAuth selection data (Headless Mode)
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
  # Fetch pending OAuth selection data (Headless Mode)
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
| **token** | **String** | The pending data token from the OAuth redirect URL (&#x60;pendingDataToken&#x60; parameter) |  |

### Return type

[**GetPendingOAuthData200Response**](GetPendingOAuthData200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_pinterest_boards

> <GetPinterestBoards200Response> get_pinterest_boards(account_id)

List Pinterest boards for a connected account

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
  # List Pinterest boards for a connected account
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
  # List Pinterest boards for a connected account
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


## get_reddit_subreddits

> <GetRedditSubreddits200Response> get_reddit_subreddits(account_id)

List Reddit subreddits for a connected account

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
  # List Reddit subreddits for a connected account
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
  # List Reddit subreddits for a connected account
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

Generate Telegram access code

Generate a unique access code for connecting a Telegram channel or group.  **Connection Flow:** 1. Call this endpoint to get an access code (valid for 15 minutes) 2. Add the bot (@LateScheduleBot or your configured bot) as an administrator in your Telegram channel/group 3. Open a private chat with the bot 4. Send: `{CODE} @yourchannel` (e.g., `LATE-ABC123 @mychannel`) 5. Poll `PATCH /v1/connect/telegram?code={CODE}` to check connection status  **Alternative for private channels:** If your channel has no public username, forward any message from the channel to the bot along with the access code. 

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
  # Generate Telegram access code
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
  # Generate Telegram access code
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

Complete OAuth token exchange manually (for server-side flows)

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
  # Complete OAuth token exchange manually (for server-side flows)
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
  # Complete OAuth token exchange manually (for server-side flows)
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

Direct Telegram connection (power users)

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
  # Direct Telegram connection (power users)
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
  # Direct Telegram connection (power users)
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

List Facebook Pages after OAuth (Headless Mode)

**Headless Mode for Custom UI**  After initiating Facebook OAuth via `/v1/connect/facebook`, you'll be redirected to  `/connect/facebook/select-page` with query params including `tempToken` and `userProfile`.  For a **headless/whitelabeled flow**, extract these params from the URL and call this  endpoint to retrieve the list of Facebook Pages the user can manage. Then build your  own UI to let users select a page.  **Note:** Use the `X-Connect-Token` header if you initiated the connection via API key  (rather than a browser session). 

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
  # List Facebook Pages after OAuth (Headless Mode)
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
  # List Facebook Pages after OAuth (Headless Mode)
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

List Google Business Locations after OAuth (Headless Mode)

**Headless Mode for Custom UI**  After initiating Google Business OAuth via `/v1/connect/googlebusiness?headless=true`, you'll be redirected  to your `redirect_url` with query params including `tempToken` and `userProfile`.  For a **headless/whitelabeled flow**, extract these params from the URL and call this  endpoint to retrieve the list of Google Business locations the user can manage. Then build your  own UI to let users select a location.  **Note:** Use the `X-Connect-Token` header if you initiated the connection via API key  (rather than a browser session). 

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
  # List Google Business Locations after OAuth (Headless Mode)
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
  # List Google Business Locations after OAuth (Headless Mode)
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

Fetch full LinkedIn organization details (Headless Mode)

**Fetch Full Organization Details for Custom UI**  After LinkedIn OAuth in headless mode, the redirect URL contains organization data with only `id`, `urn`, and `name` fields (additional details are excluded to prevent URL length issues with many organizations).  Use this endpoint to fetch full organization details including logos, vanity names, websites, and more if you want to display them in your custom selection UI.  **Note:** This endpoint requires no authentication - just the `tempToken` from the OAuth redirect. Details are fetched directly from LinkedIn's API in parallel for fast response times. 

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
  # Fetch full LinkedIn organization details (Headless Mode)
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
  # Fetch full LinkedIn organization details (Headless Mode)
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

List Pinterest Boards after OAuth (Headless Mode)

**Retrieve Pinterest Boards for Selection UI**  After initiating Pinterest OAuth via `/v1/connect/pinterest` with `headless=true`, you'll be redirected to your `redirect_url` with query params including `tempToken` and `userProfile`.  If you want to build your own fully-branded board selector (instead of Late's hosted UI), call this endpoint to retrieve the list of Pinterest Boards the user can post to. Then build your UI and call `POST /v1/connect/pinterest/select-board` to save the selection.  **Authentication:** Use `X-Connect-Token` header with the `connect_token` from the redirect URL. 

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
  # List Pinterest Boards after OAuth (Headless Mode)
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
  # List Pinterest Boards after OAuth (Headless Mode)
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

List Snapchat Public Profiles after OAuth (Headless Mode)

**Headless Mode for Custom UI**  After initiating Snapchat OAuth via `/v1/connect/snapchat?headless=true`, you'll be redirected to your `redirect_url` with query params including `tempToken`, `userProfile`, and `publicProfiles`.  If you want to build your own fully-branded profile selector (instead of Late's hosted UI), call this endpoint to retrieve the list of Snapchat Public Profiles the user can post to. Then build your UI and call `POST /v1/connect/snapchat/select-profile` to save the selection.  **Authentication:** Use `X-Connect-Token` header with the `connect_token` from the redirect URL. 

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
  # List Snapchat Public Profiles after OAuth (Headless Mode)
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
  # List Snapchat Public Profiles after OAuth (Headless Mode)
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

Select a Facebook Page to complete the connection (Headless Mode)

**Complete the Headless Flow**  After displaying your custom UI with the list of pages from the GET endpoint, call this  endpoint to finalize the connection with the user's selected page.  The `userProfile` should be the decoded JSON object from the `userProfile` query param  in the OAuth callback redirect URL.  **Note:** Use the `X-Connect-Token` header if you initiated the connection via API key. 

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
  # Select a Facebook Page to complete the connection (Headless Mode)
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
  # Select a Facebook Page to complete the connection (Headless Mode)
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

Select a Google Business location to complete the connection (Headless Mode)

**Complete the Headless Flow**  After displaying your custom UI with the list of locations from the GET `/v1/connect/googlebusiness/locations`  endpoint, call this endpoint to finalize the connection with the user's selected location.  The `userProfile` should be the decoded JSON object from the `userProfile` query param  in the OAuth callback redirect URL. It contains important token information (including refresh token).  **Note:** Use the `X-Connect-Token` header if you initiated the connection via API key. 

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
  # Select a Google Business location to complete the connection (Headless Mode)
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
  # Select a Google Business location to complete the connection (Headless Mode)
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

Select LinkedIn organization or personal account after OAuth

**Complete the LinkedIn Connection Flow**  After OAuth, the user is redirected with `organizations` in the URL params (if they have org admin access). The organizations array contains `id`, `urn`, and `name` fields. Use this data to build your UI,  then call this endpoint to save the selection.  Set `accountType` to `personal` to connect as the user's personal LinkedIn profile, or `organization` to connect as a company page (requires `selectedOrganization` object).  **Personal Profile:** To connect a personal LinkedIn account, set `accountType` to `\"personal\"` and **omit** the `selectedOrganization` field entirely. This is the simplest flow.  **Headless Mode:** Use the `X-Connect-Token` header if you initiated the connection via API key. 

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
  # Select LinkedIn organization or personal account after OAuth
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
  # Select LinkedIn organization or personal account after OAuth
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

Select a Pinterest Board to complete the connection (Headless Mode)

**Complete the Pinterest Connection Flow**  After OAuth, use this endpoint to save the selected board and complete the Pinterest account connection.  **Headless Mode:** Use the `X-Connect-Token` header if you initiated the connection via API key. 

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
  # Select a Pinterest Board to complete the connection (Headless Mode)
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
  # Select a Pinterest Board to complete the connection (Headless Mode)
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

Select a Snapchat Public Profile to complete the connection (Headless Mode)

**Complete the Snapchat Connection Flow**  After OAuth, use this endpoint to save the selected Public Profile and complete the Snapchat account connection. Snapchat requires a Public Profile to publish Stories, Saved Stories, and Spotlight content.  **Headless Mode:** Use the `X-Connect-Token` header if you initiated the connection via API key.  After initiating Snapchat OAuth via `/v1/connect/snapchat?headless=true`, you'll be redirected to your `redirect_url` with query params including: - `tempToken` - Temporary access token - `userProfile` - URL-encoded JSON with user info - `publicProfiles` - URL-encoded JSON array of available public profiles - `connect_token` - Short-lived token for API authentication - `platform=snapchat` - `step=select_public_profile`  Parse `publicProfiles` to build your custom selector UI, then call this endpoint with the selected profile. 

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
  # Select a Snapchat Public Profile to complete the connection (Headless Mode)
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
  # Select a Snapchat Public Profile to complete the connection (Headless Mode)
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

Update selected Facebook page for a connected account

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
  # Update selected Facebook page for a connected account
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
  # Update selected Facebook page for a connected account
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

Update selected Google Business Profile location for a connected account

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
  # Update selected Google Business Profile location for a connected account
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
  # Update selected Google Business Profile location for a connected account
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

Switch LinkedIn account type (personal/organization)

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
  # Switch LinkedIn account type (personal/organization)
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
  # Switch LinkedIn account type (personal/organization)
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

Set default Pinterest board on the connection

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
  # Set default Pinterest board on the connection
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
  # Set default Pinterest board on the connection
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

Set default subreddit on the connection

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
  # Set default subreddit on the connection
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
  # Set default subreddit on the connection
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

