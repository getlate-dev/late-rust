# \LogsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_log**](LogsApi.md#get_log) | **GET** /v1/logs/{logId} | Get a single log entry
[**get_post_logs**](LogsApi.md#get_post_logs) | **GET** /v1/posts/{postId}/logs | Get logs for a specific post
[**list_logs**](LogsApi.md#list_logs) | **GET** /v1/logs | Get publishing logs



## get_log

> models::GetLog200Response get_log(log_id)
Get a single log entry

Retrieve detailed information about a specific log entry, including full request and response bodies for debugging. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**log_id** | **String** | The log entry ID | [required] |

### Return type

[**models::GetLog200Response**](getLog_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_post_logs

> models::GetPostLogs200Response get_post_logs(post_id, limit)
Get logs for a specific post

Retrieve all publishing logs for a specific post. Shows the complete history of publishing attempts for that post across all platforms. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | The post ID | [required] |
**limit** | Option<**i32**> | Maximum number of logs to return (max 100) |  |[default to 50]

### Return type

[**models::GetPostLogs200Response**](getPostLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_logs

> models::ListLogs200Response list_logs(status, platform, action, days, limit, skip)
Get publishing logs

Retrieve publishing logs for all posts. Logs show detailed information about each publishing attempt including API requests, responses, and timing data.  **Filtering:** - Filter by status (success, failed, pending, skipped) - Filter by platform (instagram, twitter, linkedin, etc.) - Filter by action (publish, retry, rate_limit_pause, etc.)  **Retention:** Logs are automatically deleted after 7 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**status** | Option<**String**> | Filter by log status |  |
**platform** | Option<**String**> | Filter by platform |  |
**action** | Option<**String**> | Filter by action type |  |
**days** | Option<**i32**> | Number of days to look back (max 7) |  |[default to 7]
**limit** | Option<**i32**> | Maximum number of logs to return (max 100) |  |[default to 50]
**skip** | Option<**i32**> | Number of logs to skip (for pagination) |  |[default to 0]

### Return type

[**models::ListLogs200Response**](listLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

