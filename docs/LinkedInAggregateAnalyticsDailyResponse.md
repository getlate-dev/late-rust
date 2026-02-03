# LinkedInAggregateAnalyticsDailyResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**account_type** | Option<**String**> |  | [optional]
**username** | Option<**String**> |  | [optional]
**aggregation** | Option<**Aggregation**> |  (enum: DAILY) | [optional]
**date_range** | Option<[**models::LinkedInAggregateAnalyticsTotalResponseDateRange**](LinkedInAggregateAnalyticsTotalResponseDateRange.md)> |  | [optional]
**analytics** | Option<[**models::LinkedInAggregateAnalyticsDailyResponseAnalytics**](LinkedInAggregateAnalyticsDailyResponseAnalytics.md)> |  | [optional]
**skipped_metrics** | Option<**Vec<String>**> | Metrics that were skipped due to API limitations | [optional]
**note** | Option<**String**> |  | [optional]
**last_updated** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


