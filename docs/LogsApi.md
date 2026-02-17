# \LogsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_post_logs**](LogsApi.md#get_post_logs) | **GET** /v1/posts/{postId}/logs | Get post logs
[**list_connection_logs**](LogsApi.md#list_connection_logs) | **GET** /v1/connections/logs | List connection logs
[**list_posts_logs**](LogsApi.md#list_posts_logs) | **GET** /v1/posts/logs | List publishing logs



## get_post_logs

> models::GetPostLogs200Response get_post_logs(post_id, limit)
Get post logs

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


## list_connection_logs

> models::ListConnectionLogs200Response list_connection_logs(platform, event_type, status, days, limit, skip)
List connection logs

Retrieve connection event logs showing account connection and disconnection history. Event types: connect_success, connect_failed, disconnect, reconnect_success, reconnect_failed. Logs are automatically deleted after 7 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform |  |
**event_type** | Option<**String**> | Filter by event type |  |
**status** | Option<**String**> | Filter by status (shorthand for event types) |  |
**days** | Option<**i32**> | Number of days to look back (max 7) |  |[default to 7]
**limit** | Option<**i32**> | Maximum number of logs to return (max 100) |  |[default to 50]
**skip** | Option<**i32**> | Number of logs to skip (for pagination) |  |[default to 0]

### Return type

[**models::ListConnectionLogs200Response**](listConnectionLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_posts_logs

> models::ListPostsLogs200Response list_posts_logs(status, platform, action, days, limit, skip)
List publishing logs

Retrieve publishing logs for all posts with detailed information about each publishing attempt. Filter by status, platform, or action. Logs are automatically deleted after 7 days. 

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

[**models::ListPostsLogs200Response**](listPostsLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

