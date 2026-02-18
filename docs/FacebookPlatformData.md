# FacebookPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content_type** | Option<**ContentType**> | Set to 'story' for Page Stories (24h ephemeral) or 'reel' for Reels (short vertical video). Defaults to feed post if omitted. (enum: story, reel) | [optional]
**title** | Option<**String**> | Reel title (only for contentType=reel). Separate from the caption/content field. | [optional]
**first_comment** | Option<**String**> | Optional first comment to post immediately after publishing (feed posts only, not stories or reels) | [optional]
**page_id** | Option<**String**> | Target Facebook Page ID for multi-page posting. If omitted, uses the default page. Use GET /v1/accounts/{id}/facebook-page to list pages. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


