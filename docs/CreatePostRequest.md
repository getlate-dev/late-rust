# CreatePostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> |  | [optional]
**content** | Option<**String**> | Post caption/text. Optional when media is attached or all platforms have customContent. Required for text-only posts. | [optional]
**media_items** | Option<[**Vec<models::CreatePostRequestMediaItemsInner>**](CreatePostRequestMediaItemsInner.md)> |  | [optional]
**platforms** | Option<[**Vec<models::CreatePostRequestPlatformsInner>**](CreatePostRequestPlatformsInner.md)> |  | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**publish_now** | Option<**bool**> |  | [optional][default to false]
**is_draft** | Option<**bool**> |  | [optional][default to false]
**timezone** | Option<**String**> |  | [optional][default to UTC]
**tags** | Option<**Vec<String>**> | Tags/keywords. YouTube constraints: each tag max 100 chars, combined max 500 chars, duplicates auto-removed. | [optional]
**hashtags** | Option<**Vec<String>**> |  | [optional]
**mentions** | Option<**Vec<String>**> |  | [optional]
**crossposting_enabled** | Option<**bool**> |  | [optional][default to true]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**tiktok_settings** | Option<[**models::TikTokPlatformData**](TikTokPlatformData.md)> | Root-level TikTok settings applied to all TikTok platforms. Merged into each platform's platformSpecificData, with platform-specific settings taking precedence. | [optional]
**queued_from_profile** | Option<**String**> | Profile ID to schedule via queue. When provided without scheduledFor, the post is auto-assigned to the next available slot. Do not call /v1/queue/next-slot and use that time in scheduledFor, as that bypasses queue locking. | [optional]
**queue_id** | Option<**String**> | Specific queue ID to use when scheduling via queue. Only used when queuedFromProfile is also provided. If omitted, uses the profile's default queue.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


