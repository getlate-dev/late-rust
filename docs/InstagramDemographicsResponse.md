# InstagramDemographicsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**account_id** | Option<**String**> | The Zernio SocialAccount ID | [optional]
**platform** | Option<**String**> |  | [optional]
**metric** | Option<**Metric**> |  (enum: follower_demographics, engaged_audience_demographics) | [optional]
**timeframe** | Option<**Timeframe**> | The timeframe used for demographic data (enum: this_week, this_month) | [optional]
**demographics** | Option<[**std::collections::HashMap<String, Vec<models::InstagramDemographicsResponseDemographicsValueInner>>**](Vec.md)> | Object keyed by breakdown dimension (age, city, country, gender) | [optional]
**note** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


