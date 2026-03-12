# Late::WhatsAppApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_whats_app_broadcast_recipients**](WhatsAppApi.md#add_whats_app_broadcast_recipients) | **PATCH** /v1/whatsapp/broadcasts/{broadcastId}/recipients | Add recipients |
| [**bulk_delete_whats_app_contacts**](WhatsAppApi.md#bulk_delete_whats_app_contacts) | **DELETE** /v1/whatsapp/contacts/bulk | Bulk delete contacts |
| [**bulk_update_whats_app_contacts**](WhatsAppApi.md#bulk_update_whats_app_contacts) | **POST** /v1/whatsapp/contacts/bulk | Bulk update contacts |
| [**cancel_whats_app_broadcast_schedule**](WhatsAppApi.md#cancel_whats_app_broadcast_schedule) | **DELETE** /v1/whatsapp/broadcasts/{broadcastId}/schedule | Cancel scheduled broadcast |
| [**create_whats_app_broadcast**](WhatsAppApi.md#create_whats_app_broadcast) | **POST** /v1/whatsapp/broadcasts | Create broadcast |
| [**create_whats_app_contact**](WhatsAppApi.md#create_whats_app_contact) | **POST** /v1/whatsapp/contacts | Create contact |
| [**create_whats_app_template**](WhatsAppApi.md#create_whats_app_template) | **POST** /v1/whatsapp/templates | Create template |
| [**delete_whats_app_broadcast**](WhatsAppApi.md#delete_whats_app_broadcast) | **DELETE** /v1/whatsapp/broadcasts/{broadcastId} | Delete broadcast |
| [**delete_whats_app_contact**](WhatsAppApi.md#delete_whats_app_contact) | **DELETE** /v1/whatsapp/contacts/{contactId} | Delete contact |
| [**delete_whats_app_group**](WhatsAppApi.md#delete_whats_app_group) | **DELETE** /v1/whatsapp/groups | Delete group |
| [**delete_whats_app_template**](WhatsAppApi.md#delete_whats_app_template) | **DELETE** /v1/whatsapp/templates/{templateName} | Delete template |
| [**get_whats_app_broadcast**](WhatsAppApi.md#get_whats_app_broadcast) | **GET** /v1/whatsapp/broadcasts/{broadcastId} | Get broadcast |
| [**get_whats_app_broadcast_recipients**](WhatsAppApi.md#get_whats_app_broadcast_recipients) | **GET** /v1/whatsapp/broadcasts/{broadcastId}/recipients | List recipients |
| [**get_whats_app_broadcasts**](WhatsAppApi.md#get_whats_app_broadcasts) | **GET** /v1/whatsapp/broadcasts | List broadcasts |
| [**get_whats_app_business_profile**](WhatsAppApi.md#get_whats_app_business_profile) | **GET** /v1/whatsapp/business-profile | Get business profile |
| [**get_whats_app_contact**](WhatsAppApi.md#get_whats_app_contact) | **GET** /v1/whatsapp/contacts/{contactId} | Get contact |
| [**get_whats_app_contacts**](WhatsAppApi.md#get_whats_app_contacts) | **GET** /v1/whatsapp/contacts | List contacts |
| [**get_whats_app_groups**](WhatsAppApi.md#get_whats_app_groups) | **GET** /v1/whatsapp/groups | List contact groups |
| [**get_whats_app_template**](WhatsAppApi.md#get_whats_app_template) | **GET** /v1/whatsapp/templates/{templateName} | Get template |
| [**get_whats_app_templates**](WhatsAppApi.md#get_whats_app_templates) | **GET** /v1/whatsapp/templates | List templates |
| [**import_whats_app_contacts**](WhatsAppApi.md#import_whats_app_contacts) | **POST** /v1/whatsapp/contacts/import | Bulk import contacts |
| [**remove_whats_app_broadcast_recipients**](WhatsAppApi.md#remove_whats_app_broadcast_recipients) | **DELETE** /v1/whatsapp/broadcasts/{broadcastId}/recipients | Remove recipients |
| [**rename_whats_app_group**](WhatsAppApi.md#rename_whats_app_group) | **POST** /v1/whatsapp/groups | Rename group |
| [**schedule_whats_app_broadcast**](WhatsAppApi.md#schedule_whats_app_broadcast) | **POST** /v1/whatsapp/broadcasts/{broadcastId}/schedule | Schedule broadcast |
| [**send_whats_app_broadcast**](WhatsAppApi.md#send_whats_app_broadcast) | **POST** /v1/whatsapp/broadcasts/{broadcastId}/send | Send broadcast |
| [**send_whats_app_bulk**](WhatsAppApi.md#send_whats_app_bulk) | **POST** /v1/whatsapp/bulk | Bulk send template messages |
| [**update_whats_app_business_profile**](WhatsAppApi.md#update_whats_app_business_profile) | **POST** /v1/whatsapp/business-profile | Update business profile |
| [**update_whats_app_contact**](WhatsAppApi.md#update_whats_app_contact) | **PUT** /v1/whatsapp/contacts/{contactId} | Update contact |
| [**update_whats_app_template**](WhatsAppApi.md#update_whats_app_template) | **PATCH** /v1/whatsapp/templates/{templateName} | Update template |


## add_whats_app_broadcast_recipients

> <AddWhatsAppBroadcastRecipients200Response> add_whats_app_broadcast_recipients(broadcast_id, add_whats_app_broadcast_recipients_request)

Add recipients

Add recipients to a draft broadcast. Maximum 1000 recipients per request. Duplicate phone numbers are automatically skipped. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
broadcast_id = 'broadcast_id_example' # String | Broadcast ID
add_whats_app_broadcast_recipients_request = Late::AddWhatsAppBroadcastRecipientsRequest.new({recipients: [Late::AddWhatsAppBroadcastRecipientsRequestRecipientsInner.new({phone: 'phone_example'})]}) # AddWhatsAppBroadcastRecipientsRequest | 

begin
  # Add recipients
  result = api_instance.add_whats_app_broadcast_recipients(broadcast_id, add_whats_app_broadcast_recipients_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->add_whats_app_broadcast_recipients: #{e}"
end
```

#### Using the add_whats_app_broadcast_recipients_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AddWhatsAppBroadcastRecipients200Response>, Integer, Hash)> add_whats_app_broadcast_recipients_with_http_info(broadcast_id, add_whats_app_broadcast_recipients_request)

```ruby
begin
  # Add recipients
  data, status_code, headers = api_instance.add_whats_app_broadcast_recipients_with_http_info(broadcast_id, add_whats_app_broadcast_recipients_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AddWhatsAppBroadcastRecipients200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->add_whats_app_broadcast_recipients_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **broadcast_id** | **String** | Broadcast ID |  |
| **add_whats_app_broadcast_recipients_request** | [**AddWhatsAppBroadcastRecipientsRequest**](AddWhatsAppBroadcastRecipientsRequest.md) |  |  |

### Return type

[**AddWhatsAppBroadcastRecipients200Response**](AddWhatsAppBroadcastRecipients200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## bulk_delete_whats_app_contacts

> <BulkDeleteWhatsAppContacts200Response> bulk_delete_whats_app_contacts(bulk_delete_whats_app_contacts_request)

Bulk delete contacts

Permanently delete multiple contacts at once (max 500 per request).

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
bulk_delete_whats_app_contacts_request = Late::BulkDeleteWhatsAppContactsRequest.new({contact_ids: ['contact_ids_example']}) # BulkDeleteWhatsAppContactsRequest | 

begin
  # Bulk delete contacts
  result = api_instance.bulk_delete_whats_app_contacts(bulk_delete_whats_app_contacts_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->bulk_delete_whats_app_contacts: #{e}"
end
```

#### Using the bulk_delete_whats_app_contacts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BulkDeleteWhatsAppContacts200Response>, Integer, Hash)> bulk_delete_whats_app_contacts_with_http_info(bulk_delete_whats_app_contacts_request)

```ruby
begin
  # Bulk delete contacts
  data, status_code, headers = api_instance.bulk_delete_whats_app_contacts_with_http_info(bulk_delete_whats_app_contacts_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BulkDeleteWhatsAppContacts200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->bulk_delete_whats_app_contacts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bulk_delete_whats_app_contacts_request** | [**BulkDeleteWhatsAppContactsRequest**](BulkDeleteWhatsAppContactsRequest.md) |  |  |

### Return type

[**BulkDeleteWhatsAppContacts200Response**](BulkDeleteWhatsAppContacts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## bulk_update_whats_app_contacts

> <BulkUpdateWhatsAppContacts200Response> bulk_update_whats_app_contacts(bulk_update_whats_app_contacts_request)

Bulk update contacts

Perform bulk operations on multiple contacts (max 500 per request). Supported actions: addTags, removeTags, addGroups, removeGroups, optIn, optOut, block, unblock. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
bulk_update_whats_app_contacts_request = Late::BulkUpdateWhatsAppContactsRequest.new({action: 'addTags', contact_ids: ['contact_ids_example']}) # BulkUpdateWhatsAppContactsRequest | 

begin
  # Bulk update contacts
  result = api_instance.bulk_update_whats_app_contacts(bulk_update_whats_app_contacts_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->bulk_update_whats_app_contacts: #{e}"
end
```

#### Using the bulk_update_whats_app_contacts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BulkUpdateWhatsAppContacts200Response>, Integer, Hash)> bulk_update_whats_app_contacts_with_http_info(bulk_update_whats_app_contacts_request)

```ruby
begin
  # Bulk update contacts
  data, status_code, headers = api_instance.bulk_update_whats_app_contacts_with_http_info(bulk_update_whats_app_contacts_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BulkUpdateWhatsAppContacts200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->bulk_update_whats_app_contacts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bulk_update_whats_app_contacts_request** | [**BulkUpdateWhatsAppContactsRequest**](BulkUpdateWhatsAppContactsRequest.md) |  |  |

### Return type

[**BulkUpdateWhatsAppContacts200Response**](BulkUpdateWhatsAppContacts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## cancel_whats_app_broadcast_schedule

> <CancelWhatsAppBroadcastSchedule200Response> cancel_whats_app_broadcast_schedule(broadcast_id)

Cancel scheduled broadcast

Cancel a scheduled broadcast and return it to draft status. Only broadcasts in scheduled status can be cancelled. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
broadcast_id = 'broadcast_id_example' # String | Broadcast ID

begin
  # Cancel scheduled broadcast
  result = api_instance.cancel_whats_app_broadcast_schedule(broadcast_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->cancel_whats_app_broadcast_schedule: #{e}"
end
```

#### Using the cancel_whats_app_broadcast_schedule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CancelWhatsAppBroadcastSchedule200Response>, Integer, Hash)> cancel_whats_app_broadcast_schedule_with_http_info(broadcast_id)

```ruby
begin
  # Cancel scheduled broadcast
  data, status_code, headers = api_instance.cancel_whats_app_broadcast_schedule_with_http_info(broadcast_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CancelWhatsAppBroadcastSchedule200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->cancel_whats_app_broadcast_schedule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **broadcast_id** | **String** | Broadcast ID |  |

### Return type

[**CancelWhatsAppBroadcastSchedule200Response**](CancelWhatsAppBroadcastSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_whats_app_broadcast

> <CreateWhatsAppBroadcast200Response> create_whats_app_broadcast(create_whats_app_broadcast_request)

Create broadcast

Create a new draft broadcast. Optionally include initial recipients. After creation, add recipients and then send or schedule the broadcast. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
create_whats_app_broadcast_request = Late::CreateWhatsAppBroadcastRequest.new({account_id: 'account_id_example', name: 'name_example', template: Late::SendWhatsAppBulkRequestTemplate.new({name: 'name_example', language: 'language_example'})}) # CreateWhatsAppBroadcastRequest | 

begin
  # Create broadcast
  result = api_instance.create_whats_app_broadcast(create_whats_app_broadcast_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->create_whats_app_broadcast: #{e}"
end
```

#### Using the create_whats_app_broadcast_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateWhatsAppBroadcast200Response>, Integer, Hash)> create_whats_app_broadcast_with_http_info(create_whats_app_broadcast_request)

```ruby
begin
  # Create broadcast
  data, status_code, headers = api_instance.create_whats_app_broadcast_with_http_info(create_whats_app_broadcast_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateWhatsAppBroadcast200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->create_whats_app_broadcast_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_whats_app_broadcast_request** | [**CreateWhatsAppBroadcastRequest**](CreateWhatsAppBroadcastRequest.md) |  |  |

### Return type

[**CreateWhatsAppBroadcast200Response**](CreateWhatsAppBroadcast200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_whats_app_contact

> <CreateWhatsAppContact200Response> create_whats_app_contact(create_whats_app_contact_request)

Create contact

Create a new WhatsApp contact. Phone number must be unique per account and in E.164 format (e.g., +1234567890). 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
create_whats_app_contact_request = Late::CreateWhatsAppContactRequest.new({account_id: 'account_id_example', phone: 'phone_example', name: 'name_example'}) # CreateWhatsAppContactRequest | 

begin
  # Create contact
  result = api_instance.create_whats_app_contact(create_whats_app_contact_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->create_whats_app_contact: #{e}"
end
```

#### Using the create_whats_app_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateWhatsAppContact200Response>, Integer, Hash)> create_whats_app_contact_with_http_info(create_whats_app_contact_request)

```ruby
begin
  # Create contact
  data, status_code, headers = api_instance.create_whats_app_contact_with_http_info(create_whats_app_contact_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateWhatsAppContact200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->create_whats_app_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_whats_app_contact_request** | [**CreateWhatsAppContactRequest**](CreateWhatsAppContactRequest.md) |  |  |

### Return type

[**CreateWhatsAppContact200Response**](CreateWhatsAppContact200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_whats_app_template

> <CreateWhatsAppTemplate200Response> create_whats_app_template(create_whats_app_template_request)

Create template

Create a new message template. Supports two modes:  **Custom template:** Provide `components` with your own content. Submitted to Meta for review (can take up to 24h).  **Library template:** Provide `library_template_name` instead of `components` to use a pre-built template from Meta's template library. Library templates are **pre-approved** (no review wait). You can optionally customize parameters and buttons via `library_template_body_inputs` and `library_template_button_inputs`.  Browse available library templates at: https://business.facebook.com/wa/manage/message-templates/ 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
create_whats_app_template_request = Late::CreateWhatsAppTemplateRequest.new({account_id: 'account_id_example', name: 'name_example', category: 'AUTHENTICATION', language: 'language_example'}) # CreateWhatsAppTemplateRequest | 

begin
  # Create template
  result = api_instance.create_whats_app_template(create_whats_app_template_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->create_whats_app_template: #{e}"
end
```

#### Using the create_whats_app_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateWhatsAppTemplate200Response>, Integer, Hash)> create_whats_app_template_with_http_info(create_whats_app_template_request)

```ruby
begin
  # Create template
  data, status_code, headers = api_instance.create_whats_app_template_with_http_info(create_whats_app_template_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateWhatsAppTemplate200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->create_whats_app_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_whats_app_template_request** | [**CreateWhatsAppTemplateRequest**](CreateWhatsAppTemplateRequest.md) |  |  |

### Return type

[**CreateWhatsAppTemplate200Response**](CreateWhatsAppTemplate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_whats_app_broadcast

> <UnpublishPost200Response> delete_whats_app_broadcast(broadcast_id)

Delete broadcast

Delete a broadcast. Only draft or cancelled broadcasts can be deleted.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
broadcast_id = 'broadcast_id_example' # String | Broadcast ID

begin
  # Delete broadcast
  result = api_instance.delete_whats_app_broadcast(broadcast_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->delete_whats_app_broadcast: #{e}"
end
```

#### Using the delete_whats_app_broadcast_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UnpublishPost200Response>, Integer, Hash)> delete_whats_app_broadcast_with_http_info(broadcast_id)

```ruby
begin
  # Delete broadcast
  data, status_code, headers = api_instance.delete_whats_app_broadcast_with_http_info(broadcast_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UnpublishPost200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->delete_whats_app_broadcast_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **broadcast_id** | **String** | Broadcast ID |  |

### Return type

[**UnpublishPost200Response**](UnpublishPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_whats_app_contact

> <UnpublishPost200Response> delete_whats_app_contact(contact_id)

Delete contact

Permanently delete a WhatsApp contact.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
contact_id = 'contact_id_example' # String | Contact ID

begin
  # Delete contact
  result = api_instance.delete_whats_app_contact(contact_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->delete_whats_app_contact: #{e}"
end
```

#### Using the delete_whats_app_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UnpublishPost200Response>, Integer, Hash)> delete_whats_app_contact_with_http_info(contact_id)

```ruby
begin
  # Delete contact
  data, status_code, headers = api_instance.delete_whats_app_contact_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UnpublishPost200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->delete_whats_app_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** | Contact ID |  |

### Return type

[**UnpublishPost200Response**](UnpublishPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_whats_app_group

> <RenameWhatsAppGroup200Response> delete_whats_app_group(delete_whats_app_group_request)

Delete group

Delete a contact group. This removes the group from all contacts but does not delete the contacts themselves.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
delete_whats_app_group_request = Late::DeleteWhatsAppGroupRequest.new({account_id: 'account_id_example', group_name: 'group_name_example'}) # DeleteWhatsAppGroupRequest | 

begin
  # Delete group
  result = api_instance.delete_whats_app_group(delete_whats_app_group_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->delete_whats_app_group: #{e}"
end
```

#### Using the delete_whats_app_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RenameWhatsAppGroup200Response>, Integer, Hash)> delete_whats_app_group_with_http_info(delete_whats_app_group_request)

```ruby
begin
  # Delete group
  data, status_code, headers = api_instance.delete_whats_app_group_with_http_info(delete_whats_app_group_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RenameWhatsAppGroup200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->delete_whats_app_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delete_whats_app_group_request** | [**DeleteWhatsAppGroupRequest**](DeleteWhatsAppGroupRequest.md) |  |  |

### Return type

[**RenameWhatsAppGroup200Response**](RenameWhatsAppGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_whats_app_template

> <UnpublishPost200Response> delete_whats_app_template(template_name, account_id)

Delete template

Permanently delete a message template by name.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
template_name = 'template_name_example' # String | Template name
account_id = 'account_id_example' # String | WhatsApp social account ID

begin
  # Delete template
  result = api_instance.delete_whats_app_template(template_name, account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->delete_whats_app_template: #{e}"
end
```

#### Using the delete_whats_app_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UnpublishPost200Response>, Integer, Hash)> delete_whats_app_template_with_http_info(template_name, account_id)

```ruby
begin
  # Delete template
  data, status_code, headers = api_instance.delete_whats_app_template_with_http_info(template_name, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UnpublishPost200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->delete_whats_app_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_name** | **String** | Template name |  |
| **account_id** | **String** | WhatsApp social account ID |  |

### Return type

[**UnpublishPost200Response**](UnpublishPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_whats_app_broadcast

> <GetWhatsAppBroadcast200Response> get_whats_app_broadcast(broadcast_id)

Get broadcast

Retrieve detailed information about a single broadcast including delivery statistics.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
broadcast_id = 'broadcast_id_example' # String | Broadcast ID

begin
  # Get broadcast
  result = api_instance.get_whats_app_broadcast(broadcast_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_broadcast: #{e}"
end
```

#### Using the get_whats_app_broadcast_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWhatsAppBroadcast200Response>, Integer, Hash)> get_whats_app_broadcast_with_http_info(broadcast_id)

```ruby
begin
  # Get broadcast
  data, status_code, headers = api_instance.get_whats_app_broadcast_with_http_info(broadcast_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWhatsAppBroadcast200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_broadcast_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **broadcast_id** | **String** | Broadcast ID |  |

### Return type

[**GetWhatsAppBroadcast200Response**](GetWhatsAppBroadcast200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_whats_app_broadcast_recipients

> <GetWhatsAppBroadcastRecipients200Response> get_whats_app_broadcast_recipients(broadcast_id, opts)

List recipients

List recipients of a broadcast with their delivery status. Supports filtering by delivery status and pagination. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
broadcast_id = 'broadcast_id_example' # String | Broadcast ID
opts = {
  status: 'pending', # String | Filter by recipient delivery status
  limit: 56, # Integer | Maximum results (default 100)
  skip: 56 # Integer | Offset for pagination
}

begin
  # List recipients
  result = api_instance.get_whats_app_broadcast_recipients(broadcast_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_broadcast_recipients: #{e}"
end
```

#### Using the get_whats_app_broadcast_recipients_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWhatsAppBroadcastRecipients200Response>, Integer, Hash)> get_whats_app_broadcast_recipients_with_http_info(broadcast_id, opts)

```ruby
begin
  # List recipients
  data, status_code, headers = api_instance.get_whats_app_broadcast_recipients_with_http_info(broadcast_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWhatsAppBroadcastRecipients200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_broadcast_recipients_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **broadcast_id** | **String** | Broadcast ID |  |
| **status** | **String** | Filter by recipient delivery status | [optional] |
| **limit** | **Integer** | Maximum results (default 100) | [optional][default to 100] |
| **skip** | **Integer** | Offset for pagination | [optional][default to 0] |

### Return type

[**GetWhatsAppBroadcastRecipients200Response**](GetWhatsAppBroadcastRecipients200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_whats_app_broadcasts

> <GetWhatsAppBroadcasts200Response> get_whats_app_broadcasts(account_id, opts)

List broadcasts

List all WhatsApp broadcasts for an account. Returns broadcasts sorted by creation date (newest first) without the full recipients list for performance. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
account_id = 'account_id_example' # String | WhatsApp social account ID
opts = {
  status: 'draft', # String | Filter by broadcast status
  limit: 56, # Integer | Maximum results (default 50)
  skip: 56 # Integer | Offset for pagination
}

begin
  # List broadcasts
  result = api_instance.get_whats_app_broadcasts(account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_broadcasts: #{e}"
end
```

#### Using the get_whats_app_broadcasts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWhatsAppBroadcasts200Response>, Integer, Hash)> get_whats_app_broadcasts_with_http_info(account_id, opts)

```ruby
begin
  # List broadcasts
  data, status_code, headers = api_instance.get_whats_app_broadcasts_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWhatsAppBroadcasts200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_broadcasts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | WhatsApp social account ID |  |
| **status** | **String** | Filter by broadcast status | [optional] |
| **limit** | **Integer** | Maximum results (default 50) | [optional][default to 50] |
| **skip** | **Integer** | Offset for pagination | [optional][default to 0] |

### Return type

[**GetWhatsAppBroadcasts200Response**](GetWhatsAppBroadcasts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_whats_app_business_profile

> <GetWhatsAppBusinessProfile200Response> get_whats_app_business_profile(account_id)

Get business profile

Retrieve the WhatsApp Business profile for the account (about, address, description, email, websites, etc.).

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
account_id = 'account_id_example' # String | WhatsApp social account ID

begin
  # Get business profile
  result = api_instance.get_whats_app_business_profile(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_business_profile: #{e}"
end
```

#### Using the get_whats_app_business_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWhatsAppBusinessProfile200Response>, Integer, Hash)> get_whats_app_business_profile_with_http_info(account_id)

```ruby
begin
  # Get business profile
  data, status_code, headers = api_instance.get_whats_app_business_profile_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWhatsAppBusinessProfile200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_business_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | WhatsApp social account ID |  |

### Return type

[**GetWhatsAppBusinessProfile200Response**](GetWhatsAppBusinessProfile200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_whats_app_contact

> <GetWhatsAppContact200Response> get_whats_app_contact(contact_id)

Get contact

Retrieve a single WhatsApp contact by ID with full details.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
contact_id = 'contact_id_example' # String | Contact ID

begin
  # Get contact
  result = api_instance.get_whats_app_contact(contact_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_contact: #{e}"
end
```

#### Using the get_whats_app_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWhatsAppContact200Response>, Integer, Hash)> get_whats_app_contact_with_http_info(contact_id)

```ruby
begin
  # Get contact
  data, status_code, headers = api_instance.get_whats_app_contact_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWhatsAppContact200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** | Contact ID |  |

### Return type

[**GetWhatsAppContact200Response**](GetWhatsAppContact200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_whats_app_contacts

> <GetWhatsAppContacts200Response> get_whats_app_contacts(account_id, opts)

List contacts

List WhatsApp contacts for an account. Supports filtering by tags, groups, opt-in status, and text search. Returns contacts sorted by name with available filter options. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
account_id = 'account_id_example' # String | WhatsApp social account ID
opts = {
  search: 'search_example', # String | Search contacts by name, phone, email, or company
  tag: 'tag_example', # String | Filter by tag
  group: 'group_example', # String | Filter by group
  opted_in: 'true', # String | Filter by opt-in status
  limit: 56, # Integer | Maximum results (default 50)
  skip: 56 # Integer | Offset for pagination
}

begin
  # List contacts
  result = api_instance.get_whats_app_contacts(account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_contacts: #{e}"
end
```

#### Using the get_whats_app_contacts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWhatsAppContacts200Response>, Integer, Hash)> get_whats_app_contacts_with_http_info(account_id, opts)

```ruby
begin
  # List contacts
  data, status_code, headers = api_instance.get_whats_app_contacts_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWhatsAppContacts200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_contacts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | WhatsApp social account ID |  |
| **search** | **String** | Search contacts by name, phone, email, or company | [optional] |
| **tag** | **String** | Filter by tag | [optional] |
| **group** | **String** | Filter by group | [optional] |
| **opted_in** | **String** | Filter by opt-in status | [optional] |
| **limit** | **Integer** | Maximum results (default 50) | [optional][default to 50] |
| **skip** | **Integer** | Offset for pagination | [optional][default to 0] |

### Return type

[**GetWhatsAppContacts200Response**](GetWhatsAppContacts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_whats_app_groups

> <GetWhatsAppGroups200Response> get_whats_app_groups(account_id)

List contact groups

List all contact groups for a WhatsApp account with contact counts. Groups are derived from the groups field on contacts, not stored as separate documents. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
account_id = 'account_id_example' # String | WhatsApp social account ID

begin
  # List contact groups
  result = api_instance.get_whats_app_groups(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_groups: #{e}"
end
```

#### Using the get_whats_app_groups_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWhatsAppGroups200Response>, Integer, Hash)> get_whats_app_groups_with_http_info(account_id)

```ruby
begin
  # List contact groups
  data, status_code, headers = api_instance.get_whats_app_groups_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWhatsAppGroups200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_groups_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | WhatsApp social account ID |  |

### Return type

[**GetWhatsAppGroups200Response**](GetWhatsAppGroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_whats_app_template

> <GetWhatsAppTemplate200Response> get_whats_app_template(template_name, account_id)

Get template

Retrieve a single message template by name.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
template_name = 'template_name_example' # String | Template name
account_id = 'account_id_example' # String | WhatsApp social account ID

begin
  # Get template
  result = api_instance.get_whats_app_template(template_name, account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_template: #{e}"
end
```

#### Using the get_whats_app_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWhatsAppTemplate200Response>, Integer, Hash)> get_whats_app_template_with_http_info(template_name, account_id)

```ruby
begin
  # Get template
  data, status_code, headers = api_instance.get_whats_app_template_with_http_info(template_name, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWhatsAppTemplate200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_name** | **String** | Template name |  |
| **account_id** | **String** | WhatsApp social account ID |  |

### Return type

[**GetWhatsAppTemplate200Response**](GetWhatsAppTemplate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_whats_app_templates

> <GetWhatsAppTemplates200Response> get_whats_app_templates(account_id)

List templates

List all message templates for the WhatsApp Business Account (WABA) associated with the given account. Templates are fetched directly from the WhatsApp Cloud API. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
account_id = 'account_id_example' # String | WhatsApp social account ID

begin
  # List templates
  result = api_instance.get_whats_app_templates(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_templates: #{e}"
end
```

#### Using the get_whats_app_templates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWhatsAppTemplates200Response>, Integer, Hash)> get_whats_app_templates_with_http_info(account_id)

```ruby
begin
  # List templates
  data, status_code, headers = api_instance.get_whats_app_templates_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWhatsAppTemplates200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->get_whats_app_templates_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | WhatsApp social account ID |  |

### Return type

[**GetWhatsAppTemplates200Response**](GetWhatsAppTemplates200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## import_whats_app_contacts

> <ImportWhatsAppContacts200Response> import_whats_app_contacts(import_whats_app_contacts_request)

Bulk import contacts

Import up to 1000 contacts at once. Each contact requires a phone number and name. Duplicates are skipped by default. Supports default tags and groups applied to all imported contacts. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
import_whats_app_contacts_request = Late::ImportWhatsAppContactsRequest.new({account_id: 'account_id_example', contacts: [Late::ImportWhatsAppContactsRequestContactsInner.new({phone: 'phone_example', name: 'name_example'})]}) # ImportWhatsAppContactsRequest | 

begin
  # Bulk import contacts
  result = api_instance.import_whats_app_contacts(import_whats_app_contacts_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->import_whats_app_contacts: #{e}"
end
```

#### Using the import_whats_app_contacts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImportWhatsAppContacts200Response>, Integer, Hash)> import_whats_app_contacts_with_http_info(import_whats_app_contacts_request)

```ruby
begin
  # Bulk import contacts
  data, status_code, headers = api_instance.import_whats_app_contacts_with_http_info(import_whats_app_contacts_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImportWhatsAppContacts200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->import_whats_app_contacts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **import_whats_app_contacts_request** | [**ImportWhatsAppContactsRequest**](ImportWhatsAppContactsRequest.md) |  |  |

### Return type

[**ImportWhatsAppContacts200Response**](ImportWhatsAppContacts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## remove_whats_app_broadcast_recipients

> <RemoveWhatsAppBroadcastRecipients200Response> remove_whats_app_broadcast_recipients(broadcast_id, remove_whats_app_broadcast_recipients_request)

Remove recipients

Remove recipients from a draft broadcast by phone number.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
broadcast_id = 'broadcast_id_example' # String | Broadcast ID
remove_whats_app_broadcast_recipients_request = Late::RemoveWhatsAppBroadcastRecipientsRequest.new({phones: ['phones_example']}) # RemoveWhatsAppBroadcastRecipientsRequest | 

begin
  # Remove recipients
  result = api_instance.remove_whats_app_broadcast_recipients(broadcast_id, remove_whats_app_broadcast_recipients_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->remove_whats_app_broadcast_recipients: #{e}"
end
```

#### Using the remove_whats_app_broadcast_recipients_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RemoveWhatsAppBroadcastRecipients200Response>, Integer, Hash)> remove_whats_app_broadcast_recipients_with_http_info(broadcast_id, remove_whats_app_broadcast_recipients_request)

```ruby
begin
  # Remove recipients
  data, status_code, headers = api_instance.remove_whats_app_broadcast_recipients_with_http_info(broadcast_id, remove_whats_app_broadcast_recipients_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RemoveWhatsAppBroadcastRecipients200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->remove_whats_app_broadcast_recipients_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **broadcast_id** | **String** | Broadcast ID |  |
| **remove_whats_app_broadcast_recipients_request** | [**RemoveWhatsAppBroadcastRecipientsRequest**](RemoveWhatsAppBroadcastRecipientsRequest.md) |  |  |

### Return type

[**RemoveWhatsAppBroadcastRecipients200Response**](RemoveWhatsAppBroadcastRecipients200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## rename_whats_app_group

> <RenameWhatsAppGroup200Response> rename_whats_app_group(rename_whats_app_group_request)

Rename group

Rename a contact group. This updates the group name on all contacts that belong to the group.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
rename_whats_app_group_request = Late::RenameWhatsAppGroupRequest.new({account_id: 'account_id_example', old_name: 'old_name_example', new_name: 'new_name_example'}) # RenameWhatsAppGroupRequest | 

begin
  # Rename group
  result = api_instance.rename_whats_app_group(rename_whats_app_group_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->rename_whats_app_group: #{e}"
end
```

#### Using the rename_whats_app_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RenameWhatsAppGroup200Response>, Integer, Hash)> rename_whats_app_group_with_http_info(rename_whats_app_group_request)

```ruby
begin
  # Rename group
  data, status_code, headers = api_instance.rename_whats_app_group_with_http_info(rename_whats_app_group_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RenameWhatsAppGroup200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->rename_whats_app_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rename_whats_app_group_request** | [**RenameWhatsAppGroupRequest**](RenameWhatsAppGroupRequest.md) |  |  |

### Return type

[**RenameWhatsAppGroup200Response**](RenameWhatsAppGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## schedule_whats_app_broadcast

> <ScheduleWhatsAppBroadcast200Response> schedule_whats_app_broadcast(broadcast_id, schedule_whats_app_broadcast_request)

Schedule broadcast

Schedule a draft broadcast for future sending. The scheduled time must be in the future and no more than 30 days in advance. The broadcast must be in draft status and have recipients. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
broadcast_id = 'broadcast_id_example' # String | Broadcast ID
schedule_whats_app_broadcast_request = Late::ScheduleWhatsAppBroadcastRequest.new({scheduled_at: Time.now}) # ScheduleWhatsAppBroadcastRequest | 

begin
  # Schedule broadcast
  result = api_instance.schedule_whats_app_broadcast(broadcast_id, schedule_whats_app_broadcast_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->schedule_whats_app_broadcast: #{e}"
end
```

#### Using the schedule_whats_app_broadcast_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ScheduleWhatsAppBroadcast200Response>, Integer, Hash)> schedule_whats_app_broadcast_with_http_info(broadcast_id, schedule_whats_app_broadcast_request)

```ruby
begin
  # Schedule broadcast
  data, status_code, headers = api_instance.schedule_whats_app_broadcast_with_http_info(broadcast_id, schedule_whats_app_broadcast_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ScheduleWhatsAppBroadcast200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->schedule_whats_app_broadcast_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **broadcast_id** | **String** | Broadcast ID |  |
| **schedule_whats_app_broadcast_request** | [**ScheduleWhatsAppBroadcastRequest**](ScheduleWhatsAppBroadcastRequest.md) |  |  |

### Return type

[**ScheduleWhatsAppBroadcast200Response**](ScheduleWhatsAppBroadcast200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## send_whats_app_broadcast

> <SendWhatsAppBroadcast200Response> send_whats_app_broadcast(broadcast_id)

Send broadcast

Start sending a broadcast immediately. The broadcast must be in draft or scheduled status and have at least one recipient. Messages are sent sequentially with rate limiting. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
broadcast_id = 'broadcast_id_example' # String | Broadcast ID

begin
  # Send broadcast
  result = api_instance.send_whats_app_broadcast(broadcast_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->send_whats_app_broadcast: #{e}"
end
```

#### Using the send_whats_app_broadcast_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SendWhatsAppBroadcast200Response>, Integer, Hash)> send_whats_app_broadcast_with_http_info(broadcast_id)

```ruby
begin
  # Send broadcast
  data, status_code, headers = api_instance.send_whats_app_broadcast_with_http_info(broadcast_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SendWhatsAppBroadcast200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->send_whats_app_broadcast_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **broadcast_id** | **String** | Broadcast ID |  |

### Return type

[**SendWhatsAppBroadcast200Response**](SendWhatsAppBroadcast200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## send_whats_app_bulk

> <SendWhatsAppBulk200Response> send_whats_app_bulk(send_whats_app_bulk_request)

Bulk send template messages

Send a template message to multiple recipients in a single request. Maximum 100 recipients per request. Only template messages are supported for bulk sending (not free-form text).  Each recipient can have optional per-recipient template variables for personalization. Returns detailed results for each recipient. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
send_whats_app_bulk_request = Late::SendWhatsAppBulkRequest.new({account_id: 'account_id_example', recipients: [Late::SendWhatsAppBulkRequestRecipientsInner.new({phone: 'phone_example'})], template: Late::SendWhatsAppBulkRequestTemplate.new({name: 'name_example', language: 'language_example'})}) # SendWhatsAppBulkRequest | 

begin
  # Bulk send template messages
  result = api_instance.send_whats_app_bulk(send_whats_app_bulk_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->send_whats_app_bulk: #{e}"
end
```

#### Using the send_whats_app_bulk_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SendWhatsAppBulk200Response>, Integer, Hash)> send_whats_app_bulk_with_http_info(send_whats_app_bulk_request)

```ruby
begin
  # Bulk send template messages
  data, status_code, headers = api_instance.send_whats_app_bulk_with_http_info(send_whats_app_bulk_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SendWhatsAppBulk200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->send_whats_app_bulk_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **send_whats_app_bulk_request** | [**SendWhatsAppBulkRequest**](SendWhatsAppBulkRequest.md) |  |  |

### Return type

[**SendWhatsAppBulk200Response**](SendWhatsAppBulk200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_whats_app_business_profile

> <UnpublishPost200Response> update_whats_app_business_profile(update_whats_app_business_profile_request)

Update business profile

Update the WhatsApp Business profile. All fields are optional; only provided fields will be updated. Constraints: about max 139 chars, description max 512 chars, max 2 websites. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
update_whats_app_business_profile_request = Late::UpdateWhatsAppBusinessProfileRequest.new({account_id: 'account_id_example'}) # UpdateWhatsAppBusinessProfileRequest | 

begin
  # Update business profile
  result = api_instance.update_whats_app_business_profile(update_whats_app_business_profile_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->update_whats_app_business_profile: #{e}"
end
```

#### Using the update_whats_app_business_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UnpublishPost200Response>, Integer, Hash)> update_whats_app_business_profile_with_http_info(update_whats_app_business_profile_request)

```ruby
begin
  # Update business profile
  data, status_code, headers = api_instance.update_whats_app_business_profile_with_http_info(update_whats_app_business_profile_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UnpublishPost200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->update_whats_app_business_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **update_whats_app_business_profile_request** | [**UpdateWhatsAppBusinessProfileRequest**](UpdateWhatsAppBusinessProfileRequest.md) |  |  |

### Return type

[**UnpublishPost200Response**](UnpublishPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_whats_app_contact

> <UpdateWhatsAppContact200Response> update_whats_app_contact(contact_id, update_whats_app_contact_request)

Update contact

Update an existing WhatsApp contact. All fields are optional; only provided fields will be updated. Custom fields are merged with existing values. Set a custom field to null to remove it. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
contact_id = 'contact_id_example' # String | Contact ID
update_whats_app_contact_request = Late::UpdateWhatsAppContactRequest.new # UpdateWhatsAppContactRequest | 

begin
  # Update contact
  result = api_instance.update_whats_app_contact(contact_id, update_whats_app_contact_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->update_whats_app_contact: #{e}"
end
```

#### Using the update_whats_app_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateWhatsAppContact200Response>, Integer, Hash)> update_whats_app_contact_with_http_info(contact_id, update_whats_app_contact_request)

```ruby
begin
  # Update contact
  data, status_code, headers = api_instance.update_whats_app_contact_with_http_info(contact_id, update_whats_app_contact_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateWhatsAppContact200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->update_whats_app_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** | Contact ID |  |
| **update_whats_app_contact_request** | [**UpdateWhatsAppContactRequest**](UpdateWhatsAppContactRequest.md) |  |  |

### Return type

[**UpdateWhatsAppContact200Response**](UpdateWhatsAppContact200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_whats_app_template

> <UpdateWhatsAppTemplate200Response> update_whats_app_template(template_name, update_whats_app_template_request)

Update template

Update a message template's components. Only certain fields can be updated depending on the template's current approval state. Approved templates can only have components updated. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WhatsAppApi.new
template_name = 'template_name_example' # String | Template name
update_whats_app_template_request = Late::UpdateWhatsAppTemplateRequest.new({account_id: 'account_id_example', components: [3.56]}) # UpdateWhatsAppTemplateRequest | 

begin
  # Update template
  result = api_instance.update_whats_app_template(template_name, update_whats_app_template_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->update_whats_app_template: #{e}"
end
```

#### Using the update_whats_app_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateWhatsAppTemplate200Response>, Integer, Hash)> update_whats_app_template_with_http_info(template_name, update_whats_app_template_request)

```ruby
begin
  # Update template
  data, status_code, headers = api_instance.update_whats_app_template_with_http_info(template_name, update_whats_app_template_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateWhatsAppTemplate200Response>
rescue Late::ApiError => e
  puts "Error when calling WhatsAppApi->update_whats_app_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_name** | **String** | Template name |  |
| **update_whats_app_template_request** | [**UpdateWhatsAppTemplateRequest**](UpdateWhatsAppTemplateRequest.md) |  |  |

### Return type

[**UpdateWhatsAppTemplate200Response**](UpdateWhatsAppTemplate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

