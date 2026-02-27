# ValidateMedia200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valid** | Option<**bool**> |  | [optional]
**url** | Option<**String**> |  | [optional]
**error** | Option<**String**> | Error message if valid is false | [optional]
**content_type** | Option<**String**> |  | [optional]
**size** | Option<**i32**> | File size in bytes | [optional]
**size_formatted** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> |  (enum: image, video, unknown) | [optional]
**platform_limits** | Option<[**std::collections::HashMap<String, models::ValidateMedia200ResponsePlatformLimitsValue>**](ValidateMedia200ResponsePlatformLimitsValue.md)> | Per-platform size limit comparison (only present when size and type are known) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


