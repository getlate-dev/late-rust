# AnalyticsListResponsePostsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**late_post_id** | Option<**String**> | Original Late post ID if scheduled via Late | [optional]
**content** | Option<**String**> |  | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**published_at** | Option<**String**> |  | [optional]
**status** | Option<**String**> |  | [optional]
**analytics** | Option<[**models::PostAnalytics**](PostAnalytics.md)> |  | [optional]
**platforms** | Option<[**Vec<models::PlatformAnalytics>**](PlatformAnalytics.md)> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**platform_post_url** | Option<**String**> |  | [optional]
**is_external** | Option<**bool**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**thumbnail_url** | Option<**String**> |  | [optional]
**media_type** | Option<**MediaType**> |  (enum: image, video, gif, document, carousel, text) | [optional]
**media_items** | Option<[**Vec<models::AnalyticsSinglePostResponseMediaItemsInner>**](AnalyticsSinglePostResponseMediaItemsInner.md)> | All media items for this post. Carousel posts contain one entry per slide. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


