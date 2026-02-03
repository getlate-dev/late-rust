# CreatePostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> |  | [optional]
**content** | Option<**String**> | Post caption/text content. Optional when media is attached (images, videos, etc.). Required for text-only posts. Can also be omitted if all platforms have customContent set.  | [optional]
**media_items** | Option<[**Vec<models::CreatePostRequestMediaItemsInner>**](CreatePostRequestMediaItemsInner.md)> |  | [optional]
**platforms** | Option<[**Vec<models::CreatePostRequestPlatformsInner>**](CreatePostRequestPlatformsInner.md)> |  | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**publish_now** | Option<**bool**> |  | [optional][default to false]
**is_draft** | Option<**bool**> |  | [optional][default to false]
**timezone** | Option<**String**> |  | [optional][default to UTC]
**tags** | Option<**Vec<String>**> | Tags/keywords for the post. YouTube-specific constraints: - No count limit; duplicates are automatically removed - Each tag must be ≤ 100 characters - Combined total across all tags ≤ 500 characters (YouTube's limit)  | [optional]
**hashtags** | Option<**Vec<String>**> |  | [optional]
**mentions** | Option<**Vec<String>**> |  | [optional]
**crossposting_enabled** | Option<**bool**> |  | [optional][default to true]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**tiktok_settings** | Option<[**models::TikTokPlatformData**](TikTokPlatformData.md)> | Root-level TikTok settings applied to all TikTok platforms in the request. This is a convenience shorthand. Settings here are merged into each TikTok platform's platformSpecificData, with platform-specific settings taking precedence.  | [optional]
**queued_from_profile** | Option<**String**> | Profile ID to schedule via queue.  When provided (without `scheduledFor`), the post will be automatically assigned to the next available slot from the profile's queue. The system uses distributed locking to prevent race conditions when multiple posts are scheduled concurrently. Do not call `/v1/queue/next-slot` and then use that time in `scheduledFor`. That bypasses the queue system and can cause duplicate slot assignments.  | [optional]
**queue_id** | Option<**String**> | Specific queue ID to use when scheduling via queue. Only used when queuedFromProfile is also provided. If omitted, uses the profile's default queue.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


