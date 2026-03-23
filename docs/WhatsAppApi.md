# \WhatsAppApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_whats_app_broadcast_recipients**](WhatsAppApi.md#add_whats_app_broadcast_recipients) | **PATCH** /v1/whatsapp/broadcasts/{broadcastId}/recipients | Add recipients
[**bulk_delete_whats_app_contacts**](WhatsAppApi.md#bulk_delete_whats_app_contacts) | **DELETE** /v1/whatsapp/contacts/bulk | Bulk delete contacts
[**bulk_update_whats_app_contacts**](WhatsAppApi.md#bulk_update_whats_app_contacts) | **POST** /v1/whatsapp/contacts/bulk | Bulk update contacts
[**cancel_whats_app_broadcast_schedule**](WhatsAppApi.md#cancel_whats_app_broadcast_schedule) | **DELETE** /v1/whatsapp/broadcasts/{broadcastId}/schedule | Cancel scheduled broadcast
[**create_whats_app_broadcast**](WhatsAppApi.md#create_whats_app_broadcast) | **POST** /v1/whatsapp/broadcasts | Create broadcast
[**create_whats_app_contact**](WhatsAppApi.md#create_whats_app_contact) | **POST** /v1/whatsapp/contacts | Create contact
[**create_whats_app_template**](WhatsAppApi.md#create_whats_app_template) | **POST** /v1/whatsapp/templates | Create template
[**delete_whats_app_broadcast**](WhatsAppApi.md#delete_whats_app_broadcast) | **DELETE** /v1/whatsapp/broadcasts/{broadcastId} | Delete broadcast
[**delete_whats_app_contact**](WhatsAppApi.md#delete_whats_app_contact) | **DELETE** /v1/whatsapp/contacts/{contactId} | Delete contact
[**delete_whats_app_group**](WhatsAppApi.md#delete_whats_app_group) | **DELETE** /v1/whatsapp/groups | Delete group
[**delete_whats_app_template**](WhatsAppApi.md#delete_whats_app_template) | **DELETE** /v1/whatsapp/templates/{templateName} | Delete template
[**get_whats_app_broadcast**](WhatsAppApi.md#get_whats_app_broadcast) | **GET** /v1/whatsapp/broadcasts/{broadcastId} | Get broadcast
[**get_whats_app_broadcast_recipients**](WhatsAppApi.md#get_whats_app_broadcast_recipients) | **GET** /v1/whatsapp/broadcasts/{broadcastId}/recipients | List recipients
[**get_whats_app_broadcasts**](WhatsAppApi.md#get_whats_app_broadcasts) | **GET** /v1/whatsapp/broadcasts | List broadcasts
[**get_whats_app_business_profile**](WhatsAppApi.md#get_whats_app_business_profile) | **GET** /v1/whatsapp/business-profile | Get business profile
[**get_whats_app_contact**](WhatsAppApi.md#get_whats_app_contact) | **GET** /v1/whatsapp/contacts/{contactId} | Get contact
[**get_whats_app_contacts**](WhatsAppApi.md#get_whats_app_contacts) | **GET** /v1/whatsapp/contacts | List contacts
[**get_whats_app_display_name**](WhatsAppApi.md#get_whats_app_display_name) | **GET** /v1/whatsapp/business-profile/display-name | Get display name and review status
[**get_whats_app_groups**](WhatsAppApi.md#get_whats_app_groups) | **GET** /v1/whatsapp/groups | List contact groups
[**get_whats_app_template**](WhatsAppApi.md#get_whats_app_template) | **GET** /v1/whatsapp/templates/{templateName} | Get template
[**get_whats_app_templates**](WhatsAppApi.md#get_whats_app_templates) | **GET** /v1/whatsapp/templates | List templates
[**import_whats_app_contacts**](WhatsAppApi.md#import_whats_app_contacts) | **POST** /v1/whatsapp/contacts/import | Bulk import contacts
[**remove_whats_app_broadcast_recipients**](WhatsAppApi.md#remove_whats_app_broadcast_recipients) | **DELETE** /v1/whatsapp/broadcasts/{broadcastId}/recipients | Remove recipients
[**rename_whats_app_group**](WhatsAppApi.md#rename_whats_app_group) | **POST** /v1/whatsapp/groups | Rename group
[**schedule_whats_app_broadcast**](WhatsAppApi.md#schedule_whats_app_broadcast) | **POST** /v1/whatsapp/broadcasts/{broadcastId}/schedule | Schedule broadcast
[**send_whats_app_broadcast**](WhatsAppApi.md#send_whats_app_broadcast) | **POST** /v1/whatsapp/broadcasts/{broadcastId}/send | Send broadcast
[**send_whats_app_bulk**](WhatsAppApi.md#send_whats_app_bulk) | **POST** /v1/whatsapp/bulk | Bulk send template messages
[**update_whats_app_business_profile**](WhatsAppApi.md#update_whats_app_business_profile) | **POST** /v1/whatsapp/business-profile | Update business profile
[**update_whats_app_contact**](WhatsAppApi.md#update_whats_app_contact) | **PUT** /v1/whatsapp/contacts/{contactId} | Update contact
[**update_whats_app_display_name**](WhatsAppApi.md#update_whats_app_display_name) | **POST** /v1/whatsapp/business-profile/display-name | Request display name change
[**update_whats_app_template**](WhatsAppApi.md#update_whats_app_template) | **PATCH** /v1/whatsapp/templates/{templateName} | Update template
[**upload_whats_app_profile_photo**](WhatsAppApi.md#upload_whats_app_profile_photo) | **POST** /v1/whatsapp/business-profile/photo | Upload profile picture



## add_whats_app_broadcast_recipients

> models::AddWhatsAppBroadcastRecipients200Response add_whats_app_broadcast_recipients(broadcast_id, add_whats_app_broadcast_recipients_request)
Add recipients

**Deprecated.** Use `POST /v1/broadcasts/{id}/recipients` instead. Add recipients to a draft broadcast. Maximum 1000 recipients per request. Duplicate phone numbers are automatically skipped. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** | Broadcast ID | [required] |
**add_whats_app_broadcast_recipients_request** | [**AddWhatsAppBroadcastRecipientsRequest**](AddWhatsAppBroadcastRecipientsRequest.md) |  | [required] |

### Return type

[**models::AddWhatsAppBroadcastRecipients200Response**](addWhatsAppBroadcastRecipients_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bulk_delete_whats_app_contacts

> models::BulkDeleteWhatsAppContacts200Response bulk_delete_whats_app_contacts(bulk_delete_whats_app_contacts_request)
Bulk delete contacts

**Deprecated.** Use `DELETE /v1/contacts/{id}` for individual deletes instead. Permanently delete multiple contacts at once (max 500 per request). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**bulk_delete_whats_app_contacts_request** | [**BulkDeleteWhatsAppContactsRequest**](BulkDeleteWhatsAppContactsRequest.md) |  | [required] |

### Return type

[**models::BulkDeleteWhatsAppContacts200Response**](bulkDeleteWhatsAppContacts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bulk_update_whats_app_contacts

> models::BulkUpdateWhatsAppContacts200Response bulk_update_whats_app_contacts(bulk_update_whats_app_contacts_request)
Bulk update contacts

**Deprecated.** Use `PATCH /v1/contacts/{id}` for individual updates instead. Perform bulk operations on multiple contacts (max 500 per request). Supported actions: addTags, removeTags, addGroups, removeGroups, optIn, optOut, block, unblock. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**bulk_update_whats_app_contacts_request** | [**BulkUpdateWhatsAppContactsRequest**](BulkUpdateWhatsAppContactsRequest.md) |  | [required] |

### Return type

[**models::BulkUpdateWhatsAppContacts200Response**](bulkUpdateWhatsAppContacts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## cancel_whats_app_broadcast_schedule

> models::CancelWhatsAppBroadcastSchedule200Response cancel_whats_app_broadcast_schedule(broadcast_id)
Cancel scheduled broadcast

**Deprecated.** Use `POST /v1/broadcasts/{id}/cancel` instead. Cancel a scheduled broadcast and return it to draft status. Only broadcasts in scheduled status can be cancelled. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** | Broadcast ID | [required] |

### Return type

[**models::CancelWhatsAppBroadcastSchedule200Response**](cancelWhatsAppBroadcastSchedule_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_whats_app_broadcast

> models::CreateWhatsAppBroadcast200Response create_whats_app_broadcast(create_whats_app_broadcast_request)
Create broadcast

**Deprecated.** Use `POST /v1/broadcasts` instead. Create a new draft broadcast. Optionally include initial recipients. After creation, add recipients and then send or schedule the broadcast. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_whats_app_broadcast_request** | [**CreateWhatsAppBroadcastRequest**](CreateWhatsAppBroadcastRequest.md) |  | [required] |

### Return type

[**models::CreateWhatsAppBroadcast200Response**](createWhatsAppBroadcast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_whats_app_contact

> models::CreateWhatsAppContact200Response create_whats_app_contact(create_whats_app_contact_request)
Create contact

**Deprecated.** Use `POST /v1/contacts` instead. Create a new WhatsApp contact. Phone number must be unique per account and in E.164 format (e.g., +1234567890). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_whats_app_contact_request** | [**CreateWhatsAppContactRequest**](CreateWhatsAppContactRequest.md) |  | [required] |

### Return type

[**models::CreateWhatsAppContact200Response**](createWhatsAppContact_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_whats_app_template

> models::CreateWhatsAppTemplate200Response create_whats_app_template(create_whats_app_template_request)
Create template

Create a new message template. Supports two modes:  **Custom template:** Provide `components` with your own content. Submitted to Meta for review (can take up to 24h).  **Library template:** Provide `library_template_name` instead of `components` to use a pre-built template from Meta's template library. Library templates are **pre-approved** (no review wait). You can optionally customize parameters and buttons via `library_template_body_inputs` and `library_template_button_inputs`.  Browse available library templates at: https://business.facebook.com/wa/manage/message-templates/ 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_whats_app_template_request** | [**CreateWhatsAppTemplateRequest**](CreateWhatsAppTemplateRequest.md) |  | [required] |

### Return type

[**models::CreateWhatsAppTemplate200Response**](createWhatsAppTemplate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_whats_app_broadcast

> models::UnpublishPost200Response delete_whats_app_broadcast(broadcast_id)
Delete broadcast

**Deprecated.** Use `DELETE /v1/broadcasts/{id}` instead. Delete a broadcast. Only draft or cancelled broadcasts can be deleted. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** | Broadcast ID | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_whats_app_contact

> models::UnpublishPost200Response delete_whats_app_contact(contact_id)
Delete contact

**Deprecated.** Use `DELETE /v1/contacts/{id}` instead. Permanently delete a WhatsApp contact. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**contact_id** | **String** | Contact ID | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_whats_app_group

> models::RenameWhatsAppGroup200Response delete_whats_app_group(delete_whats_app_group_request)
Delete group

**Deprecated.** Use contact tags via `PATCH /v1/contacts/{id}` instead. Delete a contact group. This removes the group from all contacts but does not delete the contacts themselves. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**delete_whats_app_group_request** | [**DeleteWhatsAppGroupRequest**](DeleteWhatsAppGroupRequest.md) |  | [required] |

### Return type

[**models::RenameWhatsAppGroup200Response**](renameWhatsAppGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_whats_app_template

> models::UnpublishPost200Response delete_whats_app_template(template_name, account_id)
Delete template

Permanently delete a message template by name. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_name** | **String** | Template name | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_broadcast

> models::GetWhatsAppBroadcast200Response get_whats_app_broadcast(broadcast_id)
Get broadcast

**Deprecated.** Use `GET /v1/broadcasts/{id}` instead. Retrieve detailed information about a single broadcast including delivery statistics. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** | Broadcast ID | [required] |

### Return type

[**models::GetWhatsAppBroadcast200Response**](getWhatsAppBroadcast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_broadcast_recipients

> models::GetWhatsAppBroadcastRecipients200Response get_whats_app_broadcast_recipients(broadcast_id, status, limit, skip)
List recipients

**Deprecated.** Use `GET /v1/broadcasts/{id}/recipients` instead. List recipients of a broadcast with their delivery status. Supports filtering by delivery status and pagination. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** | Broadcast ID | [required] |
**status** | Option<**String**> | Filter by recipient delivery status |  |
**limit** | Option<**i32**> | Maximum results (default 100) |  |[default to 100]
**skip** | Option<**i32**> | Offset for pagination |  |[default to 0]

### Return type

[**models::GetWhatsAppBroadcastRecipients200Response**](getWhatsAppBroadcastRecipients_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_broadcasts

> models::GetWhatsAppBroadcasts200Response get_whats_app_broadcasts(account_id, status, limit, skip)
List broadcasts

**Deprecated.** Use `GET /v1/broadcasts?profileId={profileId}` instead. List all WhatsApp broadcasts for an account. Returns broadcasts sorted by creation date (newest first) without the full recipients list for performance. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |
**status** | Option<**String**> | Filter by broadcast status |  |
**limit** | Option<**i32**> | Maximum results (default 50) |  |[default to 50]
**skip** | Option<**i32**> | Offset for pagination |  |[default to 0]

### Return type

[**models::GetWhatsAppBroadcasts200Response**](getWhatsAppBroadcasts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_business_profile

> models::GetWhatsAppBusinessProfile200Response get_whats_app_business_profile(account_id)
Get business profile

Retrieve the WhatsApp Business profile for the account (about, address, description, email, websites, etc.). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppBusinessProfile200Response**](getWhatsAppBusinessProfile_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_contact

> models::GetWhatsAppContact200Response get_whats_app_contact(contact_id)
Get contact

**Deprecated.** Use `GET /v1/contacts/{id}` instead. Retrieve a single WhatsApp contact by ID with full details. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**contact_id** | **String** | Contact ID | [required] |

### Return type

[**models::GetWhatsAppContact200Response**](getWhatsAppContact_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_contacts

> models::GetWhatsAppContacts200Response get_whats_app_contacts(account_id, search, tag, group, opted_in, limit, skip)
List contacts

**Deprecated.** Use `GET /v1/contacts?profileId={profileId}` instead. List WhatsApp contacts for an account. Supports filtering by tags, groups, opt-in status, and text search. Returns contacts sorted by name with available filter options. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |
**search** | Option<**String**> | Search contacts by name, phone, email, or company |  |
**tag** | Option<**String**> | Filter by tag |  |
**group** | Option<**String**> | Filter by group |  |
**opted_in** | Option<**String**> | Filter by opt-in status |  |
**limit** | Option<**i32**> | Maximum results (default 50) |  |[default to 50]
**skip** | Option<**i32**> | Offset for pagination |  |[default to 0]

### Return type

[**models::GetWhatsAppContacts200Response**](getWhatsAppContacts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_display_name

> models::GetWhatsAppDisplayName200Response get_whats_app_display_name(account_id)
Get display name and review status

Fetch the current display name and its Meta review status for a WhatsApp Business account. Display name changes require Meta approval and can take 1-3 business days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppDisplayName200Response**](getWhatsAppDisplayName_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_groups

> models::GetWhatsAppGroups200Response get_whats_app_groups(account_id)
List contact groups

**Deprecated.** Use contact tags via `GET /v1/contacts` for grouping instead. WhatsApp groups have no cross-platform equivalent. List all contact groups for a WhatsApp account with contact counts. Groups are derived from the groups field on contacts, not stored as separate documents. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppGroups200Response**](getWhatsAppGroups_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_template

> models::GetWhatsAppTemplate200Response get_whats_app_template(template_name, account_id)
Get template

Retrieve a single message template by name. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_name** | **String** | Template name | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppTemplate200Response**](getWhatsAppTemplate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_templates

> models::GetWhatsAppTemplates200Response get_whats_app_templates(account_id)
List templates

List all message templates for the WhatsApp Business Account (WABA) associated with the given account. Templates are fetched directly from the WhatsApp Cloud API. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppTemplates200Response**](getWhatsAppTemplates_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## import_whats_app_contacts

> models::ImportWhatsAppContacts200Response import_whats_app_contacts(import_whats_app_contacts_request)
Bulk import contacts

**Deprecated.** Use `POST /v1/contacts/bulk` instead. Import up to 1000 contacts at once. Each contact requires a phone number and name. Duplicates are skipped by default. Supports default tags and groups applied to all imported contacts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**import_whats_app_contacts_request** | [**ImportWhatsAppContactsRequest**](ImportWhatsAppContactsRequest.md) |  | [required] |

### Return type

[**models::ImportWhatsAppContacts200Response**](importWhatsAppContacts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_whats_app_broadcast_recipients

> models::RemoveWhatsAppBroadcastRecipients200Response remove_whats_app_broadcast_recipients(broadcast_id, remove_whats_app_broadcast_recipients_request)
Remove recipients

**Deprecated.** Use `POST /v1/broadcasts/{id}/recipients` with removal flag instead. Remove recipients from a draft broadcast by phone number. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** | Broadcast ID | [required] |
**remove_whats_app_broadcast_recipients_request** | [**RemoveWhatsAppBroadcastRecipientsRequest**](RemoveWhatsAppBroadcastRecipientsRequest.md) |  | [required] |

### Return type

[**models::RemoveWhatsAppBroadcastRecipients200Response**](removeWhatsAppBroadcastRecipients_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## rename_whats_app_group

> models::RenameWhatsAppGroup200Response rename_whats_app_group(rename_whats_app_group_request)
Rename group

**Deprecated.** Use contact tags via `PATCH /v1/contacts/{id}` instead. Rename a contact group. This updates the group name on all contacts that belong to the group. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rename_whats_app_group_request** | [**RenameWhatsAppGroupRequest**](RenameWhatsAppGroupRequest.md) |  | [required] |

### Return type

[**models::RenameWhatsAppGroup200Response**](renameWhatsAppGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## schedule_whats_app_broadcast

> models::ScheduleWhatsAppBroadcast200Response schedule_whats_app_broadcast(broadcast_id, schedule_whats_app_broadcast_request)
Schedule broadcast

**Deprecated.** Use `POST /v1/broadcasts/{id}/schedule` instead. Schedule a draft broadcast for future sending. The scheduled time must be in the future and no more than 30 days in advance. The broadcast must be in draft status and have recipients. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** | Broadcast ID | [required] |
**schedule_whats_app_broadcast_request** | [**ScheduleWhatsAppBroadcastRequest**](ScheduleWhatsAppBroadcastRequest.md) |  | [required] |

### Return type

[**models::ScheduleWhatsAppBroadcast200Response**](scheduleWhatsAppBroadcast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_whats_app_broadcast

> models::SendWhatsAppBroadcast200Response send_whats_app_broadcast(broadcast_id)
Send broadcast

**Deprecated.** Use `POST /v1/broadcasts/{id}/send` instead. Start sending a broadcast immediately. The broadcast must be in draft or scheduled status and have at least one recipient. Messages are sent sequentially with rate limiting. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** | Broadcast ID | [required] |

### Return type

[**models::SendWhatsAppBroadcast200Response**](sendWhatsAppBroadcast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_whats_app_bulk

> models::SendWhatsAppBulk200Response send_whats_app_bulk(send_whats_app_bulk_request)
Bulk send template messages

**Deprecated.** Use `POST /v1/broadcasts` to create a broadcast, `POST /v1/broadcasts/{id}/recipients` to add recipients, then `POST /v1/broadcasts/{id}/send` to send. Send a template message to multiple recipients in a single request. Maximum 100 recipients per request. Only template messages are supported for bulk sending (not free-form text).  Each recipient can have optional per-recipient template variables for personalization. Returns detailed results for each recipient. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_whats_app_bulk_request** | [**SendWhatsAppBulkRequest**](SendWhatsAppBulkRequest.md) |  | [required] |

### Return type

[**models::SendWhatsAppBulk200Response**](sendWhatsAppBulk_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_business_profile

> models::UnpublishPost200Response update_whats_app_business_profile(update_whats_app_business_profile_request)
Update business profile

Update the WhatsApp Business profile. All fields are optional; only provided fields will be updated. Constraints: about max 139 chars, description max 512 chars, max 2 websites. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_whats_app_business_profile_request** | [**UpdateWhatsAppBusinessProfileRequest**](UpdateWhatsAppBusinessProfileRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_contact

> models::UpdateWhatsAppContact200Response update_whats_app_contact(contact_id, update_whats_app_contact_request)
Update contact

**Deprecated.** Use `PATCH /v1/contacts/{id}` instead. Update an existing WhatsApp contact. All fields are optional; only provided fields will be updated. Custom fields are merged with existing values. Set a custom field to null to remove it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**contact_id** | **String** | Contact ID | [required] |
**update_whats_app_contact_request** | [**UpdateWhatsAppContactRequest**](UpdateWhatsAppContactRequest.md) |  | [required] |

### Return type

[**models::UpdateWhatsAppContact200Response**](updateWhatsAppContact_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_display_name

> models::UpdateWhatsAppDisplayName200Response update_whats_app_display_name(update_whats_app_display_name_request)
Request display name change

Submit a display name change request for the WhatsApp Business account. The new name must follow WhatsApp naming guidelines (3-512 characters, must represent your business). Changes require Meta review and approval, which typically takes 1-3 business days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_whats_app_display_name_request** | [**UpdateWhatsAppDisplayNameRequest**](UpdateWhatsAppDisplayNameRequest.md) |  | [required] |

### Return type

[**models::UpdateWhatsAppDisplayName200Response**](updateWhatsAppDisplayName_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_template

> models::UpdateWhatsAppTemplate200Response update_whats_app_template(template_name, update_whats_app_template_request)
Update template

Update a message template's components. Only certain fields can be updated depending on the template's current approval state. Approved templates can only have components updated. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_name** | **String** | Template name | [required] |
**update_whats_app_template_request** | [**UpdateWhatsAppTemplateRequest**](UpdateWhatsAppTemplateRequest.md) |  | [required] |

### Return type

[**models::UpdateWhatsAppTemplate200Response**](updateWhatsAppTemplate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_whats_app_profile_photo

> models::UnpublishPost200Response upload_whats_app_profile_photo(account_id, file)
Upload profile picture

Upload a new profile picture for the WhatsApp Business Profile. Uses Meta's resumable upload API under the hood: creates an upload session, uploads the image bytes, then updates the business profile with the resulting handle. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |
**file** | **std::path::PathBuf** | Image file (JPEG or PNG, max 5MB, recommended 640x640) | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

