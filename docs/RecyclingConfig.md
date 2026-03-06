# RecyclingConfig

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | Option<**bool**> | Set to false to disable recycling on this post | [optional][default to true]
**gap** | Option<**i32**> | Number of interval units between each repost. Required when enabling recycling. | [optional]
**gap_freq** | Option<**GapFreq**> | Interval unit for the gap. Defaults to 'month'. (enum: week, month) | [optional][default to Month]
**start_date** | Option<**String**> | When to start the recycling cycle. Defaults to the post's scheduledFor date. | [optional]
**expire_count** | Option<**i32**> | Stop recycling after this many copies have been created | [optional]
**expire_date** | Option<**String**> | Stop recycling after this date, regardless of count | [optional]
**content_variations** | Option<**Vec<String>**> | Array of content variations for recycled copies. On each recycle, the next variation is used in round-robin order. Recommended for Twitter and Pinterest to avoid duplicate content flags. If omitted, the original post content is used for all recycled copies. Send an empty array [] to clear existing variations. Must have 2+ entries when setting variations. Platform-level customContent still overrides the base content per platform.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


