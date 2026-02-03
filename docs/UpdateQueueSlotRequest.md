# UpdateQueueSlotRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**queue_id** | Option<**String**> | Queue ID to update (optional) | [optional]
**name** | Option<**String**> | Queue name | [optional]
**timezone** | **String** |  | 
**slots** | [**Vec<models::QueueSlot>**](QueueSlot.md) |  | 
**active** | Option<**bool**> |  | [optional][default to true]
**set_as_default** | Option<**bool**> | Make this queue the default | [optional]
**reshuffle_existing** | Option<**bool**> | Whether to reschedule existing queued posts to match new slots | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


