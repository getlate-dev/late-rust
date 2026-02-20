# MediaItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | Option<**Type**> |  (enum: image, video, gif, document) | [optional]
**url** | Option<**String**> |  | [optional]
**title** | Option<**String**> | Optional title for the media item. Used as the document title for LinkedIn PDF/carousel posts. If omitted, falls back to the post title, then the filename. | [optional]
**filename** | Option<**String**> |  | [optional]
**size** | Option<**i32**> | Optional file size in bytes | [optional]
**mime_type** | Option<**String**> | Optional MIME type (e.g. image/jpeg, video/mp4) | [optional]
**thumbnail** | Option<**String**> | Optional thumbnail image URL for videos | [optional]
**instagram_thumbnail** | Option<**String**> | Optional custom cover image URL for Instagram Reels | [optional]
**tiktok_processed** | Option<**bool**> | Internal flag indicating the image was resized for TikTok | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


