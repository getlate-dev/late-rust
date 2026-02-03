# AnalyticsListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**overview** | Option<[**models::AnalyticsOverview**](AnalyticsOverview.md)> |  | [optional]
**posts** | Option<[**Vec<models::AnalyticsListResponsePostsInner>**](AnalyticsListResponsePostsInner.md)> |  | [optional]
**pagination** | Option<[**models::Pagination**](Pagination.md)> |  | [optional]
**accounts** | Option<[**Vec<models::SocialAccount>**](SocialAccount.md)> | Connected social accounts (followerCount and followersLastUpdated only included if user has analytics add-on) | [optional]
**has_analytics_access** | Option<**bool**> | Whether user has analytics add-on access | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


