# GetAccountHealth200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | Overall health status (enum: healthy, warning, error) | [optional]
**token_status** | Option<[**models::GetAccountHealth200ResponseTokenStatus**](GetAccountHealth200ResponseTokenStatus.md)> |  | [optional]
**permissions** | Option<[**models::GetAccountHealth200ResponsePermissions**](GetAccountHealth200ResponsePermissions.md)> |  | [optional]
**issues** | Option<**Vec<String>**> | List of issues found | [optional]
**recommendations** | Option<**Vec<String>**> | Actionable recommendations to fix issues | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


