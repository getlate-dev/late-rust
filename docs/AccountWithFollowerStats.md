# AccountWithFollowerStats

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**profile_id** | Option<[**models::SocialAccountProfileId**](SocialAccountProfileId.md)> |  | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**profile_url** | Option<**String**> | Full profile URL for the connected account on its platform. | [optional]
**is_active** | Option<**bool**> |  | [optional]
**followers_count** | Option<**f64**> | Follower count (only included if user has analytics add-on) | [optional]
**followers_last_updated** | Option<**String**> | Last time follower count was updated (only included if user has analytics add-on) | [optional]
**profile_picture** | Option<**String**> |  | [optional]
**current_followers** | Option<**f64**> | Current follower count | [optional]
**last_updated** | Option<**String**> |  | [optional]
**growth** | Option<**f64**> | Follower change over period | [optional]
**growth_percentage** | Option<**f64**> | Percentage growth | [optional]
**data_points** | Option<**f64**> | Number of historical snapshots | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


