# \QueueApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_queue_slot**](QueueApi.md#create_queue_slot) | **POST** /v1/queue/slots | Create schedule
[**delete_queue_slot**](QueueApi.md#delete_queue_slot) | **DELETE** /v1/queue/slots | Delete schedule
[**get_next_queue_slot**](QueueApi.md#get_next_queue_slot) | **GET** /v1/queue/next-slot | Get next available slot
[**list_queue_slots**](QueueApi.md#list_queue_slots) | **GET** /v1/queue/slots | List schedules
[**preview_queue**](QueueApi.md#preview_queue) | **GET** /v1/queue/preview | Preview upcoming slots
[**update_queue_slot**](QueueApi.md#update_queue_slot) | **PUT** /v1/queue/slots | Update schedule



## create_queue_slot

> models::CreateQueueSlot201Response create_queue_slot(create_queue_slot_request)
Create schedule

Create an additional queue for a profile. The first queue created becomes the default. Subsequent queues are non-default unless explicitly set. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_queue_slot_request** | [**CreateQueueSlotRequest**](CreateQueueSlotRequest.md) |  | [required] |

### Return type

[**models::CreateQueueSlot201Response**](createQueueSlot_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_queue_slot

> models::DeleteQueueSlot200Response delete_queue_slot(profile_id, queue_id)
Delete schedule

Delete a queue from a profile. Requires queueId to specify which queue to delete. If deleting the default queue, another queue will be promoted to default. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |
**queue_id** | **String** | Queue ID to delete | [required] |

### Return type

[**models::DeleteQueueSlot200Response**](deleteQueueSlot_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_next_queue_slot

> models::GetNextQueueSlot200Response get_next_queue_slot(profile_id, queue_id)
Get next available slot

Returns the next available queue slot for preview purposes. To create a queue post, use POST /v1/posts with queuedFromProfile instead of scheduledFor.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |
**queue_id** | Option<**String**> | Specific queue ID (optional, defaults to profile's default queue) |  |

### Return type

[**models::GetNextQueueSlot200Response**](getNextQueueSlot_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_queue_slots

> models::ListQueueSlots200Response list_queue_slots(profile_id, queue_id, all)
List schedules

Returns queue schedules for a profile. Use all=true for all queues, or queueId for a specific one. Defaults to the default queue.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Profile ID to get queues for | [required] |
**queue_id** | Option<**String**> | Specific queue ID to retrieve (optional) |  |
**all** | Option<**String**> | Set to 'true' to list all queues for the profile |  |

### Return type

[**models::ListQueueSlots200Response**](listQueueSlots_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## preview_queue

> models::PreviewQueue200Response preview_queue(profile_id, count)
Preview upcoming slots

Returns the next N upcoming queue slot times for a profile as ISO datetime strings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |
**count** | Option<**i32**> |  |  |[default to 20]

### Return type

[**models::PreviewQueue200Response**](previewQueue_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_queue_slot

> models::UpdateQueueSlot200Response update_queue_slot(update_queue_slot_request)
Update schedule

Create a new queue or update an existing one. Without queueId, creates/updates the default queue. With queueId, updates a specific queue. With setAsDefault=true, makes this queue the default for the profile. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_queue_slot_request** | [**UpdateQueueSlotRequest**](UpdateQueueSlotRequest.md) |  | [required] |

### Return type

[**models::UpdateQueueSlot200Response**](updateQueueSlot_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

