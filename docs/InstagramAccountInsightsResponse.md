# InstagramAccountInsightsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**account_id** | Option<**String**> | The Zernio SocialAccount ID | [optional]
**platform** | Option<**String**> |  | [optional]
**date_range** | Option<[**models::InstagramAccountInsightsResponseDateRange**](InstagramAccountInsightsResponseDateRange.md)> |  | [optional]
**metric_type** | Option<**MetricType**> |  (enum: time_series, total_value) | [optional]
**breakdown** | Option<**String**> | Breakdown dimension used (only present when breakdown was requested) | [optional]
**metrics** | Option<[**std::collections::HashMap<String, models::InstagramAccountInsightsResponseMetricsValue>**](InstagramAccountInsightsResponseMetricsValue.md)> | Object keyed by metric name. For time_series: each metric has \"total\" (number) and \"values\" (array of {date, value}). For total_value: each metric has \"total\" (number) and optionally \"breakdowns\" (array of {dimension, value}).  | [optional]
**data_delay** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


