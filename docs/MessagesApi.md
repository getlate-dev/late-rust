# \MessagesApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**edit_inbox_message**](MessagesApi.md#edit_inbox_message) | **PATCH** /v1/inbox/conversations/{conversationId}/messages/{messageId} | Edit message
[**get_inbox_conversation**](MessagesApi.md#get_inbox_conversation) | **GET** /v1/inbox/conversations/{conversationId} | Get conversation
[**get_inbox_conversation_messages**](MessagesApi.md#get_inbox_conversation_messages) | **GET** /v1/inbox/conversations/{conversationId}/messages | List messages
[**list_inbox_conversations**](MessagesApi.md#list_inbox_conversations) | **GET** /v1/inbox/conversations | List conversations
[**send_inbox_message**](MessagesApi.md#send_inbox_message) | **POST** /v1/inbox/conversations/{conversationId}/messages | Send message
[**update_inbox_conversation**](MessagesApi.md#update_inbox_conversation) | **PUT** /v1/inbox/conversations/{conversationId} | Update conversation status



## edit_inbox_message

> models::EditInboxMessage200Response edit_inbox_message(conversation_id, message_id, edit_inbox_message_request)
Edit message

Edit the text and/or reply markup of a previously sent Telegram message. Only supported for Telegram. Returns 400 for other platforms. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**message_id** | **String** | The Telegram message ID to edit | [required] |
**edit_inbox_message_request** | [**EditInboxMessageRequest**](EditInboxMessageRequest.md) |  | [required] |

### Return type

[**models::EditInboxMessage200Response**](editInboxMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_conversation

> models::GetInboxConversation200Response get_inbox_conversation(conversation_id, account_id)
Get conversation

Retrieve details and metadata for a specific conversation. Requires accountId query parameter.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. | [required] |
**account_id** | **String** | The social account ID | [required] |

### Return type

[**models::GetInboxConversation200Response**](getInboxConversation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_conversation_messages

> models::GetInboxConversationMessages200Response get_inbox_conversation_messages(conversation_id, account_id)
List messages

Fetch messages for a specific conversation. Requires accountId query parameter.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. | [required] |
**account_id** | **String** | Social account ID | [required] |

### Return type

[**models::GetInboxConversationMessages200Response**](getInboxConversationMessages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox_conversations

> models::ListInboxConversations200Response list_inbox_conversations(profile_id, platform, status, sort_order, limit, cursor, account_id)
List conversations

Fetch conversations (DMs) from all connected messaging accounts in a single API call. Supports filtering by profile and platform. Results are aggregated and deduplicated. Supported platforms: Facebook, Instagram, Twitter/X, Bluesky, Reddit, Telegram. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile ID |  |
**platform** | Option<**String**> | Filter by platform |  |
**status** | Option<**String**> | Filter by conversation status |  |
**sort_order** | Option<**String**> | Sort order by updated time |  |[default to desc]
**limit** | Option<**i32**> | Maximum number of conversations to return |  |[default to 50]
**cursor** | Option<**String**> | Pagination cursor for next page |  |
**account_id** | Option<**String**> | Filter by specific social account ID |  |

### Return type

[**models::ListInboxConversations200Response**](listInboxConversations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_inbox_message

> models::SendInboxMessage200Response send_inbox_message(conversation_id, send_inbox_message_request)
Send message

Send a message in a conversation. Supports text, attachments, quick replies, buttons, and message tags. Attachment and interactive message support varies by platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. | [required] |
**send_inbox_message_request** | [**SendInboxMessageRequest**](SendInboxMessageRequest.md) |  | [required] |

### Return type

[**models::SendInboxMessage200Response**](sendInboxMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json, multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_inbox_conversation

> models::UpdateInboxConversation200Response update_inbox_conversation(conversation_id, update_inbox_conversation_request)
Update conversation status

Archive or activate a conversation. Requires accountId in request body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. | [required] |
**update_inbox_conversation_request** | [**UpdateInboxConversationRequest**](UpdateInboxConversationRequest.md) |  | [required] |

### Return type

[**models::UpdateInboxConversation200Response**](updateInboxConversation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

