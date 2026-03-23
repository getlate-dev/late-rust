# \BroadcastsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_broadcast_recipients**](BroadcastsApi.md#add_broadcast_recipients) | **POST** /v1/broadcasts/{broadcastId}/recipients | Add recipients to a broadcast
[**cancel_broadcast**](BroadcastsApi.md#cancel_broadcast) | **POST** /v1/broadcasts/{broadcastId}/cancel | Cancel a broadcast
[**create_broadcast**](BroadcastsApi.md#create_broadcast) | **POST** /v1/broadcasts | Create a broadcast draft
[**delete_broadcast**](BroadcastsApi.md#delete_broadcast) | **DELETE** /v1/broadcasts/{broadcastId} | Delete a broadcast (draft only)
[**get_broadcast**](BroadcastsApi.md#get_broadcast) | **GET** /v1/broadcasts/{broadcastId} | Get broadcast details
[**list_broadcast_recipients**](BroadcastsApi.md#list_broadcast_recipients) | **GET** /v1/broadcasts/{broadcastId}/recipients | List broadcast recipients
[**list_broadcasts**](BroadcastsApi.md#list_broadcasts) | **GET** /v1/broadcasts | List broadcasts
[**schedule_broadcast**](BroadcastsApi.md#schedule_broadcast) | **POST** /v1/broadcasts/{broadcastId}/schedule | Schedule broadcast for later
[**send_broadcast**](BroadcastsApi.md#send_broadcast) | **POST** /v1/broadcasts/{broadcastId}/send | Trigger immediate send
[**update_broadcast**](BroadcastsApi.md#update_broadcast) | **PATCH** /v1/broadcasts/{broadcastId} | Update a broadcast



## add_broadcast_recipients

> models::AddBroadcastRecipients200Response add_broadcast_recipients(broadcast_id, add_broadcast_recipients_request)
Add recipients to a broadcast

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** |  | [required] |
**add_broadcast_recipients_request** | [**AddBroadcastRecipientsRequest**](AddBroadcastRecipientsRequest.md) |  | [required] |

### Return type

[**models::AddBroadcastRecipients200Response**](addBroadcastRecipients_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## cancel_broadcast

> models::CancelBroadcast200Response cancel_broadcast(broadcast_id)
Cancel a broadcast

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** |  | [required] |

### Return type

[**models::CancelBroadcast200Response**](cancelBroadcast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_broadcast

> create_broadcast(create_broadcast_request)
Create a broadcast draft

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_broadcast_request** | [**CreateBroadcastRequest**](CreateBroadcastRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_broadcast

> delete_broadcast(broadcast_id)
Delete a broadcast (draft only)

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_broadcast

> models::GetBroadcast200Response get_broadcast(broadcast_id)
Get broadcast details

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** |  | [required] |

### Return type

[**models::GetBroadcast200Response**](getBroadcast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_broadcast_recipients

> models::ListBroadcastRecipients200Response list_broadcast_recipients(broadcast_id, status, limit, skip)
List broadcast recipients

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** |  | [required] |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListBroadcastRecipients200Response**](listBroadcastRecipients_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_broadcasts

> models::ListBroadcasts200Response list_broadcasts(profile_id, status, platform, limit, skip)
List broadcasts

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile. Omit to list across all profiles |  |
**status** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListBroadcasts200Response**](listBroadcasts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## schedule_broadcast

> models::ScheduleBroadcast200Response schedule_broadcast(broadcast_id, schedule_broadcast_request)
Schedule broadcast for later

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** |  | [required] |
**schedule_broadcast_request** | [**ScheduleBroadcastRequest**](ScheduleBroadcastRequest.md) |  | [required] |

### Return type

[**models::ScheduleBroadcast200Response**](scheduleBroadcast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_broadcast

> models::SendBroadcast200Response send_broadcast(broadcast_id)
Trigger immediate send

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** |  | [required] |

### Return type

[**models::SendBroadcast200Response**](sendBroadcast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_broadcast

> models::UpdateBroadcast200Response update_broadcast(broadcast_id)
Update a broadcast

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** |  | [required] |

### Return type

[**models::UpdateBroadcast200Response**](updateBroadcast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

