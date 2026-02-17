# \WebhooksApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_webhook_settings**](WebhooksApi.md#create_webhook_settings) | **POST** /v1/webhooks/settings | Create webhook
[**delete_webhook_settings**](WebhooksApi.md#delete_webhook_settings) | **DELETE** /v1/webhooks/settings | Delete webhook
[**get_webhook_logs**](WebhooksApi.md#get_webhook_logs) | **GET** /v1/webhooks/logs | Get delivery logs
[**get_webhook_settings**](WebhooksApi.md#get_webhook_settings) | **GET** /v1/webhooks/settings | List webhooks
[**test_webhook**](WebhooksApi.md#test_webhook) | **POST** /v1/webhooks/test | Send test webhook
[**update_webhook_settings**](WebhooksApi.md#update_webhook_settings) | **PUT** /v1/webhooks/settings | Update webhook



## create_webhook_settings

> models::UpdateWebhookSettings200Response create_webhook_settings(create_webhook_settings_request)
Create webhook

Create a new webhook configuration. Maximum 10 webhooks per user.  **Note:** Webhooks are automatically disabled after 10 consecutive delivery failures. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_webhook_settings_request** | [**CreateWebhookSettingsRequest**](CreateWebhookSettingsRequest.md) |  | [required] |

### Return type

[**models::UpdateWebhookSettings200Response**](updateWebhookSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_webhook_settings

> models::UpdateRedditSubreddits200Response delete_webhook_settings(id)
Delete webhook

Permanently delete a webhook configuration.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Webhook ID to delete | [required] |

### Return type

[**models::UpdateRedditSubreddits200Response**](updateRedditSubreddits_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_webhook_logs

> models::GetWebhookLogs200Response get_webhook_logs(limit, status, event, webhook_id)
Get delivery logs

Retrieve webhook delivery history. Logs are automatically deleted after 7 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**limit** | Option<**i32**> | Maximum number of logs to return (max 100) |  |[default to 50]
**status** | Option<**String**> | Filter by delivery status |  |
**event** | Option<**String**> | Filter by event type |  |
**webhook_id** | Option<**String**> | Filter by webhook ID |  |

### Return type

[**models::GetWebhookLogs200Response**](getWebhookLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_webhook_settings

> models::GetWebhookSettings200Response get_webhook_settings()
List webhooks

Retrieve all configured webhooks for the authenticated user. Supports up to 10 webhooks per user.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::GetWebhookSettings200Response**](getWebhookSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## test_webhook

> models::UnpublishPost200Response test_webhook(test_webhook_request)
Send test webhook

Send a test webhook to verify your endpoint is configured correctly. The test payload includes `event: \"webhook.test\"` to distinguish it from real events. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**test_webhook_request** | [**TestWebhookRequest**](TestWebhookRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_webhook_settings

> models::UpdateWebhookSettings200Response update_webhook_settings(update_webhook_settings_request)
Update webhook

Update an existing webhook configuration. All fields except `_id` are optional - only provided fields will be updated.  **Note:** Webhooks are automatically disabled after 10 consecutive delivery failures. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_webhook_settings_request** | [**UpdateWebhookSettingsRequest**](UpdateWebhookSettingsRequest.md) |  | [required] |

### Return type

[**models::UpdateWebhookSettings200Response**](updateWebhookSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

