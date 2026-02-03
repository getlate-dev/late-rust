# QueueSchedule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> | Unique queue identifier | [optional]
**profile_id** | Option<**String**> | Profile ID this queue belongs to | [optional]
**name** | Option<**String**> | Queue name (e.g., \"Morning Posts\", \"Evening Content\") | [optional]
**timezone** | Option<**String**> | IANA timezone (e.g., America/New_York) | [optional]
**slots** | Option<[**Vec<models::QueueSlot>**](QueueSlot.md)> |  | [optional]
**active** | Option<**bool**> | Whether the queue is active | [optional]
**is_default** | Option<**bool**> | Whether this is the default queue for the profile (used when no queueId specified) | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


