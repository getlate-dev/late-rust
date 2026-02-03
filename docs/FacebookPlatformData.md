# FacebookPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content_type** | Option<**ContentType**> | Set to 'story' to publish as a Facebook Page Story (24-hour ephemeral content). Requires media. (enum: story) | [optional]
**first_comment** | Option<**String**> | Optional first comment to post immediately after publishing (feed posts only, not stories) | [optional]
**page_id** | Option<**String**> | Target Facebook Page ID for multi-page posting. If omitted, uses the selected/default page on the connection. Use GET /api/v1/accounts/{id}/facebook-page to list available pages.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


