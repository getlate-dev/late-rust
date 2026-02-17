# Post

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**user_id** | Option<[**models::PostUserId**](PostUserId.md)> |  | [optional]
**title** | Option<**String**> | YouTube: title must be ≤ 100 characters.  | [optional]
**content** | Option<**String**> |  | [optional]
**media_items** | Option<[**Vec<models::MediaItem>**](MediaItem.md)> |  | [optional]
**platforms** | Option<[**Vec<models::PlatformTarget>**](PlatformTarget.md)> |  | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**timezone** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: draft, scheduled, publishing, published, failed, partial) | [optional]
**tags** | Option<**Vec<String>**> | YouTube constraints: each tag max 100 chars, combined max 500 chars, duplicates removed. | [optional]
**hashtags** | Option<**Vec<String>**> |  | [optional]
**mentions** | Option<**Vec<String>**> |  | [optional]
**visibility** | Option<**Visibility**> |  (enum: public, private, unlisted) | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**queued_from_profile** | Option<**String**> | Profile ID if the post was scheduled via the queue | [optional]
**queue_id** | Option<**String**> | Queue ID if the post was scheduled via a specific queue | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


