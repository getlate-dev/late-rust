# CreatePostRequestPlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**custom_content** | Option<**String**> |  | [optional]
**custom_media** | Option<[**Vec<models::CreatePostRequestMediaItemsInner>**](CreatePostRequestMediaItemsInner.md)> |  | [optional]
**scheduled_for** | Option<**String**> | Optional per-platform scheduled time override. When omitted, the top-level scheduledFor is used. | [optional]
**platform_specific_data** | Option<[**models::CreatePostRequestPlatformsInnerPlatformSpecificData**](CreatePostRequestPlatformsInnerPlatformSpecificData.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


