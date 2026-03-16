# AnalyticsSinglePostResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_id** | Option<**String**> |  | [optional]
**late_post_id** | Option<**String**> | Original Late post ID if scheduled via Late | [optional]
**status** | Option<**Status**> | Overall post status. \"partial\" when some platforms published and others failed. (enum: published, failed, partial) | [optional]
**content** | Option<**String**> |  | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**published_at** | Option<**String**> |  | [optional]
**analytics** | Option<[**models::PostAnalytics**](PostAnalytics.md)> |  | [optional]
**platform_analytics** | Option<[**Vec<models::PlatformAnalytics>**](PlatformAnalytics.md)> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**platform_post_url** | Option<**String**> |  | [optional]
**is_external** | Option<**bool**> |  | [optional]
**sync_status** | Option<**SyncStatus**> | Overall sync state across all platforms (enum: synced, pending, partial, unavailable) | [optional]
**message** | Option<**String**> | Human-readable status message for pending, partial, or failed states | [optional]
**thumbnail_url** | Option<**String**> |  | [optional]
**media_type** | Option<**MediaType**> |  (enum: image, video, carousel, text) | [optional]
**media_items** | Option<[**Vec<models::AnalyticsSinglePostResponseMediaItemsInner>**](AnalyticsSinglePostResponseMediaItemsInner.md)> | All media items for this post. Carousel posts contain one entry per slide. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


