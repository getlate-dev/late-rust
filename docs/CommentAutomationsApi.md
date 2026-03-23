# \CommentAutomationsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_comment_automation**](CommentAutomationsApi.md#create_comment_automation) | **POST** /v1/comment-automations | Create a comment-to-DM automation
[**delete_comment_automation**](CommentAutomationsApi.md#delete_comment_automation) | **DELETE** /v1/comment-automations/{automationId} | Delete automation and all logs
[**get_comment_automation**](CommentAutomationsApi.md#get_comment_automation) | **GET** /v1/comment-automations/{automationId} | Get automation details with recent logs
[**list_comment_automation_logs**](CommentAutomationsApi.md#list_comment_automation_logs) | **GET** /v1/comment-automations/{automationId}/logs | List trigger logs for an automation
[**list_comment_automations**](CommentAutomationsApi.md#list_comment_automations) | **GET** /v1/comment-automations | List comment-to-DM automations
[**update_comment_automation**](CommentAutomationsApi.md#update_comment_automation) | **PATCH** /v1/comment-automations/{automationId} | Update automation settings



## create_comment_automation

> create_comment_automation(create_comment_automation_request)
Create a comment-to-DM automation

Create a keyword-triggered DM automation on an Instagram or Facebook post. When someone comments a matching keyword, they automatically receive a DM. Only one active automation per post is allowed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_comment_automation_request** | [**CreateCommentAutomationRequest**](CreateCommentAutomationRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_comment_automation

> delete_comment_automation(automation_id)
Delete automation and all logs

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_comment_automation

> get_comment_automation(automation_id)
Get automation details with recent logs

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_comment_automation_logs

> list_comment_automation_logs(automation_id, status, limit, skip)
List trigger logs for an automation

Paginated list of every comment that triggered this automation, with send status and commenter info.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**status** | Option<**String**> | Filter by result status |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_comment_automations

> models::ListCommentAutomations200Response list_comment_automations(profile_id)
List comment-to-DM automations

List all comment-to-DM automations for a profile. Returns automations with their stats.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Profile ID | [required] |

### Return type

[**models::ListCommentAutomations200Response**](listCommentAutomations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_comment_automation

> update_comment_automation(automation_id, update_comment_automation_request)
Update automation settings

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**update_comment_automation_request** | Option<[**UpdateCommentAutomationRequest**](UpdateCommentAutomationRequest.md)> |  |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

