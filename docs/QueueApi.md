# \QueueApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_queue_slot**](QueueApi.md#create_queue_slot) | **POST** /v1/queue/slots | Create a new queue for a profile
[**delete_queue_slot**](QueueApi.md#delete_queue_slot) | **DELETE** /v1/queue/slots | Delete a queue schedule
[**get_next_queue_slot**](QueueApi.md#get_next_queue_slot) | **GET** /v1/queue/next-slot | Preview the next available queue slot (informational only)
[**list_queue_slots**](QueueApi.md#list_queue_slots) | **GET** /v1/queue/slots | Get queue schedules for a profile
[**preview_queue**](QueueApi.md#preview_queue) | **GET** /v1/queue/preview | Preview upcoming queue slots for a profile
[**update_queue_slot**](QueueApi.md#update_queue_slot) | **PUT** /v1/queue/slots | Create or update a queue schedule



## create_queue_slot

> models::CreateQueueSlot201Response create_queue_slot(create_queue_slot_request)
Create a new queue for a profile

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
Delete a queue schedule

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
Preview the next available queue slot (informational only)

Returns the next available queue slot for preview/informational purposes.  **Important: To schedule a post to the queue, do NOT use this endpoint's response with `scheduledFor`.** That creates a manual post, not a queue post.  Instead, use `POST /v1/posts` with `queuedFromProfile` (and optionally `queueId`). The system will automatically assign the next available slot with proper locking to prevent race conditions.  This endpoint is useful for: - Showing users when their next post will go out before they commit - Debugging/verifying queue configuration - Building UI previews  If no queueId is specified, uses the profile's default queue. 

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
Get queue schedules for a profile

Retrieve queue schedules for a profile. Each profile can have multiple queues. - Without `all=true`: Returns the default queue (or specific queue if queueId provided) - With `all=true`: Returns all queues for the profile 

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
Preview upcoming queue slots for a profile

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
Create or update a queue schedule

Create a new queue or update an existing one. - Without queueId: Creates or updates the default queue - With queueId: Updates the specific queue - With setAsDefault=true: Makes this queue the default for the profile 

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

