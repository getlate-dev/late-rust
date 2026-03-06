# RecyclingState

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | Option<**bool**> | Whether recycling is currently active | [optional]
**gap** | Option<**i32**> | Number of interval units between reposts | [optional]
**gap_freq** | Option<**GapFreq**> | Interval unit (week or month) (enum: week, month) | [optional]
**start_date** | Option<**String**> |  | [optional]
**expire_count** | Option<**i32**> |  | [optional]
**expire_date** | Option<**String**> |  | [optional]
**content_variations** | Option<**Vec<String>**> | Content variations for recycled copies (if configured) | [optional]
**content_variation_index** | Option<**i32**> | Current position in the content variations rotation (read-only) | [optional]
**recycle_count** | Option<**i32**> | How many recycled copies have been created so far (read-only) | [optional]
**next_recycle_at** | Option<**String**> | When the next recycled copy will be created (read-only) | [optional]
**last_recycled_at** | Option<**String**> | When the last recycled copy was created (read-only) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


